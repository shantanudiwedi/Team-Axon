# AXON — Pump-Survivable Steam

## AI-Enabled Well-to-Surface Digital Twin for CSS & SRP Optimization

**Smart India Hackathon 2026 — SIH 2026**

| Parameter                 | Details                                                                                                                                                     |
| ------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Problem Statement ID**  | SIH26120                                                                                                                                                    |
| **Problem Statement**     | Digital Twin for Well-to-Surface Optimization of Cyclic Steam Stimulation (CSS) and Sucker Rod Pump (SRP) Operations for Heavy Oil Wells of Baghewala Field |
| **Organization**          | Oil India Limited                                                                                                                                           |
| **Department**            | Oil India Limited                                                                                                                                           |
| **Category**              | Software                                                                                                                                                    |
| **Theme**                 | Smart Automation                                                                                                                                            |
| **Team**                  | AXON                                                                                                                                                        |
| **Target Field**          | Baghewala Field, Rajasthan                                                                                                                                  |
| **Reservoir**             | Jodhpur Sandstone                                                                                                                                           |
| **Crude**                 | Heavy crude, approximately 17–19° API                                                                                                                       |
| **Reservoir Temperature** | Approximately 46–48°C                                                                                                                                       |

---

# 1. Executive Overview

**AXON** is an AI-enabled **well-to-surface digital twin** designed for the optimization of **Cyclic Steam Stimulation (CSS)** and **Sucker Rod Pump (SRP)** operations in heavy-oil wells at Baghewala Field.

Baghewala produces heavy crude from the Jodhpur Sandstone reservoir. The field is characterized by high crude viscosity, high asphaltene content, low reservoir pressure, low reservoir temperature and poor oil mobility under primary recovery. Thermal stimulation and artificial lift are therefore important for sustained production.

The central problem is that **CSS-cycle design and SRP operation are treated as separate operational decisions**.

AXON connects them.

The digital twin combines:

* Reservoir behaviour
* Steam injection
* CSS cycle phases
* Wellbore conditions
* Heavy-oil viscosity
* SRP operating conditions
* Rod loading
* Pump behaviour
* Production response
* Failure-risk indicators

The system then predicts how a CSS cycle will affect both **production and artificial-lift performance**, and recommends operating conditions that balance production with equipment constraints.

### Core USP

> **Pump-Survivable Steam**

Instead of optimizing a CSS cycle only for additional oil production, AXON optimizes the cycle around **what the rod and pump can safely survive**.

The objective is not simply:

**Maximum barrels**

but:

**Maximum sustainable production within pump-life and operating constraints.**

---

# 2. Why Baghewala Needs an Integrated Digital Twin

Baghewala's heavy crude has high viscosity and poor mobility under reservoir conditions. Steam is used to increase temperature and reduce viscosity, improving oil mobility and production.

However, the thermal benefit does not remain constant throughout a production cycle.

The general operating relationship is:

```text
Steam Injection
      ↓
Reservoir Heating
      ↓
Lower Oil Viscosity
      ↓
Improved Oil Mobility
      ↓
Higher Production
      ↓
Reservoir / Wellbore Cooling
      ↓
Increasing Oil Viscosity
      ↓
Higher Pump Load / Reduced Efficiency
      ↓
Rod Floating / Impact Loading
      ↓
Pump Unsetting / Rod Failure Risk
```

The SIH problem specifically identifies rod floating, impact loading, pump unsetting, rod failures, increased maintenance, higher Steam-Oil Ratio and reduced production efficiency as operational challenges.

AXON addresses the complete chain instead of optimizing only one section.

---

# 3. Problem Being Solved

## Current Operational Gap

### CSS decisions

Important CSS parameters include:

* Steam volume
* Injection pressure
* Soak time
* Production cut-off

The SIH problem describes these as being largely based on historical operating practices.

### SRP decisions

Important SRP parameters include:

