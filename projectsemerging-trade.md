---
layout: default
title: "Emerging Market Trade Trends Dashboard"
permalink: /projects/emerging-trade/
---

# Emerging Market Trade Trends Dashboard

**Problem Statement / Objectives**  
- Analyze trade flows for Nigeria, India, and Vietnam (2015–2023) using UN Comtrade data.  
- Identify fastest-growing commodities, top trading partners, and overall Year-over-Year growth.

**Data Source & Acquisition**  
- Data downloaded from UN Comtrade (CSV):  
  - Reporter Countries: Nigeria, India, Vietnam  
  - Partner Countries: All  
  - Years: 2015–2023  
  - HS 6-digit classification, both Import & Export flows

**Excel Data Preparation**  
1. Imported raw CSV into Excel sheet “RawData.”  
2. Converted trade-flow codes (e.g., 1 = Import, 2 = Export) into text (“Import”/“Export”) using:  
   ```excel
   =IF([@[FlowCode]] = 1, "Import", IF([@[FlowCode]] = 2, "Export", "Other"))
