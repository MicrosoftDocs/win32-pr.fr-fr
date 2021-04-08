---
title: Gestion des fenêtres
description: Cet article traite de l’emplacement par défaut des fenêtres lorsqu’elles sont initialement affichées sur l’écran, de leur ordre d’empilement par rapport à d’autres fenêtres (ordre de plan), de leur taille initiale et de la façon dont leur affichage affecte le focus d’entrée.
ms.assetid: d81bd71c-6d8f-45a9-82cb-bdb9b8bcbb11
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: dc194741713a139f643ad84b829294577d020d94
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103953324"
---
# <a name="window-management"></a>Gestion des fenêtres

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Cet article traite de l’emplacement par défaut des fenêtres lorsqu’elles sont initialement affichées sur l’écran, de leur ordre d’empilement par rapport à d’autres fenêtres ([ordre de plan](glossary.md)), de leur taille initiale et de la façon dont leur affichage affecte le focus d’entrée.

Pour connaître les instructions suivantes :

-   Une fenêtre de niveau supérieur n’a pas de fenêtre propriétaire et est affichée dans la barre des tâches. Exemples : fenêtres d’application. Dans Windows Vista et versions ultérieures, les boîtes de dialogue sans fenêtres propriétaires et feuilles de propriétés sont également considérées comme de niveau supérieur.
-   Une fenêtre propriétaire a une fenêtre propriétaire et n’est pas affichée dans la barre des tâches. Exemples : boîtes de dialogue modales, boîtes de dialogue non modales.
-   Une fenêtre initiée par l’utilisateur est affichée en tant que résultat direct de l’action d’un utilisateur. Dans le cas contraire, il est lancé par le programme s’il est initié par un programme ou par le système lancé par Microsoft Windows. Par exemple, une boîte de dialogue Options est lancée par l’utilisateur, mais un rappel de réunion est initié par le programme.
-   Une fenêtre contextuelle est une fenêtre initiée par l’utilisateur qui a une relation forte avec l’objet à partir duquel elle a été lancée. Par exemple, les fenêtres affichées par les menus contextuels ou les icônes de la zone de notification sont contextuelles, mais les fenêtres affichées par les barres de menus ne le sont pas.
-   Le moniteur actif est le moniteur sur lequel le programme actif est en cours d’exécution.
-   Le moniteur par défaut est celui contenant le menu Démarrer, la barre des tâches et la zone de notification.

## <a name="design-concepts"></a>Principes de conception

La gestion des fenêtres est l’une des activités les plus fondamentales de l’utilisateur. Avant Windows Vista, Windows avait souvent des tailles par défaut réduites et placées au milieu de l’écran. Cette approche fonctionne bien pour les anciennes analyses de faible résolution, mais pas pour le matériel vidéo moderne.

Windows est conçu pour prendre en charge le matériel vidéo moderne, qui s’exécute souvent à des résolutions nettement supérieures à la résolution d’écran minimale prise en charge et peut avoir plusieurs moniteurs. Procédez ainsi :

-   Permet aux utilisateurs de tirer pleinement parti de leur matériel avancé.
-   Nécessite moins d’efforts de la part des utilisateurs pour déplacer leur souris sur de plus grandes distances.
-   Rend le positionnement de la fenêtre plus prévisible et, par conséquent, plus facile à trouver.

### <a name="the-minimum-supported-screen-resolution"></a>Résolution d’écran minimale prise en charge

La [résolution d’écran](glossary.md) minimale prise en charge par Windows est de 800x600 pixels. Cela signifie que les fenêtres à taille fixe doivent s’afficher entièrement à la résolution minimale (tout en réservant de l’espace pour la barre des tâches), mais les fenêtres redimensionnables peuvent être optimisées pour une résolution efficace de 1 024 pixels, à condition qu’elles soient fonctionnelles à la résolution minimale.

Alors que les résolutions d’écran physiques les plus courantes pour les PC Windows sont de 1024 x 768 pixels ou plus, le ciblage de 800 x 600 pixels permet à Windows d’effectuer les opérations suivantes :