* Stroke length
* Strokes per minute (SPM)
* VFD settings

These may be adjusted manually and reactively based on changing well conditions.

### Result

The reservoir, wellbore, pump and surface production system are not treated as one coupled optimization problem.

This can contribute to:

* Higher Steam-Oil Ratio (SOR)
* Higher energy consumption
* Reduced production efficiency
* Rod floating
* Impact loading
* Pump unsetting
* Rod failures
* Increased maintenance
* Reduced equipment availability

---

# 4. AXON's Solution

AXON introduces a **cycle-aware well-to-surface digital twin**.

The system continuously connects:

```text
RESERVOIR
    ↓
THERMAL RESPONSE
    ↓
WELLBORE FLUID CONDITIONS
    ↓
SRP / ROD RESPONSE
    ↓
SURFACE PRODUCTION
    ↓
FAILURE RISK
    ↓
OPTIMIZATION
```

The resulting recommendation can include:

* CSS steam schedule
* Soak duration
* Production cut-off
* VFD setting
* SRP speed
* Stroke-related operating conditions
* Pump-safe operating envelope

The final recommendation is presented to an engineer rather than directly controlling the physical well.

---

# 5. USP — Pump-Survivable Steam

### Conventional approach

```text
CSS Optimization
      ↓
Production Objective

Pump Reliability
      ↓
Maintenance Objective
```

### AXON approach

```text
                 ┌───────────────┐
                 │ CSS Schedule  │
                 └───────┬───────┘
                         ↓
                  Thermal Response
                         ↓
                  Fluid Properties
                         ↓
                 Pump / Rod Loading
                         ↓
                  Failure Risk
                         ↓
             ┌───────────┴───────────┐
             ↓                       ↓
      Production Objective    Equipment Constraint
             └───────────┬───────────┘
                         ↓
                JOINT OPTIMIZATION
                         ↓
               PUMP-SAFE CSS PLAN
```

### Key innovation

The novelty is **not simply using a digital twin**.

Reservoir-to-surface modelling already exists in petroleum engineering literature.

AXON's proposed differentiator is the **cycle-aware coupling between CSS planning and rod/pump-life constraints**.

This means pump-life risk becomes part of the steam and production optimization decision rather than being treated only as a downstream maintenance problem.

---

# 6. System Architecture

AXON follows a five-layer architecture.

```text
┌───────────────────────────────────────────────┐
│ LAYER 5 — ENGINEER INTERFACE                  │
│ Dashboard • What-if Simulator • Alerts        │
│ Approve / Reject                              │
├───────────────────────────────────────────────┤
│ LAYER 4 — OPTIMIZATION ENGINE                 │
│ Steam • Soak • Cycle • VFD • SRP              │
│ Pump-life constrained optimization             │
├───────────────────────────────────────────────┤
│ LAYER 3 — AI & ANALYTICS                      │
│ Failure Risk • Production Forecast            │
│ Anomaly Detection                             │
├───────────────────────────────────────────────┤
│ LAYER 2 — DIGITAL TWIN CORE                   │
│ Reservoir • Thermal • Wellbore • Pump         │
│ CSS ↔ Pump-Life Coupling                      │
├───────────────────────────────────────────────┤
│ LAYER 1 — DATA & INTEGRATION                  │
│ SCADA • VFD • CSS • Production • Well Data   │
└───────────────────────────────────────────────┘
```

This architecture corresponds to the five-layer structure in the AXON SIH presentation.

---

# 7. Layer 1 — Data & Integration

AXON is designed around the data categories identified in the SIH problem statement.

### Production Data

* Historical production rate
* Production trends
* Cycle-level production history

### CSS Data

* Steam injection parameters
* CSS cycle records
* Injection duration
* Soak duration
* Production phase

### Artificial-Lift Data

* VFD data
* SRP operating parameters
* Stroke information
* SPM
* Pump operating behaviour

### Failure Data

