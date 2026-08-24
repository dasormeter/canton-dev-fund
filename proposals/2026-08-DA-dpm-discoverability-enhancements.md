## **Development Fund Proposal**

**Author:** Digital Asset
**Status:** Draft
**Created:** 2026-08-22
**Updated:** 2026-08-24
**Label:** daml-tooling
**Champion:** Curtis Hrischuk

---

## **Abstract**

- OCI DAR Managment Work
- DevNet/TestNet/MainNet tagging support
- Dpm Cleanup
- Assorted Enhancements and Improvements

---

## **Specification**

### **1. Objective**


### **2. Implementation Mechanics**
- [DAR file main-package-id support in daml.yaml](https://github.com/digital-asset/dpm/issues/297)
- [DPM cleans up after itself](https://github.com/digital-asset/dpm/issues/295)
- [Harmonization of dependencies and data-dependencies](https://github.com/digital-asset/dpm/issues/298)
- [dpm publish append index](https://github.com/digital-asset/dpm/issues/296]
- [Self-Updating Dpm](https://github.com/digital-asset/dpm/issues/294)
- [Support components implementing cli sub-commands](https://github.com/digital-asset/dpm/issues/121)
- [DevNet/TestNet/MainNet Easy Discoverability of Artifacts](https://github.com/digital-asset/dpm/issues/309)
- [OCI Dar Publish and Consume](https://github.com/digital-asset/dpm/issues/308)

#### **Scope limits**


### **3. Architectural Alignment**


Relevant governance alignment:

- CIP-0082: Development Fund support for common-good ecosystem development
- CIP-0100: milestone-based funding and transparent review process

### **4. Backward Compatibility**



---

## **Milestones and Deliverables**

### **Milestone 1: Design, Implementation, and Upstream PR**

- **Effort:** xxx person-months.
- **Allocation:** xxx engineers.
- **Delivery Status:** Substantially complete and ready for maintainer review.
- **Focus:** 
- **Deliverables / Value Metrics:**
    

### **Milestone 2: Maintainer Review and Upstream Merge**

- **Estimated Effort:** x person-month.
- **Allocation:** x engineers.
- **Estimated Delivery:** x weeks after Milestone 1
    - **External Dependency:** 
- **Focus:** Incorporate maintainer feedback and support the contribution through the upstream review process.
- **Deliverables / Value Metrics:**
    - maintainer feedback addressed on the upstream `dpm` PR or agreed contribution branch
    - updated implementation, tests, and documentation based on review comments
    - updated reference project showing Git-hosted DAR dependency resolution using representative Splice DARs stored in Git, without custom download scripts
    - upstream PR merged into the official `dpm` repository

### **Milestone 3: Ecosystem Validation and Enablement**

- **Estimated Delivery:** 1 month after Milestone 2
- **Focus:** Validate the completed workflow with ecosystem developers and publish lightweight adoption materials.
- **Deliverables / Value Metrics:**
    - documentation updates based on validation feedback, including any remaining limitations or follow-up items
    - 1 recorded demo or walkthrough
    - 1 short technical writeup or case study explaining the workflow and its value for Canton/Daml developers
    - optional live walkthrough or office-hours session for interested ecosystem developers, coordinated with the Canton Foundation if useful

### **Milestone 4: Maintenance Period**

- **Estimated Effort**: Maximum of 20 hours per month.
- **Allocation**: 1 engineer.
- **Estimated Delivery:** Six-month maintenance period beginning when the upstream PR is merged at the end of Milestone 2. This milestone runs concurrently with Milestone 3.
- **Focus:** Maintain the Git-based DAR dependency functionality after its upstream merge.
- **Deliverables / Value Metrics:**

#### **Optional Maintenance Extension**



---

## **Acceptance Criteria**

Project-specific acceptance conditions:

- Developers can declare Git-hosted DAR dependencies in `daml.yaml` using `dependencies`.
- `dpm install package` / `dpm install` can fetch, cache, and pin supported Git-hosted DAR dependencies.
- `dpm build` can compile a package using the resolved Git-hosted DAR dependencies through the normal Daml build workflow.
- `dpm test` works with Git-hosted DAR dependencies, including test dependency workflows.
- `dpm add dar` supports adding GitHub HTTPS DAR references and inserts the resolved dependency into `daml.yaml`.
- `dpm update` can resolve supported HTTPS artifact references to pinned SHA references.
- Git-hosted DARs can be resolved from both `dependencies` and `data-dependencies`.
- Repository aliasing is supported for repeated DAR references from the same source.
- Documentation explains the required Git dependency syntax, including any limitations.
- A reference or representative project demonstrates the workflow replacing a manual DAR download script, checked-in DAR artifact, or manually managed dependency path.

---

## **Funding**

**Total Funding Request:** 000,000 CC

### **Payment Breakdown by Milestone**

- **Milestone 1:**
- **Milestone 2:**
- **Milestone 3:**
- **Milestone 4:**
- **Milestone Maintenance Extension:**
- **Milestone Payment Terms:** 

---

## **Volatility Stipulation**

The project timeline is under 6 months. Should the project timeline extend beyond 6 months due to Committee-requested scope changes, any remaining milestones must be renegotiated to account for significant USD/CC price volatility.

---

## **Co-Marketing**


---

## **Motivation**

Expected benefits include:

- fewer manual `.dar` handling steps
- less duplicated scripting across projects
- standard install, build, and test behavior through `dpm`
- a foundation for future dependency-management improvements inside `dpm`

---

## **Rationale**

---

## **Future Work**


---