-   Travaillez bien avec tout le matériel moderne, y compris les petits PC Notebooks.
-   Prise en charge des paramètres haute résolution (points par pouce).
-   Prend en charge des polices de plus grande taille pour l’accessibilité.
-   Prise en charge du matériel utilisé sur une base globale.

Le choix de la résolution minimale pour la prise en charge requiert un bon équilibre. Le ciblage d’une résolution plus élevée se traduirait par une expérience non optimale pour un pourcentage significatif de matériel moderne, tandis que le ciblage d’une résolution inférieure empêche les concepteurs de tirer pleinement parti de l’espace d’écran disponible.

Si vous pensez que vos utilisateurs cibles utilisent des résolutions nettement supérieures à celles de la version Windows minimale, vous pouvez concevoir votre programme pour tirer pleinement parti de l’espace d’écran supplémentaire en utilisant des fenêtres redimensionnables qui évoluent bien.

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Général

-   **Prendre en charge la résolution effective Windows minimale de 800x600 pixels.** Pour les interfaces utilisateur (IU) critiques qui doivent fonctionner en mode sans échec, prennent en charge une résolution efficace de 640 x 480 pixels. Veillez à tenir compte de l’espace utilisé par la barre des tâches en réservant 48 [pixels relatifs](glossary.md) verticaux pour les fenêtres affichées avec la barre des tâches.
-   **Optimisez les dispositions de fenêtres redimensionnables pour une résolution efficace de 1024 x 768 pixels.** Redimensionnez automatiquement ces fenêtres pour réduire la résolution de l’écran d’une manière qui reste fonctionnelle.
-   **Veillez à tester vos fenêtres en 96 ppp (100%) à 800 x 600 pixels, 120 DPI (125%) à 1 024 x 768 pixels et 144 dpi (150%) à 1200x900 pixels.** Vérifiez les problèmes de disposition, tels que le découpage des contrôles, du texte et des fenêtres, et l’étirement des icônes et des bitmaps.
-   **Pour les programmes qui utilisent des scénarios tactiles et mobiles, optimisez pour 120 ppp.** Les écrans haute résolution sont actuellement répandus sur les PC tactiles et les ordinateurs portables.
-   **Les fenêtres redimensionnables ne doivent plus afficher le glyphe de redimensionnement** dans l’angle inférieur droit, car :
    -   Tous les côtés et les bords d’une fenêtre sont redimensionnables, pas seulement le coin inférieur droit.
    -   Le glyphe requiert l’affichage d’une barre d’État, mais de nombreuses fenêtres redimensionnables ne fournissent pas de barres d’État.
    -   Les pointeurs de bordure et de redimensionnement de fenêtre redimensionnables sont plus efficaces pour communiquer qu’une fenêtre est redimensionnable que le glyphe de redimensionnement.

### <a name="title-bar-controls"></a>Contrôles de barre de titre

Utilisez les contrôles de barre de titre comme suit :

-   **Plus.** Toutes les fenêtres primaires et secondaires avec un frame de fenêtre standard doivent avoir un bouton Fermer dans la barre de titre. Le fait de cliquer sur Fermer a pour effet d’annuler ou de fermer la fenêtre.

![capture d’écran de la boîte de dialogue sans bouton Fermer ](images/win-window-mgt-image1.png)

Dans cet exemple, la boîte de dialogue n’a pas de bouton Fermer dans la barre de titre.

-   **Icône.** Toutes les fenêtres principales et les fenêtres secondaires non modales en mode longue (telles que les boîtes de dialogue de progression) doivent avoir un bouton réduire. Le fait de cliquer sur réduire réduit la fenêtre à son bouton de la barre des tâches. Par conséquent, les fenêtres qui peuvent être réduites nécessitent une icône de barre de titre.
-   **Optimiser/restaurer.** Toutes les fenêtres redimensionnables doivent avoir un bouton d’agrandissement/de restauration. Le fait de cliquer sur agrandir affiche la fenêtre dans sa plus grande taille, ce qui, pour la plupart des fenêtres, est plein écran. tandis que cliquer sur Restaurer vers le haut affiche la fenêtre dans sa taille précédente. Toutefois, certaines fenêtres ne tirent pas parti de l’utilisation d’un écran plein. par conséquent, ces fenêtres doivent s’agrandir à leur plus grande taille utile.