* Rod failure history
* Pump-unsetting history
* Failure timing
* Failure occurrence by CSS phase

### Well Data

* Well completion information
* Reservoir properties
* Pressure data
* Fluid properties
* PVT information

The SIH statement explicitly identifies these categories as relevant available field data.

---

# 8. Layer 2 — Digital Twin Core

The digital twin represents the relationship between the reservoir, wellbore, artificial lift and surface system.

## Reservoir / CSS Model

The model represents:

* Steam input
* Reservoir heating
* Cooling behaviour
* Production response
* CSS cycle phases

### Main state variables

```text
Temperature
Pressure
Fluid viscosity
Production rate
Steam input
Cycle phase
```

## Heavy-Oil Behaviour

As temperature decreases:

```text
Temperature ↓
      ↓
Viscosity ↑
      ↓
Mobility ↓
      ↓
Production / Pump Efficiency ↓
```

## Rod & Pump Model

The artificial-lift model considers:

* Rod loading
* Pump loading
* Operating speed
* Stroke conditions
* Fluid conditions
* Thermal effects
* Potential rod-floating behaviour

The final implementation should use calibrated engineering relationships appropriate to the Baghewala well configuration.

---

# 9. Layer 3 — AI & Analytics

The analytics layer provides predictive information to the digital twin.

### A. Rod Failure Risk

Predicts the likelihood of elevated rod-failure risk under the current operating conditions.

Output:

```text
LOW
MEDIUM
HIGH
```

with a numerical risk score.

### B. Pump-Unsetting Risk

Identifies operating conditions associated with elevated pump-unsetting risk.

### C. CSS Production Forecast

Predicts production behaviour for alternative CSS-cycle scenarios.

### D. Anomaly Detection

Detects abnormal SRP / operating behaviour and potential rod-floating or impact-loading conditions.

### Model Framework

The project architecture supports:

* **scikit-learn**
* **PyTorch**
* Physics/engineering models
* Historical time-series data
* Feature-based predictive analytics

The exact production model should be selected after evaluating the available field dataset rather than hard-coding a model choice without validation.

---

# 10. Layer 4 — Optimization Engine

The optimizer searches for operating conditions that satisfy production and equipment constraints.

### Optimization variables

```text
Steam Volume
Injection Pressure
Soak Time
Production Cut-Off
Stroke Length
SPM
VFD Setting
```

The SIH problem explicitly calls for optimization of CSS parameters and continuous SRP adjustment based on well conditions.

### Optimization objective

Conceptually:

```text
MAXIMIZE

Production / Economic Value

SUBJECT TO

Pump-Life Constraint
+
Operating Limits
+
Surface Constraints
+
CSS Constraints
+
Well Conditions
```

AXON's presentation expresses the optimization objective as:

> **Net oil per rod-life**

while maintaining operational constraints.

---

# 11. Layer 5 — Engineer Interface

The engineer dashboard provides:

### Well Overview

* Current CSS phase
* Temperature
* Pressure
* Production
* Steam usage
* SOR
* Pump-life risk

### Risk Panel

```text
Pump-Life Risk
████████░░  HIGH

Rod Failure Risk
██████░░░░  MEDIUM

Pump-Unsetting Risk
████░░░░░░  LOW
```

### What-If Simulator

Engineers can compare alternative scenarios:

```text
Scenario A
High Steam
Long Soak
High Production
Higher Equipment Risk

VS

Scenario B
Moderate Steam
Optimized Soak
Slightly Lower Peak Production
Lower Equipment Risk
```

### Recommendation

```text
RECOMMENDED CSS PLAN

Steam Volume       → [Calculated]
Soak Duration      → [Calculated]
Production Cutoff  → [Calculated]
VFD / SPM          → [Calculated]

Pump-Life Risk     → [Calculated]
Production Forecast → [Calculated]

[ APPROVE ]     [ REJECT ]
```

---

