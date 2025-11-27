# cyberbullying-detection-and-escalation-tool
A lightweight, offline, real-time system Cyberbullying Detection and Escalation Tool using Python, Trie, and SQLite. Detects offensive text in real time with multi-language support, context analysis, and severity-based actions like warnings, suspension, and bans. Lightweight, offline, and ideal for small platforms
This project implements a lightweight, offline system designed to detect cyberbullying in text-based communication. It uses Python along with Trie data structures, contextual text analysis, and an SQLite database to classify harmful messages and determine appropriate escalation actions based on user behavior and message severity.

The system begins by preprocessing the input text, normalizing it, and performing keyword detection using a Trie for efficient O(n) lookup. Offensive keywords are organized by severity levels, allowing the system to classify messages as mild, moderate, or severe. In addition to keyword detection, the tool evaluates contextual cues such as uppercase intensity, punctuation patterns, and the presence of long aggressive words. These contextual factors increase the severity score and help differentiate between direct and implied harmful intent.

An SQLite database tracks user history, storing previous offenses, timestamps, and lockout durations. If repeated harmful messages occur within a short timeframe, the system increases the severity score to reflect repeat behavior. Based on the final score, the tool issues warnings, temporary suspensions, or permanent bans. All messages and actions are logged for audit and review.

The system supports English, Spanish, and French, making it suitable for multilingual environments. It is designed to run fully offline, making it ideal for schools, colleges, small platforms, gaming communities, and secure internal communication systems where lightweight and explainable moderation is preferred.

Planned enhancements include voice-based detection, image and meme analysis, and the use of machine learning models to capture deeper contextual meaning and sarcasm.
Features

Real-time keyword detection using Trie

Multi-language support (English, Spanish, French)

Context analysis for tone and punctuation

Severity scoring and automatic escalation

User history tracking with SQLite

Offline, fast, and easy to run