### <a name="window-size"></a>Taille de la fenêtre

-   **Choisissez une taille de fenêtre par défaut adaptée à son contenu.** N’hésitez pas à utiliser des tailles de fenêtre initiales supérieures si vous pouvez utiliser l’espace de manière efficace.
-   **Utilisez des fenêtres redimensionnables quand cela est possible pour éviter les barres de défilement et les données tronquées.** Windows avec du contenu dynamique et des listes tirent le meilleur parti des fenêtres redimensionnables.
-   **Pour les documents texte, envisagez une longueur de ligne maximale de 65 caractères** pour faciliter la lecture du texte. (Les caractères incluent des lettres, des signes de ponctuation et des espaces.)
-   Fenêtres à taille fixe :
    -   **Doit être entièrement visible et dimensionné pour s’ajuster à la zone de travail.**
-   Fenêtres redimensionnables :
    -   **Peut être optimisé pour des résolutions plus élevées, mais en fonction des besoins au moment de l’affichage de la résolution réelle de l’écran.**
    -   **Pour les tailles de fenêtre progressivement supérieures, doit afficher progressivement plus d’informations.** Assurez-vous qu’au moins une partie ou un contrôle de fenêtre a un contenu redimensionnable.
    -   **Doit éviter les tailles restaurées par défaut qui sont agrandies ou presque agrandies.** Au lieu de cela, choisissez une taille par défaut qui est généralement la plus utile sans être en mode plein écran. Supposons que les utilisateurs agrandissent la fenêtre au lieu de la redimensionner pour la rendre en plein écran.
    -   **Doit définir une taille de fenêtre minimale s’il existe une taille au-dessous de laquelle le contenu n’est plus utilisable.** Pour les contrôles redimensionnables, définissez la taille minimale des éléments redimensionnables sur leur plus petite taille fonctionnelle, telle que la largeur minimale des colonnes fonctionnelles dans les affichages de liste.
    -   **Si vous modifiez la présentation, le contenu est utilisable à des tailles plus petites.**

![capture d’écran des boutons du lecteur multimédia ](images/win-window-mgt-image2.png)

Dans cet exemple, le lecteur Windows Media modifie son format lorsque la fenêtre devient trop petite pour le format standard.

### <a name="window-location"></a>Emplacement de la fenêtre

-   **Pour les recommandations suivantes, le « centrage » signifie que vous devez placer un positionnement vertical légèrement vers le haut de l’écran, au lieu de le placer exactement au milieu.** Placez 45% de l’espace entre le haut du moniteur/propriétaire et la fenêtre supérieure, et 55% entre le bas du moniteur/propriétaire et la fenêtre en bas. Procédez comme suit, car l’œil est naturellement biaisé vers le haut de l’écran.

    ![figure de fenêtre placée légèrement au-dessus du centre ](images/win-window-mgt-image3.png)

    « Centrage » signifie que le placement vertical est légèrement en haut du moniteur.

-   **Si une fenêtre est contextuelle, affichez-la toujours près de l’objet à partir duquel elle a été lancée.** Placez-le en dehors de la façon dont l’objet source n’est pas couvert par la fenêtre.

    -   S’il est affiché à l’aide de la souris, lorsque cela est possible, placez-le sur le décalage vers la droite et vers la droite.

    ![figure de la fenêtre contextuelle placée à droite de l’objet ](images/win-window-mgt-image4.png)

    Afficher les fenêtres contextuelles près de l’objet à partir duquel elle a été lancée.

    ![figure de la fenêtre de la zone de notification ](images/win-window-mgt-image5.png)

    Les fenêtres lancées à partir des icônes de la zone de notification sont affichées près de la zone de notification.

