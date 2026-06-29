# Chapter 04 - Tasker Metadata Knowledge Base

## 4.1 Objective

Atlas Nexus uses official Tasker metadata as the authoritative source for XML generation. Reverse engineering is used only to validate behavior, never to replace official metadata.

## 4.2 Metadata Sources

1. capabilities.xml
2. datadef.xml
3. tasker.js
4. Verified Task XML Exports

## 4.3 Responsibilities

### capabilities.xml

Defines:
- Actions
- Events
- States
- Conditions
- Plugins
- Feature availability

### datadef.xml

Defines:
- Action parameters
- Argument types
- Default values
- XML schema
- Serialization rules

### tasker.js

Defines:
- JavaScript API
- Runtime interface
- Helper functions
- Variable access

### Verified XML

Defines:
- Real importable XML
- Action IDs
- Parameter ordering
- Export behavior
- Compatibility validation

## 4.4 Knowledge Hierarchy

Metadata
→ XML Schema
→ Template
→ Pattern
→ Engine
→ Runtime

## 4.5 Engineering Rules

- Never invent Action IDs.
- Never invent XML attributes.
- Always validate against exported XML.
- Prefer official metadata over inferred structures.
- Use verified exports to confirm implementation details.

## 4.6 AI Generator Requirements

The XML Generator shall load metadata before XML generation.
Generation must remain deterministic and metadata-driven.