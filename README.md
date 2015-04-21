# CurrencyFair
Java Engineer Test
Market Trade Processor
Author: Arsen Dernersissian
Contact: arsendm@gmail.com (+58) 412-3309249

---------------------------------------------

The approach for this test was:

- Build an app called "API" based on a RESTful API that manages requests and responses transmitting transactions to a PostgreSQL database where they are stored and accessed.

- Build an app called "MarketTradeViewer" based on Java Dynamic Web Project, which connects via servlets to the RESTful API to request information to feed the graphics. The graphics of this web project are automatically refreshed every 15 seconds via AJAX.

Development environment:
- Java(TM) SE Runtime Environment (build 1.7.0_67-b01)
- Tomcat v7.0 Server (v7.0.52)
- PostgreSQL 9.3

————— API app configuration ——————

1) Create a new PostgreSQL database (suggested name: “currency”)
   Restore it with backup located at:
   
   [your_path]/API/backup/currency_bk.backup
   
   suggested user: currency
   suggested pass: currency

2) Update information (database name, port, username and password)
   inside config.properties located at:

   [your_path]/API/src/main/java/config.properties
   
3) Ready to deploy!

Test App:
After deploying/running the app, now you can test the API
using all of the Java Applications (example clients) located at:

  [your_path]/API/src/main/java/com/currencyfair/client/

- AddMessageClient.java: Java Application used to test the add new Message functionality.
- GetAllMessagesClient.java: Java Application used to test the list all Messages functionality.
- GetAmountsSumByCurrency.java: Java Application used to test the list amounts sum by month functionality.
- GetCountriesSumByCurrency.java: Java Application used to test the list amounts sum by country functionality.
- GetRateAvgByCurrency.java: Java Application used to test the list average rates by month functionality.

—————— MarketTradeViewer Project ——————

ViewerServlet: Main Servlet, it loads the basic web to manage graphics

=========== Deploy Apps ========= 

After configuring the API you can deploy both applications using your app server and go to this URL:
http://localhost:8080/MarketTradeViewer/ViewerServlet
