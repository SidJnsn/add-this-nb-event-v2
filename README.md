# add-this-nb-event-v2
New version of Ian Patrick Hines' Add Event plugin for NationBuilder
Add This (NationBuilder) Event (Ver 2)
This version of the ATE plugin was built standing on the shoulders of Ian Patrick Hines as implemented at https://github.com/ianpatrickhines/add-this-nationbuilder-event/blob/master/README.md  This document reuses some of his wording.
Add This (NationBuilder) Event is a simple plugin for using the popular Add This Event plugin on your NationBuilder event pages. It will allow your supporters to add your events to their preferred calendars from your NationBuilder event pages with a single click.
Copyright / License
Add This (NationBuilder) Event is a simple port of of Add This Event, and is subject to the same licensing requirements.  For more information, see http://addthisevent.com.
Below is where we begin diverging from the original, so read carefully!
How to use this theme
To use this plugin:
    Upload all the files contained in this repository to your theme’s directory.
    Add {% include "partial_add_nb_event_js" %}  to your layout.html file just before the </body> tag at the bottom of the file.
    Add {% include "partial_add_nb_event_this_event_link" %} to your pages_show_event.html and pages_show_event_wide.html templates where you’d like the “Add to Calendar” link to appear.
After uploading the files and completing addition of the above three includes, look at the Theme Files screen.  If any files indicate that they are awaiting processing, select the Publish dropdown for each file. 
Note that the uploaded files have an underscore prefix, but the underscore and the file extension are left off in the include statement.
Go to http://AddThisEven.com and register for a free Hobby license.  Following the instructions on the site, add the domain you will be using to your profile; e.g., mydomain.nationbuilder.com.  Find your client id in the same area.  Copy and paste that client id to the License parameter in the _partial_add_nb_event_js.html file.
Apparently, there is a monthly limit on how many times the link can be used in a month on the free license.
***** I currently have not included an .SCSS file for customizing styling.  Several template examples of the Add This Even button are available at the above link, and the .CSS files there should provide a good starting point for anyone wanting to customize the button/dropdown.
In this version, I have set the data-direct = "google" attribute.  Because of that, the button displayed currently works only for a google calendar.  Code for other current calendars is in place, so removing the attribute will result in the dropdown showing the other calendar options.  I have not tested these other options.
For extended documentation on how to customize the plugin, see https://www.addevent.com/add-to-calendar-button
This implementation is configured for America/Chicago timezone.  If you need to change that, adjust it in the _partial_add_nb_event_this_event_link.html file  The time zone designations can be found at https://en.wikipedia.org/wiki/List_of_tz_database_time_zones
