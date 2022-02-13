
# Import module
import sqlite3

# Connecting to sqlite
conn = sqlite3.connect('MOVIES.db')

# Creating a cursor object using the cursor() method
cursor = conn.cursor()

# Creating table
table ="""CREATE TABLE MOVIES(MOVIENAME VARCHAR(255),
								LEADACTOR CHAR(255),
								ACTRESS int,
								YEAROFRELEASE int,
								DIRECTOR CHAR(255));"""
cursor.execute(table)
print('Table Created!')

# Queries to INSERT records.![Screenshot 2022-02-13 173314](https://user-images.githubusercontent.com/99593010/153752214-5c421e93-ac75-4126-aa0a-819af1b6115f.png)

cursor.execute('''INSERT INTO MOVIES(MOVIENAME,LEADACTOR,ACTRESS,YEAROFRELEASE,DIRECTOR)
					VALUES ('Pushpa','Alluarjun','Rashmika',2022,'Sukumar')''')
cursor.execute('''INSERT INTO MOVIES(MOVIENAME,LEADACTOR,ACTRESS,YEAROFRELEASE,DIRECTOR)
					VALUES ('Sarkaruvaripaata','Maheshbabu','Keerthisuresh',2022,'Parusuram')''')
cursor.execute('''INSERT INTO MOVIES(MOVIENAME,LEADACTOR,ACTRESS,YEAROFRELEASE,DIRECTOR)
					VALUES ('Radhesyam','Prabhas','Poojahedge',2022,'Radhakrishna')''')
cursor.execute('''INSERT INTO MOVIES(MOVIENAME,LEADACTOR,ACTRESS,YEAROFRELEASE,DIRECTOR)
					VALUES ('KGF2','Yash','Srinidhishetty',2022,'Prasanthneil')''')
print('Data inserted into the table')

# Commit your changes in the database	
conn.commit()
# Closing the connection
conn.close()

![Screenshot 2022-02-13 173343](https://user-images.githubusercontent.com/99593010/153752251-4bdc3891-9210-4678-b0e0-4c0f118dac48.png)
![Screenshot 2022-02-13 173314](https://user-images.githubusercontent.com/99593010/153752252-cfd19e58-f5f6-4b1a-a21c-8c29b001a9ac.png)
