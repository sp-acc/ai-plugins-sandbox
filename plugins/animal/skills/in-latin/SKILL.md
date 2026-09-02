---
name: in-latin
description: >-
  Educational skill that gives an animal's scientific (Latin) name, family, and
  classification plus a short natural-history note. Use whenever the user invokes
  /in-latin, or asks for the Latin name, scientific name, binomial/species name, or
  taxonomy of an animal — "what is the scientific name of a dolphin?", "lion in
  latin", "/in-latin shark", "taxonomy of the wolf", "how do you say eagle in
  latin". Trigger even when the phrasing doesn't say "scientific" or "latin" but
  clearly asks how a creature is formally classified, and when /in-latin is used
  with no animal given.
argument-hint: "[animal name]"
user-prompt: /in-latin
---

# in-latin — Animal names in Latin

This skill exists for learning: when someone names an animal and wants its
scientific (Latin) name, you give the correct binomial plus enough
classification and natural-history context to make the answer stick. A Latin
name is a fixed fact, not something to improvise — a confidently wrong answer
teaches the wrong fact, which is worse than saying you're unsure.

## Resolve what the user is asking for

- Normalize the input before answering: drop articles and possessives ("the",
  "a", "my"), ignore capitalization, and reduce plurals and obvious variants
  ("lions" → "lion", "lioness" → "lion", "dodos" → "dodo") to the plain animal
  name.
- Accept recognizable animal names in any language, and answer in English. It is
  friendlier and just as educational to answer "perro" with the dog's binomial
  as it is to refuse — a hard English-only rule just turns away a curious user.
- A request may name several animals at once ("wolf and tiger") or name none (a
  bare `/in-latin`). Answer each animal separately with its own block; when no
  animal is given, pick 2–3 familiar animals from different habitats (e.g., one
  terrestrial, one marine, one avian) so the response shows the range of the
  skill.

## Identify the taxon honestly

Most common names do not map 1:1 to a species. Work out which of these cases
you're in before you write anything:

- **A single famous species.** "Lion", "tiger", "giraffe" → one binomial
  (*Panthera leo*, *Panthera tigris*, *Giraffa camelopardalis*). Answer
  directly.
- **A whole group.** "Shark", "bear", "dolphin", "monkey" are not species —
  "dolphin" is roughly 40 species in the family Delphinidae. Give the group and
  family, name the best-known species as a concrete example, and briefly mention
  1–2 others. Don't present one species as if it were the only one.
- **Genuinely ambiguous between a few well-known species.** "Wolf" most often
  means the gray wolf (*Canis lupus*), but a red wolf (*Canis rufus*) also
  exists; "puma", "cougar", and "mountain lion" are all one animal. If you answer
  the most common species, say that is the one you're using; if the ambiguity
  could mislead, name the main alternatives.
- **You aren't sure of the binomial.** Rare or obscure animals, common names you
  can't confidently place: say plainly that you're not certain and give what you
  do know (genus or family) rather than guessing at a species. Honest partial
  information beats fabricated precision.
- **Not a real animal.** Fictional or mythical creatures ("dragon", "unicorn")
  have no scientific name. Note that there is no Latin name for a fictional
  creature and invite a real animal instead.

## Response format

Use these labeled blocks so answers scan consistently, and italicize
*Genus species*. Adapt the block rather than forcing every answer into one
shape.

For a single species:

```
Common Name: Lion
Scientific Name: *Panthera leo* (Family: *Felidae*)
Status: Extant
Description: 2–3 sentences on appearance, habitat, or behavior worth knowing.
```

For an extinct species, replace "Extant" with the era or disappearance:

```
Common Name: Dodo
Scientific Name: *Raphus cucullatus* (Family: *Columbidae*)
Status: Extinct — last recorded in the late 17th century on Mauritius
Description: ...
```

For a group or category term, swap the species fields for a group + example
structure:

```
Group: Bear (Family: *Ursidae*)
Example species: Brown bear — *Ursus arctos*
Also includes: American black bear (*Ursus americanus*), polar bear (*Ursus maritimus*)
Status: Extant
Description: ...
```

When the request names several animals (or none), emit one block per animal.
Keep the description to 2–3 sentences and make it genuinely informative — size,
where it lives, something distinctive — rather than generic filler.
