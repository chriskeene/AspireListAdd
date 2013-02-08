
AspireListAdd Juice plugin
==========================
This plugin adds a link to interface of a catalogue that uses the Juice extension framework that will add the item to Talis Aspire if the item has an ISBN

Links:
Project Juice http://code.google.com/p/juice-project/
Project Juice and Prism http://juice-project.org/PrismJuice
Project Juice extentions http://juice-project.org/extensions_bazaar
This plugin on github 
Aspire Bookmarklet api http://support.talisaspire.com/entries/20358351-bookmarklet-api-specification

Install:
- ensure Juice had been added to your catalogue
- download AspirelistAdd.js save to your ~/js/extentions directory
- edit your 'extend' file (often called extend_my_prism.js on Prism 3 installations)
  - a sample extend file located here http://code.google.com/p/juice-project/source/browse/trunk/examples/talis-prism/extend-simple.js
  - inside the itemPage function add a line such as the following:
    new AspireListAdd('#footer','liblists.sussex.ac.uk','Add to Aspire Reading List');
  - near the top of the file look for a line that starts "$.juice.loadExtensions" and add AspireListAdd as one of the list items, e.g.
    $.juice.loadExtensions('JuiceSimpleInsert','GBSEmbed','AspireListAdd');
    
Configure:
Your extend file calls AspireListAdd with three options: the class/identifier to add the link to; the hostname of your Aspire tennacy and the text to use for the link.
 	
Todo:
Currently only displays a link if there is an ISBN, add check for DOI and other identifers as well.


Chris Keene
Feb 2013




