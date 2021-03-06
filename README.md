# Crypto Breakout Bot

## Install dependencies:
```
pip install numpy
pip install pandas
pip install python-telegram-bot
```

## File needed
Create a file named ```private.txt``` and put it in the same folder of main.py.
The content of the file must be:

```
<telegram_bot_token>
<chat_id>
```

## How the bot works
* The bot keeps cycling over all tokens listend on Binance against USDT.
* For every token, it checks if it is consolidating and if is pumping. The functions that define this behavior are defined in the file ```strategy.py```.
* If a token is found to be both consolidating and pumping, a message is sent to the chat_id.

## Other files
* analysis.py: to check quickly if a symbol between two dates satisfies the breakout criteria.
* test_breakouts.py: test a database of breakouts. The test data is in a csv file in the format: startDate, endDate, symbol. The test data should satisfy the breakout criteria.