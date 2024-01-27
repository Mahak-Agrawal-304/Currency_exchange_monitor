# Currency Exchange Monitor

OVERVIEW

The currency_exchange_monitor.py script provides a user-friendly interface for the following functions:

Currency exchange between the base currency and foreign currency entered by the user.
Monitoring exchange rates for selected currencies using custom alert agents
Receiving alert notifications when the rates cross user-defined upper and lower thresholds.


PREREQUISITE:

To run the currency_exchange_monitor.py script, you need to have the following prerequisites installed:
1. Python 3.x
2. Tkinter library for GUI implementation (usually included with Python)
3. Requests library for accessing API
```
pip install requests
```
4. uAgents library for alert notifications
```
pip install uagents
```


HOW TO USE:

-Run the script currency_exchange_monitor.py using Python 3.x.
-The application's GUI will appear.
-Select the base currency and target currency from the dropdown menus.
-Enter upper and lower limits for monitoring exchange rate.
-Click the "OK" button to start monitoring exchange rates and to trigger alert agents.
-The application will display the exchange rate and conversion result in the GUI.
-Clear all button to reset the input fields.
-You will receive alert messages if the exchange rate crosses the specified upper or lower limits when you close the current tkinter window, powered by custom alert agents.


FEATURES:

1. Real-time exchange rate monitoring with user-defined upper and lower limits.
2. Alert messages for rate limit breaches, using custom alert agents.
3. Clear button to reset the input fields.


CODE STRUCTURE:

The script follows a modular structure, using functions for different tasks.
It utilizes threading to run currency conversion and rate monitoring concurrently.
The GUI is created using Tkinter widgets.
Exchange rate data is fetched from an external API using the Requests library.
Custom alert agents are integrated to provide notifications when rate limits are breached.


API KEY:

The script uses an API key to fetch exchange rate data from an external source. The API key used in this script may be subject to rate limits or restrictions. If you plan to use this script in a production environment, consider obtaining your API key from a reliable source and replacing the placeholder API key in the headers dictionary.


ALERT AGENTS:

Custom alert agents have been added to the script to provide rate monitoring and notifications using uAgents (Micro Agents). These agents continuously check the exchange rate between the selected currencies and trigger alerts when the rate crosses the user-defined upper or lower limit. The alerts are displayed as pop-up messages in the GUI.
