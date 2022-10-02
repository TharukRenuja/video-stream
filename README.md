<h2 align="centre">VIDEO STREAM BOT</h2>

Telegram bot project for streaming video on telegram video chat, powered by [py-tgcalls](https://github.com/pytgcalls/pytgcalls) and [pyrogram](https://github.com/pyrogram/pyrogram)

<p align="center"><a href="https://t.me/videostreamvcslbot"><img src="https://telegra.ph/file/1fbd730aed41f0e70cf68.jpg" width="400"></a></p>
<p align="center">
    <a href="https://www.python.org/" alt="made-with-python"> <img src="https://img.shields.io/badge/Made%20with-Python-black.svg?style=flat-square&logo=python&logoColor=blue&color=red" /></a>
</p>

## ✨ Features
- Stable video streaming
- Clear video & audio quality
- Support youtube live streaming
- Support youtube video streaming
- Support streaming video from mp4 video/file video
- Join & Leave command for assistant
- Support inline search video
- Support youtube search video link
- Support PornHub direct link streaming 🔞
- Video downloader feature
- Song downloader feature
- Have many other interesting features

## 🛠 Commands:
- ``/vplay`` (reply to video/give yt url) - to start video streaming
- ``/vstop`` - to stop video streaming
- ``/song`` (song name) - to download song
- ``/vsong`` (video name) - to download video
- ``/vjoin`` - invite the assistant join to your group
- ``/vleave`` - order the assistant to leave from your group
- ``/lyric`` (query) - lyric scrapper
- ``/tts`` (reply to text) - text to speech
- ``/alive`` - check the bot alive status
- ``/ping`` - check the bot ping status
- ``/uptime`` - check the bot uptime status
- ``/sysinfo`` - show the bot system information

## 🧙🏻‍♂️ Sudo Only:
- ``/rmd`` - clear all downloaded files
- ``/rmw`` - clear all downloaded raw files
- ``/leaveall`` - order the assistant to leave from all group

📝 Note: From now, /vstream & /vstop command can only be used by group admins.

## 🧪 Get STRING_SESSION from below:

TAP THIS: [![GenerateString](https://img.shields.io/badge/repl.it-generateString-yellowgreen)](https://replit.com/@levinalab/StringSession#main.py)

## 💜 Deploy To Heroku
The easy way to host this bot, deploy to Heroku

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/murtixc/video-stream)

## 🚄 Deploy To Railway
[![Deploy+on+Railway](https://railway.app/button.svg)](https://railway.app/new/template?template=https://github.com/TharukRenuja/video-stream&envs=API_ID,API_HASH,BOT_TOKEN,BOT_USERNAME,ASSISTANT_NAME,SESSION_NAME,SUDO_USERS,DURATION_LIMIT)

## 🌀 Run On Workflows

- fork this repository
- Go to your forked repository settings
- Scroll down and select the `secrets` tab
- Click on `New repository secret` button
- Add the environmental vars as mentioned here
- Then create new file with structure `.github/workflows/run.yml`
- Now in `run.yml` file, fill with this code below, just copy it and paste in `run.yml` file


<details>
  <summary>
    <b>View code</b>
  </summary>  

```sh
name: Run on workflows
on:
    schedule:
      - cron: "0 */6 * * *"
    push:
      branches: [ main ]
    workflow_dispatch:
    
env:
  API_ID: "${{ secrets.API_ID }}"
  API_HASH: "${{ secrets.API_HASH }}"
  SESSION_NAME: "${{ secrets.SESSION_NAME }}"
  BOT_USERNAME: "${{ secrets.BOT_USERNAME }}"
  ASSISTANT_NAME: "${{ secrets.ASSISTANT_NAME }}"
  DURATION_LIMIT: "${{ secrets.DURATION_LIMIT }}"
  BOT_TOKEN: "${{ secrets.BOT_TOKEN }}"
  SUDO_USERS: "${{ secrets.SUDO_USERS }}"

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
       - uses: actions/checkout@v2
         with:
            ref: beta
       - uses: styfle/cancel-workflow-action@0.9.0
         name: "Cancelling duplicate workflow runs"
         with:
            all_but_latest: true
            access_token: ${{ github.token }}
       - uses: actions/setup-node@v2
         with:
            node-version: '16'
       - name: Set up Python 3.9
         uses: actions/setup-python@v2.2.2
         with:
           python-version: 3.9
       - name: cloning repo and install

         continue-on-error: true
         run: |
           sudo apt -qq update && sudo apt -qq install -y --no-install-recommends ffmpeg neofetch
           pip3 install -r requirements.txt
          #  echo "API_ID=${{ secrets.API_ID }} | tee .env
          #  echo "API_HASH=${{ secrets.API_HASH }} | tee -a .env
          #  echo "BOT_USERNAME=${{ secrets.BOT_USERNAME }} | tee -a .env
          #  echo "ASSISTANT_NAME=${{ secrets.ASSISTANT_NAME }} | tee -a .env
          #  echo "SESSION_NAME=${{ secrets.SESSION_NAME }} | tee -a .env
          #  echo "DURATION_LIMIT=${{ secrets.DURATION_LIMIT }} | tee -a .env
          #  echo "SUDO_USERS=${{ secrets.SUDO_USERS }} | tee -a .env
          #  echo "BOT_TOKEN=${{ secrets.BOT_TOKEN }} | tee -a .env || echo "Proceeding with bot"
          #  cat .env
       - name: Running
         timeout-minutes: 350
         continue-on-error: true
         run: |
           python3 -m bot
           echo "Bot Died"
```
</details>


- After adding all, Go to the Actions tab and start/run the workflows

## VPS Deployment
```sh
- sudo apt update && upgrade -y
- sudo apt install python3-pip -y virtualenv
- sudo apt install ffmpeg -y
- nvm install v16.5.0
- npm i -g npm
- git clone https://github.com/TharukRenuja/video-stream
- cd video-stream
- virtualenv venv #Create Virtual Environment.
- source venv/bin/activate #Activate Virtual Environment
- pip3 install --upgrade pip
- pip3 install -U -r requirements.txt
- cp -r sample.env local.env
- nano local.env #Fill it with your variables value.
- python3 -m bot
```

# Special Credits 💖

- [Tharuk](https://github.com/TharukRenuja) ``Dev``
- [Levina](https://github.com/levina-lab) ``Dev``
- [Sammy-XD](https://github.com/Sammy-XD) ``Dev``
- [Zxce3](https://github.com/Zxce3) ``Dev``
- [DoellBarr](https://github.com/DoellBarr) ``Dev``
- [tofikdn](https://github.com/tofikdn) ``Dev``
- [Laky's](https://github.com/Laky-64) for [``pytgcalls``](https://github.com/MarshalX)
- [Dan](https://github.com/delivrance) for [``Pyrogram``](https://github.com/pyrogram)

### Support & Updates 🎑
<a href="https://t.me/trtechguide"><img src="https://img.shields.io/badge/Join-Group%20Support-blue.svg?style=for-the-badge&logo=Telegram"></a> <a href="https://t.me/SLBotsOfficial"><img src="https://img.shields.io/badge/Join-Updates%20Channel-blue.svg?style=for-the-badge&logo=Telegram"></a>
