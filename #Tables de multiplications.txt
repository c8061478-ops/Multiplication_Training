#Tables de multiplications
while True : 
    Title=(input("1 - Afficher une table de multiplication \n2 - Afficher toutes les tables de multiplications \n3 - Interroger sur une table de multiplication \n4 - Interroger sur plusieurs tables de multiplications \n5 - Interroger sur toutes les tables de multiplications \n6 - Quitter l'application \n------------------------------------------------- \nChoisissez un programme : "))
    if Title=='1':
        Choix=int(input("Quelle table de multiplication voulez-vous effectuer ?"))
        for i in range (1,11):
            Réponse=i*Choix
            print(i, 'X', Choix, '=', Réponse)
    if Title=='2':
        for i in range(1,11):
            print(49*"-")
            for h in range(1,11):
                Réponse=i*h
                print(i, 'X', h, '=', Réponse)
    if Title=='3':
        choix=int(input("Sur quelle table de multiplication voulez-vous être interroger ? "))
        choix2=int(input("Combien de questions voulez-vous avoir ? "))
        from random import randint
        bonne_reponse=0
        for i in range(1,choix2+1):
            nombre_aléatoire=randint(1,10)
            Réponse=int(input(f"Combien font {choix} X {nombre_aléatoire} ? "))
            if Réponse==choix*nombre_aléatoire:
                print("Vrai !")
                bonne_reponse=bonne_reponse+1
            else:
                print("Faux, la bonne réponse est", choix*nombre_aléatoire)
        print("Votre score est de", bonne_reponse, "sur", choix2, "ce qui équivaut a :", bonne_reponse/choix2*100, "%")
    if Title=='4':
        choix=int(input("Quelle est la première table de multiplication sur laquelle vous voulez être interroger ? "))
        choix3=int(input("Quelle est la dernière table de multiplication sur laquelle vous voulez être interroger ? "))
        choix2=int(input("Combien de questions voulez-vous avoir ? "))
        from random import randint
        bonne_reponse=0
        for i in range(1,choix2+1):
            nombre_aléatoire=randint(1,10)
            nombre_aléatoire2=randint(choix,choix3)
            Réponse=int(input(f"Combien font {nombre_aléatoire2} X {nombre_aléatoire} ? "))
            if Réponse==nombre_aléatoire2*nombre_aléatoire:
                print("Vrai !")
                bonne_reponse=bonne_reponse+1
            else:
                print("Faux, la bonne réponse est", nombre_aléatoire2*nombre_aléatoire)
        print("Votre score est de", bonne_reponse, "sur", choix2, "ce qui équivaut a :", bonne_reponse/choix2*100, "%")
    if Title=='5':
        choix2=int(input("Combien de questions voulez-vous avoir ? "))
        from random import randint
        bonne_reponse=0
        for i in range(1,choix2+1):
            nombre_aléatoire=randint(1,10)
            nombre_aléatoire2=randint(1,10)
            Réponse=int(input(f"Combien font {nombre_aléatoire2} X {nombre_aléatoire} ? "))
            if Réponse==nombre_aléatoire2*nombre_aléatoire:
                print("Vrai !")
                bonne_reponse=bonne_reponse+1
            else:
                print("Faux, la bonne réponse est", nombre_aléatoire2*nombre_aléatoire)
        print("Votre score est de", bonne_reponse, "sur", choix2, "ce qui équivaut a :", bonne_reponse/choix2*100, "%")
    if Title=='6':
        print("Fin du programme")
        break
    Fin=input("Voulez-vous continuez le programme (oui/non) ? ")
    if Fin!='oui':
        print("Fin du programme")
        break