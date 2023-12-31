CONTENTS OF THIS FILE
---------------------
   
 * Introduction
 * Security Warning
 * Requirements
 * Installation
 * Configuration
 * How to find a display id 
 * Performance
 * Maintainers


INTRODUCTION
------------

Insert view filter allows to embed views using tags. The tag syntax is
relatively simple: [view:name=display=args]. The parameters are: view name, view
display id, view arguments. For example [view:tracker=page=1] says, embed a view
named "tracker", use the "page" display, and supply the argument "1". The
display and args parameters can be omitted. If the display is left empty, the
view's default display is used. Multiple arguments are separated with slash. The
args format is the same as used in the URL (or view preview screen).

Valid examples:
[view:my_view]
[view:my_view=my_display]
[view:my_view=my_display=arg1/arg2/arg3]
[view:my_view==arg1/arg2/arg3]


SECURITY WARNING
----------------
This filter is powerful, therefore it should be granted to trusted users only.
If you allow this filter to untrusted users, then you have to make sure that
EVERY VIEW EVERY DISPLAY (default display also!) has correct views access
settings.


REQUIREMENTS
------------

No special requirements


INSTALLATION
------------

Install as you would normally install a contributed Drupal module. See:
https://drupal.org/documentation/install/modules-themes/modules-8 for further
information.


CONFIGURATION
-------------

 * Once Insert view is installed, visit the the input formats page at
/admin/settings/filters and click the "configure" link for the input format(s)
for which you wish to enable the Insert view filter. Then simply check the
checkbox for the filter.


HOW TO FIND A DISPLAY ID
------------------------
On the edit page for the view in question, you'll find a list of displays at the
left side of the control area. "Defaults" will be at the top of that list. Hover
your mouse pointer over the name of the display you want to use. A URL will
appear in the status bar of your browser.  This is usually at the bottom of the
window, in the chrome. Everything after #views-tab- is the display ID. For
example in admin/build/views/edit/tracker?destination=node%2F51#views-tab-page
the display ID would be "page".


PERFORMANCE
-----------
To display views correctly, Insert view turns off caching for the input formats
for which it is enabled. That means every node using this input format will not
be cacheable. This can impact site performance. In these cases, it is
recommended to create a special input format for use when inserting views.


MAINTAINERS
-----------

Current maintainers:
 * andrew morton (drewish) - https://www.drupal.org/user/34869
 * Renato Gonçalves (RenatoG) - https://www.drupal.org/user/3326031 
 * Adam Balsam (balsama) - https://www.drupal.org/user/223087
 * Michael Samuelson (mlsamuelson) - https://www.drupal.org/user/47411
 * Paulo Henrique Starling (paulocs) - https://www.drupal.org/user/3640109
 * Michael Samuelson (mlsamuelson) - https://www.drupal.org/user/47411
 * Artem Dmitriiev (a.dmitriiev) - https://www.drupal.org/user/3235287
