# Add_links_to_footnotes
This code adds relative path hyperlinks to files in the footnotes in a word document. Often when a user creates a long Word document(the original document) with hundreds of footnotes, a common task is to hyperlink the footnotes to supporting documents saved in other directories. this code loops through the supporting documents in a folder and adds hyperlinks to the footnootes of the original document if the footnote text contains the full name of the supporting document(ignore the file extension). 

1. please always make a copy of your original document to run the code and save it once you check the result. 
2. The code adds relative path hyperlinks so the links will stay alive even original document and its linking documents were copied and pasted to other    directories. 
2. user can only select 1 top level folder that contains the documents to link. However this top level folder can have multiple subfolders             containing the documents to link. if a document with same name both exists at top level folder and a subfolder, the one in the subfolder will be linked.
3. user shall ensure that the file name contained in the footnotes exactly matches the file name in the folder. for example, the code will treat 
   "ABC- D.doc" in the footnote as different to "ABC-D.doc" in the folder so will not add hyperlinks.  
4. for pre existing hyperlinks in the footnote, if the footnote text matches a file name in the folder, the code will remove all pre existing links and add
   new links to avoid errors.
5. This code will add multiple hyperlinks in one footnote if it matches with multiple file names. user can also include other text that does not match any      file names in the footnote. these text will not be hyperlinked. 
6. sometimes hyperlinks were not successfully added even there is a match, the index of the footnotes will be included in the log file for user to check.
7. The code will turn off track changes to avoid text in footnotes being copied twice

## Tips
  
to make sure you correctly include the supporting document's name into the footnote, single click on the document and press "F2" and Ctrl C to copy it. 