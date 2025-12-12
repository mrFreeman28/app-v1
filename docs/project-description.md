# AI Calendar Assistant (Telegram)

This project is a conversational AI assistant that plans, schedules, and manages calendar events through a Telegram bot.

The assistant allows a user to create, update, reschedule, and review meetings and time blocks using natural language. The system translates human instructions into structured actions, applies scheduling rules and constraints, and executes changes directly in the user’s calendar.

The goal is not chat.  
The goal is execution.

## Core Idea

Instead of manually managing calendars, links, and reminders, the user interacts with a Telegram bot in plain language.

**Example:**  
“Schedule a 30-minute call with Alex next week”

The assistant:
- understands intent and constraints
- checks calendar availability and rules
- proposes valid time slots if needed
- confirms with the user
- creates or updates the calendar event

No UI. No dashboards. Conversation is the interface.

## Key Capabilities

- Natural language task and meeting scheduling via Telegram
- Calendar conflict detection and resolution
- Time slot suggestions when constraints are ambiguous
- Rule-based scheduling (working hours, buffers, priorities)
- Calendar integrations (starting with Google Calendar)
- Persistent memory for user preferences and habits

## Design Principles

- **Deterministic execution, not AI guesswork**  
  The LLM parses intent only. All scheduling logic is rule-based.

- **Minimal user friction**  
  Ask only when necessary. Default intelligently.

- **Conversation as control**  
  Telegram is the primary and only interface.

- **Opinionated by design**  
  The assistant respects predefined rules instead of asking permission for everything.

## High-Level Architecture

- **Telegram Bot**  
  User interaction and confirmations

- **AI Intent Parser**  
  Converts free-form language into structured actions

- **Scheduling Engine**  
  Applies rules, resolves conflicts, proposes time slots

- **Calendar Integration**  
  Executes changes via calendar APIs

- **Memory & Rules Store**  
  Stores preferences, constraints, and history

## Non-Goals

- Productivity coaching or habit tracking
- Complex UI or dashboards
- Autonomous decision-making without confirmation
- Multi-user team scheduling in early versions

## Intended Use

This project is built primarily for personal use as a private scheduling assistant.  
It is designed to be extensible for additional calendars, messaging platforms, and advanced automation later.

## Status

Early development.  
Focused on correctness, clarity, and reliability over features.