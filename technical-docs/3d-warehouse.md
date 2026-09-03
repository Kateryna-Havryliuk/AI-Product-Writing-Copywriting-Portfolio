# 3D Smart Warehouse — User Guide

## Project Description

3D Smart Warehouse is an interactive visualization and inventory management system for a private enterprise. The system allows warehouse workers to find goods in a three-dimensional warehouse space of 738 m² (41×18 m) in real time.

## Warehouse Specifications

- Area: 738 m² (41 m × 18 m)
- Height: 4 m
- Racks: 19 units
- Zones: 5 (North, South, East, West, Central)
- Shelves: 4 to 6 per rack
- Entrances: 3 (main south, 2 side west)

## Functionality

**Navigation & Search:**
- 3D visualization with all racks and passages
- Text search with autocomplete
- Voice search (Ukrainian)
- Barcode scanner (EAN-13, Code 128, Code 39)
- Optimal routes from nearest entrance

**Goods Management:**
- Adding via form or import
- Quantity editing with validation
- Moving between racks and shelves
- Deletion with confirmation
- Operation history (who, when, what changed)

**Roles:**
- Senior Warehouse Worker — full access (PIN)
- Warehouse Worker — quantity editing, moving (PIN)
- View Only — no changes

## External Integrations

**1C:Enterprise:**
- COM connection (Windows)
- XML/Excel export files
- OData API
- Auto-update (5/15/30/60 min)

**Excel / Google Sheets:**
- Google Sheets via public CSV export
- Excel Online via OneDrive shared links
- Local network paths

## Quick Start

```bash
pip install -r requirements.txt
python app.py
# http://127.0.0.1:5001
