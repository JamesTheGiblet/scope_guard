#📐 ScopeGuard - Profitability Analyzer**ScopeGuard** is a specialized calculator for freelancers, agencies, and consultants working on **Fixed-Fee Projects**. It visualizes the "Profitability Cliff"—the exact moment a project becomes unprofitable due to scope creep, revisions, and technical debt.

It helps answering the question: *"At what point does this $5,000 project stop paying me my target rate of $75/hr?"*

##✨ Key Features* **Effective Rate Visualizer:** A real-time chart showing how your hourly rate decays as hours are added to a project.
* **Scope Simulator:** Add "Events" like *Legacy Code*, *Vague Briefs*, or *Reusable Assets* to see how they impact your bottom line.
* **Complexity Modeling:** Adjust for Simple Sites vs. Complex SaaS applications to get realistic baseline hour estimates.
* **Break-Even Detection:** Instantly calculates exactly how many hours you have left before you are "paying the client" to work.
* **Blueprint UI:** A clean, technical interface designed for professionals.

##🚀 Quick Start1. **Download** the `index.html` file.
2. **Open** it in any web browser (Chrome, Firefox, Edge, Safari).
3. **Start Planning:**
* Set your **Fixed Fee** (e.g., $10,000).
* Set your **Target Hourly Rate** (e.g., $125/hr).
* Add **Scope Events** to see how "Scope Creep" destroys your margin.



##🧮 The Math Behind the ToolScopeGuard relies on an **Inverse Relationship** model. Unlike hourly billing (where revenue scales with time), fixed-fee revenue is static, meaning your effective rate drops with every hour worked.

###Logic Breakdown1. **Baseline:** The tool estimates initial hours based on the fee and a complexity multiplier.
2. **Stack Impact:**
* **Scope Creep:** Increases the denominator (Lowers Rate).
* **Assets/Tools:** Decreases the denominator (Increases Rate).


3. **Strict Contract:** Toggling this reduces total hours by 10%, simulating the efficiency of "No Revision" clauses.

##⚙️ CustomizationYou can define your own "Scope Events" in the `config` object within the source code:

```javascript
const config = {
    presets: [
        // Negative values ADD hours (Bad for Fixed Fee)
        { id: 1, name: 'Scope Creep', value: -8, icon: '👻', desc: '+8 Hours' },
        
        // Positive values REMOVE hours (Good for Fixed Fee)
        { id: 5, name: 'Reusable Asset', value: 8, icon: '📦', desc: '-8 Hours' }
    ]
};

```

##🛠️ Tech Stack* **Frontend:** HTML5, CSS3, Vanilla JavaScript.
* **Charting:** [Plotly.js](https://plotly.com/javascript/).
* **Icons:** [FontAwesome](https://fontawesome.com/).

##📄 LicenseThis project is open-source. Feel free to modify it for your agency or freelance practice.
