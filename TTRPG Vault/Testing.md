# The Test
Hello! This is a tes!

> ###### Notable Characters
> [[👨‍👩‍👧‍👦 NPC Database|Add New NPC]]
> ```dataview
table Art, Gender, Race, join(Occupation, ", ") AS "Occupation(s)", join(link(AssociatedGroup), ", ") AS "Associated Group(s)", join(link(AssociatedReligion), ", ") AS "Associated Religion(s)"
WHERE contains(Location, this.file.name) AND contains(NoteIcon, "Character") AND !contains(Condition, "Dead")
SORT choice(Type = "Player", "1", choice(Type = "VIP", "2", choice(Type = "Hostile", "3", choice(Type = "Family", "4", choice(Type = "Friend", "5", choice(Type = "NPC", "6", "7")))))) ASC

