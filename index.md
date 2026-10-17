---
layout: project_page
permalink: /
title: "Plastic Mold Factory: Capacity-Load Forecasting & Economic Analysis System"
authors:
  - He Zhang
tags: [Flask, Machine Learning, Scheduling, Economic Analysis, ECharts]
code: https://github.com/wyl-ctrl-c-v/moju-website
description: A capacity-load forecasting and cost-reduction & efficiency-improvement analysis system for plastic mold factories, integrating data simulation, machine-learning forecasting, scheduling optimization, economic analysis, and a visualization dashboard.
---

<div class="columns is-centered has-text-centered">
    <div class="column is-four-fifths">
        <h2>Abstract</h2>
        <div class="content has-text-justified">
This system targets capacity management and cost-reduction &amp; efficiency-improvement needs in plastic mold factories. It integrates five stages: <b>data simulation, machine-learning forecasting, scheduling optimization, economic analysis, and a visualization dashboard</b>. Based on five types of data &mdash; equipment load, orders, processes, material loss, and finance &mdash; it builds a capacity-load forecasting model with scikit-learn to predict equipment load rate, idle rate, and energy consumption over the next 30 days. On top of that, it performs scheduling optimization and cost-saving analysis to quantify efficiency gains, providing data support for capacity planning and operational decisions.
        </div>
    </div>
</div>

---

## Background

Plastic mold factories commonly face unbalanced equipment load, difficult order-delivery control, and opaque cost structures:

- **Large equipment-load fluctuations**: some equipment is chronically overloaded while others sit idle, lacking forward-looking capacity forecasts;
- **Experience-based scheduling**: order scheduling relies on manual experience, making it hard to coordinate urgent and delayed orders and stabilize on-time delivery;
- **No clear lever for cost reduction**: labor, material, energy, and maintenance costs lack quantitative analysis, making it hard to evaluate cost-reduction measures.

## Objective

The goal is to build a closed loop of <i>data modeling &rarr; capacity forecasting &rarr; scheduling optimization &rarr; economic analysis &rarr; visualization</i>, and thereby:

1. Provide machine-learning forecasts of equipment load rate, idle rate, and energy consumption over the next 30 days;
2. Optimize scheduling based on forecasts to reduce idle rate and order-delay rate;
3. Quantify the cost structure and savings potential to support cost-reduction and efficiency-improvement decisions.

## Core Features

- **Overview dashboard**: key indicators at a glance &mdash; total machines, average load rate, order-delay rate, monthly profit, urgent-order ratio, and more;
- **Capacity-load forecasting**: predict equipment load rate / idle rate / energy consumption for the next 30 days from 30 days of history, with an overload alert line;
- **Scheduling optimization**: compare cycle efficiency, idle rate, and on-time delivery before vs. after optimization, quantifying scheduling gains;
- **Economic analysis**: monthly cost trends, cost-saving breakdown (labor / material / energy / maintenance), and raw-material loss analysis;
- **Equipment detail**: per-machine load details and output statistics;
- **Data upload**: upload custom CSV data; the prediction model is automatically retrained in the background.

## Architecture

![System architecture]({{ site.baseurl }}/static/image/pipeline.svg)
<div class="fig-caption">Figure 1: System data flow and module architecture</div>

## Screenshots

![System dashboard]({{ site.baseurl }}/static/image/dashboard.svg)
<div class="fig-caption">Figure 2: Overview dashboard (sample screenshot)</div>

## Modules

| Module | Function | Key technology |
|--------|----------|----------------|
| Data simulation | Generate equipment-load / order / process / material-loss / finance data | pandas, numpy |
| Capacity forecasting | Forecast load rate, idle rate, and energy over the next 30 days | scikit-learn |
| Scheduling optimization | Order scheduling, urgent/delayed order coordination, gain quantification | Heuristic scheduling |
| Economic analysis | Cost structure, savings breakdown, material-loss analysis | pandas aggregation |
| Visualization | Interactive dashboard and charts | ECharts |
| Data upload | CSV upload + automatic model retraining | Flask, multithreading |

## Tech Stack

- **Backend**: Flask (REST API)
- **Data &amp; models**: pandas, numpy, scikit-learn
- **Frontend**: HTML/CSS/JavaScript, ECharts
- **Deployment**: Gunicorn (deployable to platforms such as Render / Railway)

## Citation

```
@misc{moju2026capacity,
  title={Plastic Mold Factory: Capacity-Load Forecasting & Economic Analysis System},
  author={He Zhang},
  year={2026},
  note={A Flask + scikit-learn system for capacity forecasting, scheduling optimization, and economic analysis},
  howpublished={\url{https://github.com/wyl-ctrl-c-v/moju-website}}
}
```
