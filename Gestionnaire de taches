#!/usr/bin/env python3
# coding:utf-8

class Taches:
    def __init__(self):
        # Liste des tâches
        self.taches = []
        # Statut des tâches
        self.termine = []  

    def ajouter(self, tache):
        # Ajoute la tâche
        self.taches.append(tache)
        # Marque la tâche comme en cours
        self.termine.append("En cours")  

    def idx_valide(self, idx):
        # Vérifie que l'indice est valide
        if 0 <= idx < len(self.termine):
            return True
        else:
            print("Erreur: Indice hors limites")
            return False

    def terminer(self, idx):
        # Marque la tâche comme terminée si l'indice est valide
        if self.idx_valide(idx):
            self.termine[idx] = "Fait"

    def supprimer(self, idx):
        # Supprime la tâche et son statut si l'indice est valide
        if self.idx_valide(idx):
            del self.taches[idx]
            del self.termine[idx]

    def afficher(self):
        # Affiche toutes les tâches avec leur statut
        print('------------------')
        for i, t in enumerate(self.taches):
            print(f"{i} : {t} - {self.termine[i]}")


taches = Taches()

while True:
    cmd = input("Entrez une commandes (+ Ajouter une Tâche, -: Terminer une Tâche, s: Supprimer une Tâche, a: Afficher les tâches, q: Quitter) ")

    if cmd == "+":
        tache = input("Entrez le nom: ")
        taches.ajouter(tache)
    elif cmd == "-":
        idx = int(input("Entrez l'id de la tâche: "))
        taches.terminer(idx)
    elif cmd == "s":
        idx = int(input("Entrez l'id de la tâche: "))
        taches.supprimer(idx)
    elif cmd == "a":
        taches.afficher()
    elif cmd == "q":
        break
    else:
        print("Commande invalide")
