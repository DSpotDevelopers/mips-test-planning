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

* Regular Text

```md
When entering text in the search input and hitting 
Enter or stopping the typing it searchs and displays 
the MIPs containing the search text in the Title or the Summary fields.

```

* `MIPS` Special Search
* Dollar Sign search `$`

  * `@` Search
  The @ search for the MIPs having the entered Status
  * `#` Tags Search
  The # search for the MIPs having the entered tag
  * `AND OR ()` Combined Operations
  When using AND it searchs for the MIPS having both conditions true
  When using OR it searchs for the MIPs having any of the conditions true

### Normal View

* Regular View It displays the MIPs in a table using these columns: #, Title, Summary, Status and Links initially sorted by #
* Sort By Title View Clicking the Title header sorts the list by Title ascendingly or descendingly
* Sort By Status Clicking the Status header sorts the list by Status ascendingly or descendingly
* Pagination on Scroll Initially only a subset of MIPS are loaded. Scrolling down the window loads and makes visible next MIPS of the list.
* Component opens on MIPS where they are present
* SubProposals opens on MIPS where they are present

---

### MipSets View
When clicking "MIP sets" on Views menu it displays the MIPs grouped by these tags: collateral-onboarding-mipset, core-governance-mipset, core-unit-framework-mipset

### Multi-queries View
On the menu Views->Core Units displays MIPs list using different filters criteria using query params.

## Details View
When clicking a row of the MIPs list it opens the given MIP details view. This view contains on the left the Headings, the full content in the middle and the various fields values on the right.

## MD Viewer View

The MD viewer opens when clicking a MD file link. It contains on the left links to the headings of the document and the full content on the right.
## Extra

* 404 View
  When entering an unexistent URL the Not Found page is displayed. It contains a descriptive message and a link to the Home page.

* Menu Interactions
  The three submenus are displayed when clicking the corresponding menu items:Learn, Views and Get in Touch. In each submenu the subsubmenu appear when hovering over the corresponding submenu item.

* Dark Mode Test
When click the icon the site switchs to dark or normal mode
* Change Language Feature
The component allows to switch between Spanish and English language
* News Interactions
