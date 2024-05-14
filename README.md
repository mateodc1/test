import yfinance as yf

# Crear objeto para Tesla
tesla = yf.Ticker("TSLA")

# Obtener datos históricos de acciones de Tesla
tesla_stock_data = tesla.history(period='max')

# explorar más los datos de las acciones de Tesla aquí
print(tesla_stock_data.head())
                               Open      High       Low     Close     Volume  \
Date                                                                           
2010-06-29 00:00:00-04:00  1.266667  1.666667  1.169333  1.592667  281494500   
2010-06-30 00:00:00-04:00  1.719333  2.028000  1.553333  1.588667  257806500   
2010-07-01 00:00:00-04:00  1.666667  1.728000  1.351333  1.464000  123282000   
2010-07-02 00:00:00-04:00  1.533333  1.540000  1.247333  1.280000   77097000   
2010-07-06 00:00:00-04:00  1.333333  1.333333  1.055333  1.074000  103003500   

                           Dividends  Stock Splits  
Date                                                
2010-06-29 00:00:00-04:00        0.0           0.0  
2010-06-30 00:00:00-04:00        0.0           0.0  
2010-07-01 00:00:00-04:00        0.0           0.0  
2010-07-02 00:00:00-04:00        0.0           0.0  
2010-07-06 00:00:00-04:00        0.0           0.0  

import requests
from bs4 import BeautifulSoup

# URL de donde extraeremos los datos de ingresos de Tesla
url = "https://www.macrotrends.net/stocks/charts/TSLA/tesla/revenue"

# Realizar la solicitud GET
response = requests.get(url)

# Analizar los datos HTML utilizando BeautifulSoup
soup = BeautifulSoup(response.text, 'html.parser')

# Encontrar la tabla que contiene los datos de ingresos
revenue_table = soup.find('table', class_='historical_data_table')

# Puedes explorar más cómo extraer los datos de la tabla aquí
print(revenue_table)
NONE

import yfinance as yf

# Crear objeto para GameStop
gamestop = yf.Ticker("GME")

# Obtener datos históricos de acciones de GameStop
gamestop_stock_data = gamestop.history(period='max')

# Puedes explorar más los datos de las acciones de GameStop aquí
print(gamestop_stock_data.head())
                               Open      High       Low     Close    Volume  \
Date                                                                          
2002-02-13 00:00:00-05:00  1.620128  1.693350  1.603296  1.691667  76216000   
2002-02-14 00:00:00-05:00  1.712707  1.716074  1.670626  1.683250  11021600   
2002-02-15 00:00:00-05:00  1.683250  1.687458  1.658001  1.674834   8389600   
2002-02-19 00:00:00-05:00  1.666418  1.666418  1.578047  1.607504   7410400   
2002-02-20 00:00:00-05:00  1.615921  1.662210  1.603296  1.662210   6892800   

                           Dividends  Stock Splits  
Date                                                
2002-02-13 00:00:00-05:00        0.0           0.0  
2002-02-14 00:00:00-05:00        0.0           0.0  
2002-02-15 00:00:00-05:00        0.0           0.0  
2002-02-19 00:00:00-05:00        0.0           0.0  
2002-02-20 00:00:00-05:00        0.0           0.0  


import requests
from bs4 import BeautifulSoup

# URL de donde extraeremos los datos de ingresos de GameStop
url = "https://www.macrotrends.net/stocks/charts/GME/gamestop/revenue"

# Realizar la solicitud GET
response = requests.get(url)

# Analizar los datos HTML utilizando BeautifulSoup
soup = BeautifulSoup(response.text, 'html.parser')

# Encontrar la tabla que contiene los datos de ingresos
revenue_table = soup.find('table', class_='historical_data_table')

# Puedes explorar más cómo extraer los datos de la tabla aquí
print(revenue_table)
NONE
