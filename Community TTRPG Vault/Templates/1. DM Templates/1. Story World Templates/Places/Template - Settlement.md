![Showcase](https://i.gyazo.com/51f7b904dbffdf061d24766ffc07dcfd.jpg)

![Showcase](https://i.gyazo.com/b6e0330ee8288c3c26cc0e43fb229154.png)

# How to use:
Below is a template, when placed in Obsidian will look like the showcase above. To use this, you simple need to cope and past the box below and find the two lines telling you to delete them. Once you have done this, with the correct plugins installed, you will have the above template. This template talks to a Settlement Database folder that I have not made a template for, so be patient for that!

```
DELETE THIS LINE AND THE ONE ABOVE

> [!infobox]
> # `=this.file.name`
> **Pronounced:**  "`=this.Pronounced`"
> ![[PlaceholderImage.png]]
> ###### Info
>  |
> ---|---|
> **Alias** | `=this.alias` |
> **Type** | `=this.type` |
> **Population** | `=this.population` |
> **Theme** | TBD |
> **Region** | `=link(this.Region)` |
> **Terrain** | `=this.terrain` |
> ###### Politics
>  |
> ---|---|
> **Ruler(s)** | TBD |
> **Leaders** | TBD |
> **Govt Type** | `=this.GovtType` |
> **Defenses** | `=this.defences` |
> **Religion(s)** | `=link(this.religions)` |
> ###### Commerce
>  |
> ---|---|
> **Imports** | TBD |
> **Exports** | TBD |
> ###### Groups
> [[🔰 Group Database|Add New Group]]
> ```dataview 
table join(Type, ", ") AS Type
WHERE contains(Location, this.file.name) AND contains(NoteIcon, "Group")
SORT Type ASC

# **`=this.file.name`**
> [!info|bg-c-purple]- Overview
TBD

## Map
> ```leaflet
> id: TBD
> image: [[PlaceholderImage.png]]
> height: 600px
> width: 640px
> lat: 50
> long: 50
> minZoom: 1
> maxZoom: 5
> defaultZoom: 1
> unit: meters
> scale: 1
> darkMode: false
> ```

## Notable Locations

> [!info|bg-c-purple]- Districts
TBD

> ###### Notable Shops/Services
> [[💲 Shop & Service Database|Add New Shop/Service]]
> ```dataview
table join(Type, ", ") AS Type, join(link(AffiliatedGroup), ", ") AS "Affiliated Group(s)"
WHERE contains(Location, this.file.name) AND contains(NoteIcon, "Shop")
SORT file.name ASC

> ###### Notable Points of Interest
> [[❓ POI Database|Add New Point of Interest]]
> ```dataview
table join(Type, ", ") AS Type, join(link(AffiliatedGroup), ", ") AS "Affiliated Group(s)"
WHERE contains(Location, this.file.name) AND contains(NoteIcon, "POI")
SORT file.name ASC

## Notable Characters

> ###### Notable Characters
> [[👨‍👩‍👧‍👦 NPC Database|Add New NPC]]
> ```dataview
table Art, Party1Standing AS "Party 1 Standing", join(Occupation, ", ") AS "Occupation(s)", join(link(AssociatedGroup), ", ") AS "Associated Group(s)", join(link(AssociatedReligion), ", ") AS "Associated Religion(s)"
WHERE contains(Location, this.file.name) AND contains(NoteIcon, "Character") AND !contains(Condition, "Dead")
SORT file.name ASC

## History
TBD

## DM Notes
### Plot Hooks


### Hidden Details


### General Notes

DELETE THIS LINE AND THE ONE BELOW
```

