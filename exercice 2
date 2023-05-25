'''
1. Combien de lames « entières » sont nécessaires pour le tablier en position fermée ?
    → (Longueur du tablier / largeur d'une lame) = (2.4 m / 0.036 m) ≈ 67 lames nécessaires

2. En déduire la longueur à enrouler.
    → (Nombre de lames * Largeur d'une lame étirée) = (67 * 40 m) = Longueur à enrouler de 2680 mm

3. Donner l’équation de la suite arithmétique du diamètre « dn » pour le tour « n ».
    → dn = Diamètre initial de l'axe + (2 * Épaisseur d'une lame * Nombre de tours)
    (Donné comme résultat de la fonction calcul_diametre)

4. En déduire la circonférence parcourue « cn » pour le tour « n ».
    → Pi * (Diamètre de l'axe au tour n - 1)
    (Donné comme valeur de la variable circonference_parcourue)

5. Calculer la longueur enroulée « Ln » au tour « n ».
    → Pi * (Diamètre de l'axe au tour n)

6. En réalité, afin que les attaches du tablier ne soient pas en extension ou tendues lorsqu’il est fermé, on considère que le tablier reste enroulé sur 2 tours.
    → ???
'''

import math   # Pour utiliser Pi dans nos calculs

epaisseur_lame = 9   # Épaisseur d'une lame, augmentée pour tenir compte de l'enroulement (7.5 mm + 1.5 mm)

# Récupération des entrées de l'utilisateur
diametre_axe_initial = int(input("Veuillez entrer le diamètre initial de l'axe en mm : "))
nombre_tours = int(input("Veuillez entrer le nombre de tours à effectuer : "))

longueur_enroulee = 0   # Initialisation du compteur de la longueur enroulée


def calcul_diametre(nombre_tours):   # Fonction de calcul du diamètre de l'axe pour chaque tour

    return diametre_axe_initial + (2 * epaisseur_lame * nombre_tours)


print()
for tour in range(1, nombre_tours + 1):   # Calcul et affichage du diamètre et de la longueur enroulée pour chaque tour

    longueur_enroulee += math.pi * calcul_diametre(tour)   # Calcul de la longueur enroulée à ce tour
    print(f"Tour : {tour}  -  Diamètre [mm] : {calcul_diametre(tour)}  -  Longueur enroulée [mm] : {round(longueur_enroulee)}")


circonference_initiale = math.pi * calcul_diametre(0)   # Circonférence de l'axe avant enroulement
circonference_parcourue = math.pi * calcul_diametre(nombre_tours - 1)   # Circonférence de l'axe au tour n

# Calcul de la longueur enroulée en utilisant la formule de la somme d'une progression arithmétique
longueur_par_formule = (nombre_tours / 2) * (circonference_initiale + circonference_parcourue)

'''
Formule utilisée: somme d'une progression arithmétique

S = (n/2) * (a1+an)

Avec:

n = nombre de termes dans la progression (ici le nombre de tours)
a1 = premier terme de la progression (ici la circonférence initiale de l'axe, avant le début de l'enroulement)
an = dernier terme de la progression (ici la circonférence finale de l'axe, une fois l'enroulement terminé)
'''

print("\nCalcul de la longueur L par formule :")
print(f"→ Longueur [mm] pour {nombre_tours} tours : {longueur_par_formule}")
