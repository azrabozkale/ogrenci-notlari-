# ogrenci-notlari-
# Öğrenci sözlüğü
notlar = {
    "Ahmet": {"Matematik": 80, "Fizik": 75, "Kimya": 90},
    "Ayşe": {"Matematik": 95, "Fizik": 85, "Kimya": 100},
    "Mehmet": {"Matematik": 60, "Fizik": 70, "Kimya": 65}
}

# Kullanıcıdan bilgi alma
isim = input("Öğrenci ismi giriniz: ")
ders = input("Ders ismi giriniz (Matematik/Fizik/Kimya): ")

if isim in notlar and ders in notlar[isim]:
    print("{} adlı öğrencinin {} notu: {}".format(isim, ders, notlar[isim][ders]))
else:
    print("Bilgiler bulunamadı.")

# -------------------------------
# Sözlük üzerinde değişiklikler
# -------------------------------

# 1. Mevcut öğrencinin notunu değiştirme
print("\nAhmet'in Matematik notunu 90 yapalım...")
notlar["Ahmet"]["Matematik"] = 90

# 2. Yeni öğrenci ekleme
print("Yeni öğrenci Zeynep'i ekleyelim...")
notlar["Zeynep"] = {"Matematik": 88, "Fizik": 92, "Kimya": 85}

# 3. Kullanıcıya istediği öğrencinin tüm bilgilerini gösterme
isim2 = input("\nBilgilerini görmek istediğiniz öğrenci ismini giriniz: ")
if isim2 in notlar:
    print("{} adlı öğrencinin notları: {}".format(isim2, notlar[isim2]))
else:
    print("Öğrenci bulunamadı.")

# Güncel sözlük ekrana yazdırma
print("\nGüncel Sözlük:", notlar)