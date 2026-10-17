# Valluvam (வள்ளுவம்)

### Thirukkural · Open Knowledge · AI

**An open-source initiative to make Thirukkural searchable, understandable, and accessible in Tamil, English, and Tanglish.**

Valluvam is part of **TamilX — First-Class Tamil for the AI Era**, an initiative to build open data, knowledge, and AI infrastructure for Tamil.

> **1,330 Kurals. Multiple languages. Open knowledge for everyone.**

---

## 🌱 Why Valluvam?

Thirukkural is one of the most important works of classical Tamil literature, containing 1,330 couplets organized into 133 chapters.

Its wisdom continues to inspire people across generations. However, discovering a relevant Kural can be difficult when people search using different languages, transliterations, or everyday expressions.

Valluvam aims to make this knowledge easier to discover and explore.

A user should be able to search in Tamil, English, or Tanglish and find relevant Kurals without needing to know the exact wording.

**Our goal is not just to digitize Thirukkural. It is to make its knowledge accessible to the digital world.**

---

## 🎯 Vision

Build an open, structured, and reusable Thirukkural knowledge base that developers, educators, researchers, and AI applications can use.

Valluvam begins with multilingual search and evolves toward source-grounded explanations, semantic exploration, and AI-powered learning.

---

## 🔎 What Can Valluvam Do?

### 1. Search in Tamil

Example:

`நட்பு பற்றி திருக்குறள்`

Discover Kurals related to friendship.

### 2. Search in English

Example:

`What does Thirukkural say about friendship?`

Find relevant couplets using English search terms and meanings.

### 3. Search in Tanglish

Example:

`natpu pathi thirukkural enna solluthu?`

Search using Tamil expressed in the Roman alphabet, with support for common spelling variations.

### 4. Search by Kural Number

Example:

`133`

Retrieve the corresponding couplet.

### 5. Explore Knowledge

Discover relationships between Kurals, chapters, themes, concepts, and interpretations.

### 6. AI-Powered Explanations — Future

Enable users to explore Kurals through simple Tamil explanations, English meanings, contextual examples, and educational questions, grounded in verified sources.

---

## 🧱 Why Open Knowledge Format (OKF)?

Valluvam uses **Open Knowledge Format (OKF)** as its intended canonical knowledge representation.

Rather than keeping Thirukkural content in an application-specific database, we aim to maintain human-readable, version-controlled knowledge documents that can be reused across applications.

Our design principles include:

- **Human-readable:** Knowledge should be easy to inspect and improve.
- **Structured:** Each Kural should have a stable identity and consistent metadata.
- **Interoperable:** Other applications should be able to consume the knowledge.
- **Traceable:** Sources and attributions should be recorded.
- **Version-controlled:** Changes should be reviewable through Git.
- **AI-ready:** The knowledge should support retrieval, semantic search, and AI applications.

OKF is the canonical knowledge layer. Search indexes and application-specific representations can be generated from it.

