# Weekday

from datetime import date
def get_weekday(n: str, birthday: str) -> date.weekday:
    WEEKDAY = {0:'LUNI', 1:'MARTI', 2:'MIERCURI', 3:'JOI', 4:'VINERI', 5:'SAMBATA', 
    6:'DUMINICA'}      
    Years = int(n) 
    An_curent = date.today().year
    birthday = f'{An_curent + Years}{birthday[birthday.find("-")::]}'
    return WEEKDAY[date.fromisoformat(birthday).weekday()] 
    

if __name__ == '__main__':
    birthday = input('zi de nastere: ' ) 
    n = input('număr de ani: ' ) 
    Day = get_weekday(n, birthday)
    print(Day)
