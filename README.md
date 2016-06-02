This is a mirror of http://www.vim.org/scripts/script.php?script_id=273

The "Tag List" plugin is a source code browser plugin for Vim and
provides an overview of the structure of source code files and allows
you to efficiently browse through source code files for different
programming languages.  You can visit the taglist plugin home page for
more information:

      http://vim-taglist.sourceforge.net

You can subscribe to the taglist mailing list to post your questions
or suggestions for improvement or to report bugs. Visit the following
page for subscribing to the mailing list:

      http://groups.yahoo.com/group/taglist/

For more information about using this plugin, after installing the
taglist plugin, use the ":help taglist" command.

### This is a fork of vim-scripts/taglist.vim
- ##### Patched the error: "Error detected while processing function 2x_Tlist_Refresh_Folds"
 - Solution from the Internet :

``` 
 function! s:Tlist_Refresh_Folds()
+
+    if g:Tlist_Show_One_File
+      return
+    endif
+
     let winnum = bufwinnr(g:TagList_title)
     if winnum == -1
         return
```


