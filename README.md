# 🧪 Week 4 Assignment: Test Design Techniques Lab

## 📌 Objectives
- Apply **black-box** (equivalence partitioning, boundary analysis, decision tables) and **white-box** (statement, decision coverage) techniques.
- Identify and document bugs via GitHub Issues.
- Summarize findings in a structured `Test_Report.md`.

---

## 🛠️ Setup
1. **Code**: Use the provided [e-commerce filter system](index.html).
2. **Testing Tools**:
   - Jest (for white-box testing)
   - Mermaid.js (for diagrams, optional)

---

## 📋 Tasks

### 1. Black-Box Testing (3 Hours)
#### Techniques to Apply:
| Technique          | Target Component       | Expected Artifact       |
|--------------------|------------------------|-------------------------|
| Equivalence Partitioning | Brand/Price/Storage filters | `test_cases/partitions.csv` |
| Boundary Analysis  | Storage input (64GB-1024GB) | `test_cases/boundary_tests.csv` |
| Decision Table     | Filter combinations    | `test_cases/decision_table.md` |

#### Steps:
1. Test valid/invalid inputs for each filter.
2. Document **2+ bugs** as GitHub Issues with:
   ```markdown
   - **Steps**: Select price range "1000-1500"
   - **Expected**: Shows iPhone 14 Pro ($1499)
   - **Actual**: No products displayed
   - **Label**: `black-box`

## 2. White-Box Testing (2 Hours)

### 🎯 Coverage Goals
| Function          | Coverage Target      | Test File               |
|-------------------|----------------------|-------------------------|
| `applyFilters()`  | 100% statement       | `tests/coverage.test.js` |
| `renderProducts()`| Decision coverage    | `tests/render.test.js`   |

### 📝 Steps
1. **Write Jest tests** to cover:
   - All paths in `applyFilters()` (validation, filtering logic)
   - Decision points in `renderProducts()` (empty array, product rendering)

2. **Identify untested branches**:
   ```javascript
   // Example: This branch isn't tested in renderProducts()
   if (products.length === 0) {
     // Empty state handling
   }
3. **Create GitHub Issues for code flaws (1+ required):**
      ```markdown
    - **File**: `index.html`, Line 105
    - **Bug**: Storage filter requires exact match (should be "≥")
    - **Expected**: `storage=128` should show products with 128GB+
    - **Actual**: Only shows exact 128GB matches
    - **Label**: `white-box`

