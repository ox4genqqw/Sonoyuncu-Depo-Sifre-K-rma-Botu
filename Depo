import pyautogui
import time

coords = {
    "0": (958, 635),
    "1": (911, 503),
    "2": (956, 502),
    "3": (1000, 501),
    "4": (912, 545),
    "5": (958, 546),
    "6": (999, 544),
    "7": (912, 590),
    "8": (957, 590),
    "9": (999, 588),
    "onayla": (1000, 634),
    "olmadı": (890, 543)
}

def olmadı():
    time.sleep(0.15)
    pyautogui.moveTo(coords["olmadı"][0], coords["olmadı"][1], duration=0.2)
    time.sleep(0.15)
    pyautogui.click()
    time.sleep(0.15)

denenenler = []

# Başlamadan önce hazırlık süresi
time.sleep(3)

# 0000 - 0003 arasındaki şifreleri dener (0003 dahil)
for i in range(4):
    denenen_sayi = f"{i:04d}"
    denenenler.append(denenen_sayi)
    
    print(f"\nDenenen sayı: {denenen_sayi}")

    # Şifreyi gir
    for rakam in denenen_sayi:
        pyautogui.moveTo(coords[rakam][0], coords[rakam][1], duration=0.2)
        time.sleep(0.1)
        pyautogui.click()
        time.sleep(0.1)  # Tuşlar arası güvenli bekleme

    # Şifre yazımı bittikten sonra onayla butonuna geçmeden hafif es ver
    time.sleep(0.15)

    # Onayla butonuna git ve tıkla
    pyautogui.moveTo(coords["onayla"][0], coords["onayla"][1], duration=0.2)
    time.sleep(0.15)
    pyautogui.click()
    time.sleep(0.15)


    # Ekranın güncellenmesi ve kontrol için yeterli bekleme
    time.sleep(0.5)

    # kitap.png'yi ara
    kitap = pyautogui.locateOnScreen("kitap.png", confidence=0.70)

    if kitap:
        print("Başarı durumu: Başarısız (Yanlış şifre)")
        olmadı()
    else:
        print("Başarı durumu: Başarılı (Doğru Şifre Bulundu!)")
        break

print("\n--- İŞLEM TAMAMLANDI ---")
print(f"Denenen tüm sayılar: {denenenler}")
print(f"Son denenen (Doğru) sayı: {denenenler[-1]}")
