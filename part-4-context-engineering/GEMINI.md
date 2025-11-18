## 1. Project Overview & Purpose

This project contains the English source files for Google Workspace's public
documentation, which is published on https://developers.google.com/workspace.
Its purpose is to provide comprehensive guides, tutorials, and reference
materials to help users understand and utilize Google Workspace products and
services effectively.

---

## 2. Documentation Audience & Goals

* **Primary Audience:** The content targets a technical audience, including
    external cloud developers, software architects, enterprise system
    administrators, and data scientists.
* **Documentation Goals:** The primary goal is to enable users to successfully
    learn, adopt, and manage Google Workspace services. This includes guiding
    them through initial setup, providing comprehensive API and command-line
    references, explaining architectural concepts, and offering best practices
    and troubleshooting advice.

---

## 3. Style & branding guidelines

* **Tone & Voice:** The tone must be professional, clear, and direct,
    consistent with Google Workspace's brand voice.
* **Line Length**: All markdown lines, including code blocks and prose,
    **must not exceed 80 characters**.
* **Style Guide Authority**: Your content must adhere to the style guidelines
    provided in Google's developer documentation style guide. All the style
    guidance lives within the following directory:
    https://developers.google.com/style

### 3.1 Product Naming and Branding (MANDATORY)

All references to Google Workspace products, features, and APIs **MUST** use
the approved product names.
*   **Single Source of Truth:** The definitive list of all approved product
        name variables is available on this page
        https://developers.google.com/workspace/products
*   **Branding Context and Guidelines:** Before writing any content, you
        **MUST** thoroughly review all files in the branding directory to
        understand the full usage context:
        https://developers.google.com/style/product-names
*   **Verification Step:** Before finalizing any documentation edit or
        creation, you must verify that all product names have been used.
        Failure to do so will result in incorrect and inconsistent
        documentation.

### 3.2 Content templates and structure

Each page of content must follow a template and content type:

   * Quickstart: Give users a quick and fast way to get familiar with using a
     product or API feature. These task-based guides should be short (~15min to
     complete). By the end, the developer should have a "Hello world!"
     experience.

   * How-to guide (Task): A how-to guide provides procedural, action-oriented
     instructions to help a user achieve a single, specific goal. It answers
     the question "How do I...?" by guiding the user through a numbered sequence
     of steps, leading to a clear and expected outcome.

   * Concept: A concept document provides background knowledge that helps users
     understand a product, feature, or technology. It answers "What is...?"
     and "Why is it important?" questions by explaining principles,
     definitions, and the relationships between components, enabling users to
     make informed decisions and effectively use the product.

   * Troubleshooting: A troubleshooting guide helps users diagnose and solve
     problems. It is structured around a problem-solution format, typically
     presenting a symptom (the problem), potential causes, and a sequence of
     steps (the solution) to correct the issue.