See the [Open Knowledge Format project](https://github.com/antonykanagu/thirukkural-okf) for the existing Thirukkural OKF work that can inform our implementation.

---

## 🏗️ Architecture

```text
             TamilX Valluvam
                    |
                    v
           OKF Knowledge Base
                    |
        +-----------+-----------+
        |           |           |
        v           v           v
      Kurals     Chapters     Sources
        |           |           |
        +-----------+-----------+
                    |
                    v
             Search Index
                    |
        +-----------+-----------+
        |           |           |
        v           v           v
      Tamil      English    Tanglish
        |           |           |
        +-----------+-----------+
                    |
                    v
             Search Results
                    |
                    v
         Future AI Applications
```

The initial implementation prioritizes correctness, discoverability, and simplicity. Semantic search and AI-generated explanations will be added incrementally.

---

## 📚 Knowledge Model

Each Kural should be represented as a distinct knowledge record.

A record may include:

| Field | Purpose |
|---|---|
| `id` | Stable identifier |
| `kural_number` | Canonical Kural number |
| `chapter_number` | Chapter reference |
| `chapter_title` | Tamil chapter title |
| `text_tamil` | Original Tamil couplet |
| `transliteration` | Romanized Tamil |
| `meaning_tamil` | Verified Tamil explanation |
| `meaning_english` | Attributed English translation |
| `search_terms` | Tamil, English, and Tanglish terms |
| `sources` | Source and edition information |
| `license` | Applicable usage and redistribution terms |
| `status` | Draft, reviewed, or verified |

The exact schema will evolve as the project develops.

Original text, translations, traditional commentaries, and AI-generated explanations must remain distinguishable.

---

## 🚀 Roadmap

### Phase 1 — Knowledge Foundation

- [ ] Establish the Valluvam OKF conventions.
- [ ] Identify a reliable source for all 1,330 Kurals.
- [ ] Record source, edition, attribution, and licensing information.
- [ ] Create validation rules for knowledge records.
- [ ] Publish the initial repository structure.

### Phase 2 — Multilingual Search

- [ ] Search by Kural number.
- [ ] Search exact Tamil text.
- [ ] Search English meanings and keywords.
- [ ] Support Tanglish transliteration.
- [ ] Handle common spelling variations.
- [ ] Return the original Tamil couplet with its source.

### Phase 3 — Semantic Discovery

- [ ] Search by topic and meaning.
- [ ] Connect related Kurals and concepts.
- [ ] Improve ranking across languages.
- [ ] Evaluate search quality using community-tested queries.

### Phase 4 — Valluvam AI

- [ ] Explain Kurals in simple Tamil.
- [ ] Explain concepts in English.
- [ ] Compare attributed commentaries.
- [ ] Provide contextual examples.
- [ ] Support learning questions and quizzes.
- [ ] Ground generated explanations in verified knowledge.

### Phase 5 — Open Ecosystem

- [ ] Publish reusable APIs.
- [ ] Provide machine-readable knowledge exports.
- [ ] Enable integration with other AI agents.
- [ ] Build educational tools and community applications.

---

## 🛠️ Technology Direction

The initial technology choices will favor simplicity and reproducibility.

| Component | Initial direction |
|---|---|
| Knowledge representation | Open Knowledge Format |
| Source control | Git and GitHub |
| Data validation | Python |
| Search | SQLite FTS or equivalent |
| Application API | Python and FastAPI |
| Prototype UI | Streamlit or a lightweight web application |
| Semantic search | Embeddings, introduced later |
| AI explanations | Pluggable LLM integration |

These are implementation choices, not mandatory dependencies of the knowledge format.

The initial search experience should work without requiring an LLM API.

---

## 🤝 Contributing

Valluvam welcomes contributions from Tamil scholars, educators, students, developers, researchers, and open-source enthusiasts.

You can contribute by:

- Improving Tamil text accuracy.
- Reviewing transliterations.
- Adding search terms and topic associations.
- Verifying source references.
- Improving the OKF schema.
- Building search and indexing tools.
- Testing Tamil, English, and Tanglish queries.
- Developing AI-powered learning experiences.
- Improving documentation and accessibility.

### Contribution principles

1. Preserve the canonical Tamil text.
2. Provide references for corrections and interpretations.
3. Respect copyright and source licenses.
4. Keep AI-generated content distinguishable from verified sources.
5. Make changes reviewable and reproducible.

---

## 📜 Data, Attribution, and Licensing

The software license and the licenses of knowledge content may differ.

Before redistributing any source dataset, translation, commentary, or derived content, verify its licensing terms and attribution requirements.

The project aims to preserve provenance for every content source and to use openly reusable material wherever possible.

A repository-wide license and content-specific licensing policy will be documented as the initial sources are finalized.

---

## 🌍 Part of TamilX

**TamilX — First-Class Tamil for the AI Era**

TamilX is an open-source initiative to build the data, knowledge, and AI infrastructure needed to make Tamil a first-class digital language.

Valluvam is one step toward that vision: transforming a timeless literary work into accessible, structured, and reusable digital knowledge.

---

## ❤️ Join Us

You do not need to be an AI researcher to contribute.

You can help by verifying one Kural, improving one transliteration, testing one search query, or writing one line of code.

> **Don't just preserve Tamil. Build the future in Tamil.**

**Valluvam — Thirukkural. Connected Knowledge. Open AI.**

**Built in the open, for everyone.**
