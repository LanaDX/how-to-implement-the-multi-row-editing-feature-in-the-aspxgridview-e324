<!-- default badges list -->
![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/128541386/19.1.8%2B)
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/E324)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
<!-- default badges end -->
<!-- default file list -->
*Files to look at*:

* [Record.cs](./CS/Record.cs) (VB: [Record.vb](./VB/Record.vb))
* [Default.aspx](./CS/Default.aspx) (VB: [Default.aspx](./VB/Default.aspx))
* [Default.aspx.cs](./CS/Default.aspx.cs) (VB: [Default.aspx.vb](./VB/Default.aspx.vb))
<!-- default file list end -->
# How to implement the multi-row editing feature in the ASPxGridView
<!-- run online -->
**[[Run Online]](https://codecentral.devexpress.com/e324/)**
<!-- run online end -->


<p><strong>UPDATED:</strong><br><br>Starting with version 13.2, the ASPxGridView control offers the basic "Batch Editing Mode" functionality that allows accomplishing a similar task with less effort and does not require so much extra code. See the <a href="https://community.devexpress.com/blogs/aspnet/archive/2013/12/16/asp-net-webforms-amp-mvc-gridview-batch-edit-what-39-s-new-in-13-2.aspx">ASP.NET WebForms & MVC: GridView Batch Edit </a>blog post to learn more about this new functionality.<br><br>Starting with version 14.1, the ASPxGridView control offers advanced "Batch Editing Mode" programming options.<br><br>You can find a standalone DB-independent solution in our Code Examples base at:<br><a href="https://www.devexpress.com/Support/Center/p/E5045">ASPxGridView - A simple Batch Editing implementation</a><br><br>If you have version v14.1+ available, consider using the built-in functionality instead of the approach detailed below.<br>If you need further assistance with this functionality, please create a new ticket in our Support Center.<br><br>The project below allows you to edit all rows on a current page at once. To implement this, I added the ASPxTextBox to the DataItemTemplate Container of several columns and bound these editors to the underlying data source. This will force the ASPxGridView to always display editors in these columns. So, the end-user can input values in these editors. After that click the PostModifications button to preserve the changes made. NOTE, this is done without switching the ASPxGridView to the EditMode and back.</p>
<p>To preserve the changes made, I saved editor values to the List<object> and then used these values by setting the UpdateParameters of the ASPxGridView's DataSource. Finally, to obtain editors and their values, I used the <a href="https://docs.devexpress.com/AspNet/DevExpress.Web.ASPxGridView.FindRowCellTemplateControl(System.Int32-DevExpress.Web.GridViewDataColumn-System.String)"><u>ASPxGridView.FindRowCellTemplateControl</u></a> method.</p>
<p><strong>See Also:</strong><br> <a href="https://www.devexpress.com/Support/Center/p/E1318">How to implement the multi-edit functionality with a multi-page grid that is bound dynamically</a><br> <a href="https://www.devexpress.com/Support/Center/p/E1468">Custom client-side logic implementation in the grid with multi-row editing</a><br> <a href="https://www.devexpress.com/Support/Center/p/E2026">How to edit multiple selected rows in a single Edit Form</a><br> <a href="https://www.devexpress.com/Support/Center/p/E1447">How to force the grid to stay in Edit mode</a><br> <a href="https://www.devexpress.com/Support/Center/p/E2333">How to perform ASPxGridView instant updating using different editors in the DataItem template</a><u></u></p>
<p><u></u>Question:<u> </u><a href="https://www.devexpress.com/Support/Center/p/Q311992">E324 - How to calculate the ASPxGridView group summaries on the client side</a></p>
<p><br><strong>MVC:</strong><br><a href="https://www.devexpress.com/Support/Center/p/E4236">How to implement the multi-row editing feature in the ASPxGridView</a></p>

<br/>


