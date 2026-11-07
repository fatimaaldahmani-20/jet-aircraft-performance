# Jet Aircraft Performance Explorer

Front-end AERO301 aircraft-performance application for VS Code.

## Run in VS Code

1. Open the `aero-performance-app` folder in VS Code.
2. Open `index.html` in a browser, or use the VS Code Live Server extension if it is installed.
3. Enter the aircraft and operating-condition inputs.
4. Select **Run analysis**.

No Node.js, backend, database, package installation, or internet connection is required.

## Implemented model

- ISA troposphere from 0–11,000 m.
- Steady, level, unaccelerated flight.
- Parabolic drag polar: `CD = CD0 + K CL²`, with `K = 1/(π e AR)`.
- Constant jet thrust available: `TA = TA,input`.
- Power available: `PA = TA V`.
- Stall speed, minimum thrust and power, maximum level-flight speed, excess thrust and power, rate of climb, maximum `L/D`, and best-glide condition.
- Required thrust, power, excess-thrust, excess-power, and rate-of-climb plots.

The application rejects missing, non-numeric, non-finite, physically invalid, and out-of-range inputs. It also reports speeds below stall, speeds above Mach 0.7, unavailable intersections, insufficient thrust, and non-positive climb capability.
