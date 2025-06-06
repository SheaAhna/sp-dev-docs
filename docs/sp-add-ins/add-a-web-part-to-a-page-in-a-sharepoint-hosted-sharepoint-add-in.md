---
title: Add a web part to a page in a SharePoint-hosted SharePoint Add-in
description: Add a web part to a page, and run and test the add-in.
ms.date: 06/13/2022
ms.prod: sharepoint
ms.localizationpriority: high
---

# Add a web part to a page in a SharePoint-hosted SharePoint Add-in

This is the fifth in a series of articles about the basics of developing SharePoint-hosted SharePoint Add-ins. You should first be familiar with [SharePoint Add-ins](sharepoint-add-ins.md) and the previous articles in this series, which you can find at [Get started creating SharePoint-hosted SharePoint Add-ins | Next steps](get-started-creating-sharepoint-hosted-sharepoint-add-ins.md#next-steps).

> [!NOTE]
> If you have been working through this series about SharePoint-hosted add-ins, you have a Visual Studio solution that you can use to continue with this topic. You can also download the repository at [SharePoint_SP-hosted_Add-Ins_Tutorials](https://github.com/OfficeDev/SharePoint_SP-hosted_Add-Ins_Tutorials) and open the BeforeWebPart.sln file.

In this article, you add a web part to the default page of the Employee Orientation SharePoint Add-in.

## Add a web part to a page

1. In **Solution Explorer**, open the Default.aspx file.
1. Because we'll be adding a list view web part to the page that surfaces the New Employees in Seattle list, we no longer need a link to the list view page for the list. Remove the **\<asp:HyperLink\>** element from the **\<asp:Content\>** element whose **ContentPlaceHolderId** is `PlaceHolderMain`.
1. Inside the same **\<asp:Content\>** element, add the following **WebPartZone**.

    ```XML
      <WebPartPages:WebPartZone runat="server" FrameType="TitleBarOnly"
          ID="HomePage1" Title="loc:full" />
    ```

1. Save and close the file.
1. In **Solution Explorer**, open the elements.xml file for the page in the **Pages** node.
1. If the **File** element is self-closing, remove the "/" character from it and add the end tag `</File>`.
1. In the **File** element, add a child **AllUsersWebPart** element, and set its **WebPartZoneID** to the ID of the web part zone that you created on the page. The file's contents should now look like the following. This markup tells SharePoint to insert an **AllUsersWebPart** into the web part zone that is named "HomePage1".

    ```xml
    <Elements xmlns="https://schemas.microsoft.com/sharepoint/">
      <Module Name="Pages">
        <File Path="Pages\Default.aspx" Url="Pages/Default.aspx" ReplaceContent="TRUE" >
          <AllUsersWebPart WebPartZoneID="HomePage1" WebPartOrder="1">

          </AllUsersWebPart>
        </File>
      </Module>
    </Elements>

    ```

1. Add a **CDATA** element as a child of the **AllUsersWebPart**, and then add a **webParts** element as a child of the **CDATA**, as shown in the following markup.

    ```xml
    <AllUsersWebPart WebPartZoneID="HomePage1" WebPartOrder="1">
      <![CDATA[
        <webParts>

        </webParts>
      ]]>
    </AllUsersWebPart>
    ```

1. Add the following **webPart** markup as a child of the **webParts** element. This markup adds an **XsltListViewWebPart** and tells the web part to show the **New Employees in Seattle** list. Note that the **ViewContentTypeId** property value is just `0x`, not the actual ID of the **NewEmployee** content type.

    ```xml
    <webPart xmlns="https://schemas.microsoft.com/WebPart/v3">
      <metaData>
        <type name="Microsoft.SharePoint.WebPartPages.XsltListViewWebPart,
                      Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral,
                      PublicKeyToken=71e9bce111e9429c" />
      </metaData>
      <data>
        <properties>
          <property name="ListUrl">Lists/NewEmployeesInSeattle</property>
          <property name="IsIncluded">True</property>
          <property name="NoDefaultStyle">True</property>
          <property name="Title">New Employees in Seattle</property>
          <property name="PageType">PAGE_NORMALVIEW</property>
          <property name="Default">False</property>
          <property name="ViewContentTypeId">0x</property>
        </properties>
      </data>
    </webPart>
    ```

## Run and test the add-in

1. Use the F5 key to deploy and run your add-in. Visual Studio makes a temporary installation of the add-in on your test SharePoint site and immediately runs the add-in.
1. When the add-in's default page opens, the list view web part is on it and the list is displayed.

    *Figure 1. Default page with list view web part*

    ![Default page of the add-in with the "New Employees in Seattle" list displayed in a web part.](../images/31e8e4b1-e2e6-416b-b360-9979a1f16fc7.PNG)

1. Try adding new items to the list and editing existing items.
1. To end the debugging session, close the browser window or stop debugging in Visual Studio. Each time that you press F5, Visual Studio will retract the previous version of the add-in and install the latest one.
1. You will work with this add-in and Visual Studio solution in other articles, and it's a good practice to retract the add-in one last time when you are done working with it for a while. Right-click the project in **Solution Explorer** and select **Retract**.

## Next steps

In the next article in this series, you'll [add a workflow to a SharePoint-hosted SharePoint Add-in](add-a-workflow-to-a-sharepoint-hosted-sharepoint-add-in.md).
