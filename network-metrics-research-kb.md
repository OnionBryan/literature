# Network Metrics Research Knowledge Base
**Purpose:** Document research-based thresholds, metrics, and validated calculations for weak ties interactive tools.

**Last Updated:** 2025-11-12

---

## SOURCE 1: Granovetter (1973) - The Strength of Weak Ties

### EMPIRICAL DATA (N=282 job seekers in Newton, MA)

**Sample:**
- 282 professional, technical, and managerial workers
- 54 respondents found jobs through personal contacts

**Tie Strength Operationalization:**
- **Strong ties:** Saw contact "often" (≥2 times per week) → **16.7%** of job leads
- **Moderate ties:** Saw contact "occasionally" (>1x/year but <2x/week) → **55.6%** of job leads
- **Weak ties:** Saw contact "rarely" (≤1 time per year) → **27.8%** of job leads

**Key Finding:**
- **83.4%** of jobs found through moderate or weak ties (NOT strong ties)

### THEORETICAL CONSTRUCTS (No Empirical Thresholds)

**Forbidden Triad:**
- If A-B strong AND A-C strong → B-C tie will form
- ⚠️ NO PERCENTAGE THRESHOLD - just theoretical principle

**Local Bridges:**
- Definition: Tie representing only/shortest path between social circles
- ⚠️ Granovetter did NOT provide "optimal number of bridges"

**Overlap Principle:**
- "The degree of overlap in friendship networks varies directly with tie strength"
- ⚠️ NO SPECIFIC OVERLAP PERCENTAGES PROVIDED

**What Granovetter DID NOT Measure:**
- Network density thresholds
- Clustering coefficient ranges
- Optimal weak tie ratios
- Specific overlap percentages for strong vs weak ties
- Number of bridges that's "good" vs "bad"

---

## GAPS TO RESEARCH:

### 1. Network Density Thresholds
**Question:** What density ranges indicate sparse vs dense networks?
**Status:** ❌ NOT FOUND IN GRANOVETTER
**Need:** Research on social network density interpretation

### 2. Clustering Coefficient Ranges
**Question:** What clustering values indicate high redundancy?
**Status:** ❌ NOT FOUND IN GRANOVETTER
**Need:** Network analysis literature on clustering

### 3. Overlap Percentages
**Question:** How much overlap do strong ties typically have vs weak ties?
**Status:** ❌ NOT FOUND IN GRANOVETTER
**Need:** Empirical studies measuring friendship network overlap

### 4. Bridge Counts
**Question:** How many bridges is considered "good diversity"?
**Status:** ❌ NOT FOUND IN GRANOVETTER
**Need:** Research on structural holes and brokerage

### 5. Information Reach Calculations
**Question:** How to calculate unique reach accounting for overlap?
**Status:** ❌ NOT FOUND IN GRANOVETTER
**Need:** Network diffusion models, Burt's structural holes work

---

## SOURCE 2: Network Density Research (2024)

**Finding:** ❌ **NO UNIVERSAL THRESHOLDS EXIST**

**Research Summary:**
- Network density ranges from 0 (no connections) to 1 (all connections)
- Dense networks: High proportion of ties (significant sharing/commonalities)
- Sparse networks: Low proportion of ties (low sharing, little in common)
- **CRITICAL:** Interpretation is **highly context-dependent**
- Large networks tend to be sparse (size matters)
- Comparison by mean degree is better than absolute density

**Source:** Multiple 2024 studies including Taylor & Francis, PMC, ScienceDirect

**Implication for Tools:** Cannot provide "0-30% = sparse" thresholds - must compare to random baseline or similar-sized networks

---

## SOURCE 3: Clustering Coefficient (Watts-Strogatz Small-World)

**Finding:** ❌ **NO ABSOLUTE THRESHOLDS** - Use ratio to random graph

**Key Research:**
- **Small-world criterion:** C ≫ C_random (clustering much higher than random)
- **Empirical example:** Film actors = 0.79 clustering vs 0.00027 random
- **Theoretical minimum:** Some configurations have C ≥ 0.33
- **Range:** 0 (no clustering) to 1 (complete clustering)

**What matters:** Ratio to equivalent random graph, not absolute value

**Source:** Watts-Strogatz (1998), PMC small-world network studies

**Implication for Tools:** Must compare user's network clustering to random baseline, not absolute ranges

---

## SOURCE 4: Burt's Structural Holes (Network Constraint)

**Finding:** ⚠️ **CONTEXT-DEPENDENT** - Use z-scores within sample

**Key Metrics:**
- **Network Constraint:** Measures "straitjacket" limiting vision/support
- **Range:** 0 (no constraint, many structural holes) to ~100 (maximum constraint)
- **Empirical examples from Burt:**
  - Low constraint: 14.8 (good brokerage position)
  - Medium constraint: 30.9
  - High constraint: 59-65 (dense/hierarchical networks)
  - Maximum: 84-93 (very dense, 3-contact networks)

**Interpretation:** Use **z-scores** relative to sample, not absolute thresholds

