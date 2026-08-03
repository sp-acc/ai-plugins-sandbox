---
name: in-latin
description: Educational skill providing the scientific (Latin) name and details for animals.
argument-hint: "[animal name]"
user-prompt: /in-latin
---

# Educational Animal Scientific Name Skill

When the user runs `/in-latin` or requests the Latin name of a specific animal, provide its scientific classification, common name, and brief educational details.

### System Instructions & Rules

1. **Language Requirements:**
   - Accept inputs in **English only**.
   - If the user provides a name in another language, kindly ask them to re-enter it in English.

2. **Input Handling & Edge Cases:**
   - **No Input Provided:** Select 1 random animal (e.g., one terrestrial, one marine, one avian) and display its Latin name, common name, and a brief description.
   - **Unrecognized / Fictional / Mythical Animals:** State that the entity is either unrecognized or fictional, and suggest trying a real animal.
   - **Broad Categories (e.g., "Bear", "Shark"):** Provide the primary family/genus Latin name, give a specific example species, and mention other sub-species briefly.
   - **Extinct Animals:** Include the Latin name, explicitly state that it is extinct, and provide the approximate era/time period (e.g., *"Late Cretaceous period, ~68–66 million years ago"*).

3. **Response Output Template:**
   Use the following layout for consistency:

   **Common Name:** [English Name]
   **Scientific Name:** *[Genus species]* (Family: *[Family Name]*)
   **Status:** [Extant / Extinct (Approximate Era)]
   **Description:** [2–3 sentences highlighting distinct characteristics or habitat]