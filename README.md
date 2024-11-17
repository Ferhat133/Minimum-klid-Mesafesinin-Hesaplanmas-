# Minimum-klid-Mesafesinin-Hesaplanmas-
import math

# 2D uzayda iki nokta arasındaki Öklid mesafesini hesaplayan fonksiyon
def euclideanDistance(point1, point2):
    # Noktalar arasındaki farkların karesini alıp toplayarak mesafeyi hesapla
    distance = math.sqrt((point2[0] - point1[0])*2 + (point2[1] - point1[1])*2)
    return distance

# Noktalar listesi: her bir eleman bir tuple (x, y) şeklinde temsil edilecek
points = [(1, 2), (3, 4), (5, 6), (7, 8), (2, 1)]

# Mesafeleri saklayacak liste
distances = []

# Noktalar arasındaki mesafeleri hesapla
for i in range(len(points)):
    for j in range(i + 1, len(points)):  # Her çift nokta için mesafe hesapla
        distance = euclideanDistance(points[i], points[j])
        distances.append(distance)

# Hesaplanan mesafeler listesinin minimum değerini bulma
min_distance = min(distances)

# Sonuçları yazdırma
print(f"Mesafeler: {distances}")
print(f"Minimum mesafe: {min_distance}")
Mesafeler: [2.8284271247461903, 5.656854249492381, 7.810249675906654, 1.4142135623730951, 4.242640687119285, 2.8284271247461903]
Minimum mesafe: 1.4142135623730951
