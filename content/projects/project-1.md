---
date: 2025-06-02T18:37:37
description: "Bill and "
featured_image: ""
tags: []
title: "Receipt Analyzer - Personal Expense Tracker"
---

"Receipt Analyzer," is a robust personal finance management tool designed to automate the tracking and settlement of household expenses. At its core, it features an intelligent receipt parser, currently optimized for receipts from Biedronka (a popular Polish supermarket chain). All parsed information is meticulously stored in a PostgreSQL database hosted on AWS, ensuring scalability and reliability.

The application is engineered for high availability and ease of deployment, utilizing Docker for containerization and hosted on an AWS EC2 instance. This setup streamlines the migration process and ensures consistent performance.

Core Functionality & Problem Solving
The primary function of the Receipt Analyzer is to streamline shared expense management. It addresses the common challenge of splitting bills among partners or housemates by intelligently prorating costs. When a new receipt is processed, the system interactively prompts the user to specify the percentage of each item's price to be paid by the "main user" – providing a consistent reference point for expense allocation.

To further automate this process, the application employs a unique "card description" recognition system. Upon encountering a new, unique card description (e.g., a specific payment method or card ID), it queries the user to assign it to a specific individual (e.g., "Husband," "Wife," "Roommate 1," etc.). This one-time assignment allows the system to automatically identify who paid for subsequent receipts associated with that card, significantly reducing manual input and ensuring accurate expense attribution.

Future Enhancements & Vision
The vision for Receipt Analyzer extends far beyond basic expense tracking, leveraging the rich historical purchase data collected:

AI-Powered Shopping Assistant: Future integration with an LLM (Large Language Model) API will enable users to "converse" with their purchase history. Imagine asking questions like "What did I buy last week?" or "How much did we spend on groceries last month?".
Smart Alerts & Forecasts: The LLM integration will also facilitate setting up alerts and forecasts for product expiration dates, helping to minimize waste and manage inventory more effectively.
Diet Tracking Integration: A planned integration with a diet tracking application aims to automatically identify when purchased food items have been consumed, providing a more holistic view of dietary habits and consumption patterns.
Current Status
The project is currently functional in a local development environment, with the core parsing and database functionalities running smoothly. The PostgreSQL database on AWS is fully operational. I am actively engaged in the process of migrating the application to AWS EC2 using Docker, simultaneously refining the codebase and optimizing the database structure for enhanced performance and maintainability.