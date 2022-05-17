# market-forecast
Cryptos, Stocks, or Forex: Which is better to trade? Forecast with Streamlit 

# Disclosures

## Risk Disclosure

I am not
not a certified financial planner/advisor
not a certified financial analyst
not an economist
not a CPA
not an accountant
not a lawyer
not responsible for any losses or damages caused by the use of this tool.

I am not a finance professional through formal education. I am an individuas who believes and takes pride in showing people the power of Cryptos, Stocks and/or Forex trading. The contents on this site are for informational and entertainment purposes only and does not constitute financial, accounting, or legal advice. I can’t promise that the information shared on our posts is appropriate for you or anyone else. By using this site, you agree to hold the site owner, web hosting company, and any contributors harmless from any ramifications, financial or otherwise, that occur to you as a result of acting on information found on this site.


## AFFILIATE PROGRAMS
I am not promoting educational programs for Forex Trading.


## FOREX RISK DISCLOSURE
U.S. Government Required Disclaimer – Trading foreign exchange on margin carries a high level of risk and may not be suitable for all investors. The high degree of leverage can work against you as well as for you. Before deciding to invest in foreign exchange, you should carefully consider your investment objectives, level of experience, and risk appetite. The possibility exists that you could sustain a loss of some or all of your initial investment and therefore you should not invest money that you cannot afford to lose. You should be aware of all the risks associated with foreign exchange trading, and seek advice from an independent financial advisor if you have any doubts.

The purchase, sale or advice regarding a currency can only be performed by a licensed Broker/Dealer; Neither us, nor our affiliates or associates involved in the production and maintenance of this service or this site, is a registered Broker/Dealer or Investment Advisor in any State or Federally-sanctioned jurisdiction. All purchasers of services or products referenced at this site are encouraged to consult with a licensed representative of their choice regarding any particular trade or trading strategy. No representation is being made that any account will or is likely to achieve profits or losses similar to those discussed on this website. The past performance of any trading system or methodology is not necessarily indicative of future results.

You must clearly understand this: Information contained here and in the alert service(s) is not an invitation to trade any specific investments. Trading requires risking money in pursuit of future gain. That is your decision. Do not risk any money you cannot afford to lose. This document does not take into account your own individual financial and personal circumstances. It is intended for educational purposes only and NOT as individual investment advice. Do not act on this without advice from your investment professional who will verify what is suitable for your particular needs and circumstances. Failure to seek detailed professional, personally tailored advice prior to acting could lead you to act contrary to your own best interests and could lead to losses of capital.


# Development

## Cloning the repository

1. Create a projects folder (if you don't have one): `mkdir path_to_project_folder`
2. Go to the projects folder: `$ cd path_to_project_folder`
3. To clone a repository with git clone <url>. `$ git clone https://github.com/xandrade/alpha-api.git`


## Linux (Ubuntu-20.04) through WSL 2

1. Go to the project folder, for example: `$ cd path_to_project_folder`
2. Create virtual enviroment: `$ python3 -m venv .venv`
3. Activte enviroment: `$ source .venv/bin/activate`
4. After the virtual environment is active, we are going to want to ensure that a couple of essential Python packages within the virtual environment are up to date: `(.venv)$ pip install -U setuptools pip`
5. Install the requirements: `(.venv)$ pip install -r requirements.txt`
6. Open VSCode `(.venv)$ code .`


## WSL Port Forwarding

1. Allow Windows & Linux to reach each other. On Linux get IP address: `$ip r`
2. Run CMD as Administrator: `netsh interface portproxy add v4tov4 listenport=5000 listenaddress=0.0.0.0 connectport=5000 connectaddress=LINUX_IP_ADDRESS` and don't forget to update the ports and IP address.
2.1 Get WSL2 IP address: `ip addr show eth0 | grep 'inet\b' | awk '{print $2}' | cut -d/ -f1`


# Running the web app

1. Go to the project folder `$ cd path_to_project`
2. Activate environment `$ source .venv/bin/activate`
3. Go to app folder `$ cd ./alpha-api/app`
4. Run `$ streamlit run main.py`

## Running in product

1. Go to the project folder `$ cd path_to_project`
2. Activate environment `$ source .venv/bin/activate`
3. Go to app folder `$ cd ./alpha-api/app`
4. Run `$ hypercorn --bind '0.0.0.0:5000'  main:app -w 1 --worker-class uvloop`

# ToDo

Try using [/PyScript](https://pyscript.net/) to run the app.