# WikiSearch Devlog
A search engine built in Go, indexed on Wikipedia. Built from scratch to understand
how search actually works (I want to try this without any use of AI).

## Goals
- Parse Wikipedia XML dumps
- Build an inverted index with TF-IDF
- Implement a query engine
- Phase 3 (eventually): hybrid semantic search + LLM synthesis

## Phases
| Phase | Dataset | Goal |
|-------|---------|------|
| 1 | Simple English Wikipedia (~800MB) | Build and validate the full pipeline |
| 2 | Full English Wikipedia (~105GB) | Stress test at scale |
| 3 | Same + embeddings + LLM | Hybrid search, natural language answers |

---

## Phase 1 — Simple English Wikipedia

### 2026-02-17 — Preplanning and Project Setup
**12:00** </br>
I've been thinking about this for a while. Finally starting. Read the Google PageRank
paper (The Anatomy of a Large-Scale Hypertextual Web Search Engine) — understood the
broad strokes but lost the plot around forward vs inverted indexing. Will make more
sense once I'm actually building it.

I don't know Go. I don't know how any of this fits together yet. But that's the point — I want to build things I have to figure out.
- Download the Simple English Wikipedia dump as a manageable starting point
- Build the full pipeline: parse → tokenize → index → search
- Don't move to Phase 2 until Phase 1 actually works

**13:34** </br>
The first task is to learn Golang. I will use [Sriniously's Production Grade Go from Scratch](https://www.youtube.com/playlist?list=PLui3EUkuMTPhxPWqrrIvr5ckMepIbMilJ) YouTube playlist for this.

*Footnote: Devlog structure and formatting assisted by AI. All content, decisions, and code are my own.*