-   S’il est affiché à l’aide d’un stylet, si possible, placez-le afin qu’il ne soit pas couvert par la main de l’utilisateur. Pour les utilisateurs droitiers, afficher à gauche ; Sinon, s’affiche à droite.

    ![figure de la fenêtre contextuelle placée à gauche de l’objet ](images/win-window-mgt-image6.png)

    Lorsque vous utilisez un stylet, affichez également des fenêtres contextuelles afin qu’elles ne soient pas couvertes par la main de l’utilisateur.

-   **Développeurs :** Vous pouvez faire la distinction entre les événements de souris et les événements de stylet à l’aide de l’API [GetMessageExtraInfo](../tablet/system-events-and-mouse-messages.md) . Vous pouvez déterminer la [gauche](/previous-versions/ms819495(v=msdn.10)) de l’utilisateur à l’aide de l’API [SystemParametersInfo](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) avec SPI \_ GETMENUDROPALIGNMENT.
-   **Placez les boîtes de dialogue de progression dans le coin inférieur droit de l’écran actif.**

    ![figure de la barre de progression dans le coin inférieur droit ](images/win-window-mgt-image7.png)

    Placez les boîtes de dialogue de progression dans le coin inférieur droit.

-   **Si une fenêtre n’est pas associée au contexte actuel ou à l’action de l’utilisateur, placez-la en dehors de l’emplacement du pointeur actuel.** Cela empêche toute interaction accidentelle.
-   **Si une fenêtre est un document ou une application de niveau supérieur, en cascade son origine dans le coin supérieur gauche du moniteur.** S’il est créé par le programme actif, utilisez le moniteur actif. dans le cas contraire, utilisez le moniteur par défaut.

    ![figure de trois fenêtres en cascade en haut à gauche ](images/win-window-mgt-image8.png)

    Montez en cascade les fenêtres d’application ou de document de niveau supérieur dans le coin supérieur gauche du moniteur.

-   **Si une fenêtre est un utilitaire de niveau supérieur, affiche toujours « centré » dans le moniteur.** S’il est créé par le programme actif, utilisez le moniteur actif. dans le cas contraire, utilisez le moniteur par défaut.

    ![figure de la fenêtre utilitaire centrée dans l’analyse ](images/win-window-mgt-image9.png)

    Centrer les fenêtres de l’utilitaire de niveau supérieur.

-   **Si une fenêtre est une fenêtre enfant, affiche initialement « centré » en haut de la fenêtre propriétaire.** Pour l’affichage suivant, envisagez de l’afficher à son dernier emplacement (par rapport à la fenêtre propriétaire) si cela est susceptible d’être plus pratique.

    ![figure de la fenêtre possédée centrée sur la fenêtre propriétaire ](images/win-window-mgt-image10.png)

    Au départ, les fenêtres détenues sont en haut de la fenêtre propriétaire.

-   **Pour les boîtes de dialogue non modales, affiche toujours au début de la fenêtre propriétaire pour faciliter leur recherche.** Toutefois, si l’utilisateur active la fenêtre propriétaire, cela peut masquer la boîte de dialogue non modale.

    ![figure de la boîte de dialogue non modale sur la fenêtre propriétaire ](images/win-window-mgt-image11.png)

    Affichez les boîtes de dialogue non modales initialement en haut de la fenêtre propriétaire pour les rendre plus faciles à trouver.

-   **Si nécessaire, ajustez l’emplacement initial afin que la fenêtre entière soit visible dans le moniteur cible.** Si une fenêtre redimensionnable est plus grande que le moniteur cible, réduisez-la pour l’ajuster.

### <a name="window-order-z-order"></a>Ordre des fenêtres (ordre de plan)

