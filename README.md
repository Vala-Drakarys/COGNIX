# COGNIX AI — Diagnostic Agent

**Team Novix | Agent-a-Thon 2026**

## Overview

COGNIX AI is an adaptive learning system designed to understand where a student is struggling and help guide their learning journey.

For the Agent-a-Thon, we are building a focused **Diagnostic Agent** rather than the complete COGNIX system.

The Diagnostic Agent investigates why a student is struggling with a programming concept, tests possible misconceptions or prerequisite gaps, revises its hypothesis when evidence contradicts it, involves the student in confirming the diagnosis, and stores the resulting learner state.

## Problem

A student may say:

> "I understand recursion, but I can't solve recursion problems."

A normal AI response may immediately provide an explanation. The problem is that the visible failure does not necessarily reveal the actual cause.

The student may have difficulty with:

- Base-case reasoning
- Call-stack tracing
- Parameter/state tracking
- A prerequisite concept

COGNIX treats diagnosis as an investigation rather than a single answer.

## Diagnostic Agent

The agent follows a controlled loop:

```text
Student Problem
      ↓
Observe
      ↓
Form Hypothesis
      ↓
Ask Diagnostic Check
      ↓
Evaluate Evidence
      ↓
 ┌───────────────┐
 │               │
Contradicted   Supported
 │               │
 ↓               ↓
Revise        Confirm
 │               │
 └───────→ Store State
                ↓
               Stop
