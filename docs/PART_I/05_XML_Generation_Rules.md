# Chapter 05 - XML Generation Rules

## 5.1 Objective
This chapter defines the mandatory rules for generating Tasker XML within Atlas Nexus.

## 5.2 Core Principles
- XML-first engineering
- Metadata-first generation
- Deterministic output
- Incremental deployment
- Round-trip validation

## 5.3 Metadata Sources
Generation shall use the following sources in order of precedence:
1. capabilities.xml
2. datadef.xml
3. tasker.js
4. Verified Tasker XML exports

## 5.4 Generation Rules
1. Never invent Action IDs.
2. Never invent XML attributes.
3. Use only verified actions and parameters.
4. Generate Task XML before Profile XML.
5. Generate Project XML only after Task validation.
6. Prefer reusable templates and patterns over duplicated actions.
7. Keep each Task focused on a single responsibility.

## 5.5 Validation
Every generated XML artifact must successfully complete Generate → Import → Execute → Export → Compare before being accepted into the repository.