# 12. Closed-Loop Workflow

AXON operates as a continuous learning loop.

### Step 1 — Ingest

Collect:

* Production
* CSS
* Steam
* SRP/VFD
* Well
* Reservoir
* Failure history

### Step 2 — Calibrate

The twin is calibrated against historical CSS-cycle and pump behaviour.

### Step 3 — Predict

Predict:

* Production response
* Temperature response
* Pump behaviour
* Rod/pump failure risk

### Step 4 — Optimize

Evaluate candidate CSS and SRP settings under pump-life constraints.

### Step 5 — Recommend

Provide:

* Recommended setpoints
* Risk
* Expected production
* What-if comparison
* Confidence / model information

### Step 6 — Learn

Actual cycle results are fed back into the twin for recalibration.

This closed-loop workflow is defined in the AXON technical architecture.

---

# 13. Technology Stack

## Backend

* Python
* FastAPI

## Data Layer

* PostgreSQL
* TimescaleDB for time-series operational data

## AI / ML

* scikit-learn
* PyTorch

## Frontend

* React
* Plotly

## Deployment

* Docker

The proposed stack is consistent with the technology stack specified in the AXON SIH presentation.

---

# 14. Data Pipeline

```text
SCADA / Historian
       │
       ├── Production Data
       ├── Steam Data
       ├── VFD Data
       └── SRP Data
              │
              ▼
        Data Ingestion
              │
              ▼
     Cleaning & Alignment
              │
              ▼
     Feature Engineering
              │
       ┌──────┴───────┐
       ▼              ▼
Physics Model       ML Model
       │              │
       └──────┬───────┘
              ▼
        Digital Twin
              │
              ▼
       Risk Prediction
              │
              ▼
      Optimization Engine
              │
              ▼
     Engineer Dashboard
              │
              ▼
       Approved Plan
              │
              ▼
      Actual Well Outcome
              │
              └──────────→ Recalibration
```

---

# 15. Prototype Strategy

Because the SIH prototype does not have direct access to Oil India operational systems, the MVP is designed around **synthetic/anonymized data and simulated field interfaces**.

This allows demonstration of:

* Data ingestion
* CSS simulation
* Thermal response
* Pump-risk modelling
* Production forecasting
* Optimization
* What-if analysis
* Dashboard visualization

The prototype should explicitly distinguish simulated outputs from field-validated results.

### Prototype Status

**Prototype type:** Decision-support digital twin

**Field data:** Not embedded in the prototype

**Live OIL/SCADA integration:** Not available during the prototype stage

**Operational control:** Not enabled

**Engineering assumptions:** Clearly documented and configurable

---

# 16. Validation Strategy

The most important validation question is:

> **Would AXON have identified elevated rod/pump risk before historical failure events while maintaining acceptable production performance?**

## Validation 1 — Production Forecast

Compare:

```text
Predicted Production
        VS
Observed / Reference Production
```

Metric:

**Production prediction error**

Target:

**[To be established from historical validation dataset]**

## Validation 2 — Failure Prediction

Compare:

```text
Predicted High-Risk Events
        VS
Historical Rod / Pump Failures
```

Metrics:

* Precision
* Recall
* F1-score
* Lead time before failure

## Validation 3 — CSS Optimization

Compare baseline and optimized scenarios on:

* Oil production
* Steam consumption
* SOR
* Energy consumption
* Pump-risk score

## Validation 4 — Equipment Impact

Evaluate:

* Rod-floating events
* Impact-loading indicators
* Pump-unsetting events
* Rod failures

The SIH requirement specifically calls for detection/minimization of rod floating and impact loading and improvement in pump reliability.

---

# 17. Success Metrics

AXON should be evaluated using measurable operational KPIs.

