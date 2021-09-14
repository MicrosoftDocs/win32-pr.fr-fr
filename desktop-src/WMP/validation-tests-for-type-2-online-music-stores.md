---
title: Tests de validation pour les magasins de type 2 en ligne intégrés
description: Cette rubrique décrit les tests que Microsoft effectuera pour valider votre magasin de type 2 en ligne. Microsoft vous demande d’exécuter ces tests avant de soumettre une version Release candidate. Votre magasin en ligne doit réussir à publier ces tests.
ms.assetid: 1da51772-9711-4913-b05d-830fabe49da2
keywords:
- Lecteur Windows Media Magasins en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beefd0945f9d1a9ae61e61f8be74beada1695baf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010839"
---
# <a name="validation-tests-for-on-boarding-type-2-online-stores"></a>Tests de validation pour les magasins de type 2 en ligne intégrés

Cette rubrique décrit les tests que Microsoft effectuera pour valider votre magasin de type 2 en ligne. Microsoft vous demande d’exécuter ces tests avant de soumettre une version Release candidate. Votre magasin en ligne doit réussir à publier ces tests.

> [!Note]  
> Si votre magasin est de type 1 au lieu de type 2, vous pouvez utiliser cette rubrique comme indication pour comprendre l’étendue des tests de certification couverts pour les magasins de type 1. Pour l’ensemble complet des tests pour les magasins de type 1, contactez [support Microsoft](https://support.microsoft.com/ph/7763#tab0).

 

Cette rubrique contient les sections suivantes.

-   [Liste de vérification des tests](#test-checklist)
    -   [Préparation de la passe de test](#test-pass-preparation)
-   [Environnement de test](#test-environment)
-   [Configuration et installation](#configuration-and-setup)
    -   [Configuration d’un ordinateur de test](#setting-up-a-test-machine)
    -   [Configuration d’un magasin](#setting-up-a-store)
    -   [Création d’un compte](#creating-an-account)
    -   [Configuration de la mise en cache des informations d’identification](#setting-up-credential-caching)
-   [Acquisition de contenu](#content-acquisition)
    -   [Contenu de diffusion en continu](#streaming-content)
    -   [Obtention de contenu](#obtaining-content)
    -   [Gravage de contenu](#burning-content)
    -   [Transfert de contenu](#transferring-content)
-   [Fonctionnalités du Store](#store-features)
    -   [Gestion d’un compte](#managing-an-account)
    -   [Gestion d’info Center](#managing-the-info-center)
-   [Interaction du Store](#store-interaction)
    -   [Donner au magasin actif](#yielding-to-the-active-store)
    -   [Empêcher le magasin testé de prendre le contrôle du magasin actif](#preventing-the-tested-store-from-taking-over-the-active-store)
    -   [Accès à un magasin en mode High-Contrast](#accessing-a-store-in-high-contrast-mode)
    -   [Sécurisation d’un magasin](#securing-a-store)

## <a name="test-checklist"></a>Liste de vérification des tests

Utilisez la liste de contrôle figurant dans le tableau suivant pour valider votre boutique en ligne de type 2 que vous souhaitez mettre à l’esprit.



Test

Windows XP

Windows Vista

Windows 7

Résultat (réussite/échec/non applicable)

32

64

32

64

32

64

1. Vérifiez que le logiciel est installé.

2. Vérifiez que le logiciel est désinstallé.

3. Vérifiez que le logiciel ne s’exécute pas dans la barre d’État.

4. Vérifiez que l’onglet Store fonctionne.

5. Vérifiez que le magasin dispose d’une option pour créer un nouveau compte.

6. Vérifiez que le compte créé peut se connecter.

7. Vérifiez que le magasin a une option permettant d’enregistrer les informations utilisateur.

8. Vérifiez que la mise en cache des informations d’identification est présente et opérationnelle.

9. Vérifiez que l’utilisateur est invité à fournir les informations d’identification si elles ne sont pas mises en cache.

10. Vérifiez que tous les types de flux de contenu disponibles.

11. vérifiez que le contenu est lu dans Microsoft Lecteur Windows Media.

12. Vérifiez que le prix calculé est correct.

13. Vérifiez que le contenu acheté est téléchargé dans la bibliothèque.

14. Vérifiez que les métadonnées sont téléchargées pour l’achat.

15. Vérifiez que les droits d’utilisation du média sont corrects pour l’achat.

16. Vérifiez que le contenu acheté peut être lu.

17. Vérifiez que cliquer sur le bouton **acheter** **ou acheter bascule** sur le Store.

18. Vérifiez que le contenu acheté a été téléchargé.

19. Vérifiez que le contenu acheté peut être gravé.

20. Vérifiez que le nombre de brûlures est décrémenté.

21. Vérifiez que le contenu peut être transféré vers un autre ordinateur.

22. Vérifiez que le contenu est transféré vers un appareil.

23. Vérifiez que le nombre de synchronisations est décrémenté.

24. Vérifiez que l’historique des achats effectue le suivi des achats précédents.

25. Vérifiez qu’un achat précédent peut être restauré.

26. Vérifier la fonctionnalité d’un magasin pour gérer plusieurs ordinateurs.

27. Vérifiez que le centre d’informations est désactivé par défaut.

28. Vérifiez que le centre d’informations contient des informations sur le média dans la zone de diffusion en cours.

29. Vérifiez que les liens naviguent vers le magasin.

30. Vérifiez que le magasin testé produit le magasin actif.

31. Vérifiez que le magasin testé ne prend pas en charge le magasin actuel.

32. Vérifiez que le magasin est accessible en mode de contraste élevé.

33. Vérifiez que le magasin est sécurisé.



 

### <a name="test-pass-preparation"></a>Préparation de la passe de test

Avant d’exécuter un test, vous devez vous assurer que le magasin et les comptes de test sont prêts pour le test. Vous devez déterminer les informations suivantes avant le démarrage de la passe. Si vous pouvez déterminer les informations quelques jours avant la réussite du test, la réussite s’exécutera plus efficacement.

-   Déterminez les informations suivantes sur les comptes de test qui sont fournis par le magasin :
    -   Les comptes et les mots de passe fonctionnent pour permettre à un utilisateur de se connecter
    -   Les comptes sont financés correctement et de manière adéquate pour chaque type de mode d’entreprise proposé par le magasin
    -   Les comptes sont valides pour tous les paramètres régionaux à tester, ou des comptes existent pour chaque paramètre régional si les comptes ne peuvent pas traverser les paramètres régionaux
-   Déterminez les paramètres régionaux à tester.
-   Déterminez les langues à tester.
-   Déterminez les informations suivantes sur l’environnement de test :

    -   magasins en direct qui fonctionnent avec Windows XP, Windows Vista et Windows 7
    -   Magasin non-Live à tester
    -   vérifiez que la banque non active à tester est visible dans toutes les versions du système d’exploitation et toutes les versions de la plateforme Lecteur Windows Media.

-   Déterminez les informations suivantes sur le magasin à tester :

    -   Nom de la banque
    -   Graphiques et étiquette du logo onglet de la boutique ATTENDU
    -   Le magasin est-il actif pour toutes les versions de système d’exploitation ?
    -   S’agit-il d’une nouvelle version du magasin testé ?
    -   Le magasin teste-t-il un magasin de type 1 ou de type 2 ?
    -   Le type de magasin a-t-il changé ?

-   Déterminez les versions et les plateformes de système d’exploitation pour lesquelles vous envisagez de tester le magasin.
-   Déterminez que le programme d’installation et le plug-in fonctionnent sur toutes les versions et plateformes du système d’exploitation à tester.
-   Déterminez si un document de navigation est requis.
-   Déterminez les informations suivantes sur le support offert par le magasin :

    -   Formats
    -   Tout logiciel propriétaire est-il requis ?
    -   Devez-vous tester tous les types de média, ou seulement un sous-ensemble de types de média ?

-   Déterminez les informations suivantes sur les droits d’utilisation de média :

    -   Le support de stockage dispose-t-il d’une protection de contenu ?
    -   Si c’est le cas, déterminez le type de protection de contenu que le média a.
    -   Si c’est le cas, déterminez le comportement protégé attendu.
    -   Les droits d’utilisation des médias incluent-ils le partage d’ordinateur à ordinateur ?
    -   Droits de synchronisation
    -   Les droits de gravure
    -   Droits de lecture
    -   Dates d’expiration, le cas échéant

-   Déterminez si vous disposez de suffisamment de supports (un grand catalogue) pour fournir un exemple significatif.
-   Déterminez ce que l’étape passe : RC 0, conformité, etc.
-   Déterminez si la réussite du test est un type particulier : régression, fumée, et ainsi de suite.

## <a name="test-environment"></a>Environnement de test

Vous devez procéder à des tests sur les configurations suivantes :

-   systèmes d’exploitation Microsoft Lecteur Windows Media 11 sur Windows XP avec Service Pack 3 (SP3) 32 bits et 64 bits
-   Lecteur Windows Media 11 sur les systèmes d’exploitation Windows Vista 32 bits et 64 bits (32 bits Lecteur Windows Media)
-   systèmes d’exploitation Microsoft Lecteur Windows Media 12 sur Windows 7 32 bits et 64 bits (32 bits Lecteur Windows Media)

même si vous devez effectuer des tests sur toutes les versions et plateformes du système d’exploitation répertoriées, les versions 32 bits de Windows Vista et Windows 7 sont les versions de système d’exploitation ciblées en priorité. Vous devez tester l’installation de tous les logiciels sur toutes les plateformes.

Les captures d’écran de cette rubrique utilisent un magasin fictif, Proseware, pour illustrer l’utilisation de l’interface utilisateur.

## <a name="configuration-and-setup"></a>Configuration et installation

Les sections suivantes décrivent comment configurer et configurer un test de validation sur un magasin de type 2 en ligne.

### <a name="setting-up-a-test-machine"></a>Configuration d’un ordinateur de test

Procédez comme suit pour configurer un ordinateur de test :

1.  Pointez l’ordinateur de test vers les serveurs de test de contenu en ajoutant une clé de Registre spécifique au magasin.
2.  Définissez les valeurs de la langue et des paramètres régionaux appropriés dans la boîte de dialogue **Options régionales et linguistiques** . Pour définir la langue, sélectionnez l’onglet **formats** , puis sélectionnez la langue à partir de la zone de liste déroulante **format actuel** . Pour définir la région, sélectionnez l’onglet **emplacement** , puis sélectionnez la région dans la zone de liste déroulante **emplacement actuel** . En outre, pour les magasins qui nécessitent l’installation d’un plug-in ou d’un logiciel personnalisé spécifique au magasin, vous devrez peut-être modifier les paramètres régionaux système en fonction de la langue des paramètres régionaux du magasin pour faciliter l’installation. Le programme d’installation du logiciel doit prendre en charge les caractères de type simple et double octet et doit s’exécuter sur n’importe quel paramètre régional. Vous devez tester les paramètres régionaux natifs. Pour définir les paramètres régionaux natifs, ouvrez la boîte de dialogue **région et langue** , sélectionnez l’onglet **administration** , puis cliquez sur le bouton **modifier les paramètres régionaux du système** , comme indiqué dans la capture d’écran suivante. cliquez sur ce bouton pour afficher la boîte **de dialogue Paramètres de la région et de la langue** . La zone de liste déroulante **paramètres régionaux actuels** dans cette boîte de dialogue modifie les paramètres régionaux système.

    Les captures d’écran suivantes montrent les onglets sur lesquels vous pouvez définir la région et la langue :

    ![capture d’écran de la boîte de dialogue Options régionales et linguistiques](images/reg-lang-opt.png)

    ![capture d’écran montrant comment modifier les paramètres régionaux du système actuel](images/reg-lang-settings.png)

3.  désactivez l’affichage du centre d’informations d’un magasin en définissant Lecteur Windows Media pour lire une visualisation. la principale différence entre les plateformes est que, dans Lecteur Windows Media 11, vous commencez par cliquer sur **playing**, tandis que dans Lecteur Windows Media 12, vous commencez par cliquer avec le bouton droit sur la fenêtre principale.

    la capture d’écran suivante montre la séquence d’options de menu qui joue une visualisation dans Lecteur Windows Media 11 :

    ![capture d’écran montrant comment lire une visualisation dans le lecteur Windows Media 11](images/wmp11-visual.png)

    la capture d’écran suivante montre la séquence d’options de menu qui joue une visualisation dans Lecteur Windows Media 12 :

    ![capture d’écran montrant comment lire une visualisation dans le lecteur Windows Media 12](images/wmp12-visual.png)

### <a name="setting-up-a-store"></a>Configuration d’un magasin

Tout d’abord, effectuez les étapes suivantes pour configurer un magasin, puis effectuez les étapes qui suivent les étapes initiales pour vérifier la configuration du magasin :

1.  lancez Lecteur Windows Media et patientez quelques secondes pour obtenir le dernier fichier de AllServices.xml.
2.  pour les Windows XP et Windows Vista, pour sélectionner un magasin en ligne, cliquez d’abord sur l’onglet qui se divise entre la vue du Guide multimédia et la vue magasins en ligne. Ensuite, dans le menu, cliquez sur **parcourir tous les magasins en ligne**, puis sélectionnez le magasin en cliquant sur son icône dans la liste des magasins. pour Windows 7, cliquez sur le bouton dans le volet de navigation de la bibliothèque qui fractionne entre le bouton du **Guide multimédia** et le bouton **magasins en ligne** . Ensuite, dans le menu, cliquez sur **parcourir tous les magasins en ligne**, puis sélectionnez le magasin en cliquant sur son icône dans la liste des magasins.

    la capture d’écran suivante montre comment sélectionner un magasin en ligne dans Lecteur Windows Media 11 :

    ![capture d’écran montrant comment sélectionner un magasin en ligne dans le lecteur Windows Media 11](images/wmp11-set-store.png)

    la capture d’écran suivante montre comment sélectionner un magasin en ligne dans Lecteur Windows Media 12 :

    ![capture d’écran montrant comment sélectionner un magasin en ligne dans le lecteur Windows Media 12](images/wmp12-set-store.png)

3.  Suivez les instructions de la boutique pour installer les logiciels supplémentaires nécessaires à l’utilisation du Windows Store.

**Pour vérifier la configuration du magasin**

1.  Vérifiez que le logiciel est installé.

    Vérifiez que le plug-in OCX ou tout autre logiciel du Store est téléchargé et installé sans erreur.

2.  Vérifiez que le logiciel est désinstallé.

    Vérifiez que, dans le panneau de configuration, dans l’élément **programmes et fonctionnalités** , le logiciel que le Store installe apparaît dans la liste **désinstaller ou modifier un programme** , puis vérifiez que vous pouvez le désinstaller de cette liste sans erreur.

3.  Vérifiez que le logiciel ne s’exécute pas dans la barre d’état système.

    Vérifiez qu’aucun des logiciels du Store n’ajoute d’icônes à la zone de notification du programme (dans la barre des tâches à gauche de l’horloge) avant d’avoir donné son consentement au client pour télécharger le logiciel du magasin.

    L’expérience de base du magasin ne doit pas nécessiter l’installation de logiciels supplémentaires. Une expérience de base de média, telle que la diffusion de contenu multimédia, doit être disponible. Certains magasins installent des logiciels supplémentaires, tels que les gestionnaires de téléchargement pour une expérience de média premier. ces magasins peuvent avoir des icônes dans la barre d’état système si les icônes représentent des applications distinctes de Lecteur Windows Media.

4.  Vérifiez que l’onglet Store fonctionne.

    Vérifiez que l’onglet Store change pour indiquer le magasin sélectionné.

    pour Windows XP et Windows Vista avec Lecteur Windows Media 11, vérifiez que le nom et l’icône du magasin sont visibles sur l’arrière-plan de l’Lecteur Windows Media 11 foncé.

    pour Windows 7 avec Lecteur Windows Media 12, vérifiez que le nom et l’icône du magasin sont visibles dans le volet de navigation de la bibliothèque, dans le menu contextuel du sélecteur de service.

    Vérifiez que le magasin figure en haut de la liste de sélecteurs de magasin dans le menu.

    > [!Note]  
    > Il n’y aura pas **d’option de menu Ajouter le service actuel à** si le magasin de type 2 est le magasin proposé (par défaut) pour la région.

     

    la capture d’écran suivante montre le menu qui s’affiche lorsque vous cliquez sur l’onglet situé dans le coin supérieur droit de Lecteur Windows Media 11 :

    ![capture d’écran montrant l’onglet Store dans le lecteur Windows Media 11](images/wmp11-verify-store.png)

    la capture d’écran suivante montre le menu qui s’affiche lorsque vous cliquez sur le bouton partagé dans le coin inférieur gauche de Lecteur Windows Media 12 :

    ![capture d’écran montrant l’onglet Store dans le lecteur Windows Media 12](images/wmp12-verify-store.png)

### <a name="creating-an-account"></a>Création d’un compte

**Pour vérifier la configuration du compte**

1.  Vérifiez que le magasin dispose d’une option pour créer un nouveau compte, puis suivez les instructions du magasin pour créer un nouveau compte.

    la capture d’écran suivante met en surbrillance un bouton **créer un nouveau compte** tel qu’il peut apparaître dans Lecteur Windows Media 11 :

    ![capture d’écran montrant comment vérifier la configuration de compte pour le lecteur Windows Media 11](images/wmp11-verify-account.png)

    la capture d’écran suivante met en surbrillance un bouton **créer un nouveau compte** tel qu’il peut apparaître dans Lecteur Windows Media 12 :

    ![capture d’écran montrant comment vérifier la configuration de compte pour le lecteur Windows Media 12](images/wmp12-verify-account.png)

2.  Vérifiez que vous pouvez vous connecter au compte que vous avez créé.

### <a name="setting-up-credential-caching"></a>Configuration de la mise en cache des informations d’identification

Tout d’abord, procédez comme suit pour configurer la mise en cache des informations d’identification, puis effectuez les étapes qui suivent les étapes initiales pour vérifier la configuration de la mise en cache des informations d’identification :

1.  Sur la page de connexion, entrez les informations d’identification et sélectionnez l’option permettant d’enregistrer les informations utilisateur.
2.  Vérifiez que la page de connexion a une case à cocher qui permet à l’utilisateur de mettre en cache les informations d’identification.
3.  La mise en cache facultative des informations d’identification est un point de sécurité important. La mise en cache automatique des informations d’identification peut exposer des informations d’identification personnelle des utilisateurs qui se connectent à un ordinateur public ou partagé. Vous devez protéger les informations client en proposant une case à cocher qui rend la mise en cache facultative.

**Pour vérifier la mise en cache des informations d’identification**

1.  Vérifiez que le magasin possède une case à cocher pour une option **enregistrer mes informations utilisateur** .

    1.  fermez Lecteur Windows Media.
    2.  rouvrez Lecteur Windows Media et tentez de télécharger du contenu.

2.  Vérifiez que la mise en cache des informations d’identification est présente et opérationnelle.

    1.  Déconnectez-vous du Store.
    2.  fermez Lecteur Windows Media.
    3.  rouvrez Lecteur Windows Media et tentez de télécharger du contenu.

3.  Vérifiez que l’utilisateur est invité à fournir les informations d’identification si elles ne sont pas mises en cache.

    Après la déconnexion, puis la tentative d’utilisation du magasin, le client doit être invité à fournir des informations d’identification.

## <a name="content-acquisition"></a>Acquisition de contenu

Cette section décrit les différentes façons d’acquérir du contenu et comment vérifier que le contenu a été acquis.

### <a name="streaming-content"></a>Contenu de diffusion en continu

Diffuse tous les types de contenu disponibles à partir du magasin. Par exemple, diffuser en continu le contenu radio, vidéo, audio et aperçu.

**Pour vérifier le contenu de diffusion en continu**

1.  Vérifiez que tous les types de flux de contenu disponibles.

2.  vérifiez que le contenu est lu dans Lecteur Windows Media et pas dans un autre lecteur ou contrôle.

### <a name="obtaining-content"></a>Obtention de contenu

Tout d’abord, effectuez les étapes suivantes pour acheter du contenu, puis effectuez les étapes qui suivent les étapes initiales pour vérifier l’achat et vérifier que le contenu a été téléchargé :

1.  lancez Lecteur Windows Media.
2.  Connectez-vous au compte de test.
3.  Accédez au contenu à acheter.
4.  Suivez la procédure spécifique au magasin pour acheter du contenu.

**Pour vérifier le contenu acheté et téléchargé**

1.  Vérifiez que le prix calculé est correct.

    Vérifiez que le prix est correct, en particulier lors de l’achat de plusieurs éléments de contenu à la fois, et vérifiez que les informations de solde du compte sont mises à jour correctement après l’achat. Certains contenus peuvent être achetés en tant que pistes uniques et en tant qu’albums uniquement. Vérifiez que le prix de l’album n’est pas supérieur à la somme des pistes individuelles.

2.  Vérifiez que le contenu acheté est téléchargé dans la bibliothèque.

    une fois le téléchargement terminé, accédez au contenu téléchargé dans la bibliothèque de Lecteur Windows Media. Le contenu téléchargé se trouve dans la bibliothèque de l’utilisateur actuel.

    -   pour Windows XP et Windows Vista avec Lecteur Windows Media 11, le contenu téléchargé s’affiche dans le volet de navigation de la bibliothèque, sous **bibliothèque** pivot, puis sous **chansons**.
    -   pour Windows 7 avec Lecteur Windows Media 12, le contenu téléchargé dans la bibliothèque de Lecteur Windows Media s’affiche dans le volet de navigation Lecteur Windows Media sous **Musique**.

3.  Vérifiez que les métadonnées sont téléchargées pour l’achat.

    vérifiez que les colonnes suivantes s’affichent dans la bibliothèque de Lecteur Windows Media (ajoutez-les si ce n’est pas le cas) :

    -   Artiste de l’album
    -   Intitulé
    -   Titre de l’album
    -   Fournisseur de contenu
    -   Genre

    Les colonnes précédentes doivent être remplies. Le contenu doit avoir une pochette d’album. Toutefois, une pochette d’album n’est pas nécessaire pour réussir le test de validation.

4.  Vérifiez que les droits d’utilisation du média sont corrects pour l’achat.

    Pour chaque piste téléchargée, cliquez avec le bouton droit sur la piste et sélectionnez **Propriétés**, puis sélectionnez l’onglet **droits d’utilisation du média** .

    Le magasin peut choisir de protéger son contenu avec des droits d’utilisation de média, ou choisir de ne pas protéger le contenu. L’onglet **droits d’utilisation du média** reflète cet État en répertoriant les restrictions ou en indiquant que le contenu n’est pas protégé. Le magasin doit communiquer son plan le plus récent pour les droits d’utilisation du support. Vous devez vérifier les résultats réels par rapport à ce comportement attendu.

    Les licences de droits de support doivent être pré-remises. Le client ne doit pas être obligé de lire le contenu ou de passer par un autre processus pour bénéficier de la licence. Vous devez comparer les droits d’utilisation de médias spécifiques à ce que le magasin a communiqué au client, le cas échéant. Les droits doivent pouvoir être transférés sur au moins deux autres ordinateurs. Les clients doivent être en mesure de graver et de synchroniser leurs médias.

    La capture d’écran suivante montre les droits d’utilisation du média d’un fichier protégé :

    ![capture d’écran montrant les droits d’utilisation de média pour un fichier protégé](images/media-rights-protected.png)

    Si le contenu n’est pas protégé, l’onglet **droits d’utilisation du média** indique ce fait.

    La capture d’écran suivante montre les droits d’utilisation du média d’un fichier non protégé :

    ![capture d’écran montrant les droits d’utilisation de média pour un fichier non protégé](images/media-rights-not-protected.png)

5.  Vérifiez que le contenu acheté est lu.

    vérifiez que le contenu téléchargé est lu dans Lecteur Windows Media.

    Lire tout contenu acheté dans le magasin et qui réside dans la bibliothèque locale, ou diffuser un aperçu.

    pour acheter du contenu dans Windows XP et Windows Vista avec Lecteur Windows Media 11, procédez comme suit :

    1.  Cliquez sur l’onglet en **cours de diffusion** .
    2.  Dans le volet liste, positionnez le pointeur de la souris pour pointer sur une pochette d’album afin d’afficher le lien d' **achat** .
    3.  Cliquez sur **acheter**.

    la capture d’écran suivante montre l’emplacement du lien d' **achat** dans Lecteur Windows Media 11 :

    ![capture d’écran montrant comment acheter du contenu dans le lecteur Windows Media 11](images/wmp11-verify-buy-play.png)

    pour acheter du contenu dans Windows 7 avec Lecteur Windows Media 12, procédez comme suit :

    1.  En mode bibliothèque, cliquez sur l’onglet **lecture** .
    2.  Dans la sélection, sous la pochette de l’album, cliquez sur **acheter**

    la capture d’écran suivante montre comment acheter du contenu dans Lecteur Windows Media 12 :

    ![capture d’écran montrant comment acheter du contenu dans le lecteur Windows Media 12](images/wmp12-verify-buy-play.png)

6.  Vérifiez que le fait de cliquer sur **acheter** **ou acheter** bascule dans le Store.

    le Lecteur Windows Media doit basculer vers le magasin dans la vue bibliothèque et charger l’expérience d’achat du magasin.

    Vous devez ensuite continuer à acheter le suivi.

7.  Après avoir cliqué sur **acheter** ou **acheter**, vérifiez que le contenu est téléchargé.

    Vérifiez que les droits d’utilisation du média sont appropriés pour le contenu acheté et ses métadonnées, et vérifiez que la piste est lue. En général, cette méthode d’achat doit avoir les mêmes résultats que les autres méthodes.

### <a name="burning-content"></a>Gravage de contenu

Tout d’abord, effectuez les étapes suivantes pour graver du contenu acheté (copier le contenu acheté sur un CD ou DVD inscriptible), puis effectuez les étapes qui suivent les étapes initiales pour vérifier que le contenu est en cours de gravure :

> [!Note]  
> Avant de graver une piste achetée, notez son nombre de brûlures afin de pouvoir vérifier ultérieurement si le nombre est décrémenté après avoir gravé la piste.

 

1.  Cliquez sur l’onglet **graver**
2.  Faites glisser les pistes achetées vers la **liste de gravure**.
3.  Cliquez sur le bouton **Démarrer la gravure** .

la capture d’écran suivante montre la **liste de brûlures** sur le côté droit de l’écran et le bouton **démarrer la gravure** sous la liste de **gravure** dans Lecteur Windows Media 11 :

![capture d’écran montrant comment graver du contenu dans le lecteur Windows Media 11](images/wmp11-verify-burn.png)

la capture d’écran suivante montre comment la liste de gravure s’affiche dans Lecteur Windows Media 12 après avoir fait glisser une piste vers la liste de gravure et affiche le bouton **démarrer la gravure** en haut de l’onglet **graver** :

![capture d’écran montrant comment graver du contenu dans le lecteur Windows Media 12](images/wmp12-verify-burn.png)

**Pour vérifier que le contenu acheté peut être gravé**

1.  Vérifiez que le contenu acheté émet des brûlures en lisant le CD ou le DVD une fois la gravure terminée.

2.  Vérifiez que le nombre de brûlures est décrémenté.

    Accédez à la bibliothèque et ouvrez les droits d’utilisation de support pour une piste achetée qui a été gravée.

    Si le nombre de fois qu’une piste peut être gravée est limité, vérifiez que ce nombre diminue après la gravure de la piste.

### <a name="transferring-content"></a>Transfert de contenu

Transférer du contenu vers un autre ordinateur.

**Pour vérifier que le contenu acheté peut être transféré vers un autre ordinateur**

-   Si le magasin autorise le transfert de contenu vers un autre ordinateur, transférez le contenu sur au moins deux ordinateurs.

Tout d’abord, effectuez les étapes suivantes pour synchroniser sur un appareil et transférer le contenu acheté sur cet appareil, puis effectuez les étapes qui suivent les étapes initiales pour vérifier que le contenu est transféré :

> [!Note]  
> Avant de transférer une piste achetée, notez son nombre de synchronisation afin de pouvoir vérifier ultérieurement si le nombre est décrémenté après le transfert de la piste.

 

1.  Connecter un appareil avec une horloge sécurisée. les exemples incluent des appareils qui utilisent Windows DRM pour les appareils mobiles, tels qu’un media Center portable comme iRiver H10, Creative Zen, etc.
2.  dans Lecteur Windows Media, cliquez sur l’onglet **synchronisation** .
3.  Faites glisser le contenu de la bibliothèque vers la zone de **liste synchronisation** sous l’onglet **synchronisation** .
4.  Cliquez sur le bouton **Démarrer la synchronisation** .

la capture d’écran suivante montre le suivi 1 dans la zone de **liste synchronisation** et affiche le bouton **démarrer la synchronisation** dans Lecteur Windows Media 11 :

![capture d’écran montrant comment transférer du contenu dans le lecteur Windows Media 11](images/wmp11-verify-transfer.png)

la capture d’écran suivante montre le suivi 1 dans la zone de **liste synchronisation** et affiche le bouton **démarrer la synchronisation** dans Lecteur Windows Media 12 :

![capture d’écran montrant comment transférer du contenu dans le lecteur Windows Media 12](images/wmp12-verify-transfer.png)

**Pour vérifier que le contenu acheté peut être transféré vers un autre appareil**

1.  Vérifiez que le contenu acheté est transféré vers l’appareil en lisant le contenu sur l’appareil. Le contenu transféré doit également avoir les métadonnées appropriées.

2.  Vérifiez que le nombre de synchronisations est décrémenté.

    Accédez à la bibliothèque et ouvrez les droits d’utilisation du média pour une piste transférée.

    Si le nombre de fois qu’une piste peut être synchronisée est limité, vérifiez que ce nombre diminue lorsque la piste est transférée.

## <a name="store-features"></a>Fonctionnalités du Store

Les sections suivantes décrivent comment tester diverses fonctionnalités d’un magasin en ligne intégré.

### <a name="managing-an-account"></a>Gestion d’un compte

Connectez-vous avec un compte qui a effectué des achats et ouvrez l’historique des achats.

**Pour vérifier l’historique des achats**

-   Vérifiez que l’historique des achats effectue le suivi des achats précédents.

Si le magasin ou le type de compte prend en charge cette fonctionnalité, tente de restaurer un achat supprimé.

**Pour vérifier que les achats précédents peuvent être réacquiss**

-   Vérifiez qu’un achat précédent peut être restauré.

Si le magasin prend en charge l’utilisation de plusieurs ordinateurs avec le compte, vérifiez les fonctionnalités offertes par cette fonctionnalité.

**Pour vérifier la gestion de plusieurs ordinateurs à l’aide d’un seul compte**

-   Vérifiez la fonctionnalité du magasin pour gérer plusieurs ordinateurs.

### <a name="managing-a-store-specific-account"></a>Gestion d’un compte Store-Specific

Le magasin peut ne pas avoir de types de compte, de restrictions ou de contenu typiques. Par exemple, un magasin qui loue la vidéo en continu a besoin d’une interface utilisateur pour afficher les loyers actifs et cette interface utilisateur doit être testée.

> [!Note]  
> Bien que Microsoft ne puisse pas certifier les fonctionnalités de compte spécifiques au magasin, pour garantir une expérience utilisateur correcte, vous devez tester cette fonctionnalité.

 

### <a name="managing-the-info-center"></a>Gestion d’info Center

Tout d’abord, effectuez les étapes suivantes pour préparer le test de l’État par défaut, puis effectuez l’étape suivante qui suit les étapes initiales pour vérifier que le centre d’informations est désactivé par défaut :

1.  Lire du contenu à partir du Store.
2.  Basculez en mode de diffusion en cours. dans Windows XP ou Windows Vista avec Lecteur Windows Media 11, cliquez sur l’onglet en **cours de diffusion** . dans Windows 7 avec Lecteur Windows Media 12, cliquez sur le bouton **basculer en cours de diffusion** dans le coin inférieur droit.

**Pour vérifier que le centre d’informations est désactivé par défaut**

-   Vérifiez que le centre d’informations est désactivé par défaut.

Si le magasin offre une vue Info Center, lisez du contenu à partir du Store, et Pendant que le contenu est en cours de lecture, passez en mode lecture en cours et activez le centre d’informations.

dans Windows XP ou Windows Vista avec Lecteur Windows Media 11, cliquez avec le bouton droit sur la fenêtre en cours de exécution, puis dans le menu contextuel, sélectionnez **affichage du centre d’informations**.

la capture d’écran suivante montre le menu contextuel dans Lecteur Windows Media 11 :

![capture d’écran montrant comment accéder au centre d’informations d’un magasin dans le lecteur Windows Media 11](images/wmp11-info-center.png)

dans Windows 7 avec Lecteur Windows Media 12, cliquez avec le bouton droit sur la fenêtre de diffusion en cours, puis dans le menu contextuel, sélectionnez **visualisations**, puis cliquez sur **affichage centre d’informations**.

la capture d’écran suivante montre le menu contextuel dans Lecteur Windows Media 12 :

![capture d’écran montrant comment accéder au centre d’informations d’un magasin dans le lecteur Windows Media 12](images/wmp12-info-center.png)

**Pour vérifier que le centre d’informations est fonctionnel**

-   Vérifiez que le centre d’informations affiche des informations sur le média dans la zone de diffusion en cours. La capture d’écran suivante montre un exemple d’informations de ce type de média :

    ![capture d’écran montrant les fonctionnalités du centre d’informations d’un magasin](images/media-information.png)

Si des liens d’achat ou d’autres liens apparaissent sur la page, cliquez sur les liens.

**Pour vérifier les liens dans la vue Centre d’informations**

-   Vérifiez que les liens affichent le magasin.

    le Lecteur Windows Media doit basculer vers le magasin dans sa bibliothèque.

## <a name="store-interaction"></a>Interaction du Store

Les sections suivantes décrivent comment tester l’interaction entre les autres magasins et le magasin que vous testez.

### <a name="yielding-to-the-active-store"></a>Donner au magasin actif

Basculez vers un magasin autre que le magasin en cours de test.

**Pour vérifier le rendement du magasin actif**

-   Vérifiez que le magasin testé produit le magasin actif.

### <a name="preventing-the-tested-store-from-taking-over-the-active-store"></a>Empêcher le magasin testé de prendre le contrôle du magasin actif

-   avec un autre magasin sélectionné, fermez Lecteur Windows Media et redémarrez l’ordinateur.
-   lancez Lecteur Windows Media.

**Pour vérifier que le magasin testé ne prend pas le contrôle**

-   Vérifiez que le magasin actif le plus récent s’affiche et que le magasin testé n’apparaît pas.

### <a name="accessing-a-store-in-high-contrast-mode"></a>Accès à un magasin en mode High-Contrast

Commencez par activer le mode de contraste élevé en appuyant sur MAJ gauche + ALT gauche + Impr. écran, puis procédez comme suit pour vérifier l’accessibilité à contraste élevé :

**Pour vérifier que le magasin est accessible en mode de contraste élevé**

1.  Vérifiez que l’interface utilisateur de connexion est intacte et fonctionnelle.
2.  Vérifiez que toutes les fenêtres et boîtes de dialogue s’affichent correctement.
3.  Acheter un support. Vérifiez que les boutons achat et téléchargement, les gestionnaires de téléchargement, les informations sur les prix, etc. sont visibles.
4.  Vérifiez que vous pouvez diffuser, graver et synchroniser.
5.  Recherchez du texte tronqué et des éléments d’interface utilisateur, du texte qui n’est pas lisible et d’autres défauts visibles.

### <a name="securing-a-store"></a>Sécurisation d’un magasin

Pour vérifier la sécurité du compte, procédez comme suit :

**Pour vérifier la sécurité du compte**

1.  Entrez les informations de compte incorrectes dans la page de connexion et la boîte de dialogue et vérifiez que le magasin les rejette.
2.  Connectez-vous, affichez la page du compte, puis déconnectez-vous.
3.  cliquez sur le bouton précédent dans Lecteur Windows Media et vérifiez que vous ne voyez pas les informations de compte d’utilisateur précédentes.

 

 




