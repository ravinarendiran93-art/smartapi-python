

obj = SmartConnect(api_key="YOUR_API_KEY")
# generate session as above ...
ws = WebSocket(access_token, "wss://ws.smartapi.example")  # use URL from docs
def on_message(message):
    # parse tick and feed strategy
    print(message)

ws.on_message = on_message
ws.connect()
ws.subscribe(["NSE|TATA motors|EQ"])  # example symbol format depends on SmartAPI