| KPI                  | Measurement                             |
| -------------------- | --------------------------------------- |
| Oil production       | Production rate / cumulative production |
| Steam efficiency     | Oil produced per unit steam             |
| SOR                  | Steam-Oil Ratio                         |
| Energy efficiency    | Energy consumed per barrel              |
| Rod failure          | Failure events per operating period     |
| Pump unsetting       | Unsetting events per operating period   |
| Pump efficiency      | Predicted / observed pump performance   |
| Risk prediction      | Precision / Recall / F1                 |
| Failure lead time    | Time between alert and event            |
| Production forecast  | Prediction error                        |
| Optimization benefit | Difference vs baseline                  |

The SIH statement explicitly identifies increased oil recovery, lower SOR, lower energy consumption per barrel, fewer rod failures and pump unsettings, and improved equipment life as expected benefits.

---

# 18. Feasibility

## Technical Feasibility

The problem is software-oriented and the required inputs are identified by the SIH statement.

Available data categories include:

* Production history
* CSS cycle records
* Steam injection parameters
* VFD/SRP data
* Rod failure history
* Pump-unsetting history
* Well completion data
* Reservoir data
* Fluid properties
* Pressure data

## MVP Feasibility

The prototype can be built without physical modification of the field.

The MVP uses:

* Synthetic/anonymized data
* Simulated field inputs
* Digital-twin models
* Predictive analytics
* Optimization algorithms
* Visualization

## Production Feasibility

A production deployment would require:

* OIL-approved data access
* SCADA/historian integration
* Well-specific calibration
* Petroleum-engineering validation
* Cybersecurity review
* Operational approval
* Field pilot

---

# 19. Viability

AXON targets four major operational cost drivers:

### 1. Production Loss

Improved CSS/SRP coordination can support better production decisions.

### 2. Steam Cost

Optimization can target lower Steam-Oil Ratio and better steam utilization.

### 3. Energy Consumption

SRP and steam operations can be evaluated together rather than independently.

### 4. Equipment Maintenance

Early risk identification can support intervention before severe rod/pump failure.

The SIH problem explicitly identifies high SOR, increased energy consumption, reduced production efficiency, rod failures, pump unsetting and increased maintenance as the underlying operational issues.

---

# 20. Scalability

The system can scale from one well to an entire field.

## Well Level

Each well receives:

* Individual history
* Individual model calibration
* Individual pump constraints
* Individual CSS history

## Field Level

Multiple wells can be monitored through a centralized dashboard.

```text
Baghewala Field
       │
 ┌─────┼─────┐
 ▼     ▼     ▼
Well 1 Well 2 Well 3
 │      │      │
Twin   Twin   Twin
 │      │      │
 └──────┼──────┘
        ▼
 Field Optimization Dashboard
```

## Future Scale

The architecture can be extended to:

* Additional Baghewala wells
* Other OIL heavy-oil fields
* Other thermal-recovery operations
* Additional artificial-lift systems

---

# 21. Human-in-the-Loop

AXON is a **decision-support system**, not an autonomous well-control system.

### AI / Digital Twin

The system:

* Predicts
* Simulates
* Detects anomalies
* Calculates risk
* Optimizes scenarios
* Recommends operating conditions

### Engineer

The engineer:

* Reviews the recommendation
* Evaluates operating context
* Approves or rejects the recommendation
* Remains responsible for implementation

```text
AI Recommendation
       ↓
Engineer Review
       ↓
Approve / Reject
       ↓
Field Decision
```

This design prevents the prototype from claiming unsafe autonomous control.

---

# 22. Risk Management

| Risk                                  | Mitigation                                          |
| ------------------------------------- | --------------------------------------------------- |
| Limited field data during development | Synthetic/anonymized data for MVP                   |
| Model drift                           | Recalibration after new CSS cycles                  |
| Sensor noise                          | Data-quality checks and filtering                   |
| Incorrect prediction                  | Confidence/risk indicators + engineer review        |
| Well-to-well variation                | Individual well calibration                         |
| Heavy-oil model uncertainty           | Configurable engineering parameters                 |
| Rod-dynamics uncertainty              | Domain validation with petroleum engineers          |
| Over-optimization for production      | Pump-life constraints                               |
| Excessive steam usage                 | SOR and energy constraints                          |
| Live integration risk                 | Mock interfaces during MVP                          |
| Cybersecurity risk                    | Enterprise authentication and controlled deployment |
| Operational misuse                    | Decision-support-only workflow                      |

