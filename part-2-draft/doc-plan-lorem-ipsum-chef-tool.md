# My Documentation Plan: The `lorem_ipsum_chef` Tool for Gemini CLI

| Detail | Description |
| :--- | :--- |
| **Feature** | **`lorem_ipsum_chef`**: A custom Gemini CLI tool that generates highly context-specific placeholder text based on culinary themes (e.g., pizza, tacos, soup) instead of standard Latin filler. |
| **Documentation Location** | `https://geminicli.com/docs/tools/lorem-ipsum-chef` |
| **Launch Date (Target)** | Next Minor CLI Release (v1.4.0) |

---

## 1. Tool Schema and Functionality

| Component | Detail |
| :--- | :--- |
| **Tool Name (Schema ID)** | `lorem_ipsum_chef` |
| **Schema Description** | "Generates paragraphs of high-quality, culinary-themed placeholder text (`lorem ipsum`) for document mockups or testing." |
| **Input Parameters** | The model parses the user prompt for required parameters: **`theme`** (e.g., 'pizza', 'taco') and **`count`** (number of paragraphs). |
| **Output** | A multi-line string containing the generated culinary placeholder text. |

---

## 2. Content Outline & Structure

The final documentation page will adhere strictly to the requested heading structure, which is typical for Gemini CLI tool documentation:

* Introduction
* Description
* Arguments
* How to use [tool_name] with the Gemini CLI
* [tool_name] examples
* Important notes
