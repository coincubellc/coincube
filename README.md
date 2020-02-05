## COINCUBE | Crypto Portfolio Management
##### A Python/Vue.js crypto portfolio management and trade automation program with support for 10 exchanges.

##### Powered by <a href="https://github.com/ccxt/ccxt" target="_blank">ccxt</a>.

### Manage funds across multiple exchange accounts
![Dashboard](images/Dashboard.png)

### Supported exchanges:
#### Binance, Bitfinex, Bitstamp, Bittrex, Coinbase Pro, Coss, Kraken, Kucoin, Liquid, and Poloniex

![Dashboard](images/Cube.png)

### Fully customizable portfolios
![Dashboard](images/Edit.png)

### Trade engine - periodic or one-off rebalancing with a few button clicks
![Dashboard](images/Engine.png)


## Getting Started
You will need some developer tools to get up and running. Please install <a href="https://git-scm.com/book/en/v2/Getting-Started-Installing-Git">git</a>, <a href="https://www.docker.com/products/developer-tools">docker</a>, and <a href="https://nodejs.org/en/download/">node</a>.

You will also need <a href="https://www.python.org/downloads/">python3</a>, <a href="https://pip.pypa.io/en/stable/installing/">pip</a>, and  `pycrypto` installed locally. Once you have `pip` installed, you can run:
```
pip install pycrypto
```
## Clone repo
```
git clone https://github.com/coincubellc/coincube.git
```
Change to root directory
```
cd coincube
```

## Fetch all submodules
```
git submodule update --init --recursive
```
# Access keys and encryption seed
```
cd back
```

### Add CMC_API_KEY from Coin Market Cap
1. Visit <a href="https://pro.coinmarketcap.com/signup/">Coin Market Cap</a> and signup for their free Basic API. 
2. Paste the API key into lines 46 and 72 in `docker-compose.yml`. The key should be a string: `CMC_API_KEY: 'your_CMC_API_key_here'`.
3. Save `docker-compose.yml`.

### OPTIONAL - Add new VAULT_SEED
<p>If you plan to run this software in a production environment, you may wish to securely generate a new base64 encoded RSA Private key. 
</p>

1. From inside of the `back` folder, generate a new seed `python generate_vault_seed.py` which will generate a new seed.
2. Paste the entire encoded key except for the preceding as a string on lines 18 and 113 of `docker-compose.yml` in the root `coincube` directory.
4. Save `docker-compose.yml`.

### Building and Running the App
You will need <a href="https://docker.com" target="_blank">Docker</a>.

From inside of the root `coincube` directory, build/run the Docker container(s):
```
docker-compose build
```

Run the Docker container(s):
```
docker-compose up
```

### Important!
The first time you run `docker-compose up` you will need to wait for the database to be populated. This should take 10-15 minutes.

# Using Application
Once application is running, navigate to: http://0.0.0.0:8080 in your browser.

# To connect directly to the database
TCP/IP <br>
Name: local <br>
Host: 127.0.0.1 <br>
Username: admin <br>
Password: 4pa1z&ABK78R <br>
Database: coincube <br>
Port: 3306

