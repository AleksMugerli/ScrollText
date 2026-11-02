# ScrollingText – Mobile Application Development

An educational Android application designed to manage and display extensive textual information efficiently on mobile devices. This project focuses on mastering structural text formatting, implementing vertical scrolling view mechanics, configuring nested multi-column layouts, and handling simple interface interactive triggers.

---

## 🎯 Project Objectives

*   **Scrollable Container Integration:** Understanding structural layout boundaries by implementing a scroll view container designed to hold a single root group element.
*   **Multi-Column Presentation:** Implementing a side-by-side text layout by nesting an orientation-specific view group inside a scrollable viewport.
*   **Proportional Text Allocation:** Formatting distinct text sections, including forcing multi-line text wrapping for secondary information fields via explicit width thresholds while allowing primary content fields to absorb remaining horizontal space.
*   **Externalized Resource Architecture:** Ensuring strict separation of layout structures and actual text content by storing all visual string data systematically within localized resource files.

---

## 📱 Functional Architecture & Layout Description

The user interface isolates long-form content within a scrollable area, ensuring that text remains readable and navigation handles predictably across different screen heights.

1.  **View Hierarchy:** The application organizes content within a multi-layered view structure. A single parent layout handles the overarching vertical alignment, nesting an interactive scroll container that houses the body of the article.
2.  **Column Configuration:** Inside the scroll layer, a horizontal group structures the text into two distinct columns:
    *   **The Left Column:** A narrow text display dedicated to titles and subheadings. It features a constrained width fixed at 100dp, forcing longer headings to break into multiple lines neatly without spilling into adjacent text areas.
    *   **The Right Column:** A broad text display that expands dynamically to occupy all remaining screen width, accommodating long paragraphs of main article content fluidly.
3.  **Interactive Elements:** A submission trigger is positioned centered below the dual-column structure. When a user interacts with this component, the application executes a click event handler that displays an instant, short-lived contextual screen message confirming the comment submission.

---

## ❓ Worksheet Evaluation Answers

### 1. View Capacity of a Scroll Container
**Correct Option: b) One View or one ViewGroup**  
A standard scroll layout is engineered to host exactly one immediate child element. To incorporate multiple distinct visual fields (such as text columns and button controls) inside a scrollable area, developers must encapsulate them within a single parent layout group.

### 2. Side-by-Side Element Orientation
**Correct Option: a) android:orientation="horizontal"**  
To instruct a linear layout group to arrange its interior children sequentially from left to right across the screen rather than stacking them vertically, the distribution direction property must be explicitly set to a horizontal value.

### 3. Container Width Within a Scrollable Viewport
**Correct Option: b) android:layout_width="match_parent"**  
To guarantee that the nested content group expands fully to occupy the complete physical horizontal boundary of the device screen, its width configuration should be instructed to match the dimensions of its parent container.

### 4. Screenshots 
<img width="200" height="400" alt="Screenshot_20261102_000716_ScrollText" src="https://github.com/user-attachments/assets/2b6eeb2c-0637-4f85-93b9-9a34a24ba460" />
<img width="200" height="400" alt="Screenshot_20261102_000720_ScrollText" src="https://github.com/user-attachments/assets/9ce4ec7c-50b1-49c2-a32b-b208dcd42535" />
