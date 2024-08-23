
# ConPro: Construction Process Simulation 

## Overview

ConPro is an agent-based model simulating construction processes, focusing on installation and related tasks in building projects. It models workers, tasks, building zones, and project dynamics to analyze productivity and logistics in construction.

## Key Features

- Time-based simulation with customizable parameters
- Multiple worker types with varied skills
- Dynamic task allocation and zone-based movement
- Realistic worker behaviors (breaks, schedules)
- Comprehensive data collection and analysis

## Requirements

- Python 3.7+
- Mesa, NumPy, Pandas, Pathfinding

## Quick Start

1. Install dependencies:
   ```
   pip install mesa numpy pandas pathfinding
   ```

2. Place input CSVs in `ConPro/` directory.

3. Basic usage:
   ```python
   from conpro_model import ConPro
   from datetime import datetime

   model = ConPro(
       width=132,
       height=132,
       n_plastering_workers=5,
       n_painting_workers=5,
       simulation_startdate=datetime(2022, 5, 16, 6, 0, 0),
       simulation_days=30
   )

   model.run_model(step_count=10000)

   results = model.datacollector.get_model_vars_dataframe()
   print(results)
   ```

## Customization

Adjust parameters like project dates, work hours, worker skills, task sequences, and zone configurations in the `ConPro` class initialization.

## Data Collection

Metrics include worker utilization, task progress, zone occupancy, and project duration. Access via `model.datacollector`.

## Future Development

- Simulation visualization
- Enhanced reporting tools
- Advanced worker decision-making
- Performance optimization

## License

Dual-licensed:

1. Open Source: GNU General Public License v3.0
2. Commercial: Available for purchase (includes additional features)

## Contact

For licensing, support, or inquiries:

Alaa Barazi
Email: alaabarazi@gmail.com