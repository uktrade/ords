# Instructions to create ORDS RDFa Metadata

## Creating & Viewing ORDS RDFa Metadata

These instructions detail a simple method to allow you to experiment with usage of the ORDS metadata standard. This is not intended to be used in a production environment where you may want something a little more sophisticated and automated.

This test process has three parts:

- The first part is to create some RDFa metadata.  
- The second part is to add this metadata to an HTML page.  
- The third (optional) part is to view the metadata in the way that a search engine or data re-user might extract it.

## Creating RDFa Metadata

1. Select a regulatory document that you want to create metadata for. It needs to be published online in HTML.

2. Open the [ORDS Template spreadsheet](template.xlsx).

3. Add appropriate metadata values to the “Value” column (Column B) of the “New Document” tab. You don’t need to complete all values for every document. You can find some examples for completed values in the “Example 1” and “Example 2” tabs in the spreadsheet.  

4. Metadata text will appear in the “HTML” column (Column D) as you complete the data entries in the “Value” column.

5. If you have multiple values for any property, you can insert a new row that is a copy of the previous row, example below.

Note: When entering date values you may need to start your row with a single quotation mark to avoid Excel altering the format, e.g. for 2023-12-19 you should type ‘2023-12-19

6. Save the spreadsheet once you have recorded all the relevant values and you can see all the required metadata in the “HTML” column (Column D).  

7. Open a text editor. You can use any text editor, e.g. Notepad, Wordpad, TextPad, Notepad++. Most Windows computers will have the Notepad application installed.

8. Copy and paste the contents of the “HTML” column (without the heading row) into the text editor and then remove any blank lines. This will leave you with some RDFa HTML metadata that can be added to a webpage.  

## Adding RDFa Metadata to an HTML Document

9. Open the HTML page for the document you are creating metadata for in your web browser.  

10. Save a copy of the HTML page to your computer. You can do this by Selecting “Save and share - Save page as…” in Chrome, “More tools – Save page as” in Edge or “Save page as…” in Firefox. Ensure you have selected “save page complete” or similar option to ensure you preserve the display styles.  

Note: You need to save the file to your desktop, your C drive, a local network drive or OneDrive. These instructions will not work for a file saved in SharePoint.

11. Open the saved HTML page in your text editor. To do this right-click on the file and select “Open with” and select your text editor. If your text editor is not listed, then select “Choose another app” and you should be able to select it from the continuation menu.  

12. Copy and paste the metadata values you created in Step.8 into the HTML in the <head> section. If there are already some <meta> values in the file it’s fine insert your values immediately after these, e.g.  

13. Save the edited HTML file.

14. You should now be able to open the edited HTML file in your browser, by double-clicking in the usual way.

Note: When you save the HTML page you should see two files. The HTML page itself and a folder that contains the stylesheets, images and any other resources required to correctly render the file. If you delete the folder or move it to a different location to the HTML file then your saved HTML page may not render correctly when opened.

## Viewing RDFa Metadata in HTML (Optional)

15. To view RDFa metadata in an HTML page in the browser install the [OpenLink Structured Data Sniffer](https://osds.openlinksw.com/) (OSDS) extension in Edge, Chrome or Firefox (Firefox may be easier as it’s less restricted). This browser extension was created by OpenLink who are responsible for the Virtuoso database product, one of the leading open source graph databases. The extension detects, extracts and displays a visualisation of semantic mark-up in HTML pages so you can see what a search engine or other tool would find in your webpage.

16. You can install the extension from the link above or by going to “Extensions” in your browser and searching for the OpenLink extension.

17. Open the edited HTML file in the browser.

18. Switch on the OpenLink Structured Data Sniffer extension. You should see your mark-up similar to the view below.

The “ORDS Example” zip file contains an example completed spreadsheet and edited HTML file for reference.

If you want to find out more about techniques and standards for adding RDFa metadata to HTML you can find more information in the [W3C RDFa 1.1 Primer](https://www.w3.org/TR/rdfa-primer/).
