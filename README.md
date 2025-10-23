🧠 CLAUDE PROMPT — Panopticon System Consolidation
🧾 CONTEXT

You are acting as a system integration AI for the Panopticon Analytics Project.
Your task is to combine multiple interdependent scripts into a unified, well-commented, and aesthetically consistent Apps Script codebase for use within Google Sheets and front-end HTML dashboards (Wall.html, MM.html, Map.html, Terminal.html).

You will not alter the data logic or creative tone — only organize, clarify, and modularize.

🧩 FILES PROVIDED

You have access to the following project components:

Pan_Analytics.txt – Core analytics engine.
Builds Pan_Master and Pan_Dict. Runs only on checked-in guests (Form Responses (Clean), column AB = "Y").

V_Cramer.txt – Correlation and association engine.
Computes Cramér’s V between categorical variables; produces V_Cramers_Categories and Edges_Top_Sim.

Guest_Similarity.txt – Compatibility layer.
Filters strong guest-to-guest and guest-to-category edges; produces final similarity and pairing data.

Pan_Validation.txt – Integrity and system-rebuild layer.
Ensures all required sheets exist; manages rebuild triggers and menu items.

⚙️ OBJECTIVE

Combine the files into a single, cohesive system script (Panopticon_Main.gs), following these rules:

1. Modular Structure

Organize functions under clear section headers:

/* ==============================
 * I. VALIDATION & SYSTEM SETUP
 * II. DATA BUILDERS
 * III. ANALYTICS COMPUTATION
 * IV. SIMILARITY ENGINE
 * V. VISUALIZATION EXPORTS
 * ============================== */


Each function must be self-contained and callable individually.

2. Function-by-Function Integration

Do not merge function bodies unless redundant.

Maintain original naming (buildPanMaster(), computeVMatrix(), buildGuestSim(), etc.).

Place dependency comments above functions indicating required inputs.

Example:
