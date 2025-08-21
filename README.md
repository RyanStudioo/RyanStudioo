<a href='https://ko-fi.com/O5O1180EK8' target='_blank'><img height='36' style='border:0px;height:20px;' src='https://storage.ko-fi.com/cdn/kofi6.png?v=6' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>
# Ryan Studio (RyanStudioo)
Hey there! I am RyanStudioo (RyanStudio was taken). I enjoy creating Discord Bots and other open-source modules!

# Favourite Projects

## [BlueMapWrapper](https://github.com/RyanStudioo/BlueMapWrapper)
BlueMapWrapper is a Pythonic lightweight API Wrapper for BlueMap!

Example Code:
~~~
import BlueMapWrapper
import datetime
import time
import asyncio

async def main():
    client = BlueMapWrapper.AsyncClient('http://map.eldrath.com:20098')   # Initialise Client
    logged_players = []
    while True:
        start = time.time()
        maps = await client.fetch_maps()   # Fetch list of available maps
        players_collection = await client.fetch_player_collection(maps[0]) # Get Player Collection obj of online players

        if players_collection.length == 0:
            print(f"{datetime.datetime.now()} No players found.")
        player_names = [i.name for i in players_collection.players]   # Get list of player names

        for i in player_names:
            if i not in logged_players:   # Check if player was in game when last logged
                print(f"[{datetime.datetime.now()}] Player {i} joined the game")   # Print current time and player

        for i in logged_players:
            if i not in player_names:   # Check if any player in logged players left the game/went invisible
                print(f"[{datetime.datetime.now()}] Player {i} left the game/went invisible")

        logged_players = player_names   # Log current players available for next minute
        seconds_until_next_minute = start+60 - time.time()   # Calculate time until next minute from starting
        await asyncio.sleep(seconds_until_next_minute)   # Wait until 1 minute from loop start

asyncio.run(main())
~~~



# Skills

## Languages 
[![Python](https://skillicons.dev/icons?i=py)](https://python.org "Python")
[![HTML](https://skillicons.dev/icons?i=html)](https://html.com/)
[![CSS](https://skillicons.dev/icons?i=css)](https://devdocs.io/css/)
[![JavaScript](https://skillicons.dev/icons?i=js)](https://www.javascript.com/)
[![Markdown](https://skillicons.dev/icons?i=md)](https://www.markdownguide.org/)

## Applications and Frameworks
[![Discord](https://skillicons.dev/icons?i=discord)](https://www.discord.com)
[![Flask](https://skillicons.dev/icons?i=flask)](https://flask.palletsprojects.com/en/stable)
[![Selenium](https://skillicons.dev/icons?i=selenium)](https://www.selenium.dev/)

