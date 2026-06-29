# Chapter 03 - Tasker XML Engineering Methodology

## 3.1 Purpose
This document defines the engineering workflow used to build Atlas Nexus XML artifacts. It is based on verified Tasker exports and official metadata.

## 3.2 Engineering Hierarchy

Action
→ Template
→ Pattern
→ Primitive
→ Primitive DAG
→ Engine
→ Runtime
→ Generator

Each layer may only depend on lower verified layers.

## 3.3 Action Layer
The Action layer consists exclusively of verified Tasker actions and parameters recovered from exports or official metadata.

## 3.4 Template Layer
Templates encapsulate reusable Action combinations with fixed parameter layouts.

Examples:
- VAR_SET
- VAR_CLEAR
- WAIT
- PERFORM_TASK
- RETURN
- HTTP_REQUEST
- JAVA_FUNCTION

## 3.5 Pattern Layer
Patterns compose multiple templates into reusable execution logic.

Examples:
- SET → RETURN
- SET → WAIT → RETURN
- VERIFY → DECISION
- OBSERVE → VERIFY → RECOVERY

## 3.6 Primitive Layer
Primitives provide stable functional units independent of business logic.

Examples:
- LOG_PRIMITIVE
- DELAY_PRIMITIVE
- HTTP_PROBE
- JAVA_QUERY

## 3.7 Engine Layer
Engines orchestrate primitives into complete execution pipelines.

Observe Engine
Verify Engine
Decision Engine
Recovery Engine
Action Engine

## 3.8 Runtime Layer
Runtime coordinates engine execution, scheduling, variables, persistence and recovery.

## 3.9 Generator Layer
The AI Generator consumes metadata, architecture specifications and templates to produce deterministic Tasker XML.

## 3.10 Validation Workflow
Design → Generate XML → Import → Execute → Export → Compare → Accept