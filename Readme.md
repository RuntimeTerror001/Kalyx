# Kalyx 🌱

We built this because a professor told us *"I know the material is outdated. I just don't have the time."*

That stuck with us.

Kalyx takes a syllabus — any format, any subject — and turns it into lecture slides, instructor notes, and a full quiz bank. Not in a day. In under 3 minutes.

---

## The problem, honestly

Preparing one good module from scratch takes 10–12 hours. Most professors don't have that, so they reuse old decks, skip updating content, or compromise on assessment quality. Students end up learning things the industry moved past years ago.

This isn't a dedication problem. It's a time problem. And that's something we can actually fix.

---

## What Kalyx does

You upload a syllabus. We read it — not just the topic names, but the learning outcomes, the depth, the sequence. Then we generate:

- Lecture slides built around what students are supposed to *achieve*, not just what the topic is called
- Instructor notes for every slide — the *why* behind each point
- A quiz bank that actually tests thinking, not just memory (we use Bloom's Taxonomy to distribute questions across all 6 cognitive levels)

Everything exports as `.pptx`, `.pdf`, or directly to your LMS.

---

## Why it's not just "ChatGPT for slides"

Fair question. The difference is that Kalyx is anchored to your syllabus. It can't hallucinate topics that aren't in your course. Every slide maps back to a specific learning outcome. And the quiz engine doesn't give you 10 recall questions — it deliberately generates questions across all six cognitive levels, from "what is X" to "design a system that does X."

ChatGPT doesn't know the difference between a recall question and an evaluation question. Kalyx does.

---

## Stack

FastAPI backend, React frontend, GPT-4o for generation, LangChain to orchestrate the pipeline, SQLite for storage, OpenTelemetry for observability, python-pptx for export.

Nothing exotic. Everything chosen because it works and gets out of the way.

---

## How it works under the hood

```
syllabus (pdf / url / text)
    → parser extracts topics, outcomes, depth
    → langchain pipeline runs per topic
    → gpt-4o generates slides + notes + quizzes
    → bloom's classifier tags each question
    → python-pptx packages the output
    → professor downloads or exports to LMS
```

---

## Roadmap

- [x] Syllabus parser (PDF, URL, raw text)
- [x] Slide generation anchored to learning outcomes
- [x] Instructor notes per slide
- [x] Bloom's Taxonomy quiz engine
- [x] PPTX / PDF export
- [ ] React frontend with live preview
- [ ] Tone and depth controls
- [ ] LMS integration (Moodle, Canvas)
- [ ] Golden dataset evaluation pipeline
- [ ] Fine-tuned model on real syllabus data

---

## The name

Kalyx is from *calyx* — the protective structure around a flower bud before it blooms. Raw syllabus goes in. Complete learning experience comes out.

---

## Team

Built by Team Debug Devils at SRMIST — five CSE students who got tired of watching good professors waste hours on slides.

| | |
|---|---|
| Aahaan Sethi | Team Lead |
| Palak Singh | Backend |
| Anushka Sharma | AI / ML |
| Devashish Pandey | Frontend |
| Arushi Singh | Design & QA |

Capgemini Hackathon 2026 · Problem #14 · Education & Learning

---

*MIT License. Build on it.*