---

# 23. What AXON Does Differently

### Conventional workflow

```text
Reservoir Team
     ↓
CSS Decision

+

Production / Artificial Lift Team
     ↓
SRP Decision

+

Maintenance Team
     ↓
Failure Response
```

### AXON workflow

```text
Reservoir
    +
CSS
    +
Wellbore
    +
SRP
    +
Production
    +
Failure Risk
        ↓
ONE DIGITAL TWIN
        ↓
JOINT OPTIMIZATION
        ↓
ENGINEER DECISION
```

The key difference is **coupling**, not merely digitization.

---

# 24. What-If Simulation

AXON allows an engineer to compare alternative strategies.

### Scenario A

```text
Steam Volume       HIGH
Soak Duration      HIGH
Production         HIGH
Pump Risk          HIGH
Energy Consumption  HIGH
```

### Scenario B

```text
Steam Volume       MODERATE
Soak Duration      OPTIMIZED
Production         ACCEPTABLE
Pump Risk          LOWER
Energy Consumption  LOWER
```

### Scenario C

```text
Steam Volume       LOW
Soak Duration      SHORT
Production         LOW
Pump Risk          LOW
```

The optimizer selects the operating point that best satisfies the defined production and equipment constraints.

---

# 25. Example Dashboard

```text
╔══════════════════════════════════════════════════════╗
║              AXON — BAGHEWALA DIGITAL TWIN          ║
╠══════════════════════════════════════════════════════╣
║ Well: BH-XX              CSS Phase: PRODUCE          ║
╠═══════════╦═══════════╦═══════════╦══════════════════╣
║ Temp      ║ Pressure  ║ Oil Rate  ║ Pump Risk        ║
║ XX °C     ║ XX bar    ║ XX BOPD   ║ MEDIUM           ║
╠═══════════╩═══════════╩═══════════╩══════════════════╣
║                                                      ║
║        CSS / PUMP RISK OVER CYCLE                    ║
║                                                      ║
║   INJECT          SOAK             PRODUCE           ║
║     │               │                 │              ║
║     └───────────────┴─────────────────┘              ║
║                       ╲                              ║
║                        ╲ Risk                        ║
║                         ╲________                    ║
║                                  ╲                   ║
║                           PUMP-LIFE LIMIT             ║
║                                                      ║
╠══════════════════════════════════════════════════════╣
║ PUMP-SAFE RECOMMENDATION                             ║
║                                                      ║
║ Steam Volume:        [Calculated]                    ║
║ Soak Duration:       [Calculated]                    ║
║ Production Cutoff:   [Calculated]                    ║
║ VFD / SPM:           [Calculated]                    ║
║                                                      ║
║ [ APPROVE ]                         [ REJECT ]        ║
╚══════════════════════════════════════════════════════╝
```

---

# 26. API / Service Architecture

The production-oriented architecture can be separated into services:

```text
Frontend
   │
   ▼
API Gateway / FastAPI
   │
   ├── Data Service
   ├── Digital Twin Service
   ├── Prediction Service
   ├── Optimization Service
   ├── Alert Service
   └── Reporting Service
          │
          ▼
 PostgreSQL / TimescaleDB
```

### API responsibilities

* Well selection
* CSS-cycle retrieval
* Sensor/time-series ingestion
* Twin simulation
* Prediction
* Optimization
* Scenario comparison
* Recommendation retrieval
* Alert generation
* Audit logging

---

# 27. Database Architecture

