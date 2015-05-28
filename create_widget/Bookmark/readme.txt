Install Instructions

Use the Starter Widget as a template to create a new widget.  Follow these steps:

1) create a copy of the Starter folder and rename it using a unique and descriptive name without any spaces or numbers
2) open the widget.js file and change the baseClass property following the naming convention 'widget_[Widget Folder Name]' (ie 'widget_Legend')
3) open the widget.css file and perform a find and replace.  Replace the string widget_Starter with the baseClass name used in step 2

the next set of files are located in the js folder
4) open the default.js file (this is the configuration) and add a widget configuration by copying the starter and change the title and parentid.  The parentid whould be unique a unique name, you can follow the naming convention '[Widget folder Name]WidgetDiv'.
5) add an enabled statement like using naming convention '[Widget Folder Name]Enabled' (ie "searchEnabled":true) 
6) open the main.js file and add the new widget class to the define statement at the top of the page.  Add "widgets/[Widget Folder Name]/widget".  In the 
7) add an if statement in the loadCustomWidgets method creating the widget
	ie	
		if (this.config.searchWidgetEnabled == true)
        	{
        		this.createWidget(this.config.widgets.search,new SearchWidget());
        	}
        }
at this point you should be able to run the application without error.  A new Starter widget should show up on the screen using the title defined in the config file
8) replace the images with a light and dark icon of yor own using the same names as the default starter widget.
9) add custom html markup in the template/widget.html file
10) start adding ui code to the initWidget method in js/[Widget Folder Name]/widget.js  