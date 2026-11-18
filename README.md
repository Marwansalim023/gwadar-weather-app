# Gwadar Weather Lab

A small web app that predicts the next day's maximum temperature in Gwadar, Pakistan, using a neural network that you choose.

**Live app:** https://gwadar-weather-app.vercel.app

## What it does

1. You choose one of three models: **RNN**, **LSTM** or **GRU**.
2. You enter the maximum temperature (°C) of the last seven days, or press "Fill with the latest Gwadar data".
3. The app predicts the maximum temperature of the next day and shows it with a chart.

## How it works

- The three models were trained in Google Colab with Keras on daily maximum temperatures for Gwadar from 2015 onwards.
- Each model reads seven days, one day at a time, and outputs the next day.
- The trained weights are saved in `models.js`. The page runs the same calculation in the browser with JavaScript, so there is no server and nothing you type is sent anywhere.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole web app: page, styling and the prediction code |
| `models.js` | The trained weights of the RNN, LSTM and GRU models |

## Run it on your own computer

Download both files into the same folder and open `index.html` in a browser.

## Data

Weather data by [Open-Meteo](https://open-meteo.com/). The historical values are a weather-model estimate (ERA5 reanalysis) for Gwadar's location, not readings from a weather station.

## Developed by

Marwan Salim
