# Smart City Traffic & Public Transport Analytics System

### Problem Statement 23 — GUVI Hackathon
---

## Project Overview

A Smart City Traffic and Public Transport Analytics System built using Informatica IICS.  
The project integrates traffic and public transport data, processes GPS and IoT sensor feeds, validates transportation records, and generates analytics dashboards.

---

## System Architecture

Oracle DB (Source)  
↓  
Informatica IICS (ETL Processing)  
↓  
Snowflake Data Warehouse  
↓  
Power BI Dashboard

---

## Technologies Used

- Oracle Database
- Informatica IICS
- Snowflake
- Power BI
- SQL
- GitHub

---

## Database Tables

### Master Tables
- TransportRoute
- Vehicle

### Transaction Tables
- TrafficRecord
- PassengerTrip
- TrafficAlert

---

## IICS Mappings

### 1. m_LD_TransportRoutes
Loads and validates transport route data.

### 2. m_Loadvehicles
Processes vehicle data and utilization analysis.

### 3. m_LoadTrafficRecords
Processes traffic congestion records and derives traffic status.

### 4. m_LoadPassengers
Handles passenger trip data with incremental loading.

### 5. m_TrafficAlert_Load
Routes traffic alerts based on severity levels.

---

## Taskflow

### tf_SmartCity_Transport_Load

Executes all mappings sequentially and sends:
- Success notification
- Failure notification

---

## Power BI Dashboard

### Dashboard Visuals
- Traffic Congestion Trends
- Route Performance
- Passenger Analytics
- Vehicle Utilization

### KPI Cards
- Average Congestion Level
- Passenger Count
- Active Routes
- Vehicle Count

---

## Features Implemented

- Incremental ETL Loading
- GPS Validation
- Traffic Alert Generation
- Vehicle Validation
- Reject Handling
- Congestion Analysis


## How to Run

1. Login to Informatica IICS
2. Open Taskflow:
   tf_SmartCity_Transport_Load
3. Click Run
4. Monitor execution in My Jobs
5. Refresh Power BI Dashboard

