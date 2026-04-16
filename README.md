# balloon-tracker-ui

**Archived.** React frontend for the **Hot Air Balloon Tracker / Weather Balloon Chaser** project. Visualizes a weather balloon in flight and displays the predicted landing zone, powered by data from the `balloon-tracker` server.

Package name: `balloon-ui`.

## About the balloon project

A university-era project for launching weather balloons and recovering them after burst. The system integrates live telemetry from HAB Hub (the amateur high-altitude-ballooning telemetry network), a landing-prediction model, and a chase-team navigation UI so ground teams can drive to the right field before the payload hits the grass.

## What this repo is

A React app that calls the `balloon-tracker` server's HTTP endpoints and renders:

- Live balloon position + altitude
- Trajectory over time (`recharts`)
- Predicted landing zone
- Toggles for display options (`react-toggle`)

## Tech stack

- **React** (create-react-app, `react-scripts`)
- **Semantic UI React** + `semantic-ui-css`
- **recharts** for trajectory / altitude graphs
- **axios** for API calls
- **react-toggle** for display toggles

## Structure

```
src/                # React app
public/
package.json        # "balloon-ui"
```

## Dev + build

```bash
yarn
yarn start          # react-scripts dev server
yarn build
```

## Related projects

The hot air balloon ecosystem in this org:

- [`balloon-tracker`](https://github.com/gitpancake/balloon-tracker) — main server — HAB Hub ingestion + landing prediction + navigation
- [`co-ordinates-logger-api`](https://github.com/gitpancake/co-ordinates-logger-api) — the co-ordinates / position backend (login, device + position CRUD)
- [`co-ordinates-tracker-dashboard`](https://github.com/gitpancake/co-ordinates-tracker-dashboard) — admin dashboard for managing users of the co-ordinates system
