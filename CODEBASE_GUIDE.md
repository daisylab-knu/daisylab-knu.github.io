# DaisyLab Blog Codebase Guide

This document provides an overview of the `daisylab-knu.github.io` repository to help AI agents understand its structure and how to navigate/modify the codebase.

## Overview
This repository contains the source code for the **DAISY LAB (Data Analytics & Intelligent System)** blog/website at KNU. It is built using **Jekyll**, a static site generator in Ruby.

## Key Directories & Files
*   `_config.yaml`: The main Jekyll configuration file. It contains site-wide settings like title, plugins, layout defaults for collections, and theme settings.
*   `_members/`: This directory holds Markdown (`.md`) files for each lab member. 
    *   **Member Files**: Files like `Jiho-Kim.md` contain front matter with member details (name, role, image, links). The `role` field (e.g., `pi`, `phd`, `ms`, `undergrad`) dictates where they appear on the Team page.
*   `team/index.md`: The main team page. It dynamically lists members from the `_members` collection using Jekyll includes, categorizing them by their roles (e.g., Professor, PhD Students, MS Students, Undergraduate Students, Alumni).
*   `projects/`: Contains the projects overview. The `projects/index.md` file renders a list of projects pulling from the `_data/projects.yaml` file.
*   `_data/`: Contains YAML data files that power various sections of the site.
    *   `projects.yaml`: Contains data about research projects.
    *   `citations.yaml`: Likely used for publications or references.
*   `_posts/`: Contains blog posts.
*   `_styles/` & `_scripts/`: Directories for custom CSS/Sass and JavaScript files respectively.
*   `_includes/` & `_layouts/`: Jekyll templates for HTML structural components and page layouts.

## Typical Workflows
1.  **Adding a Member**: Create a new Markdown file in `_members/` with the appropriate front matter (name, role, image, description, links). The site will automatically pull this data into the `team/index.md` layout.
2.  **Updating Projects**: Modify `_data/projects.yaml` to update the list of featured projects shown on the projects page.
3.  **Creating a Post**: Add a new `.md` file to `_posts/` with the standard Jekyll date format (`YYYY-MM-DD-title.md`) and front matter.

## Technologies Used
*   **Jekyll**: Static Site Generator.
*   **YAML**: For configuration (`_config.yaml`) and data (`_data/`).
*   **Markdown**: For content creation (`_posts`, `_members`, pages).
*   **Liquid**: Templating language used inside HTML components and layouts (e.g., `{% include list.html %}`).

> [!TIP]
> When modifying pages that display lists of items (like Team or Projects), verify the filter conditions (e.g., `filter="role == 'pi'"`) in the Liquid tags (`{% include ... %}`) to ensure your changes to data files or front matter will render correctly.
