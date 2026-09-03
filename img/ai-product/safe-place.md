# Safe Place — AI Product Writing & Development

## Overview

Safe Place is an emotion-aware AI web application that provides primary psycho-emotional support through empathetic AI-powered dialogue.

The system analyzes both text and voice modalities using multimodal emotion recognition, extracting paralinguistic features to better understand the user's emotional state.

---

## Development

- Full-stack: Flask backend, responsive frontend, Google Gemini API
- 18 REST API endpoints with JWT authentication and bcrypt hashing (12 rounds)
- Normalized database schema with 9 interrelated tables
- Rule-based fusion algorithm with adaptive weighting — O(1)
- Validated on 88 messages with zero false positives on critical cases

---

## Writing — UX Strings

| Context | Before | After |
|---|---|---|
| Auth error | "Authentication failed." | "That password does not match. Try again." |
| Daily check-in | "Begin emotional assessment." | "How are you feeling right now?" |
| Heavy tone | "Depressive sentiment detected." | "Sounds like today has been a lot. Want to write more?" |
| Button | "Submit" | "Send feedback" |
| Empty state | "No data" | "Nothing here yet. Add your first project." |
| Action | "See" | "Read more" |
| Button | "Add" | "Start a new chat" |

---

## Writing — System Prompt

Authored the complete system prompt for the AI assistant:

- Empathetic tone and emotional validation rules
- CBT (Cognitive Behavioral Therapy) principles
- Active listening and constructive questioning
- Crisis protocols with emergency contact integration
- Formatting guidelines (short paragraphs, no jargon, natural language)
- Multilingual support (Ukrainian + adapts to user language)

---

## Writing — Content

### 10 Self-Help Techniques
4-7-8 Breathing · 5-4-3-2-1 Grounding · Progressive Relaxation · Emotion Journal · Visualization · Circle of Influence · Reframing · STOP Technique · Cold Water · Music Therapy

### 4 Blog Articles
1. How to Talk About Feelings Without "I Feel Awkward"
2. Sleep and Anxiety: The Cycle You Can Break
3. Meditation for Beginners: 5 Simple Steps
4. Nature as Medicine: How Green Spaces Affect Mental Health

### Crisis Support Page
Trust hotlines, emergency services, online support chats, and "What to do in an acute crisis" guides.

---

## Research

- Published paper: "Interpreted Rule-Based Multimodal Fusion for Emotion Recognition" — III International Scientific and Practical Conference (2026) — Oral presentation
- Published paper: "Development of a virtual interlocutor web application 'Safe Place' using generative AI" — XI Interuniversity Seminar (2026) — Oral presentation
- 1st place, University Scientific Research Competition (2026)
- Multimodal approach improves accuracy by 17% vs text-only
- 4 critical cases detected (9.1%) with zero false positives

---

*Safe Place is not a therapist. It is a first line of emotional support.*
