# Release notes for Vaadin Designer

Vaadin Designer is available for Vaadin platform and Vaadin Framework 8. 

There is also separate product for Vaadin Framework 7. Release notes for that product can be found from https://github.com/vaadin/designer/blob/master/RELEASE-NOTES-FW7.md

The latest preview version for Vaadin platform and Framework 8 is
[Vaadin Designer 4.0.0.final](#vaadin-designer-4x).

See the full list of [releases](#releases).

Please review the requirements below and the 
[FAQ](https://vaadin.com/designer/faq) if you have problems.

### Useful links

  - Site: <http://vaadin.com/designer>
  - Get started: <http://vaadin.com/designer/get-started>
  - Documentation: 
    - Vaadin 12: <https://vaadin.com/docs/v12>
    - Vaadin 11: <https://vaadin.com/docs/v11>
    - Vaadin 10 LTS: <https://vaadin.com/docs/v10>
    - Vaadin 8: <https://vaadin.com/docs/v8>
  - FAQ: <https://vaadin.com/designer/faq>

## Vaadin Designer 4.x

### What's new in 4.0
  - Redesigned Palette, Properties and Outline views for platform designs
  - Powerful ready-made snippets that allow you to quickly create content
  - Improved editing of text nodes
  - Performance improvements for large projects

## Vaadin Designer 3.x

### What's new in 3.1
  - Gradle project support
  - Works on Eclipse Photon
  - Part of Vaadin platform 11

### What's new in 3.0
  - New Polymer template syntax for designs
  - Write Javascript and CSS directly into to the design file
  - New Palette for web components and HTML elements
  - Use any Polymer web component from Bower or WebJars
  - Support for nested designs
  - Any Flow component can be used as a companion file
  - Companion files are not overwritten on update

#### Requirements
  - Windows 10 / OS X 10.12 / Ubuntu 16.04 LTS
  - Newest Chrome, Safari, Firefox or Edge.
  - Java 8, 9 and 10.
  - Eclipse Photon, Oxygen and Neon. Java EE edition.
  - JetBrains IntelliJ IDEA 2016, 2017, 2018. Community or Ultimate edition.
  - Vaadin 8, Vaadin 11.

#### Known Issues and Limitations

##### Vaadin platform
  - External preview doesn't work on IE11.
  - Horizontal scrolling using the trackpad doesn't work on Eclipse.
  - Some keyboard shortcuts, e.g. "delete", don't work in Eclipse Oxygen and Neon.

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

## Vaadin Designer 2.x

### What's new in 2.2

  - Provide a way to access exported component through getter
      - Project wide setting.
      - Default option is not to generate getter.
      - Could be changed later per Design file.
      - [See Vaadin Docs for more
        details](https://vaadin.com/docs/v8/designer/designer-wiring.html#designer.wiring.java.getter)
  - Delay theme recompilation until save (IntelliJ)

### What's new in 2.1

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

### What's new in 2.0

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

## Releases

#### 4.1.0

Released 2018-12-20

  - Introduced a setting for disabling the shared styles import. ([#1869](https://github.com/vaadin/designer/issues/1869))
  - Fixed Grid companion file connect issue. ([#1947](https://github.com/vaadin/designer/issues/1947))
  - Fixed "render channel is already closed" exception. ([#1861](https://github.com/vaadin/designer/issues/1861))

#### 4.0.0.final

Released 2018-11-29

  - Support Java 11. ([#1906](https://github.com/vaadin/designer/issues/1906))
  - Update form layout if colspan was changed. ([#1951](https://github.com/vaadin/designer/issues/1951))
  - Select newly added component in outline. ([#1933](https://github.com/vaadin/designer/issues/1933))
  - Handle Eclipse button press in property editor as text change. ([#1953](https://github.com/vaadin/designer/issues/1953))
  - Do not show Vaadin perspective popup for platform designs. ([#1911](https://github.com/vaadin/designer/issues/1911))
  - Fix exception when Material or None theme is used in Eclipse. ([#1939](https://github.com/vaadin/designer/issues/1955))

#### 4.0.0.beta2

Released 2018-11-22

  - Allow setting the component theme for the project. ([#1868](https://github.com/vaadin/designer/issues/1868))
  - Support adding new properties to elements. ([#1716](https://github.com/vaadin/designer/issues/1716))
  - Improve Outline rendering speed. ([#1940](https://github.com/vaadin/designer/issues/1940))
  - Fix issue with properties editing from the editor. ([#1950](https://github.com/vaadin/designer/issues/1950))
  - Allow platform design creation is Java class already exists. ([#1945](https://github.com/vaadin/designer/issues/1945))
  - Report unresolved import only when it's needed. ([#1939](https://github.com/vaadin/designer/issues/1939))
  - Fix exception during change of the Grid ItemType property. ([#1946](https://github.com/vaadin/designer/issues/1946))
  - Fix exception when closing design. ([#1941](https://github.com/vaadin/designer/issues/1941))

#### 4.0.0.beta1

Released 2018-11-7

  - New Outline, Palette and Properties are used by default. ([#1926](https://github.com/vaadin/designer/issues/1926))
  - Support dragging snippets from Palette to Outline. ([#1668](https://github.com/vaadin/designer/issues/1668))
  - Support reordering elements in Outline. ([#1675](https://github.com/vaadin/designer/issues/1675))
  - Hide `style` element in Outline by default. ([#1886](https://github.com/vaadin/designer/issues/1886))
  - Fixed missing connection icon for new element in Outline. ([#1904](https://github.com/vaadin/designer/issues/1904))
  - Fixed Lumo theme doesn't render correctly. ([#1920](https://github.com/vaadin/designer/issues/1920))

#### 4.0.0.alpha6

Released 2018-10-25

  - Outline support for the Java file connection. ([#1669](https://github.com/vaadin/designer/issues/1669))
  - Text node editing improved. ([#1718](https://github.com/vaadin/designer/issues/1718))

#### 4.0.0.alpha5

Released 2018-10-11

  - Editing support for property values.
  - Indicate missing snippet imports in palette.
  - Palette usability improvements.

#### 4.0.0.alpha4

Released 2018-09-26

  - Show project components separately in the palette. ([#1828](https://github.com/vaadin/designer/issues/1828))
  - Add selection for the outline. ([#1667](https://github.com/vaadin/designer/issues/1667))

#### 4.0.0.alpha3

Released 2018-09-12

  - Save the state of palette categories before and after filtering. ([#1618](https://github.com/vaadin/designer/issues/1618))
  - Improve palette icons using predefined colors. ([#1571](https://github.com/vaadin/designer/issues/1571))
  - Group component snippets according to their main web component. ([#1829](https://github.com/vaadin/designer/issues/1829))

#### 3.1.4

Released 2018-10-25

  - Fixed charts rendering problem. ([#1876](https://github.com/vaadin/designer/issues/1876))
  - Fixed issue with templates opening in starter. ([#1897](https://github.com/vaadin/designer/issues/1897))
  - Fixed problem with Eclipse external preview in Firefox. ([#1885](https://github.com/vaadin/designer/issues/1885))  
  - Flow editor support for keyboard shortcuts in Eclipse. ([#1863](https://github.com/vaadin/designer/issues/1863))
  - License dialog UX improvements. ([#1745](https://github.com/vaadin/designer/issues/1745))
  
#### 3.1.3

Released 2018-10-11

  - Handle unresolved imports from project.
  - Reduce amount of license checking requests.

#### 3.1.2

Released 2018-09-12

  - Double-clicking a Vaadin 11 palette item now adds a sibling instead of a child. ([#1689](https://github.com/vaadin/designer/issues/1689))
  - Fixed a bug that made the licensing banner of pro components like Charts appear.
  - Correctly write Grid's item type to Vaadin 8 designs if the type is a static inner class. ([#1847](https://github.com/vaadin/designer/issues/1847))
  - Don't associate Designer with Polymer 2 templates in non-Flow project anymore. ([#1843](https://github.com/vaadin/designer/issues/1843))

#### 3.1.1

Released 2018-08-28

  - Support different frontend folder locations in spring boot projects. ([#1812](https://github.com/vaadin/designer/issues/1812))
  - Fix widgetset load issue while opening platform designs. ([#1582](https://github.com/vaadin/designer/issues/1582))
  - New platform designs include styles by default. ([#1835](https://github.com/vaadin/designer/issues/1835))  

#### 3.1.0

Released 2018-08-08

  - Added compatibility with Vaadin 11.
  - Eclipse Photon support. ([#1804](https://github.com/vaadin/designer/issues/1804))
  - JxBrowser update to 6.21. ([#1805](https://github.com/vaadin/designer/issues/1805))  

#### 3.0.6

Released 2018-07-25

  - Automatically refresh external preview. ([#1741](https://github.com/vaadin/designer/issues/1741))
  - Add String as an argument for Flow generic types. ([#1749](https://github.com/vaadin/designer/issues/1749))
  - Render dragged snippet with multiple imports correctly. ([#1682](https://github.com/vaadin/designer/issues/1682))
  - Only refresh paper when editing a data binding. ([#1801](https://github.com/vaadin/designer/issues/1801))
  - Support Gradle webjars dependencies. ([#1811](https://github.com/vaadin/designer/issues/1811))
  - Stop editing properties whenever underlying table widget is reloaded. ([#1780](https://github.com/vaadin/designer/issues/1780))
  - Change design file if root components have been rearranged. ([#1799](https://github.com/vaadin/designer/issues/1799))

#### 3.0.5

Released 2018-07-04

  - Remember paper size and position for multiple design openings. ([#1713](https://github.com/vaadin/designer/issues/1713))
  - Fixed issue when edits were not saved to template text. ([#1591](https://github.com/vaadin/designer/issues/1591))
  - Fixed issue when server address was already reserved in Eclipse. ([#1665](https://github.com/vaadin/designer/issues/1665))
  - Colspan attribute change updates form layout automatically. ([#1800](https://github.com/vaadin/designer/issues/1800))
  - Web components detection logic improved. ([#1759](https://github.com/vaadin/designer/issues/1759))
  - Modify template text only when new content differs form the previous one. ([#1649](https://github.com/vaadin/designer/issues/1649))
  - Icon set updated for better UX. ([#1782](https://github.com/vaadin/designer/issues/1782))

#### 3.0.4

Released 2018-06-20

  - Eclipse proposes correct directory for Flow template in "New design" wizard. ([#1647](https://github.com/vaadin/designer/issues/1647))
  - Fixed issue when trying to create Flow template in Vaadin project. ([#1688](https://github.com/vaadin/designer/issues/1688))
  - Support multiple roots in snippet. ([#1788](https://github.com/vaadin/designer/issues/1788))

#### 3.0.3

Released 2018-06-07

  - CSS media queries now work correctly when paper size changes.
  - Changing the 'id' property updates the corresponding @Id in the Java file. ([#1604](https://github.com/vaadin/designer/issues/1604))
  - Lumo styles are properly applied in the editor. ([#1683](https://github.com/vaadin/designer/issues/1683))
  - Palette was removed from Preview mode. ([#1568](https://github.com/vaadin/designer/issues/1568))
  - Fixed issues in working with multiple open projects. ([#1593](https://github.com/vaadin/designer/issues/1593))
  - Fixed an issue in companion file detection if it contained multiple @HtmlImports. ([#1712](https://github.com/vaadin/designer/issues/1712))
  - Support Java 10 in Eclipse Designer. ([#1757](https://github.com/vaadin/designer/issues/1757))
  - Fixed rendering of the custom wysiwyg element. ([#1778](https://github.com/vaadin/designer/issues/1778))

#### 3.0.2

Released 2018-05-24

  - Improve the Javadoc in newly created Java companion file. ([#1779](https://github.com/vaadin/designer/issues/1779))
  - Allow dropping components in the paper empty space to add a new root. ([#1777](https://github.com/vaadin/designer/issues/1777))
  - Generate id for component based on existing label property. ([#1776](https://github.com/vaadin/designer/issues/1776))
  - Hide the current design in palette components. ([#1770](https://github.com/vaadin/designer/issues/1770))
  - Fit the initial paper size to viewport size. ([#1620](https://github.com/vaadin/designer/issues/1620))
  - External preview has the same styling as deployed Flow application. ([#1617](https://github.com/vaadin/designer/issues/1617))
  - Show the warning dialog for Java 10 users in Eclipse instead of crashing.

#### 3.0.1

Released 2018-05-09

  - Improvements to newly created designs and their Java companions. ([#1646](https://github.com/vaadin/designer/issues/1646))
  - Support running Designer on Java 9. ([#1744](https://github.com/vaadin/designer/issues/1744))
  - Stability improvements in Eclipse. ([#1753](https://github.com/vaadin/designer/issues/1753))

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

#### 2.2.3

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

#### 2.2.2

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

#### 2.2.1

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

#### 2.2.0

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

#### 2.1.4

Released 2017-06-13

[List of enhacements and bug fixes in issue
tracker](https://github.com/vaadin/designer/milestone/12?closed=1)

Enhacements:

  - Made opening designs in Eclipse faster
  - Create "~/.vaadin/designer/templates" if it does not exist

Bug fixes:

  - Templates in ~/.vaadin/designer/templates are not loaded
  - License dialog keeps showing with trial license

#### 2.1.2

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

#### 2.1.1

Released 2017-05-04

[List of bug fixes in issue
tracker](https://github.com/vaadin/designer/milestone/9?closed=1)

  - Icon preview for property editor
  - Support themes in resource folder
  - Support SBT projects
  - Move palette mode buttons to tool window
  - Exception setting value after date field resolution was changed
  - Experimental Chromium browser for Eclipse

#### 2.1.0

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

First beta version of Vaadin Designer 2.0 for Vaadin Framework 8.
Requires Vaadin Framework 8 and Java 8. Does not support Vaadin
Framework 7. You can have both Designer 1 and 2 installed at the same
time. Design files in Vaadin 7 project, will be opened in Designer 1.x
and designs in Vaadin 8 project will be opened in Designer 2.x.
