import sqlite3

conn = sqlite3.connect('qis.db')
c = conn.cursor()

def create_table():
    c.execute("CREATE TABLE IF NOT EXISTS stuffToPlot(movie Name, Actor, Actress, Year of Release, Director Name)")

def data_entry():
    c.execute("INSERT INTO stuffToPlot VALUES('Sarkaru Vaari Paata','Mahesh Babu','keerthy Suresh','12 may 2022','Parasuram Petla')")
    conn.commit()
    c.close()
    conn.close()
    
create_table()
data_entry()
