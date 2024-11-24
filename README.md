### INTRODUCTION 
FLUIDEFI® is an award-winning platform that provides near real-time <sup><a name="footnote1">1</a></sup> compliant & auditable analytics, portfolio management, and alerting for thousands of decentralized financial (DeFi) digital assets. FLUIDEFI's metrics are calculated using blockchain transaction logs, not third party APIs. FLUIDEFI is blockchain, network, and automatic market-maker (AMM) agnostic.

The FLUIDEFI RESTful API allows developers to:
- obtain detailed, accurate analytics of digital asset to identify investment opportunities across multiple blockchains, networks, and platforms;
- create portfolios of various digital assets from multiple platforms;
- model the portfolio's performance based on historical returns;
- optimize the balances of the portfolios to maximize future profitability;
- monitor and receive alerts when digital asset metrics reach specified values or change over periods of time;
- analyze the actual profit and loss of digital asset holdings including those spread across multiple portfolios (wallets);
- swap digital assets;
- add and remove liquidity from liquidity pools;

<sup>[1](#footnote1)</sup> The term "near real-time" refers to the time delay introduced by 1) automated data processing and 2) network transmission between the occurrence of an event and the request of the processed data (the API call). The API responses include <em>as_of_timestamp</em> that specifies the UTC date/time that the API response was generated and <em>last_processed</em> which includes the UTC date/time the information was last calculated. FLUIDEFI uses ISO 8601 format for datetimes.


### ACCESS TO THE FLUIDEFI API
Accessing the FLUIDEFI RESTful API requires:

1. A username and password. This information is provided when enrolling for the FLUIDEFI services. If you do not have an account, [contact us](https://fluidefi.com/#contact) to schedule a demonstration or get access.

2. The API endpoint to use. The API end-point will be in the form of a URL. For example: https://my-api.fluidefi.com  
> NOTE: **The API end-point URL for your account is provided when enrolling for the FLUIDEFI services.** Do not use the example listed.

3. Depending on your subscription level, the IP address(es) of your computer(s) making API requests may need to be <em>white-listed</em> with the FLUIDEFI network firewall. Please send an email with your username and the IP address(es) to be whitelisted to FLUIDEFI Support. Static IP addresses are recommended. Note: when using dynamic IP addresses, the FLUIDEFI firewall does not automatically update when your dynamic IP address changes.

All API requests must be made to your designated API URL using HTTPS protocol with TLS v1.3 or later via TCP/IP port 443. All FLUIDEFI servers use SSL certificates with sha256RSA signature algorithms issued by <em>Sectigo RSA Domain Validation Secure Server CA</em>. 

> It is important to note that some API calls can generate very long responses. Please review this documentation for performance recommendations.


### FLUIDEFI DEVELOPER TOOLS 
The FLUIDEFI RESTful API calls are fully documented and can be tested with 27 different programming language/frameworks using [FLUIDEFI API Documentation](https://analytics.fluidefi.com/api/docs/)


### FLUIDEFI SUPPORT
Your Service Level Agreement (SLA) is based on your subscription level.

- Priority email support (SLA 1-2 business days): <support@fluidefi.com>
- Dedicated Slack channel (SLA: 6 hours): Created when establishing your account. 
- Support Email & Slack Monitoring Hours: 10:30 AM UTC - 02:30 AM UTC


### FLUIDEFI'S LIQUIDITY POOL METRICS

| Key                       | Description                                                                                           |
| :---------------------    | :-------------------------------------------------------------------------------------------------    |
| open_timestamp_utc        | Start date/time for information in this record. The first record will begin on this date              |
| close_timestamp_utc       | End date/time for information in this record. The close of the last record is this date  				|
| total_period_return 		| Total rate of return for a liquidity pool in the specified period 									|
| yield_on_lp_fees 			| Return from fees in the specified period 		 														|
| price_change_ret 			| Return from the change in price of the underlying tokens in the specified period 						|
| misc_return               | Return from fees earned from flashloans and incentives                                                | 
| hodl_return 			    | Return if tokens were held (not staked in a liquidity pool) in the specified period 						                |
| fees_apy  			    | Return from fees in the specified period, annualized 						                            |
| total_apy 			    | Total rate of return for a liquidity pool in the specified period, annualized 						|
| token_0_fees_croi         | Cumulative return from fees earned in the form token 0 				    							|
| token_1_fees_croi         | Cumulative return from fees earned in the form token 1     											|
| misc_croi                 | Cumulative total return on investment for misc (see above) in base_currency          				    |
| total_croi				| Cumulative total return on investment in base_currency 												|
| fees_croi					| Cumulative return from fees in base_currency															|
| price_change_croi			| Cumulative return from the change in underlying tokens' values, this includes impermanent loss 		|
| hodl_token_0_croi 		| Cumulative total return for token 0's hodler                                                        |
| hodl_token_1_croi			| Cumulative total return for token 1's hodler                                                        |
| hodl_croi					| Cumulative total return for a hodler of both token 0 and token 1                                      |
| token_0_fees_return       | Return from fees in the specified period for token 0          										|
| token_1_fees_return       | Return from fees in the specified period for token 1          										|
| accumulated_token_0_fees  | Amount of token 0 earned from the liquidity pool 	    										        |
| accumulated_token_1_fees  | Amount of token 1 earned from the liquidity pool   											        |
| open_lp_token_price       | Open Liquidity Pool Open Price in the specified period                                                |          
| close_lp_token_price      | Close Liquidity Pool Open Price in the specified period                                               |
| impermanent_loss_level 	| The percentage difference in portfolio value between staking tokens in an AMM and holding tokens in a wallet. Fees are not taken into account in this calculation |
| impermanent_loss_impact 	| The percentage difference in ROI between staking tokens in an AMM and holding tokens in a wallet. Fees are not taken into account in this calculation |
| volume_0					| Number of token 0's traded																				|
| volume_1					| Number of token 1's traded																				|
| volume_0_base_curr		| Token 0's volume in base_currency (default is USD) in the specified time period													|
| volume_1_base_curr		| Token 1's volume in base_currency (default is USD) in the specified time period													|
| volume 		            | Volume in USD in the specified time period                                                            |
| transactions_period       | Number of transactions recorded during the time_period specified                                      |
| num_swaps 				| Number of swaps in the specified period 																|
| num_swaps_0 				| Number of swaps of token 0 in the specified period 													|
| num_swaps_1 				| Number of swaps of token 1 in the specified period 													|
| num_mints 				| Number of mint events in the specified period 														|
| num_burns 				| Number of burn events in the specified period 														|
| num_liquidity_events 		| Total number of liquidity events in the specified period for this platform							|
| open_reserve_0            | Reserves of token 0 at the first transaction in time_period specified                          		|
| open_reserve_1            | Reserves of token 1 at the first transaction in time_period specified                          		|
| close_reserve_0           | Reserves of token 0 at the last transaction in time_period specified                           		|
| close_reserve_1           | Reserves of token 1 at the last transaction in time_period specified                           		|
| open_reserve_0_base_curr 	| Reserves of token 0 in base_currency (default is USD) at the first transaction in time_period specified 							|
| open_reserve_1_base_curr 	| Reserves of token 1 in base_currency (default is USD) at the first transaction in time_period specified 							|
| close_reserve_0_base_curr | Reserves of token 0 in base_currency (default is USD) at the last transaction in time_period specified							|
| close_reserve_1_base_curr | Reserves of token 1 in base_currency (default is USD) at the last transaction in time_period specified							|
| open_poolsize 			| Pool size in USD at the first transaction in time_period specified                                    |
| close_poolsize 			| Pool size in USD at the last transaction in time_period specified										|
| poolsize 					| Same as close_poolsize; Kept for backwards compatibility	 									        |
| open_price_0              | Price of token 0 in USD at the beginning of the specified time period                 		        |
| open_price_1              | Price of token 1 in USD at the beginning of the specified time period 	   					        |
| high_price_0				| Highest price of token 0 in USD in the specified time period											|
| high_price_1				| Highest price of token 1 in USD in the specified time period											|
| low_price_0				| Lowest price of token 0 in USD in the specified time period											|
| low_price_1				| Lowest price of token 1 in USD in the specified time period 											|
| close_price_0             | Price of token 0 in USD at the end of the specified time period           			                |
| close_price_1             | Price of token 1 in USD at the end of the specified time period 			                            |
| last_processed            | Last Date/time UTC this liquidity pool was processed through FLUIDEFI's algorithms                    |
| token0_collateral         | Collateral of token 0 in liquidity pool                                                               |
| token1_collateral         | Collateral of token 1 in liquidity pool                                                               |
| token0_symbol             | Symbol of token 0 in liquidity pool                                                                   |
| token1_symbol             | Symbol of token 1 in liquidity pool                                                                   |
| token0_address            | Contract address of token 0 in liquidity pool                                                         |
| token1_address            | Contract address of token 1 in liquidity pool                                                         |
| id                        | FLUIDEFI unique ID number for liquidity pool. Required for other API calls such as Portfolio_update   |
| platform_id               | FLUIDEFI unique ID number for decentralized exchange									 	  	        |
| lp_name                   | Name of liquidity pool using token abbreviations (Note: ETH often listed as WETH or 'wrapped ETH')    |
| contract_address          | Contract Address of smart contract for liquidity pool                                                 |
| url                       | URL of liquity pool on platform                                                                       |

### APR vs. APY: What’s the Difference?
Both annual percentage yield (APY) and annual percentage rate (APR) refer to the annual return generated from an investment, but they do so in different ways.

APY takes into account the compounding effect, and reports the annual return using one piece of information: the annual return itself.
However, APR's calculation does not factor in compounding, and therefore reports the annual return using two pieces of information: the APR + the compounding frequency.

Here's an example of how both metrics are computed.
Assume that for the past month, the total return for an investment is 2%. We calculate APR and APY as follows: 
- APR = 2% * 12 = 24%
- APY = (1+2%)<sup>12</sup> -1 = 26.82%

In this case, APY > APR due to the compounding effect that is not taken into account by APR.

Also, note that these two statements are equivalent and both report how much return to expect in a year:
1. Annual return of this investment is 26.82%
2. This investment has an APR of 24%, compounded monthly

APY is the simpler way of reporting the same information. For this reason, <b>FLUIDEFI only provides APY figures</b>.

### SUPPORTED BASE CURRENCIES FOR CALCULATIONS
FLUIDEFI currently supports 12 fiat currencies, gold, silver, and 8,000+ cryptocurrencies. Examples: USD, WETH, GBP, CAD, CHF, JPY, AUD, NZD, HKD, EUR, NOK, SEK, SGD, CNY, KRW, XAU8, & XAG. If you need a fiat currency that is not listed here, contact support using the method below.

### PRECISION
FLUIDEFI supports a precision of 160, which is the size of sqrtX96 variable in many smart-contracts used vr DeFi platforms. The precision of a number is the total count of significant digits in the whole number, or, in other words, the number of digits to both sides of the decimal point. For example: the number 123.4567 has a precision of 7. It is not uncommon to have amounts displayed as 8 digits to the left of the decimal and 16 digits to the right.

### DateTime Format
FLUIDEFI supports ISO 8601 standard format date and datetimes. All datetimes are in UTC. The GET methods support YYYY-MM-DD. Example: "2021-06-01". POST methods support datetimes. Example: "2021-10-18T19:19:06.982417".

### Rate Limiting
Rate limits are based on your subscription level and vary between 5 and 60 calls per second.

### "Currently in Alpha" and "Currently in Beta"
From time to time, the FLUIDEFI documentation may indicate an API call or parameter is currently in Alpha or Beta. "Currently in Beta" functionality is available to FLUIDEFI customers with access to our staging environment. "Currently in Alpha" functionality is available upon request to FLUIDEFI customers with dedicated servers.

### STATUS CODES AND ERROR RESPONSES

All error responses have error code and a human-readable message. All error messages are in English.

200: Successful GET request

201-202: Successful PUT or POST request

204: Successful request, but the call did not generate any results to return.

400: Bad Request - Please check the parameters passed to the API call.

500-505: Server Error - Please try again later or contact FLUIDEFI Support.

See a [full list of HTTP Status Code definitions](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html).

### RESPONSE CODES FOR TRANSACTION ROUTES

The following is a list of response codes and messages that will be included in the response when an error is encountered in a request to execute a transaction or encode transaction data fields.

### General

1000: Desired network not found in available options

1100: Cannot connect to desired network

1200: No valid account credentials found

2000: Desired platform not found in available options

3000: Invalid address

3100: Not the address of a valid token

4000: Given deadline less than minimum

4050: Gas price too low

5000: Sender's balance is 0 for input asset

5050: Sender's balance is 0 for input asset. Warning: Input asset is WETH

5100: Sender has insufficient balance for input asset

5150: Sender has insufficient balance for input asset. Warning: Input asset is WETH

5200: EVM execution error (error message will be provided if available)

### Swaps

6000: Invalid swap mode. Valid options are exactinput or exactoutput

6100: Swap path too short. List must have a minimum of 2 assets

6200: Only one of input asset and output asset can be ETH - not both

6300: For exactinput swaps, amount_in is a required field

6400: For exactouput swaps, amount_out is a required field

6500: Invalid swap path: A pool does not exist for one or more pairs of sequential tokens in path

6550: Insufficient liquidity: One or more of the pairs in the swap path does not have enough liquidity for the swap amounts

6600: Warning: Input asset is WETH. This requires sender has WETH tokens. Use ETH as input asset for swapping from ether

6610: Warning: Output asset is WETH. This will deliver WETH tokens to the recipient. Use ETH as output asset for receiving ether

### Liquidity - General

7000: Token A and token B must not be the same asset

7100: A pair does not currently exist for the given assets

### Adding Liquidity

8000: Warning: Token A is WETH. This requires sender has WETH tokens. Use ETH as token A for adding liquidity from ether

8010: Warning: Token B is WETH. This requires sender has WETH tokens. Use ETH as token B for adding liquidity from ether

8020: Sender has insufficient balance of token A

8030: Sender has insufficient balance of token B

### Removing Liquidity

9000: Amount provided in liquidity field must be greater than 0

9100: Sender has insufficient balance of LP tokens for amount provided in liquidity field

9200: Warning: Token A is WETH. Recipient will receive WETH tokens. Use ETH as token A for removing liquidity to ether

9210: Warning: Token B is WETH. Recipient will receive WETH tokens. Use ETH as token B for removing liquidity to ether

-------
© 2021 FLUIDEFI® INC. All rights reserved. 
FLUIDEFI® is a Registered Trademark of FLUIDEFI INC.