**Source:** Burt (2000, 2004), "Structural Holes vs Network Closure"

**Implication for Tools:** Cannot say "3+ bridges = excellent" - must show relative position

---

## SOURCE 5: Friendship Network Overlap

**Finding:** ✅ **LINEAR RELATIONSHIP** confirmed, but ❌ NO SPECIFIC PERCENTAGES

**Key Research:**
- "Neighborhood overlap increases as function of tie strength in **strikingly linear fashion**"
- Stronger ties = greater neighborhood overlap
- More clustered friendship circles = weaker ties

**Empirical tie strength data (from Granovetter):**
- Strong ties (≥2x/week): 16.7% of job leads
- Moderate ties (occasional): 55.6% of job leads
- Weak ties (≤1x/year): 27.8% of job leads

**BUT:** No research provides specific % overlap values (e.g., "strong ties = 80% overlap")

**Source:** Multiple network studies 2018-2022, Granovetter original data

**Implication for Tools:** Relationship is real but specific percentages are not empirically validated

---

## SOURCE 6: Information Diffusion & Reach

**Finding:** ⚠️ **COMPLEX MODELS** - No simple multipliers

**Research Models:**
- **SIR Model:** Susceptible-Infectious-Recovered (epidemiological adaptation)
- **IC Model:** Independent Cascade
- **Cascade properties:** Reach, depth, breadth, speed

**Key Findings:**
- Reach depends on: network topology, infectivity (R0), cascade size
- No simple "10x multiplier" formula
- Must simulate diffusion process with specific network structure

**Source:** PNAS 2021, PMC diffusion studies

**Implication for Tools:** "Extended reach ~10x" is oversimplified - actual reach varies greatly by network structure

---

## CURRENT TOOL ISSUES:

### ❌ UNSUPPORTED BY RESEARCH:
1. Metrics panel threshold ranges (0-30%, 30-60%, 60-100%)
2. Information Reach Calculator overlap formulas
3. "Optimal" network configurations
4. Specific bridge count recommendations
5. Network quality scoring algorithm

### ✅ SUPPORTED BY RESEARCH:
1. 16.7% / 55.6% / 27.8% empirical baseline
2. Weak ties more effective than strong ties for jobs
3. Tie strength measured by contact frequency
4. Triadic closure principle (qualitative)

---

## RESEARCH COMPLETE ✅

All searches completed. Key finding: **NO universal thresholds exist** - all interpretation is context-dependent.

---

## RECOMMENDATIONS FOR TOOL REVISIONS:

### ✅ KEEP (Research-Backed):
1. **Job Search Probability Calculator** - Uses exact Granovetter empirical data (16.7/55.6/27.8%)
2. **Tie strength definitions** - Granovetter's frequency operationalization
3. **Weak ties more effective principle** - Core finding from study

### ⚠️ REVISE (Add Context/Disclaimers):

**1. Understanding the Metrics Panel**
- **Current issue:** Fixed threshold ranges (0-30%, 30-60%, etc.)
- **Fix:** Change to relative comparisons:
  - "Higher than random network baseline = clustered"
  - "Lower than random = diverse"
  - Remove absolute % ranges
- **Add:** "Interpretation depends on network size and context"

**2. Information Reach Calculator**
- **Current issue:** Made-up overlap formulas (0.8x, 0.3x)
- **Fix options:**
  a) Add disclaimer: "Illustrative model based on Granovetter's overlap principle"
  b) Remove specific calculations, show conceptual difference only
  c) Use relative comparison: "Strong ties create MORE redundancy than weak ties"
- **Remove:** "Extended reach ~10x" multiplier (no research basis)

**3. Network Simulator Quality Score**
- **Current issue:** Arbitrary scoring algorithm
- **Fix:** Remove score OR change to "Compared to random network baseline"

### 📊 WHAT WE CAN SAY (Research-Backed):

**Qualitative statements (VALID):**
- ✅ "Stronger ties have more overlap"
- ✅ "Weak ties provide access to novel information"
- ✅ "High clustering indicates closed triads"
- ✅ "Bridges connect otherwise disconnected groups"

**Quantitative statements (NOT VALID without context):**
- ❌ "40%+ weak ties is optimal"
- ❌ "3+ bridges = excellent"
- ❌ "Strong ties have 80% overlap"
- ❌ "0-30% density is sparse"

### 🎯 RECOMMENDED APPROACH:

**Option A: Educational/Illustrative**
- Keep current calculations
- Add prominent disclaimer: "Educational model illustrating Granovetter's principles. Actual values vary by context."
- Emphasize qualitative relationships over quantitative thresholds

**Option B: Research-Pure**
- Remove all made-up thresholds
- Show only empirically validated data (16.7/55.6/27.8%)
- Use relative comparisons to random baselines
- No "optimal" recommendations

**Option C: Hybrid (RECOMMENDED)**
- Keep illustrative calculations for engagement
- Add clear "Model Assumptions" section citing that thresholds are conceptual
- Provide toggle: "Show research-only mode" vs "Show illustrative model"
- Citation links to actual papers
