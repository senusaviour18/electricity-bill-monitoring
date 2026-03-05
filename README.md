# Electrical Load Monitoring & Billing System (C++)

A small console app to register household/office appliances, estimate daily energy consumption (kWh), and calculate an electricity bill based on a cost per kWh. It also saves appliances to a file and generates a billing summary report.

## Features

- Register appliances (name, power in watts, hours used per day)
- View all registered appliances
- Search appliances by name (partial match, case-insensitive)
- Show energy usage per appliance and total daily energy
- Calculate bill using a user-provided cost per kWh
- Persist data to `appliances.txt`
- Export a report to `billing_summary.txt`

## Files Created

- `appliances.txt`  
  Stores appliances in a simple CSV format:
  `name,powerW,hoursPerDay`

- `billing_summary.txt`  
  Generated when you calculate the bill. Contains the energy breakdown and total bill.

## How It Works (Quick Math)

Daily energy for an appliance:

`kWh/day = (Watts × Hours per day) ÷ 1000`

Total daily energy is the sum of all appliances.  
Bill is calculated as:

`Bill = Total kWh/day × Cost per kWh`

## Requirements

- Any C++ compiler that supports C++11 or higher

## Compile and Run

### Windows (g++)

```bash
g++ main.cpp -o app
app
```
