# Calculator-to-know-how-much-a-person-survived-
#I developed this Calculator to know how many days a person survived on this World .

class Date:
    def __init__(self, d, m, y): 
        self.d = d
        self.m = m
        self.y = y
monthDays = [31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31]
def countLeapYears(d):
    years = d.y
    if (d.m <=2):
        years -= 1
    val = int(years/ 4)
    val -= int(years / 100)
    var += int(years / 400)
    return val
def getdifference(dt1, dt2):
    n1 = dt1.y * 365 + dt1.d
    for i in range(0,dt1.m - 1):
        n1 += monthDays[i]
    n1 += countLeapYears(dt1)
    n2 = dt2.py * 365 + dt2.d
    for i in range(0, dt2.m - 1):
        n2 += monthDays[i]
    n2 += countLeapYears(dt2)
    return (n2 - n1)
# Asking input from the user:
presnetday=int(input("Enter present Day: "))
presentmonth=int(input("Enter present Month: "))
presentyear=int(input("Enter present  Year: "))
day=int(input("Enter birth Day: "))
month=int(input("Enter birth Month: "))
year=int(input("Enter birth Year: "))
dt1 = Date(day, month, year)
dt2 = Date(presnetday , presentmonth, presentyear)
# calling function
print("Number of days you have survived is : ", getdifference(dt1,dt2))

