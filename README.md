# St. Thomas Legacy Systems Analysis
*Documenting 7 years of VBA automation before Python modernization*

## Context
I served as Data Administrator at St. Thomas Residential School (South Africa) from 2019-2024, 
managing 600+ learner records. This repository documents the legacy VBA/Excel architecture 
I built, analyzed, and am now modernizing.

**Current State (2024)**: Excel + VBA macros handling:
- Monthly fee invoicing (600+ students)
- Bank reconciliation (3-day manual process)
- Attendance tracking & reporting
- DBE (Department of Basic Education) statistical returns

**Target State (2025)**: Python + SQL + Streamlit pipeline with POPIA compliance

## Repository Structure
- `/vba_scrubbed/` - Sanitized screenshots/logic of current macros
- `/data_architecture/` - Entity relationship diagrams of current Excel structure  
- `/pain_points/` - Documented inefficiencies driving modernization
- `/migration_plan/` - VBA → Python mapping strategy

## Pain Points Catalog
1. **File corruption risk**: Single .xlsm file (120MB+) contains all financial history
2. **Version control**: "Invoice_Master_FINAL_v2_ACTUAL.xlsm" problem
3. **Load shedding vulnerability**: 3-day reconciliation lost to power outage
4. **POPIA risk**: PII scattered across 50+ worksheets, no audit trail
5. **No backups**: Manual copy-paste to backup folder

## Modernization Roadmap
- [ ] Month 1: ETL pipeline (Excel → PostgreSQL)
- [ ] Month 2: Automated reconciliation engine  
- [ ] Month 3: ML default prediction
- [ ] Month 4: Streamlit bursar dashboard

## Tech Transition
**Legacy Stack**: Excel 2016, VBA, Windows Task Scheduler, Manual email  
**Modern Stack**: Python 3.11, Pandas, PostgreSQL, Streamlit, GitHub Actions, AWS S3 (cold storage)

---
*This is living documentation of a working school's digital transformation.*
