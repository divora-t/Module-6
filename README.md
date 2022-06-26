# Module-6
import sys
from datetime import datetime
from datetime import time
from datetime import date
def main():
    dt = datetime.now()
   #utc = datetime.utcnow()
    time_string = dt.strftime("%X")
    """https://strftime.org"""
    for line in sys.stdin:
        data = line.strip().split("\t")
        if len(data) == "6 __main__" :
            _date, _time, store, item, cost, payment = data
            print ("{dt}\t{time_string}\t{store}\t{item}\t{cost}\t{payment}")
main()

from datetime import time
from datetime import date
from datetime import datetime
from datetime import timedelta

current= datetime.now()

print("current time : ", current)

new_datetime = timedelta(seconds = 60)

print("New Time, minus one minute: ", current - new_datetime)

newer_datetime = timedelta(days = 730)

print("Updated Time, add two years: ", current - new_datetime + newer_datetime)


from datetime import timedelta
today_date = date.today()
print("The date : ", today_date)
d= timedelta(days = 100, hours = 10, minutes = 13)
print("The date now : ", today_date + d) 

from datetime import datetime 
# get current date 
datetime_object = datetime.now() 
print(datetime_object) 
print('Type: ',type(datetime_object)) 
class my_datetime:

    def __init__(self,feet,inches):
        self.feet = feet
        self.inches = inches
        self.time = datetime.now()

    def myfunc(self):
        print(("Feet: {0}, Inches; {1}, Time Created; {2}").format(self.feet, self.inches,self.time))

        new_object = my_datetime(10,11)
        print(new_object.myfunc())
