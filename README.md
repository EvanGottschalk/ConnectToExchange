[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/EvanGottschalk/ConnectToExchange">
    <img src="logo.png" alt="Logo" width="250" height="130">
  </a>

  <h3 align="center">ConnectToExchange</h3>

  <p align="center">
    A simple program for remotely connecting to cryptocurrency exchanges and retrieving information from them.
    <br />
    <a href="https://github.com/EvanGottschalk/ConnectToExchange"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/EvanGottschalk/ConnectToExchange">View Demo</a>
    ·
    <a href="https://github.com/EvanGottschalk/ConnectToExchange/issues">Report Bug</a>
    ·
    <a href="https://github.com/EvanGottschalk/ConnectToExchange/issues">Request Feature</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary><h2 style="display: inline-block">Table of Contents</h2></summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

I started working on `ConnectToExchange` in 2017 during the last big bitcoin hype. Its purpose is to create the initial connection with an exchange, and to fetch basic information from the exchange, such as public price data or one's own personal trading history.

`ConnectToExchange` can be used on its own to gather information. It can also be imported into other modules to grant them the ability to communicate with exchanges, such as a module for executing trades. `ConnectToExchange` has no function for actually executing a trade itself.


### Built With

`Python3.6`

[`CCXT`](https://github.com/ccxt/ccxt) - The fantastic `CCXT` library is critical to `ConnectToExchange`. Huge thanks to [@kroitor](https://github.com/kroitor) and the many other `CCXT` contributors that made this program possible.

[`GetCurrentTime`](https://github.com/EvanGottschalk/GetCurrentTime) - This program is imported to help collect time data in a legible fashion. It also allows for the translation of time stamps. You can read more about it here: [github.com/EvanGottschalk/GetCurrentTime](https://github.com/EvanGottschalk/GetCurrentTime)

[`AudioPlayer`](https://github.com/EvanGottschalk/AudioPlayer) - This is a simple program for playing custom audio alerts. It can be used with `ConnectToExchange` to warn you if an error occurs. You can read more about it here: [github.com/EvanGottschalk/AudioPlayer](https://github.com/EvanGottschalk/AudioPlayer)



<!-- GETTING STARTED -->
## Getting Started

### Prerequisites

Before using `ConnectToExchange`, you must first obtain an API key and secret from the cryptocurrency exchange of their choosing. You also need to install the [`CCXT`](https://github.com/ccxt/ccxt) library.

### Installation

1. Install [`CCXT`](https://github.com/ccxt/ccxt). This can be done in a number of ways. I used `pip`.
   ```sh
   pip install ccxt
   ```
2. Download the `.py` files in from this repository (`ConnectToExchange.py`, `GetCurrentTime.py`, and optionally `AudioPlayer.py`).

3. In the same folder as `ConnectToExchange.py`, create a `.txt` file to store your API information. Its name should start with the exchange you are using, followed by an underscore, followed by the name of the account you're using, and ending with `_API.txt`.

    For example, if you are using your **Main** account on **Coinbase**, you would name the `.txt` file **`Coinbase_Main_API.txt`**

    If your API key is `view-only`, you can save your cryptocurrency exchange API key on the 1st line, and your API secret on the 2nd. However, **if your API key has `trade` priveleges, you should save an encrypted version of both your key and secret on those lines instead.**

    To encrypt your API information, I recommend using `CustomEncryptor.py`, which can be downloaded here: [github.com/EvanGottschalk/CustomEncryptor](https://github.com/EvanGottschalk/CustomEncryptor)

4. Run `ConnectToExchange.py`

5. Congratulations! You can now use `ConnectToExchange` to connect to your favorite exchanges and retrieve information from them!



<!-- USAGE EXAMPLES -->
## Usage

**Checking Prices** - A quick, simple, and handy feature of `ConnectToExchange` is its ease of acquiring the current price of an asset of your desire. This can be incorporated into all sorts of other programs.

**Checking Orders** - You can use `ConnectToExchange` to check the status of your orders to see if they are open or have been filled. If they have been filled, you can then use the closing information to calculate profits/losses.

**Accumulating OHCLVs** - If you run `ConnectToExchange` on a regular basis, it will accumulate OHLCV information in a Master OHLCV. This is handy if you want to really analyze granular price action over the long term. Normally, exchanges limit how many data points you can retrieve all at once. On Binance, for example, you are limited to only 500 data points. So, if you want to know the price every minute for the past 600 minutes, you're out of luck - unless you ran `ConnectToExchange` the previous day. Based on how granular you need the information to be, so long as you run `ConnectToExchange` regularly, you can completely overcome the limits set by the exchanges.

**A Whole Lot More** - The breadth of ways `ConnectToExchange` can be used in other programs is limitless. Any module that could benefit from accessing cryptocurrency prices and their relationships to each other can use `ConnectToExchange` to quickly attain that feature.

<!-- ROADMAP -->
## Roadmap

See the [open issues](https://github.com/EvanGottschalk/ConnectToExchange/issues) for a list of proposed features (and known issues).



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request



<!-- LICENSE -->
## License

Distributed under the GNU GPL-3 License. See `LICENSE` for more information.



<!-- CONTACT -->
## Contact

Evan Gottschalk - [@Fort1Evan](https://twitter.com/Fort1Evan) - magnus5557@gmail.com

Project Link: [https://github.com/EvanGottschalk/ConnectToExchange](https://github.com/EvanGottschalk/ConnectToExchange)



<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements

* Huge thanks to [@kroitor](https://github.com/kroitor) and the many other [CCXT](https://github.com/ccxt/ccxt) contributors that made this program possible.
* Thanks to [@bartmassi](https://github.com/bartmassi) for working with me to improve the program's security, and for answering numerous other questions, and also for always being a helpful, available, and informative teacher (and friend).

Thinking about contributing to this project? Please do! Your Github username will then appear here.




<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/EvanGottschalk/ConnectToExchange.svg?style=for-the-badge
[contributors-url]: https://github.com/EvanGottschalk/ConnectToExchange/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/EvanGottschalk/ConnectToExchange.svg?style=for-the-badge
[forks-url]: https://github.com/EvanGottschalk/ConnectToExchange/network/members
[stars-shield]: https://img.shields.io/github/stars/EvanGottschalk/ConnectToExchange.svg?style=for-the-badge
[stars-url]: https://github.com/EvanGottschalk/ConnectToExchange/stargazers
[issues-shield]: https://img.shields.io/github/issues/EvanGottschalk/ConnectToExchange.svg?style=for-the-badge
[issues-url]: https://github.com/EvanGottschalk/ConnectToExchange/issues
[license-shield]: https://img.shields.io/github/license/EvanGottschalk/ConnectToExchange.svg?style=for-the-badge
[license-url]: https://github.com/EvanGottschalk/ConnectToExchange/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/EvanGottschalk
