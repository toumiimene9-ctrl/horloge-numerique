# horloge-numeriqueecho 
import time
import os
from datetime import datetime

def clear_console():
    os.system("cls" if os.name == "nt" else "clear")

try:
    while True:
        now = datetime.now()
        # format HH:MM:SS (24h)
        horloge = now.strftime("%H:%M:%S")
        date = now.strftime("%d/%m/%Y")
        clear_console()
        print("=== Horloge numérique ===")
        print()
        print(f"  Heure : {horloge}")
        print(f"  Date  : {date}")
        print()
        print("Appuie sur Ctrl+C pour quitter.")
        time.sleep(1)
except KeyboardInterrupt:
    print("\nHorloge arrêtée.")