A production database can contain logical entities such as:

```text
Wells
 ├── well_id
 ├── field
 ├── reservoir
 ├── completion_data
 └── operating_limits

CSS_Cycles
 ├── cycle_id
 ├── well_id
 ├── injection_start
 ├── injection_end
 ├── soak_duration
 └── production_start

Steam_Operations
 ├── cycle_id
 ├── steam_volume
 ├── injection_pressure
 └── injection_rate

SRP_Operations
 ├── well_id
 ├── timestamp
 ├── stroke_length
 ├── SPM
 └── VFD

Production
 ├── well_id
 ├── timestamp
 ├── oil_rate
 └── water_rate

Failures
 ├── well_id
 ├── failure_type
 ├── timestamp
 └── failure_description

Predictions
 ├── well_id
 ├── timestamp
 ├── production_forecast
 └── failure_risk

Recommendations
 ├── well_id
 ├── cycle_id
 ├── recommended_parameters
 └── approval_status
```

---

# 28. Security & Operational Safety

A production deployment should include:

* Role-based access
* Authentication
* Secure API communication
* Encryption in transit
* Encryption at rest
* Audit logging
* Model/version tracking
* Controlled access to operational data
* Separation between simulation and field-control systems

Most importantly:

> **AXON's prototype does not directly control field equipment.**

The system produces recommendations for authorized engineering review.

---

# 29. Deployment Architecture

### Development

```text
Developer Machine
       │
       ├── React
       ├── FastAPI
       ├── PostgreSQL / TimescaleDB
       └── Digital Twin
```

### Pilot

```text
OIL Data Sources
       ↓
Secure Integration Layer
       ↓
AXON Digital Twin
       ↓
Prediction + Optimization
       ↓
Engineer Dashboard
       ↓
Engineer Approval
```

### Enterprise

```text
Field / SCADA
      ↓
Secure Data Gateway
      ↓
Enterprise Data Platform
      ↓
AXON Digital Twin Platform
      ├── Twin Engine
      ├── ML Engine
      ├── Optimization Engine
      └── Monitoring
             ↓
       Engineer Dashboard
```

---

# 30. Current Prototype Boundary

The SIH prototype is intended to demonstrate the **technical concept and decision-support workflow**, not claim production deployment.

### Demonstrated / intended MVP components

* Digital-twin architecture
* CSS-cycle representation
* Reservoir/thermal modelling
* Pump/rod constraint modelling
* Risk prediction
* Optimization workflow
* What-if simulation
* Engineer dashboard
* Closed-loop recalibration concept

### Not claimed

* Live Oil India SCADA integration
* Field-calibrated production performance
* Autonomous well control
* Guaranteed production increase
* Guaranteed failure reduction
* Production-grade reservoir simulation without field calibration

---

# 31. Research Foundation

The AXON concept is based on the SIH 26120 problem definition and relevant petroleum-engineering modelling concepts.

### Primary SIH Reference

**SIH 2026 — Problem Statement 26120**

Defines:

* Baghewala field context
* Heavy-oil characteristics
* CSS/SRP operational problems
* Required digital-twin capabilities
* Expected benefits
* Relevant field data

### Reservoir-to-Surface Modelling

Prior work demonstrates that integrated reservoir-to-surface modelling is an established engineering direction.

Therefore, AXON does **not** claim digital-twin integration itself as the sole novelty.

### Artificial-Lift Reliability

Rod floating, impact loading, pump unsetting and rod failures are central artificial-lift reliability concerns in heavy-oil production.

### AXON Research Gap

The proposed focus is:

> **Using the coupled CSS-cycle and rod/pump state to make pump-life constraints part of the CSS optimization loop.**

This is the specific technical hypothesis that should be validated through deeper literature review and engineering back-testing before being described as a first-of-its-kind solution.

---

# 32. Expected Benefits

If validated successfully, AXON is intended to support:

### Production

