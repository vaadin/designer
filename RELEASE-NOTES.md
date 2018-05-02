# Release notes for Vaadin Designer

Vaadin Designer is available for Vaadin 10 and 8. 

There is also separate product for Vaadin Framework 7.

The latest stable version for Vaadin 10 and 8 is 
[Vaadin Designer 3.0.0.final](#vaadin-designer-3x).

The latest Designer version for Framework 7 is 
[Vaadin Designer 1.4.3](#vaadin-designer-for-framework-7)

See the full list of [releases](#releases).

Please review the requirements below and the 
[FAQ](https://vaadin.com/designer/faq) if you have problems.

### Useful links

  - Site: <http://vaadin.com/designer>
  - Get started: <http://vaadin.com/designer/get-started>
  - Documentation: 
    - Vaadin 10: <https://vaadin.com/docs/v10>
    - Vaadin 8: <https://vaadin.com/docs/v8>
    - Vaadin 7: <https://vaadin.com/docs/v7>
  - FAQ: <https://vaadin.com/designer/faq>

## Vaadin Designer 3.x

#### What's new in 3.0

##### Vaadin 10
  - New Polymer template syntax for designs
  - Write Javascript and CSS directly into to the design file
  - New Palette for web components and HTML elements
  - Use any Polymer web component from Bower or WebJars
  - Support for nested designs
  - Any Flow component can be used as a companion file
  - Companion files are not overwritten on update

#### Requirements
  - Windows 10 / OS X 10.12 / Ubuntu 16.04 LTS
  - Newest Chrome, Safari, Firefox or Edge. IE 11+.
  - Java 8 and 9. 
  - Eclipse Oxygen, Neon and Mars. Java EE edition.
  - JetBrains IntelliJ IDEA 2016, 2017, 2018. Community or Ultimate edition.
  - Vaadin 8 or Vaadin 10.

#### Known Issues and Limitations

##### Vaadin 10
  - External preview doesn't work on IE11.
  - Horizontal scrolling using the trackpad doesn't work on macOS Eclipse.

##### Vaadin 8
  - All the components in Framework 8.4 are not supported ([#1624](https://github.com/vaadin/designer/issues/1624))
  - Custom widgetsets not used when designing. Custom (project) components
    and nested designs are shown as place holders when designing.
  - Limited support for GridLayout; no column- or row-spanning.
  - The declarative format does not currently support ClassResource (e.g for
    icons and images). The supported resources are: ThemeResource
    (theme://), ExternalResource (http://), FileResource (file://) and (for
    icons only) FontIcon (fonticon://).
  - Using a theme from another project (e.g Maven multi-module project) is
    not supported.

### Vaadin Designer 2.x

##### What's new in 2.2

  - Provide a way to access exported component through getter
      - Project wide setting.
      - Default option is not to generate getter.
      - Could be changed later per Design file.
      - [See Vaadin Docs for more
        details](https://vaadin.com/docs/v8/designer/designer-wiring.html#designer.wiring.java.getter)
  - Delay theme recompilation until save (IntelliJ)

##### What's new in 2.1

Support @PropertyId annotation for fields exported to Java companion
file

  - Ability to set the PropertyId property for fields, and the value
    will be mapped into a @PropertyId annotation in the Java companion
    file

Replace layout with another layout in the outline

  - Replace with… added to context menu in the outline. Allows replacing
    any layout with another layout, preserving contents.

Copy size when wrapping

  - Copy size from wrapped components. For example, if you wrap a
    Component in a Layout, the size of the Component is copied to the
    Layout.

Icon preview

  - Show a preview of Vaadin Icons when editing the Icon property

Improved theme support

  - Support themes in resources folders.

Create Grid columns from bean

  - Automatically create Grid columns when item-type property is changed

Experimental embedded Chromium browser in Eclipse

  - Embedded Chromium browser can be enabled from plugin settings

##### What's new in 2.0

Requires Vaadin Framework 8 and Java 8. Does not support Vaadin
Framework 7.

  - You can have both Designer 1 and 2 installed at the same time.
    Design files in Vaadin 7 project, will be opened in Designer 1.x and
    designs in Vaadin 8 project will be opened in Designer 2.x.
  - Generic types for selection components supported by ItemType
    property
  - Properties renamed to match new Vaadin 8 properties e.g. InputPrompt
    is now Placeholder
  - Stability improvements and bug fixes

## Vaadin Designer for Framework 7

##### What's new in 1.4

  - Provide a way to access exported component through getter
      - Project wide setting.
      - Default option is not to generate getter.
      - Could be changed later per Design file.
      - [See Vaadin Docs for more
        details](https://vaadin.com/docs/-/part/designer/designer-wiring.html#designer.wiring.java.getter)
  - Delay theme recompilation until save (IntelliJ)

##### What's new in 1.3

Support @PropertyId annotation for fields exported to Java companion
file

  - Ability to set the PropertyId property for fields, and the value
    will be mapped into a @PropertyId annotation in the Java companion
    file

Replace layout with another layout in the outline

  - Replace with… added to context menu in the outline. Allows replacing
    any layout with another layout, preserving contents.

Copy size when wrapping

  - Copy size from wrapped components. For example, if you wrap a
    Component in a Layout, the size of the Component is copied to the
    Layout.

Icon preview

  - Show a preview of FontAwesome icons when editing the Icon property

Improved theme support

  - Support themes in resources folders.

##### What's new in 1.2

New responsive templates available in "New Design" wizard for creating
responsive application navigation and views. See more details and usage
in: [Designer 1.2 - Responsive templates user
guide.](https://vaadin.com/designer/designer-1_2-responsive-templates-user-guide)

##### What's new in 1.1

  - No more static dummy content
      - The content for Grid, Table, Tree, TreeTable and MenuBar can be
        edited, and will appear when the application is run (unless
        replaced by java code).
      - Note the two important differences for 1.0 users:
          - When opening old designs, these components will appear empty
          - The pre-configured example content will actually end up in
            the design if you do not edit it.
      - The content can be edited in code-mode, or using the
        "Content"-property.
  - Improved Dark theme support
  - Improved GridLayout support
  - Copy&paste and drag&drop is now works with html snippets
  - Less external requirements (e.g JEE feature, Vaadin plug-in) =
    better compatibility
  - Custom content and attributes in the declarative file better
    preserved 
  - Properties re-ordered for better usability
  - Fixed multiple notorious error causes for "Could not retrieve
    controller for context path", "Failed to get component from
    mapper", "ConcurrentModificationException in ComponentModelMapper"
    and "No mapper contains the selected component".

##### Requirements

  - Windows 7 / OS X 10.9 / Ubuntu 14.04 LTS <sup>1</sup>
  - Chrome / Safari / Firefox / IE 10+ <sup>2</sup>
  - Java 7+ (Oracle Java 8
    recommended)<sup><span style="font-size: 13.3333px;">3</span></sup>
  - Eclipse Luna SR2 (4.4.2)+, Java EE edition <sup>4 </sup>
  - JetBrains IntelliJ IDEA 15+ Community/Ultimate 
  - Vaadin 7.5+
  - Does not support Vaadin 8

<sup>1</sup> In addition, libwebkitgtk 1.0 needs to be installed
(libwebkitgtk 3 not sufficient).  
Tested on Ubuntu 14.04 LTS, but other distributions known to work, as
long as libwebkitgtk 1.0 is available for Eclipse.

<sup>2</sup> Vaadin Designer makes use of your system browser to achieve
real WYSIWYG. Note that security settings (particularly on Windows / IE)
may in some instances interfere. IE8/9 not supported and results in
designer not loading.

<span style="font-size: 13.3333px;"><sup>3</sup> Java version used to
run Eclipse - your project can still use any Java version supported by
Vaadin. Refer to Eclipse documentation for more information about how to
verify and change the version used by Eclipse (note that Eclipse might
not use your system default).</span>

<sup>4</sup> Eclipse IDE for Java EE Developers preferred. Vaadin
Designer can be installed on other variants, but some update-site for
dependencies might be missing. See
the [FAQ](https://vaadin.com/designer/faq) for more details.  
Verified to work on STS 3.6.4.  
Vaadin Designer can be installed on older Luna versions, but prior to
SR2 there were serious bugs in Eclipse.

##### Limitations

#### Custom widgetsets and components

Custom widgetsets not used when designing. Custom (project) components
and nested designs are shown as place holders when designing.

#### GridLayout column- and row-spanning

Limited support for GridLayout; no column- or row-spanning.

#### ClassResource not supported

The declarative format does not currently support ClassResource (e.g for
icons and images). The supported resources are: ThemeResource
(theme://), ExternalResource (http://), FileResource (file://) and (for
icons only) FontIcon (fonticon://).

#### Using theme from separate project not supported

Using a theme from another project (e.g Maven multi-module project) is
not supported.

##### Additional limitations for IntelliJ IDEA

  - Template filtering in the New Design wizard
  - Theme selection for imported template styles

## Releases

#### 3.0.0.final

Released 2018-04-26

  - External preview works in any browsers ([#1671](https://github.com/vaadin/designer/issues/1671))
  - Dropped support for IntelliJ IDEA 15. Minimum supported version is IntelliJ IDEA 16. ([#1664](https://github.com/vaadin/designer/issues/1664))
  - "Flow template" is renamed to "Vaadin 10 design" ([#1637](https://github.com/vaadin/designer/issues/1637))
  - Fixed the bug when it was impossible to add new viewport size preset ([#1719](https://github.com/vaadin/designer/issues/1719))
  - Fixed the palette focus issue for Vaadin 10 design in Eclipse with macOS ([#1627](https://github.com/vaadin/designer/issues/1627))

#### 3.0.0.beta7

Released 2018-04-12

  - Improve design loading speed on the first design opening
  - Use an embedded license dialog for Flow design

#### 3.0.0.beta6

Released 2018-04-05

  - Shared styles fetched from wrong folder ([#1654](https://github.com/vaadin/designer/issues/1654))

#### 3.0.0.beta5

Released 2018-03-29

  - Apply new license checker using subscription based license key
  - Use the correct Polymer import after production mode build (#1606)

#### 3.0.0.beta4

Released 2018-03-22

  - Fix the bug which sometimes makes the IDE frozen and unresponsive after closing a design (#1625)

#### 3.0.0.beta3

Released 2018-03-15

  - Use correct prefix (context or frontend) for connected companion file
  - Java Companion file for flow template is generated with wrong path (#1602)

#### 3.0.0.beta2

Released 2018-03-08

  - Use Lumo variables without explicit import
  - Never show data binding property name in preview mode
  - Bugfixes: #1599, #1594

#### 3.0.0.beta1

Released 2018-03-06

  - New Polymer template syntax for designs
  - Write Javascript and CSS directly into to the design file
  - New Palette for web components and HTML elements
  - Use any Polymer web component from Bower or WebJars
  - Support for nested designs
  - Any Flow component can be used as a companion file
  - Companion files are not overwritten on update

#### 1.4.3 & 2.2.3

Released 2017-08-14

[List of enhacements and bug fixes in issue
tracker](https://github.com/vaadin/designer/milestone/16?closed=1)

Bug fixes:

  - An expired license is not accepted after extending
  - Eclipse palette is not shown completely on design opening in Linux
  - Caption of component inside FormLayout is not removed when cleared
    through field properties
  - Impossible to retrieve java companion file location in IntelliJ
  - SelectionMode property of Grid is missing from properties table
  - Generated getters is parameterized based on itemType property

#### 1.4.2 & 2.2.2

Released 2017-07-28

[List of enhacements and bug fixes in issue
tracker](https://github.com/vaadin/designer/milestone/15?closed=1)

Bug fixes:

  - Designer show file has changes and save does nothing bug Eclipse ide
  - Design file is marked as dirty after theme switching bug designfiles
    Eclipse themes
  - Saving doesn't work even though file is shown modified bug Eclipse
    ide 
  - Setting empty string to Label's value property doesn't work after it
    has been erased once  
  - Thread interrupted in LicenseDialogHandler bug Eclipse feedback
    licensing
  - "Updating preferences" task won't stop Eclipse feedback settings
  - Cannot set ComponentAlignment in IntelliJ bug feedback IntelliJ
    properties 

#### 1.4.1 & 2.2.1

Released 2017-07-13

[List of enhacements and bug fixes in issue
tracker](https://github.com/vaadin/designer/milestone/14?closed=1)

Bug fixes:

  - Properties table sets property value to wrong component
  - Changing SplitPosition property's value causes error dialog.
  - Using a Tabsheet in a design might break the design until IntelliJ
    is (force)restarted 
  - Resource folder cannot be created in IntelliJ New Design Wizard 
  - Changing split position on the editor doesn't update SplitPosition
    property's value 

#### 1.4.0 & 2.2.0

Released 2017-06-28

[List of enhacements and bug fixes in issue
tracker](https://github.com/vaadin/designer/milestone/13?closed=1)

Enhacements:

  - Companion file getters
  - Delay theme recompilation until save (IntelliJ)

Bug fixes:

  - Designer css classes no more visible
  - Modal Vaadin Designer license windows blocks Eclipse
  - Getting background "Timeout on Read" errors

#### 1.3.4 & 2.1.4

Released 2017-06-13

[List of enhacements and bug fixes in issue
tracker](https://github.com/vaadin/designer/milestone/12?closed=1)

Enhacements:

  - Made opening designs in Eclipse faster
  - Create "~/.vaadin/designer/templates" if it does not exist

Bug fixes:

  - Templates in ~/.vaadin/designer/templates are not loaded
  - License dialog keeps showing with trial license

#### 1.3.2 & 2.1.2

Released 2017-05-18

[List of bug fixes and enhancement in issue
tracker](https://github.com/vaadin/designer/milestone/10?closed=1)

Enhancement:

  - Allow unlimited offline usage with any license

Bug fixes:

  - Failed to update companion file if intellij project configuration
    files are inside custom folder 
  - Wrapping root component does not expand the new root
  - Project name is null in the external browser preview title in
    IntelliJ
  - Unable to set rows property for some components
  - Exception when inserting new design source with namespaces
  - Editor scaling issue with multi monitors configuration in macOS in
    IntelliJ
  - Can't scroll horizontally design in Windows
  - Missing icons for the Vaadin perspective in Eclipse
  - Designer crashing when design has empty user attributes
  - Proxy authorization header is not preserved on license check

#### 1.3.1 & 2.1.1

Released 2017-05-04

[List of bug fixes in issue
tracker](https://github.com/vaadin/designer/milestone/9?closed=1)

  - Icon preview for property editor
  - Support themes in resource folder
  - Support SBT projects
  - Move palette mode buttons to tool window
  - Exception setting value after date field resolution was changed
  - Experimental Chromium browser for Eclipse

#### 1.3.0 & 2.1.0

Released 2017-05-03

  - You can now set "PropertyId" in the properties panel for components,
    it will show up in java as `@PropertyId` on the field
  - You can now right-click on a layout in the outline, and choose
    "Replace with…" in the context menu, e.g to replace a Vertical
    layout with a Horizontal layout.

#### 2.0.2

Released 2017-03-24

IntelliJ only.

[List of bug fixes in issue
tracker](https://github.com/vaadin/designer/milestone/8)

  - Editing properties throws exception in IntelliJ 2017

#### 2.0.1

Released 2017-03-20

[List of bug fixes in issue
tracker](https://github.com/vaadin/designer/milestone/7?closed=1)

  - Grid throws exception when item-type is not String

#### 2.0.0

Released 2017-03-01

Vaadin Designer 2.0 for Vaadin 8. Requires Vaadin 8 and Java 8. Does not
support Vaadin 7. You can have both Designer 1 and 2 installed at the
same time. Design files in Vaadin 7 project, will be opened in Designer
1.x and designs in Vaadin 8 project will be opened in Designer 2.x.

#### 2.0.0.beta3

Released 2017-02-27

Vaadin Designer 2.0 now supports the final version of Vaadin Framework
8.

#### 2.0.0.beta2

Released 2017-02-09

Second beta version of Vaadin Designer 2.0 for Vaadin Framework 8 Beta.
Contains bugfixes and improvements for working with Framework 8
projects.

#### 2.0.0.beta1

Released 2017-01-03

First beta version of Vaadin Designer 2.0 for Vaadin Framework 8 Beta.
Requires Vaadin Framework 8 and Java 8. Does not support Vaadin
Framework 7. You can have both Designer 1 and 2 installed at the same
time. Design files in Vaadin 7 project, will be opened in Designer 1.x
and designs in Vaadin 8 project will be opened in Designer 2.x.

#### 1.2.2

Released 2017-03-24

IntelliJ only.

[List of bug fixes in issue
tracker](https://github.com/vaadin/designer/milestone/8)

  - Editing properties throws exception in IntelliJ 2017

#### 1.2.1

Released 2017-02-23

[List of fixed issues in the issue
tracker](https://github.com/vaadin/designer/milestone/4?closed=1)

  - Double-click on palette now adds to components parent
    ([\#8](https://github.com/vaadin/designer/issues/8))

#### 1.2.0

Released 2016-12-30

New responsive templates available in "New Design" wizard for creating
responsive application navigation and views. See more details and usage
in: [Designer 1.2 - Responsive templates user
guide.](https://vaadin.com/designer/designer-1_2-responsive-templates-user-guide)

[List of bug fixes in issue
tracker](https://github.com/vaadin/designer/milestone/3?closed=1)

  - Fixed wrap With TabSheet throwing an Exception
  - Prevent dropping a component inside its own content
  - Fixed Designer failing silently when using Vaadin snapshots

#### 1.1.2

Released 2016-12-12

[List of bug fixes in issue
tracker](https://github.com/vaadin/designer/milestone/2?closed=1)

In Eclipse and IntelliJ

  - Fix bug missing Designer's project properties (for ip/port
    configuration)
  - Fix bug when set margin property for Grid Layout
  - Fix unicode characters problem in editor (to display unicode
    characters in IDE UI e.g properties table, make sure that the font
    using for IDE appearance supports those characters)
  - Improve the design load performance in Windows and macOS
  - Fix the exception "Provider id not found" when closing Idea
  - Fix bug DomID property is missing in properties table

In IntelliJ only

  - Fix the palette issue in IntelliJ IC 2016.3
  - Fix bug "Write access failure" in IntelliJ IC 2016.3

#### 1.1.1

Released 2016-11-24

[List of bug fixes in issue
tracker](https://github.com/vaadin/designer/milestone/1?closed=1)

  - Double click in Palette implemented \[Intellij\]
  - Use design icon for design components in Palette \[Intellij\]
  - Show custom component name in Outline \[Intellij\]
  - Fix Outline expansion and scrolling when model changes \[Intellij\]
  - Set default tab header link in Tabsheet

#### 1.1.0.final

Released 2016-10-26

In Eclipse and IntelliJ

  - Fix NPE when dropping in panel child
  - Fix GridLayout unexpand child does not restore columnExpandRatio
  - Fix ColorPicker and ColorPickerArea throw exception on delete
  - Fix for Changing expandRatio does not move infobar
  - Fix session lock exception when adding GridLayout as root in
    Intellij
  - Lock session for error indicator removal
  - Prevent websocket from timing out
  - Fix provider not found when closing cloned editors
  - Improve prompt in error report email
  - Update client-side when palette drag is cancelled

In IntelliJ only

  - Fix double text editors when open java files
  - Fix bug cannot undo in source mode
  - Add context menu to outline
  - Prevent exceptions when closing editor during indexing
  - Update client-side when palette drag ends
  - Fix unregister provider issues
  - Improve prompt in error report email
  - Add scrollbar for content property editor
  - Fix image render off paper

#### 1.1.0.beta3

Released 2016-10-06

In IntelliJ

  - Java companion file issues fixed
  - Settings dialog implemented
  - Custom components scanning improved
  - 3rd party browser component updated
  - Not working custom themes on Windows problem fixed
  - Designer module views misbehavior corrected
  - Numerous bug fixes which were gathered from different feedback
    channels

In Eclipse

  - Missing scrollbar was added to content property editor
  - User notification in case of invalid template introduced
  - DnD to panel child bug fixed
  - Bugfixes, small UX improvements

#### 1.0.11

  - This maintenance release improves the New Design Wizard so that if
    you are using our new Maven archetypes which does not contain
    a *src/main/resources* folder the wizard will create one for you
    (if you want)\!

#### 1.0.10

  - [Eclipse Neon Windows compatibility
    resolved](https://dev.vaadin.com/query?group=status&milestone=Vaadin+Designer+1.0.10)

#### 1.0.9

  - [\#18931](https://dev.vaadin.com/ticket/18931) GridLayout OOBE in
    some situations; was causing multiple problems

#### 1.0.8

  - [\#19485](https://dev.vaadin.com/ticket/19485) No more grid lines in
    preview mode
  - [\#19607](https://dev.vaadin.com/ticket/19607) No more error
    messages if you mistype a source URL
  - [\#19762](https://dev.vaadin.com/ticket/19762) No more vaadin-ui
    package mappings in design file when you mistype a Vaadin core
    component

#### 1.0.7

  - [\#19195](https://dev.vaadin.com/ticket/19195) Component Alignment
    in GridLayout doesn't work
  - [\#19551](https://dev.vaadin.com/ticket/19551) Button to open
    external browser window does not work
  - [\#19614](https://dev.vaadin.com/ticket/19614) Project name is null
    in the external browser preview title
  - [\#19666](https://dev.vaadin.com/ticket/19666) Clicking on a link
    component in a design hangs editor
  - [\#19679](https://dev.vaadin.com/ticket/19679) JavaScriptException
    in VEditorViewport.java
  - Fixed an issue opening the design when package declaration for
    custom component contains capital letters.

#### 1.0.6

  - Fixed Panel replacing content when something is dropped on it
  - Fixed compilation problem in some environments due to non UTF-8
    character in autogenerated code
  - Fix for "The Designer failed to load system browser"
  - Fix for multiple JavaScriptException(s) reported by users
  - Fix for "unable to set url for a Link"

#### 1.0.5

  - Fixed a bug in opening context menu in Outline
  - Fixed designer styles not updating when a project has styles.css
  - Multiple other fixes. See the complete list of fixed
    defects [here](https://dev.vaadin.com/query?status=accepted&status=closed&component=Designer&milestone=Vaadin+Designer+1.0.5&col=id&col=summary&col=milestone&col=status&col=owner&col=type&col=priority&order=priority).

#### 1.0.4

  - Multiple improvements to the UI look when using the Dark Eclipse
    theme
  - Improved drag\&drop when layout has spacing turned on
    ([\#19379](https://dev.vaadin.com/ticket/19379))
  - Fixed a rare situation when the Designer could overwrite the license
    file ([\#19373](https://dev.vaadin.com/ticket/19373))
  - Fixed yet another case causing the context menu not to open
  - Styles from templates no longer imported multiple times
    ([\#19439](https://dev.vaadin.com/ticket/19439))

#### 1.0.3

  - Rulers now align properly
     ([\#19029](https://dev.vaadin.com/ticket/19029), [\#19181](https://dev.vaadin.com/ticket/19181))
  - Deleting a project with a design still open no longer causes
    problems
    ([\#19174](https://dev.vaadin.com/ticket/19174), [\#19175](https://dev.vaadin.com/ticket/19175))
  - Updated to use Vaadin 7.5.10; previous releases could leave designs
    locked after reading
    ([\#19299](https://dev.vaadin.com/ticket/19299))

#### 1.0.2

  - It is now possible to use add-ons with themes packaged into a jar
    ([\#18951](https://dev.vaadin.com/ticket/18951)). For instance, you
    might have run into this issue if you use Vaadin Spreadsheet in your
    project.
  - The Designer no longer causes a unnecessary
    "com.vaadin.designer.prefs" to be added to all your projects'
    settings ([\#19196](https://dev.vaadin.com/ticket/19196)).
  - The Outline context menu now opens on Windows even if the clipboard
    contains binary data
    ([\#19202](https://dev.vaadin.com/ticket/19202)).
  - Two situations that could cause an exception when switching to
    Preview mode were identified and fixed
    ([\#19173](https://dev.vaadin.com/ticket/19173), [\#19279](https://dev.vaadin.com/ticket/19279)).

#### 1.0.1

  - The companion Java file is now updated on disk when the design is
    saved (not while designing)
  - Adjusting viewport size no longer marks design as modified
  - Made external preview live-updating (push) more robust on slow
    connections/computers
  - Fixed missing/wrong texts in styling dialog
  - Rephrased confusing Vaadin version warning message
  - Fixed null pointer when invoking the top-level File-\>new-\>Vaadin
    Design menu item ([\#19165](https://dev.vaadin.com/ticket/19165))
  - Some preferences moved from project to global scope

#### 1.0.0

First stable release 2015.10.22
