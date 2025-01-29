<h1 align="center">
  <br>
  <a href="https://www.scuttle.gg"><img src="./scuttle_cropped.png" alt="Scuttle" width="250"></a>
  <br>
  Scuttle
  <br>
</h1>

<h3 align="center"><a href="https://www.scuttle.gg">scuttle.gg</a></h3>
<h4 align="center">A League of Legends analytics platform powered by a Discord bot, with backend services for fetching and caching match data, a frontend showcase website, and a public API.</h4>

<p align="center">
  <a href="https://www.buymeacoffee.com/eduardoalba">
    <img src="https://img.shields.io/badge/$-donate-ff69b4.svg?maxAge=2592000&amp;style=flat">
  </a>
</p>

<p align="center">
  <a href="#components">Components</a> •
  <a href="#how-to-use">How To Use</a> •
  <a href="#license">License</a>
</p>

## Overview

Scuttle is a multi-service project that helps League of Legends players track and analyze their match performance via Discord, web, and API interfaces. The project is composed of four distinct repositories working together to provide this functionality:

1. **[scuttle-bot](https://github.com/Eduardo-Projects/scuttle-bot)**: A Discord bot for adding summoners, fetching player statistics, and delivering reports.
2. **[scuttle-service](https://github.com/Eduardo-Projects/scuttle-service)**: A backend service for fetching and caching match data from the Riot Games API.
3. **[scuttle-web](https://github.com/Eduardo-Projects/scuttle-web)**: A website that showcases the bot and provides resources on how to add and use it in Discord servers.
4. **[scuttle-api](https://github.com/Eduardo-Projects/scuttle-api)**: A public API to serve data to the web.

---

![screenshot](./scuttle_demo.gif)

---

## Components

### 1. [scuttle-bot](https://github.com/Eduardo-Projects/scuttle-bot)

Scuttle is a Discord bot for analyzing League of Legends player statistics within Discord servers (guilds). It allows users to form guilds and fetch match data for summoners added to these guilds.

#### Key Features:
- Create a guild and add summoners within a Discord server.
- Fetch and cache match history for added summoners, powered by scuttle-service.
- Automatically generate reports for guild members based on match performance.
- Summoner data is updated regularly for the last 30 days of play.

#### How To Use:
1. [Add Scuttle](https://discord.com/oauth2/authorize?client_id=1222960533523796089&permissions=17600776293376&scope=bot) to your Discord server.
2. Use the `/enable` command to set up automated reports in your desired channel.
3. Add summoners with `/summoners add {name} {tag}`.
4. Data will update within an hour, after which manual reports can be retrieved using commands.

### 2. [scuttle-service](https://github.com/Eduardo-Projects/scuttle-service)

Scuttle-service is the backend responsible for fetching and caching summoner match data. It runs independently from the bot to handle Riot Games API requests while respecting rate limits.

#### Key Features:
- Fetches match data for every registered summoner in Scuttle.
- Caches match history to ensure efficient data retrieval and report generation.
- Runs hourly to update summoner match data regularly.

#### Purpose:
Scuttle-service was created to offload the heavy backend data-fetching process from the Discord bot. It ensures smooth operation by adhering to the rate limits of the Riot Games API.

### 3. [scuttle-web](https://github.com/Eduardo-Projects/scuttle-web)

Scuttle-web is a website designed to showcase the Scuttle bot and provide users with resources on how to add and use the bot within their Discord servers.

#### Key Features:
- Information about how to use the Scuttle Discord bot.
- Resources for adding the bot to a server.
- Documentation on commands and bot features.
- A hub for users to explore what Scuttle offers.

### 4. [scuttle-api](https://github.com/Eduardo-Projects/scuttle-api)

Scuttle-api is a public API that serves data the web interface.

#### Key Features:
- Provides endpoints to fetch bot statistics:
    - Guild Count
    - Summoner Count
    - Commands Count

---

## How To Use

1. [Add Scuttle-Bot](https://discord.com/oauth2/authorize?client_id=1222960533523796089&permissions=17600776293376&scope=bot) to your Discord server.
2. Visit the [Scuttle website](https://www.scuttle.gg) to learn more about how to use the bot and explore its features.

## License

MIT

---

> GitHub [@eduardoalba00](https://github.com/eduardoalba00) &nbsp;&middot;&nbsp; Website [Scuttle.gg](https://www.scuttle.gg) 

