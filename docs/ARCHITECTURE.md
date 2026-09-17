# Storyling architecture

## Core flow

1. Onboarding: target language, CEFR level, interests
2. Story generation: AI creates a level-appropriate story
3. Reader/player: text + audio + playback controls
4. Quiz: comprehension and vocabulary checks
5. Vocabulary: missed words are saved for review
6. Adaptation: future stories reuse words the learner needs to practice
7. Progress: reading, listening, vocabulary, and quiz progress

## Main application areas

- `/` Home / library
- `/onboarding` Language and learner preferences
- `/story/:id` Story reader and audiobook player
- `/quiz/:id` Comprehension practice
- `/vocabulary` Vocabulary review
- `/progress` Learning progress
- `/profile` Profile and settings

## Data/backend

The existing Storyling Supabase project is reused. The new frontend must connect to that existing backend rather than creating a new Supabase project.

No real credentials belong in GitHub. Local environment variables are loaded from `.env.local`.

## Development principle

Build the application in small vertical slices. Each slice should connect the interface to real data before moving to the next feature.