* Increased oil production
* Improved oil recovery
* Better production-cycle decisions

### Steam

* Reduced Steam-Oil Ratio
* Better steam utilization
* Reduced unnecessary steam consumption

### Energy

* Lower energy consumption per barrel
* Better SRP operating efficiency

### Equipment

* Reduced rod failures
* Reduced pump unsetting
* Reduced impact loading
* Improved equipment life
* Improved operational reliability

### Decision Making

* Predictive rather than reactive operations
* Data-driven CSS planning
* Data-driven SRP adjustment
* What-if scenario evaluation

These align with the expected benefits listed in the SIH problem statement.

---

# 33. Implementation Roadmap

## Phase 1 — MVP

**Goal:** Demonstrate the complete digital-twin workflow.

* Synthetic data generation
* CSS-cycle simulation
* Thermal response
* Heavy-oil viscosity behaviour
* SRP representation
* Risk calculation
* Dashboard
* What-if simulation

## Phase 2 — Historical Back-Testing

**Goal:** Validate against historical operating/failure data.

* Import historical CSS cycles
* Import production history
* Import SRP/VFD data
* Import failure history
* Calibrate model
* Evaluate predictions
* Measure failure lead time

## Phase 3 — Pilot

**Goal:** Run decision support alongside field operations.

* Secure OIL data integration
* Well-specific calibration
* Engineer review
* Shadow-mode recommendations
* Compare recommendations against actual operations

## Phase 4 — Field Deployment

**Goal:** Deploy validated decision-support capability.

* Production infrastructure
* Model monitoring
* Continuous recalibration
* Multi-well dashboard
* Enterprise security
* Operational governance

---

# 34. Team Structure

**Team:** AXON

### Recommended technical ownership

| Area              | Responsibility                                      |
| ----------------- | --------------------------------------------------- |
| Digital Twin      | Reservoir / thermal / wellbore model                |
| AI / ML           | Prediction and anomaly detection                    |
| Optimization      | CSS + SRP constrained optimization                  |
| Backend           | APIs, data pipeline and services                    |
| Frontend          | Engineer dashboard and visualization                |
| Data / Validation | Dataset preparation, calibration and KPI evaluation |

Individual member names should be added according to the actual team allocation rather than being invented in the README.

---

# 35. Project Identity

## Project Name

**AXON**

## USP

**Pump-Survivable Steam**

## One-Line Description

> **A cycle-aware digital twin that jointly optimizes CSS and SRP operations by treating rod and pump life as a constraint on steam and production decisions.**

## One-Sentence Pitch

> **AXON connects reservoir heating, heavy-oil behaviour and artificial-lift performance to recommend CSS and SRP operating conditions that maximize sustainable production while reducing pump and rod failure risk.**

## Judge-Friendly Explanation

> **Today, steam and pump settings are treated separately. AXON puts them inside one digital twin so the system can ask not only how much oil a CSS cycle can produce, but whether the pump can survive the way we produce it.**

---

# 36. Final Technical Principle

```text
          MORE STEAM
              ↓
        MORE HEATING
              ↓
       LOWER VISCOSITY
              ↓
       HIGHER MOBILITY
              ↓
       HIGHER PRODUCTION
              ↓
      BUT ALSO CONSIDER
              ↓
      PUMP / ROD LIMITS
              ↓
       OPTIMAL OPERATING
           WINDOW
```

AXON therefore does not optimize for maximum production at any cost.

It optimizes for:

> **Maximum sustainable production within the physical and operational limits of the well and its artificial-lift system.**

---

# 37. Final Message

## AXON — Pump-Survivable Steam

**From reservoir to pump.
From steam to production.
From prediction to decision.**

### One Digital Twin.

### One Coupled View.

### One Smarter CSS Cycle.

**CSS → Thermal Response → Fluid Behaviour → Pump Stress → Failure Risk → Optimization → Engineer Decision → Next Cycle**
