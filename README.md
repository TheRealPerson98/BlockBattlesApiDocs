# BlockBattles API Documentation

## Overview
This document outlines the usage of the BlockBattles API, providing access to player statistics, match details, leaderboards, and clan information for the BlockBattles game.

## Base URL
api.blockbattles.org

## Setup and Configuration
- Ensure you have a `.env` file set up with the necessary database connection parameters and the admin password.
- Dependencies: `express`, `mysql`, `dotenv`, `crypto`, `express-rate-limit`
- The API uses a MySQL database for data storage.

## API Endpoints

### Get Stats by Username
- **Endpoint:** `/:apikey/blockbattles/stats/:username`
- **Method:** `GET`
- **Description:** Retrieves player statistics based on the provided username.
- **Parameters:**
  - `apikey`: API key for authentication.
  - `username`: Player's username.

### Get Matches by Username
- **Endpoint:** `/:apikey/blockbattles/matches/:username`
- **Method:** `GET`
- **Description:** Fetches match details for a specified player.
- **Parameters:**
  - `apikey`: API key for authentication.
  - `username`: Player's username.

### Get Leaderboard
- **Endpoint:** `/:apikey/blockbattles/leaderboard`
- **Method:** `GET`
- **Description:** Provides the leaderboard sorted by player ELO.
- **Parameter:**
  - `apikey`: API key for authentication.

### Get All Player Statistics
- **Endpoint:** `/:apikey/blockbattles/allstats`
- **Method:** `GET`
- **Description:** Retrieves statistics for all players.
- **Parameter:**
  - `apikey`: API key for authentication.

### Get Clans
- **Endpoint:** `/:apikey/blockbattles/clans`
- **Method:** `GET`
- **Description:** Fetches information on all clans.
- **Parameter:**
  - `apikey`: API key for authentication.

### Get Clan Details
- **Endpoint:** `/:apikey/blockbattles/clan/:clanName`
- **Method:** `GET`
- **Description:** Provides detailed information about a specific clan.
- **Parameters:**
  - `apikey`: API key for authentication.
  - `clanName`: Name of the clan.

## Rate Limiting
- **Limit:** 100 requests per 15 minutes for each API key.
- **Over Limit Message:** "Too many requests, please try again later."

