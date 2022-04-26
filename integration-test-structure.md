# Integration Test

> Description of the Integration Suites Test created for the [Makerdao Mips Website](https://mips.makerdao.com/)

---

## List view

* Go Top Functionality

```md
#1 Component Initially invisible
#2 On Scroll Down Component enters from right
#3 On Hover message is shown
#4 On Click Scroll goes up smoo_🐮_oothly
#5 On scoll Up Component Stay visible
#6 On Scroll until top Component goes out to the right
```

### Search Bar

* Regular Text (**8h**)

```md
When entering text in the search box and hitting Enter it searchs and displays the MIPs containing the search text in the Title or the Summary fields. The search is case insensitive, and it works like that except for these cases: 1- when the user types MIP and a number (eg: MIP1, MIP22) 2- When the users type $ at the beginning. In the first case it searchs for MIPs whose number starts with the given one (eg:MIP5 will display MIP5, MIP50, MIP55 and so on). In the second case it will do a Special search (it's described below).

```

* `MIPS` Special Search
* Dollar Sign search `$`

  * `@` Search
  The @ searchs for the MIPs having the entered Status (**5h**)
  * `#` Tags Search
  The # search for the MIPs having the entered tag (**5h**)
  * `AND OR ()` Combined Operations (**8h**)
  When using AND it searchs for the MIPS having both conditions true
  When using OR it searchs for the MIPs having any of the conditions true

### Normal View

* Regular View It displays the MIPs in a table using these columns: #, Title, Summary, Status and Links initially sorted by # (**3h**)
* Sort By Title View Clicking the Title header sorts the list by Title ascendingly or descendingly (**3h**)
* Sort By Status Clicking the Status header sorts the list by Status ascendingly or descendingly (**3h**)
* Pagination on Scroll Initially only a subset of MIPS are loaded. Scrolling down the window loads and makes visible next MIPS of the list. (**5h**)
* Component opens on MIPS where they are present (**5h**)
* SubProposals opens on MIPS where they are present (**5h**)

---

### MipSets View (**8h**)
When clicking "MIP sets" on Views menu it displays the MIPs grouped by these tags: collateral-onboarding-mipset, core-governance-mipset, core-unit-framework-mipset. The view contains the same table of MIPS with an accordion component in which each of the mentioned tags is a group which is initially closed. Clicking any of the groups opens it and displays the list of the MIPs it contains using the same columns: #, Title, Summary, Status and Links. 

### Multi-queries View (**13h**)
On the menu Views->Core Units displays MIPs subproposals using different filters criteria using query params. The list is displayed showing on the top the name of the specific Core Unit + Subproposals. In the list there are two groupings: "Active Subproposals" and "Archive". The URL has differente query params: customViewName (The name of the Core Unit), Active_Subproposals (the conditions for the first grouping), Archive (the conditions for the second grouping), hideParents (boolean value indicating whether the MIPs are displayed with their parents), shouldBeExpandedMultiQuery (boolean value indicating if the groupings should be displayed expanded). The list displays the same column headers: #, Title, Summary, Status, Link. 

## Details View (**21h**)
When clicking a row of the MIPs list it opens the given MIP details view. This view contains on the left the Headings, the full content of the MIP in the middle and various fields on the right.

On the left content:

  * Clicking any of the headings on the left scrolls the middle content to such heading position. Also, when the user scrolls down or up the middle content the corresponding heading is highlighted on the left. Also when opening a given heading the address is updated in the address bar of the browser adding the heading id after #.

  In the middle content:
  - Hovering over a MIP link opens a popup containing the Title and the Summary of the MIP. If the link is of a component inside a MIP then the popup contains also the Title and Summary of the component.
  
  On the right content:
   *  One of the fields is Tags which contains all the tags of the MIP, clicking one of the tags opens a list of all MIPS that contain this tag. 
   *  Clicking the Author value opens a list of MIPs whose author is that one.
   *  Clicking the Contributor value opens a list of MIPs whose contributor is that one.
   *  The References field contains links to MD files, clicking any of them opens the MD viewer with it.
## MD Viewer View (**13h**)

The MD viewer opens when clicking a MD file link. It contains on the left links to the headings of the document and the full content on the right. Clicking any of the headings on the left scrolls the full content (in the middle) to the corresponding section. Also, scrolling the full content down or up highlights the corresponding heading on the left. Besides when opening a given heading the address is updated in the address bar of the browser adding the heading id after #.
## Extra

* 404 View
  When entering an unexistent URL the Not Found page is displayed. It contains a descriptive message and a link to the Home page. (**3h**)

* Menu Interactions
  The three submenus are displayed when clicking the corresponding menu items: Learn, Views and Get in Touch. In each submenu the subsubmenu appear when hovering over the corresponding submenu item. Clicking a item not containing a submenu opens the corresponding view. (**3h**)

* Dark Mode Test
When click the icon the site switchs to dark or normal mode (**5h**)
* Change Language Feature (**8h**)
The component allows to switch between Spanish and English language. When switching the language these elements are shown translated: 
  * The MIPs table headers and the header of the table itself
  * The menu items
  * In the MIPs details view: The fields labels on the right section. The headings on the left (some are translated already and some are not), the three links of the top part of the full 
  content section (GitHub, Forum and Votes).
* News Interactions (**13h**)
    * Each new must be displayed over the main table (list of MIPs) on the home page. The popup displays the icon according to the "type" field of the new (GREEN, YELLOW or RED). The fields displayed are "title" and "description". Each new is displayed again according to the time declared in its record ("timelock" field).