-   **Placez toujours les fenêtres détenues au-dessus de leur fenêtre propriétaire.** Ne placez jamais les fenêtres détenues sous leurs fenêtres propriétaires, car les utilisateurs les plus probables ne les voient pas.
-   **Respecter la sélection de l’ordre Z des utilisateurs. Lorsque les utilisateurs sélectionnent une fenêtre, mettez uniquement les fenêtres associées à cette instance du programme (la fenêtre plus tout propriétaire ou Windows détenu) en haut de l’ordre de plan.** Ne modifiez pas l’ordre de toutes les autres fenêtres, telles que les instances indépendantes du même programme.

### <a name="window-activation"></a>Activation de la fenêtre

-   **Respecter la sélection de l’état de la fenêtre des utilisateurs. Si une fenêtre existante nécessite une attention, flashez le bouton de la barre des tâches trois fois pour attirer l’attention et la garder en surbrillance, mais ne faites rien d’autre.** Ne restaurez pas ou n’activez pas la fenêtre. N’utilisez aucun effet sonore. Au lieu de cela, laissez les utilisateurs activer la fenêtre lorsqu’ils sont prêts.
    -   **Exception :** Si la fenêtre n’apparaît pas dans la barre des tâches, placez-la en haut de toutes les autres fenêtres et flashez sa barre de titre à la place.
-   La **restauration d’une fenêtre principale doit également restaurer toutes ses fenêtres secondaires**, même si ces fenêtres secondaires possèdent leur propre bouton de la barre des tâches. Lors de la restauration, placez les fenêtres secondaires au-dessus de la fenêtre principale.

### <a name="input-focus"></a>Focus d’entrée

-   **Les fenêtres affichées par les actions initiées par l’utilisateur doivent prendre le focus d’entrée, mais uniquement si la fenêtre est restituée immédiatement** (dans les 5 secondes). Une fois la fenêtre rendue, elle peut prendre le focus d’entrée une fois.
    -   Si une fenêtre s’affiche lentement (plus de 5 secondes), les utilisateurs sont susceptibles d’effectuer une autre tâche pendant qu’ils attendent. Prendre le focus à ce stade serait un ennuyeux, surtout s’il est fait plusieurs fois.
-   **Les fenêtres qui ne sont pas immédiatement affichées ou affichées par une action initiée par le système ne doivent pas prendre le focus d’entrée.** Au lieu de cela, s’affichent en haut sans le focus et permettent aux utilisateurs de les activer lorsqu’ils sont prêts.
    -   **Exception :** Gestionnaire d’informations d’identification.

### <a name="persistence"></a>Persistance

-   **Quand une fenêtre est réaffichée, envisagez de l’afficher dans le même État que le dernier accès.** Lors de la fermeture, enregistrez l’analyse utilisée, la taille de la fenêtre, l’emplacement et l’État (agrandi et Restore). Lorsque vous réaffichez, restaurez la taille, l’emplacement et l’état de la fenêtre enregistrée à l’aide de l’analyse appropriée. Envisagez également de rendre ces attributs persistants entre les instances de programme pour chaque utilisateur. **Exceptions :**
    -   N’enregistrez pas ou ne rendez pas ces attributs persistants pour Windows quand leur utilisation est telle que les utilisateurs sont beaucoup plus susceptibles de démarrer complètement.
    -   Pour les programmes susceptibles d’être utilisés sur les ordinateurs Windows tablette et Touch Technology, économisez deux États Windows en mode paysage et en mode portrait. Pour plus d’informations, consultez [conception pour différentes tailles d’affichage](/previous-versions/windows/desktop/ms695587(v=vs.85)).
-   **Si la configuration de l’analyse en cours empêche l’affichage d’une fenêtre à l’aide de son dernier État :**
    -   Essayez d’afficher la fenêtre à l’aide de sa dernière analyse.
    -   Si la fenêtre est plus grande que le moniteur, redimensionnez la fenêtre en fonction des besoins.
    -   Déplacez l’emplacement vers l’angle supérieur gauche pour qu’il s’ajuste à l’écran en fonction de vos besoins.
    -   Si les étapes ci-dessus ne résolvent pas le problème, rétablissez les règles de placement de la fenêtre par défaut. Envisagez de restaurer la taille précédente, si possible.

 

 