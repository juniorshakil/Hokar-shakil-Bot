---------

###  —͟͟͞͞𝐂𝐘𝐁𝐄𝐑 ☢️_𖣘 -𝐁𝐎𝐓 ⚠️ 𝑻𝑬𝑨𝑴_ ☢️
❖ **`A Messenger Multi Device Bot To Take Your Messenger To Another Level !`** ❖

----------

## CLICK <a href="https://github.com/cyber-Shakil/CYBER-BOT-COMMUNITY/issues">HERE IF YOU ARE NEW TO BOTS</a>

<p align="center">
  <a href="https://postimg.cc/QHC0ZhjF" target="_blank">
    <img src="https://i.postimg.cc/c4MjYLjB/20250515-215136.jpg" border="0" alt="20250515-215136"/>
  </a>
</p>

-------

<p align="center">
  <a href="#"><img src="http://readme-typing-svg.herokuapp.com?color=cyan&center=true&vCenter=true&multiline=false&lines=`𝗜𝘀𝗹𝗮𝗺𝗶𝗰𝗸+𝗰𝗵𝗮𝘁+𝗯𝗼𝘁+V2`" alt="Typing SVG"></a>
</p>

<p align="center">
  <a href="https://github.com/cyber-Shakil/"><img title="Followers" src="https://img.shields.io/github/followers/cyber-Shakil?color=blue&style=flat-square"></a>
  <a href="https://github.com/cyber-Shakil/CYBER-BOT-COMMUNITY/stargazers/"><img title="Stars" src="https://img.shields.io/github/stars/cyber-Shakil/CYBER-BOT-COMMUNITY/?color=blue&style=flat-square"></a>
  <a href="https://github.com/cyber-Shakil/CYBER-BOT-COMMUNITY/network/members"><img title="Forks" src="https://img.shields.io/github/forks/cyber-Shakil/CYBER-BOT-COMMUNITY?color=blue&style=flat-square"></a>
  <a href="https://github.com/cyber-Shakil/CYBER-BOT-COMMUNITY/"><img title="Size" src="https://img.shields.io/github/repo-size/cyber-Shakil/CYBER-BOT-COMMUNITY?style=flat-square&color=blue"></a>
  <a href="https://github.com/cyber-Shakil/CYBER-BOT-COMMUNITY/graphs/commit-activity"><img height="20" src="https://img.shields.io/badge/Maintained%3F-yes-green.svg"></a>
</p>

<div align="center"><br> 
  <img src="https://profile-counter.glitch.me/SILENT-SOBX-MD/count.svg" /><br>—͟͟͞͞𝐂𝐘𝐁𝐄𝐑 ☢️_𖣘 -𝐁𝐎𝐓 ⚠️ 𝑻𝑬𝑨𝑴_ ☢️
</div>




DEVLOPER WORKFLOW 😗

name: Node.js CI

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  build:
    runs-on: ubuntu-latest

    strategy:
      matrix:
        node-version: [20.x]
        # See supported Node.js release schedule at https://nodejs.org/en/about/releases/

    steps:
    # Step to check out the repository code
    - uses: actions/checkout@v2

    # Step to set up the specified Node.js version
    - name: Use Node.js ${{ matrix.node-version }}
      uses: actions/setup-node@v2
      with:
        node-version: ${{ matrix.node-version }}

    # Step to install dependencies
    - name: Install dependencies
      run: npm install

    # Step to run the bot with the correct port
    - name: Start the bot
      env:
        PORT: 8080
      run: npm start
