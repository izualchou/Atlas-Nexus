# Chapter 02 - Engineering Principles

## 2.1 Overview
This chapter defines the immutable engineering principles governing Atlas Nexus AI Generator.

## 2.2 XML-first
Tasker XML is the primary engineering artifact. Runtime implementation follows XML rather than preceding it.

## 2.3 Metadata-first
All generation must be derived from official Tasker metadata (capabilities.xml, datadef.xml, tasker.js) or verified exports.

## 2.4 Validation-first
Every generated artifact must be validated through import, export, and round-trip comparison before acceptance.

## 2.5 Incremental-first
Develop using small, independently importable Task XML units. Avoid replacing existing verified tasks.

## 2.6 Reusable-first
Actions compose Templates, Templates compose Patterns, Patterns compose Primitives, Primitives compose Engines.

## 2.7 Deterministic-first
Given identical inputs and metadata, the generator must produce identical XML.

## 2.8 Engineering Rules
- Never guess undocumented XML.
- Prefer verified metadata over inference.
- Separate Runtime, Generator, and Deployment responsibilities.
- Treat Project XML as a higher abstraction than Task XML.
- Preserve backward compatibility whenever practical.

## 2.9 Definition of Done
A feature is complete only after XML generation, successful import, execution verification, export, and round-trip validation.