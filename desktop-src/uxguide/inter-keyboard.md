---
title: Clavier
description: Le clavier est l’appareil d’entrée principal utilisé pour l’entrée de texte dans Microsoft Windows. Pour l’accessibilité et l’efficacité, la plupart des actions peuvent également être effectuées à l’aide du clavier.
ms.assetid: 27185c98-1233-4e26-a156-0ff080fd4db3
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c1554ca1a9769b562f154498cd0871bc1b813067
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524294"
---
# <a name="keyboard"></a>Clavier

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Le clavier est l’appareil d’entrée principal utilisé pour l’entrée de texte dans Microsoft Windows. Pour l’accessibilité et l’efficacité, la plupart des actions peuvent également être effectuées à l’aide du clavier.

Les claviers peuvent également faire référence à des claviers virtuels, à l’écran et à l’écriture de pavés utilisés par des ordinateurs sans clavier physique, tels que des ordinateurs de type tablette.

![capture d’écran du clavier visuel ](images/inter-keyboard-image1.png)

Le clavier visuel du Tablet PC et de la technologie tactile Windows.

![capture d’écran du bloc d’écriture Windows Tablet ](images/inter-keyboard-image2.png)

Le bloc d’écriture de la technologie Windows tablette et Touch.

Il existe six types de clés de base :

-   Une touche de caractère envoie un caractère littéral à la fenêtre avec le focus d’entrée.
-   Une touche de modification combinée avec une autre touche modifie la signification de la clé associée, telle que CTRL, Alt, Maj et la touche du logo Windows.
-   Les touches de navigation sont les flèches directionnelles, plus les touches début, fin, page précédente et page suivante.
-   Les touches de modification sont Insert, RET (retour arrière) et Delete (supprimer).
-   Les touches de fonction sont F1 à F12.
-   Les clés système placent le système dans un mode ou effectuent une tâche système, comme l’écran d’impression, Verr. Maj et Verr. num.

Les clés d’accès sont des clés ou des combinaisons de touches utilisées pour l’accessibilité afin d’interagir avec tous les contrôles ou éléments de menu à l’aide du clavier. Les touches de raccourci sont des clés ou des combinaisons de touches utilisées par les utilisateurs avancés pour exécuter des commandes fréquemment utilisées pour plus d’efficacité. Windows indique les touches d’accès en soulignant l’attribution de clé d’accès.

![capture d’écran des touches d’accès rapide et des touches de raccourci ](images/inter-keyboard-image3.png)

Cet exemple montre à la fois les touches d’accès rapide et les touches de raccourci.

Pour éliminer l’encombrement visuel, Windows MASQUE les soulignements de touches d’accès par défaut et les affiche uniquement lorsque la touche Alt est enfoncée. Pour maintenir la cohérence avec Windows, les images dans le Guide de l’expérience utilisateur sont également affichées avec les soulignements de clé d’accès masqués, sauf si l’instruction implique des clés d’accès.

Pour améliorer la sensibilisation des affectations de touches d’accès dans votre programme tout au long du processus de développement, vous pouvez les afficher à tout moment. Dans le panneau de configuration, accédez à la facilité d’accès, puis cliquez sur **rendre le clavier plus facile à utiliser**. Activez ensuite la case à cocher **souligner les raccourcis clavier et les touches d’accès** .

**Remarque :** Les instructions relatives à l' [accessibilité](inter-accessibility.md) sont présentées dans un article distinct.

## <a name="design-concepts"></a>Principes de conception

### <a name="elements-of-keyboard-navigation"></a>Éléments de navigation au clavier

Les utilisateurs interagissent avec une fenêtre à l’aide du clavier en accédant à contrôles, en effectuant des sélections et en exécutant des commandes. Les éléments suivants fonctionnent ensemble pour que cela se produise.

![capture d’écran de la boîte de dialogue Modifier les couleurs ](images/inter-keyboard-image4.png)

Pour illustrer les éléments de navigation au clavier dans la liste suivante, nous allons faire référence à cette boîte de dialogue.

-   **Focus d’entrée.** Le contrôle avec le focus d’entrée reçoit la plus grande partie de l’entrée au clavier. Le focus d’entrée est indiqué par un rectangle en pointillés appelé « rectangle de focus ». Une entrée au clavier est envoyée aux contrôles qui n’ont pas de focus d’entrée, comme expliqué plus loin.

    ![capture d’écran de la première ligne dans la boîte de dialogue Modifier les couleurs ](images/inter-keyboard-image5.png)

    Le premier contrôle des couleurs de base a le focus d’entrée, comme indiqué par un rectangle en pointillés.

-   **Touche Tab et taquets de tabulation.** La touche Tab est le mécanisme principal de navigation dans une fenêtre. La touche Tab visite uniquement les contrôles avec un taquet de tabulation. Tous les contrôles interactifs doivent comprendre des taquets de tabulation (sauf s’ils figurent dans un groupe), au contraire des contrôles non interactifs, tels que des étiquettes.
-   **Ordre de tabulation.** Tous les contrôles avec des taquets de tabulation sont visités dans l’ordre de tabulation. Le fait d’appuyer sur la touche Tab déplace le focus d’entrée vers le contrôle suivant dans l’ordre de tabulation, tandis que l’appui sur Maj + Tab déplace le focus d’entrée vers le contrôle précédent.
-   **Groupes de contrôles.** Un ensemble de contrôles connexes peut être créé dans un groupe et recevoir un seul taquet de tabulation. Les groupes de contrôles sont utilisés pour des ensembles de contrôles qui se comportent comme un contrôle unique, telles des cases d’option. Ils peuvent également servir quand l’abondance des contrôles rend malaisée une navigation efficace à l’aide de la seule touche de tabulation.

    ![capture d’écran des groupes de couleurs de base et personnalisés ](images/inter-keyboard-image6.png)

    Les couleurs de base et les couleurs personnalisées sont des groupes de contrôles, ce qui donne à cette boîte de dialogue cinq taquets de tabulation. Il y a tant de contrôles que la navigation serait inefficace sans utiliser de groupes de contrôle.

-   **Touches de direction.** Les touches de direction déplacent le focus d’entrée parmi les contrôles d’un groupe. Le fait d’appuyer sur la touche de direction droite déplace le focus d’entrée vers le contrôle suivant dans l’ordre de tabulation, tandis que le fait d’appuyer sur la flèche gauche déplace le focus d’entrée vers le contrôle précédent. Début, fin, haut et bas ont également leur comportement attendu au sein d’un groupe. Les utilisateurs ne peuvent pas quitter un groupe de contrôle à l’aide des touches de direction.
-   **Boutons par défaut.** Les fenêtres avec des boutons de commande et des liens de commande ont un seul bouton par défaut indiqué par une bordure en surbrillance, qui est le bouton sur lequel l’utilisateur clique quand la touche entrée est enfoncée. Il existe un seul bouton de commande par défaut ou un seul lien de commande attribué par défaut. Toutefois, le bouton par défaut se déplace lorsque l’utilisateur accède à un autre bouton de commande ou à un autre lien de commande. Par conséquent, un bouton de commande ou un lien de commande avec le focus d’entrée est également toujours le bouton par défaut.

    ![capture d’écran des boutons OK et annuler ](images/inter-keyboard-image7.png)

    Le bouton OK est normalement le bouton par défaut, comme indiqué par sa bordure en surbrillance. Toutefois, si l’utilisateur devait accéder au bouton Annuler, il deviendra le bouton par défaut et serait activé avec la touche entrée.

-   **Touche espace, entrée et ÉCHAP.** La barre d’espace active le contrôle avec le focus d’entrée, tandis que la touche entrée active le bouton par défaut. Appuyez sur la touche ÉCHAP pour annuler ou fermer la fenêtre.
-   **Clés d’accès.** Les clés d’accès sont utilisées pour interagir directement avec les contrôles au lieu de naviguer avec la touche Tab. Ils sont associés à la touche Alt et sont signalés par une lettre soulignée dans leur étiquette.
-   **Les étiquettes de clé d’accès.** Bien que certains contrôles contiennent leurs propres étiquettes, telles que les boutons de commande, les cases à cocher et les cases d’option, les autres contrôles possèdent des étiquettes externes, telles que des zones de liste et des arborescences. Pour les étiquettes externes, la touche d’accès est assignée à l’étiquette et, si elle est appelée, accède au contrôle suivant dans l’ordre de tabulation. Les boutons intitulés OK, annuler et fermer ne sont pas affectés à des clés d’accès, car ils sont appelés avec la touche entrée et la touche ÉCHAP.

    ![capture d’écran des étiquettes avec « b » et « d » soulignées ](images/inter-keyboard-image8.png)

    En appuyant sur Alt + B, vous accédez à la couleur de base sélectionnée, en appuyant sur ALT + D. pour cela, vous pouvez cliquer sur le bouton définir des couleurs personnalisées, sur le bouton OK, puis sur la touche ÉCHAP pour appeler annuler.

-   **Comportement de la clé d’accès.** Lorsqu’une touche d’accès est appelée et qu’elle est assignée de manière unique, le contrôle associé est cliqué. Si l’assignation n’est pas unique, le contrôle associé reçoit le focus d’entrée. Si l’utilisateur tape à nouveau la même clé d’accès, le contrôle suivant dans l’ordre de tabulation avec la même assignation reçoit le focus d’entrée.

Bien que ce mécanisme soit assez compliqué, il est également assez intuitif. Les utilisateurs récupèrent immédiatement ces détails, même si peu d’entre eux peuvent expliquer exactement comment ils fonctionnent.

### <a name="keyboard-support-for-accessibility-and-advanced-users"></a>Prise en charge du clavier pour l’accessibilité et les utilisateurs expérimentés

**Dans Windows, le fait de concevoir pour le clavier revient à fournir une navigation au clavier bien conçue, des touches d’accès rapide pour l’accessibilité et des touches de raccourci pour les utilisateurs expérimentés.**

Pour vous assurer que la fonctionnalité de votre programme est facilement accessible à la plus large gamme d’utilisateurs, y compris ceux présentant des handicaps et des handicaps, tous les éléments d’interface utilisateur interactifs doivent être accessibles via le clavier. En général, cela signifie que les éléments d’interface utilisateur les plus couramment utilisés sont accessibles à l’aide d’une clé d’accès unique ou d’une combinaison de touches, tandis que les éléments moins fréquemment utilisés peuvent nécessiter une navigation de tabulation ou de touche de direction supplémentaire. Pour ces utilisateurs, l’exhaustivité est plus importante que la cohérence.

Pour vous assurer que les fonctionnalités de votre programme sont efficaces pour les utilisateurs expérimentés, les éléments d’interface utilisateur couramment utilisés doivent également avoir des touches de raccourci pour accéder directement au clavier. Les utilisateurs expérimentés ont souvent une préférence marquée pour l’utilisation du clavier, car les commandes clavier peuvent être entrées plus rapidement et ne nécessitent pas de retirer les mains du clavier. Pour ces utilisateurs, l’efficacité et la cohérence sont essentielles. L’exhaustivité n’est importante que pour les commandes les plus fréquemment utilisées.

Il existe des différences subtiles lors de la conception de l’accès clavier pour ces deux groupes, c’est pourquoi Windows fournit deux mécanismes d’accès direct au clavier directs. En utilisant les accès et les touches de raccourci de manière efficace, vous pouvez fournir à vos programmes un accès clavier efficace, cohérent et complet qui tire parti de tous.

### <a name="access-keys"></a>Clés d'accès

Les touches d’accès rapide présentent les caractéristiques suivantes :

-   Elles utilisent la touche Alt associée à une touche alphanumérique.
-   Elles visent principalement l’accessibilité.
-   Elles sont affectées à l’ensemble des options de menu et à la plupart des contrôles de boîte de dialogue.
-   N’étant pas destinées à être mémorisées, elles sont indiquées directement dans l’interface utilisateur par un trait soulignant le caractère de l’étiquette de contrôle correspondant.
-   Leur incidence se limite à la fenêtre active et elles permettent d’accéder à l’option de menu ou au contrôle correspondant.
-   Elles ne sont pas attribuées de façon cohérente, car ce n’est pas toujours possible. Toutefois, il convient de les attribuer de façon cohérente pour les commandes fréquemment utilisées, en particulier les boutons de validation.
-   Elles sont localisées.

**Étant donné que les clés d’accès ne sont pas destinées à être mémorisées, elles sont affectées à un caractère qui se trouve au début de l’étiquette pour faciliter leur recherche,** même s’il existe un mot clé qui apparaît plus tard dans l’étiquette.

**Correct :**

![capture d’écran du premier caractère de l’étiquette soulignée ](images/inter-keyboard-image9.png)

**Incorrect :**

![capture d’écran du vingt-et-unième caractères souligné ](images/inter-keyboard-image10.png)

Dans l’exemple correct, la touche d’accès rapide est assignée à un caractère qui se trouve au début de l’étiquette.

### <a name="shortcut-keys"></a>Touches de raccourci

En revanche, les touches de raccourci présentent les caractéristiques suivantes :

-   Elles utilisent principalement des combinaisons basées sur la touche Ctrl et une touche de fonction (les touches de raccourci système de Windows utilisent également des combinaisons basées sur la touche Alt et une touche non alphanumérique, ainsi que la touche de logo Windows).
-   Elles visent principalement à renforcer l’efficacité pour les utilisateurs expérimentés.
-   Elles sont attribuées uniquement aux commandes les plus couramment utilisées.
-   Elles sont destinées à être mémorisées et sont indiquées uniquement dans les menus, les info-bulles et l’aide.
-   Elles sont disponibles dans l’ensemble du programme, mais n’ont aucun effet là où elles ne s’appliquent pas.
-   Elles doivent être attribuées de façon cohérente, car elles sont mémorisées et non directement indiquées.
-   Elles ne sont pas localisées.

**Étant donné que les touches de raccourci sont destinées à être mémorisées, les touches de raccourci les plus fréquemment utilisées utilisent idéalement des lettres des premiers ou derniers caractères mémorables dans les mots clés de la commande,** tels que CTRL + C pour copier et CTRL + Q pour la demande.

Des significations incohérentes pour les touches de raccourci connues sont frustrantes et provoquent des erreurs.

**Incorrect :**

![capture d’écran du bouton suivant avec la ligne’w’soulignée ](images/inter-keyboard-image11.png)

Dans cet exemple, Ctrl + F est le raccourci standard de la recherche. son affectation à Forward est donc frustrante et sujette aux erreurs. CTRL + W serait un choix plus facile et mémorable.

Enfin, étant donné qu’elles sont destinées à être mémorisées, les **touches de raccourci spécifiques à l’application n’ont de sens que pour les programmes et les fonctionnalités qui sont exécutés suffisamment souvent pour les utilisateurs motivés à mémoriser.** Les programmes et fonctionnalités rarement utilisés n’ont pas besoin de touches de raccourci. Par exemple, les programmes d’installation et la plupart des assistants n’ont pas besoin d’affectations de touches de raccourci spéciales, ni de commandes rarement utilisées dans une application de productivité.

### <a name="assigning-access-keys-in-dialog-boxes"></a>Assignation de touches d’accès dans les boîtes de dialogue

Dans la mesure du possible, assignez des clés d’accès uniques à tous les contrôles interactifs, à l’exception de ceux qui ne sont normalement pas affectés. Toutefois, en anglais, il n’y a que 26 caractères. Certains caractères peuvent ne pas apparaître dans les étiquettes, et il peut y avoir des caractères distinctifs dans toutes les étiquettes, ce qui réduit davantage ce nombre. En outre, vous devez prévoir quelques caractères non assignés pour faciliter la localisation. Par conséquent, vous ne pouvez affecter qu’environ 20 clés d’accès uniques dans une même boîte de dialogue.

Si vous avez une boîte de dialogue avec plus de 20 contrôles interactifs, n’affectez pas de clés d’accès à certains contrôles, ou, dans de rares cas, attribuez des clés d’accès en double.

![capture d’écran de la boîte de dialogue police ](images/inter-keyboard-image12.png)

Lorsqu’il existe de nombreux contrôles interactifs, tous n’ont pas besoin d’une clé d’accès assignée.

Utilisez la procédure générale suivante pour affecter des clés d’accès :

-   Tout d’abord, assignez des clés d’accès aux [boutons de validation](glossary.md) et aux liens de commande. Utilisez le tableau des affectations de touches d’accès standard lorsqu’il s’applique, sinon utilisez la première lettre du premier mot.
-   Ignorez les contrôles qui n’ont pas de clés d’accès.
-   Affectez des clés d’accès uniques aux contrôles restants (à partir du le plus fréquemment utilisé) :
    -   Si possible, attribuez la clé d’accès en fonction du tableau des affectations de touches d’accès standard.
    -   Sinon :
        -   Préférer les caractères qui apparaissent tôt dans l’étiquette, idéalement le premier caractère du premier ou du deuxième mot.
        -   Préférez une consonne distinctive ou une voyelle, telle que « x » dans « Exit ».
        -   Préférer les caractères dont la largeur est large, les lettres w, m et majuscules.
        -   Évitez d’utiliser des caractères qui rendent le soulignement difficile à voir, comme des lettres d’une largeur d’un pixel, des lettres avec des descendants et des lettres à côté d’une lettre avec un descendant.
-   Si tous les contrôles ne peuvent pas avoir des clés d’accès uniques (Démarrer avec le moins fréquemment utilisé) :
    -   S’il existe des groupes de contrôles connexes, tels que :
        -   Un seul ensemble de cases d’option
        -   Ensemble de cases à cocher associées
        -   Ensemble de contrôles connexes dans une zone de groupe

Affectez des clés d’accès aux étiquettes de groupe au lieu des contrôles individuels. Normalement, vous effectuez l’inverse. (Pour ce faire, assurez-vous qu’un groupe de contrôle est défini pour ces contrôles.)

-   Si tous les contrôles ne peuvent toujours pas avoir des clés d’accès uniques :
    -   Vous pouvez assigner des clés d’accès non uniques dans les cas suivants :
        -   Dans le cas contraire, les contrôles seraient trop difficiles à naviguer.
        -   Les clés d’accès non uniques ne sont pas en conflit avec les clés d’accès des contrôles couramment utilisés.
    -   Dans le cas contraire, les autres contrôles sont accessibles à l’aide de la navigation par tabulation et touche de direction.

![capture d’écran des groupes avec différentes clés d’accès ](images/inter-keyboard-image13.png)

Dans cet exemple, il existe des contrôles répétitifs afin que les touches d’accès sont affectées aux groupes de cases d’option.

### <a name="preventing-accidental-commands"></a>Prévention des commandes accidentelles

Si une fenêtre affichée hors contexte (et non initiée par l’utilisateur) vole le focus d’entrée, il est probable que cette fenêtre recevra une entrée destinée à une autre fenêtre. En outre, les clés d’accès prennent effet quand vous appuyez sur la touche Alt sans appuyer sur la touche Alt si la boîte de dialogue n’a aucun contrôle qui prend des entrées de texte (telles que des zones de texte et des listes). Ainsi, dans l’exemple suivant, le fait d’appuyer sur « r » active le bouton redémarrer maintenant.

En clair, une telle entrée peut avoir des conséquences inattendues significatives.

**Incorrect :**

![capture d’écran du bouton redémarrer maintenant, 'r’souligné ](images/inter-keyboard-image14.png)

Dans cet exemple, si vous tapez du texte avec des espaces, « r » ou entrez, vous redémarrez Windows par inadvertance.

Bien entendu, la meilleure solution à ce problème consiste à ne pas voler le focus d’entrée. Au lieu de cela, vous pouvez faire clignoter le bouton de la [barre des tâches](winenv-taskbar.md) du programme ou afficher une notification pour attirer l’attention de l’utilisateur.

Toutefois, si vous devez afficher une telle fenêtre, la meilleure approche consiste à ne pas assigner de bouton ou de touches d’accès par défaut et à donner le focus d’entrée initial à un contrôle autre qu’un bouton de validation.

**Correct :**

![capture d’écran du bouton redémarrer, 'r’non souligné ](images/inter-keyboard-image15.png)

Dans cet exemple, le redémarrage accidentel de Windows est beaucoup plus difficile à effectuer.

**Si vous ne faites que six choses...**

1.  Concevez une bonne navigation au clavier, avec un ordre de tabulation raisonnable et des groupes de contrôles appropriés, le focus d’entrée initial et les boutons par défaut.
2.  Affecter des clés d’accès à tous les menus et à la plupart des contrôles.
3.  Affectez les touches d’accès rapide à un caractère qui apparaît tôt dans l’étiquette, pour faciliter leur recherche.
4.  Assignez des touches de raccourci aux commandes les plus couramment utilisées.
5.  Essayez d’assigner les touches de raccourci au premier ou au plus des caractères mémorables dans les mots clés.
6.  Donnez aux touches de raccourci connues une signification cohérente.

## <a name="guidelines"></a>Consignes

### <a name="interaction"></a>Interaction

-   **N’utilisez pas la touche Maj pour modifier des commandes dans des menus ou des boîtes de dialogue.** Cela n’est pas découvert et inattendu.

    **Incorrect :**

    ![capture d’écran de la boîte de dialogue confirmer le remplacement du dossier ](images/inter-keyboard-image16.png)

    Dans cet exemple de Windows XP, maintenir la touche Maj enfoncée remplace Yes par All.

-   **Ne désactivez pas un contrôle avec le focus d’entrée. Cela peut empêcher la fenêtre de recevoir l’entrée au clavier.** Au lieu de cela, avant de désactiver un contrôle avec le focus d’entrée, déplacez le focus d’entrée vers un autre contrôle.
-   **Si une fenêtre s’affiche en dehors du contexte, il peut s’avérer nécessaire d’éviter des conséquences inattendues :**
    -   N’attribuez pas de bouton par défaut.
    -   N’affectez pas de clés d’accès.
    -   Donne le focus d’entrée initial à un contrôle autre qu’un bouton de validation.

### <a name="keyboard-navigation"></a>Navigation au clavier

-   **Affiche toujours l’indicateur de focus d’entrée. Exception :** vous pouvez supprimer temporairement l’indicateur de focus d’entrée dans les cas suivants :
    -   L’indicateur de focus d’entrée est visuellement gênant (comme avec un affichage de liste large qui n’est pas en mode Détails).
    -   L’utilisation de la clé Enter est probablement précédée d’autres entrées au clavier, telles que ALT ou les touches de direction.
    -   L’indicateur de focus d’entrée est affiché sur toute entrée au clavier.
-   **Affectez le focus d’entrée initial au contrôle que les utilisateurs sont le plus susceptibles d’interagir avec en premier,** ce qui est souvent le premier contrôle interactif. Si le premier contrôle interactif n’est pas un bon choix, envisagez de modifier la disposition de la fenêtre.
-   **Affectez des taquets de tabulation à tous les contrôles interactifs, y compris les zones d’édition en lecture seule. Exceptions**
    -   Groupes de contrôles connexes qui se comportent comme un seul contrôle, tel que les cases d’option. De tels groupes comportent un seul taquet de tabulation.
    -   Contiennent correctement des groupes afin que les touches de direction recyclent vers l’avant et vers l’arrière dans le groupe et restent dans le groupe.
-   **L’ordre de tabulation doit suivre l’ordre de lecture, qui s’enchaîne généralement de gauche à droite, de haut en bas.** Envisagez de faire des exceptions pour les contrôles couramment utilisés en les plaçant plus tôt dans l’ordre de tabulation. L’onglet doit parcourir tous les taquets de tabulation dans les deux directions sans s’arrêter.
-   **Dans un taquet de tabulation, l’ordre des touches de direction doit s’écouler de gauche à droite, de haut en bas,** sans exceptions. Les touches de direction doivent parcourir tous les éléments dans les deux directions sans s’arrêter.
-   **Présentez les boutons de validation dans l’ordre suivant :**
    -   OK/ \[ do it \] /Yes
    -   \[Ne le faites pas \] /non
    -   Annuler
    -   Appliquer (le cas échéant)

\[le cas échéant \] , \[ il \] s’agit de réponses spécifiques à l’instruction principale.

-   **Sélectionnez le plus sûr (pour empêcher la perte de données ou l’accès au système) et le bouton de commande le plus sécurisé ou le lien de commande par défaut.** Si la sécurité et la sécurité ne sont pas des facteurs, sélectionnez la réponse la plus probable ou la plus pratique.
-   **La navigation au clavier ne doit pas modifier les valeurs de contrôle ou entraîner un message d’erreur.** Ne demandez jamais aux utilisateurs de modifier la valeur initiale d’un contrôle pendant la navigation. Au lieu de cela, initialisez les contrôles qui valident à la sortie avec des valeurs valides, et validez la valeur d’un contrôle uniquement lorsqu’il a changé.

### <a name="access-keys"></a>Clés d'accès

-   **Dans la mesure du possible, affectez des clés d’accès pour les commandes couramment utilisées conformément au tableau suivant.** Bien que les attributions de clé d’accès cohérentes ne soient pas toujours possibles, elles sont certainement préférées en particulier pour les commandes fréquemment utilisées.

    |  Clé d’accès         | Commande                             |
    |---------------------------|-------------------------------------------|
    | Un<br/>              | À propos de<br/>                          |
    | Un<br/>              | Toujours visible<br/>                  |
    | Un<br/>              | Appliquer<br/>                          |
    | B<br/>              | Précédent<br/>                           |
    | B<br/>              | Gras<br/>                           |
    | B ou r<br/>         | Parcourir<br/>                         |
    | C<br/>              | Fermer<br/>                          |
    | C<br/>              | Copier<br/>                           |
    | C<br/>              | Copier ici<br/>                      |
    | s<br/>              | Créer un raccourci<br/>                |
    | s<br/>              | Créer un raccourci ici<br/>           |
    | t<br/>              | Couper<br/>                            |
    | D<br/>              | Supprimer<br/>                         |
    | D<br/>              | Ne plus afficher cet \[ élément \]<br/> |
    | E<br/>              | Modifier<br/>                           |
    | x<br/>              | Quitter<br/>                           |
    | E<br/>              | Explorer<br/>                        |
    | F<br/>              | Inférieurs<br/>                          |
    | F<br/>              | Fichier<br/>                           |
    | F<br/>              | Rechercher<br/>                           |
    | n<br/>              | Suivant<br/>                      |
    | F<br/>              | Police<br/>                           |
    | F<br/>              | Transférer<br/>                        |
    | H<br/>              | Aide<br/>                           |
    | t<br/>              | rubriques d'aide<br/>                    |
    | H<br/>              | Masquer<br/>                           |
    | I<br/>              | Insérer<br/>                         |
    | o<br/>              | Insérer un objet<br/>                  |
    | I<br/>              | Italique<br/>                         |
    | L<br/>              | Lien ici<br/>                      |
    | x<br/>              | Agrandir<br/>                       |
    | n<br/>              | Réduire<br/>                       |
    | M<br/>              | Plus<br/>                           |
    | M<br/>              | Déplacer<br/>                           |
    | M<br/>              | Déplacer ici<br/>                      |
    | N<br/>              | Nouveau<br/>                            |
    | N<br/>              | Suivant<br/>                           |
    | N<br/>              | Non<br/>                             |
    | O<br/>              | Ouvrir<br/>                           |
    | w<br/>              | Ouvrir avec<br/>                      |
    | O<br/>              | Options<br/>                        |
    | u<br/>              | Mise en page<br/>                     |
    | P<br/>              | Coller<br/>                          |
    | l<br/>              | Coller le lien<br/>                     |
    | s<br/>              | Coller le raccourci<br/>                 |
    | s<br/>              | Collage spécial<br/>                  |
    | P<br/>              | Suspendre<br/>                          |
    | P<br/>              | Lire<br/>                           |
    | P<br/>              | Impression<br/>                          |
    | P<br/>              | Imprimer ici<br/>                     |
    | r<br/>              | Propriétés<br/>                     |
    | R<br/>              | Rétablir<br/>                           |
    | R<br/>              | Répéter<br/>                         |
    | R<br/>              | Restaurer<br/>                        |
    | R<br/>              | Reprendre<br/>                         |
    | R<br/>              | Réessayer<br/>                          |
    | R<br/>              | Exécuter<br/>                            |
    | S<br/>              | Enregistrer<br/>                           |
    | a<br/>              | Enregistrer sous<br/>                        |
    | a<br/>              | Sélectionner tout<br/>                     |
    | n<br/>              | Envoyer à<br/>                        |
    | S<br/>              | Afficher<br/>                           |
    | S<br/>              | Taille<br/>                           |
    | p<br/>              | Split<br/>                          |
    | S<br/>              | Arrêter<br/>                           |
    | T<br/>              | Outils<br/>                          |
    | U<br/>              | Souligner<br/>                      |
    | U<br/>              | Annuler<br/>                           |
    | V<br/>              | Affichage<br/>                           |
    | W<br/>              | Fenêtre<br/>                         |
    | Y<br/>              | Oui<br/>                            |

    

     

-   **Préférer les caractères dont la largeur est large,** par exemple w, m et les majuscules.
-   **Préférez une consonne distinctive ou une voyelle,** telle que « x » dans « Exit ».
-   **Évitez d’utiliser des caractères qui rendent le soulignement difficile à voir,** par exemple (de la plupart des problèmes aux moins problématiques) :
    -   Caractères d’une largeur de 1 pixel, tels que i et l.
    -   Caractères avec descendants, tels que g, j, p, q et y.
    -   Caractères en regard d’une lettre avec un descendant.
-   Lorsque vous affectez des clés d’accès dans les pages de l’Assistant, n’oubliez pas de réserver « B » pour back et « N » pour l’étape suivante.
-   Quand vous assignez des clés d’accès dans des pages de propriétés, n’oubliez pas de réserver « A » pour Apply, s’il est utilisé.

### <a name="menu-access-keys"></a>Touches d’accès au menu

-   **Affectez des clés d’accès à tous les éléments de menu.** Aucune exception.
-   **Pour les éléments de menu dynamiques (tels que les fichiers récemment utilisés), assignez des touches d’accès numérique.**

    ![capture d’écran des éléments de menu avec des touches d’accès numérique ](images/inter-keyboard-image17.png)

    Dans cet exemple, le programme Paint dans Windows attribue des clés d’accès numériques aux fichiers récemment utilisés.

-   **Assigner des clés d’accès uniques au sein d’un niveau de menu.** Vous pouvez réutiliser des clés d’accès dans différents niveaux de menu.
-   **Rendez les clés d’accès faciles à trouver :**
    -   Pour les éléments de menu les plus fréquemment utilisés, choisissez caractères au début du premier ou du deuxième mot de l’étiquette, de préférence le premier caractère.
    -   Pour les éléments de menu moins fréquemment utilisés, choisissez des lettres qui sont une consonne distinctive ou une voyelle dans l’étiquette.

### <a name="dialog-box-access-keys"></a>Clés d’accès aux boîtes de dialogue

-   **Dans la mesure du possible, assignez des clés d’accès uniques à tous les contrôles interactifs ou à leurs étiquettes.** Les [zones de texte en lecture seule](ctrl-text-boxes.md) sont des contrôles interactifs (dans la mesure où les utilisateurs peuvent les faire défiler et copier du texte). ils bénéficient donc des clés d’accès. **N’affectez pas de clés d’accès à :**
    -   **Boutons OK, annuler et fermer.** Enter et ESC sont utilisés pour leurs clés d’accès. Toutefois, attribuez toujours une clé d’accès à un contrôle qui signifie OK ou annuler, mais qui a une étiquette différente.

        ![capture d’écran de la boîte de dialogue avec les boutons Oui et non ](images/inter-keyboard-image18.png)

        Dans cet exemple, une clé d’accès est assignée au bouton de validation positif.

    -   **Étiquettes de groupe.** Normalement, les contrôles individuels d’un groupe sont affectés à des clés d’accès, de sorte que l’étiquette du groupe n’a pas besoin d’une. Toutefois, attribuez une clé d’accès à l’étiquette de groupe et non aux contrôles individuels en cas de pénurie de clés d’accès.
    -   Les **boutons d’aide génériques,** accessibles via la touche F1.
    -   **Étiquettes de lien.** Il y a souvent trop de liens pour affecter des clés d’accès uniques et les traits de soulignement de lien masquent les traits de soulignement des touches d’accès. Les utilisateurs accèdent aux liens avec la touche Tab à la place.
    -   **Noms d’onglets.** Les onglets sont recycles à l’aide des touches CTRL + TAB et Ctrl + Maj + Tab.
    -   **Boutons de navigation étiquetés « ... ».** Il n’est pas possible d’affecter des clés d’accès de manière unique.
    -   **Contrôles sans étiquette,** tels que les contrôles spin, les boutons de commande graphique et les contrôles de divulgation progressive sans étiquette.
    -   **Texte ou étiquettes statiques sans étiquette pour les contrôles qui ne sont pas interactifs,** tels que les barres de progression.

-   **Affectez d’abord les clés d’accès du bouton de validation pour vous assurer qu’elles ont les attributions de clés standard.** S’il n’existe pas d’affectation de clé standard, utilisez la première lettre du premier mot. Par exemple, les boutons clé d’accès pour Oui et pas de validation doivent toujours être « Y » et « N », quels que soient les autres contrôles de la boîte de dialogue.
-   **Pour les boutons de validation négatifs (autres que annuler) formulées en tant que « ne pas », attribuez la clé d’accès au « n » dans « ne pas ».** S’il n’est pas formulées, utilisez l’attribution de clé d’accès standard ou affectez la première lettre du premier mot. En procédant ainsi, tous ne sont pas et n’ont pas de clé d’accès cohérente.
-   **Pour faciliter la recherche des clés d’accès, assignez les touches d’accès rapide à un caractère qui apparaît au début de l’étiquette,** idéalement le premier caractère, même s’il existe un mot clé qui apparaît plus tard dans l’étiquette.
-   **Affectez au maximum 20 clés d’accès,** de sorte que vous ayez quelques caractères non assignés pour faciliter la localisation.
-   **S’il y a trop de contrôles interactifs pour affecter des clés d’accès uniques, vous pouvez affecter des clés d’accès non uniques** si :
    -   Dans le cas contraire, les contrôles seraient trop difficiles à naviguer.
    -   Les clés d’accès non uniques ne sont pas en conflit avec les clés d’accès des contrôles couramment utilisés.
-   **N’utilisez pas de barres de menus dans les boîtes de dialogue.** Il est difficile d’assigner des clés d’accès uniques dans ce cas, car les contrôles de boîte de dialogue et les éléments de menu partagent les mêmes caractères.

### <a name="shortcut-keys"></a>Touches de raccourci

-   **Assignez des touches de raccourci aux commandes les plus couramment utilisées.** Les programmes et fonctionnalités rarement utilisés n’ont pas besoin de touches de raccourci, car les utilisateurs peuvent utiliser des clés d’accès à la place.
-   **Ne définissez pas une touche de raccourci comme seule façon d’effectuer une tâche.** Les utilisateurs doivent également être en mesure d’utiliser la souris ou le clavier avec la touche de tabulation, la flèche et les touches d’accès.
-   **N’affectez pas des significations différentes à des touches de raccourci connues.** Étant donné qu’elles sont mémorisées, les significations incohérentes des raccourcis bien connus sont frustrantes et sujettes aux erreurs.
-   **N’essayez pas d’affecter des touches de raccourci de programme à l’ensemble du système.** Les touches de raccourci de votre programme ne seront effectives que si votre programme a le focus d’entrée.
-   **Documentez toutes les touches de raccourci.** Les raccourcis de document dans les éléments de barre de menus, les info-bulles de barre d’outils et un article d’aide unique qui documente toutes les touches de raccourci utilisées. Cela permet aux utilisateurs de découvrir les affectations de touches de raccourci qu’ils ne doivent pas être secrets.

    -   **Exception :** N’affiche pas les affectations de touches de raccourci dans les menus contextuels. Les menus contextuels n’affichent pas les affectations de touches de raccourci, car ces menus sont optimisés pour des raisons d’efficacité.

    ![capture d’écran de l’info-bulle pour la touche de raccourci en gras ](images/inter-keyboard-image19.png)

    La touche de raccourci est documentée dans l’info-bulle.

-   **Si votre programme affecte de nombreuses touches de raccourci, offre la possibilité de personnaliser les attributions.** Cela permet aux utilisateurs de réassigner les touches de raccourci conflictuelles et de migrer à partir d’autres produits. La plupart des programmes n’attribuent pas suffisamment de touches de raccourci pour avoir besoin de cette fonctionnalité.

### <a name="choosing-shortcut-keys"></a>Choix des touches de raccourci

-   **Pour les touches de raccourci connues, utilisez les affectations standard.**
-   **Pour les affectations de touches non standard, utilisez les touches de raccourci recommandées ci-dessous pour les commandes les plus fréquemment utilisées.** Ces touches de raccourci sont recommandées, car elles ne sont pas en conflit avec les raccourcis bien connus et sont faciles à appuyer.
    -   CTRL + G, J, K, L M, Q, R ou T
    -   Ctrl + nombre quelconque
    -   F7, F8, F9 ou F12
    -   MAJ + F2, F3, F4, F5, F7, F8, F9, F11 ou F12
    -   Alt + toute touche de fonction sauf F4
-   **Utilisez les touches de raccourci recommandées suivantes pour les commandes moins fréquemment utilisées.** Ces touches de raccourci n’ont pas de conflits, mais elles sont plus difficiles à appuyer souvent sur deux mains.
    -   Ctrl + toute touche de fonction, sauf F4 et F6
    -   Ctrl + Maj + une lettre ou un chiffre
-   **Rendez les touches de raccourci fréquemment utilisées faciles à mémoriser :**
    -   Utilisez des lettres plutôt que des nombres ou des touches de fonction.
    -   Essayez d’utiliser une lettre qui se trouve dans le premier mot ou le caractère le plus mémorable dans les mots clés de la commande.
-   **Utilisez les touches de fonction pour les commandes qui ont un effet à petite échelle,** telles que les commandes qui s’appliquent à l’objet sélectionné. Par exemple, F2 Renomme l’élément sélectionné.
-   **Utilisez les combinaisons de touches Ctrl pour les commandes qui ont un effet à grande échelle,** telles que les commandes qui s’appliquent à un document entier. Par exemple, CTRL + S enregistre le document actif.
-   **Utilisez les combinaisons de touches Maj pour les commandes qui étendent ou complètent les actions de la touche de raccourci standard.** Par exemple, la touche de raccourci Alt + Tab parcourt les fenêtres primaires ouvertes, tandis que les touches Alt + Maj + Tab sont placées dans l’ordre inverse. De même, la touche F1 affiche l’aide, tandis que MAJ + F1 affiche l’aide contextuelle.
-   **Quand vous utilisez les touches de direction pour déplacer ou redimensionner un élément, utilisez CTRL + touches de direction pour un contrôle plus granulaire.**

### <a name="choosing-shortcut-keys-what-not-to-do"></a>Choix des touches de raccourci (ce qui ne doit pas être fait)

-   **Ne pas faire la distinction entre les emplacements clés.** Par exemple, Windows peut faire la distinction entre le décalage vers la gauche et vers la droite, Alt, CTRL, le [logo Windows](glossary.md)et les [touches d’application](glossary.md), ainsi que les touches du pavé numérique. L’attribution d’un comportement à un seul emplacement de clé est confuse et inattendue.
-   **N’utilisez pas la touche de modification du logo Windows pour les touches de raccourci du programme.** La touche de logo Windows est réservée à une utilisation Windows. Même si une combinaison de touches du logo Windows n’est pas utilisée par Windows maintenant, elle peut être à l’avenir.
-   **N’utilisez pas la clé d’application comme modificateur de touche de raccourci.** Utilisez les touches Ctrl, Alt et Maj à la place.
-   **N’utilisez pas les touches de raccourci utilisées par Windows pour les touches de raccourci du programme.** Cela entraînera un conflit avec les touches de raccourci système Windows lorsque votre programme a le focus d’entrée.
-   **N’utilisez pas de combinaisons de touches Alt + alphanumériques pour les touches de raccourci.** Ces touches de raccourci peuvent entrer en conflit avec les touches d’accès rapide.
-   **N’utilisez pas les caractères suivants pour les touches de raccourci :** @ $ {} \[ \] \\  ~  \| ^ '  < >. Ces caractères nécessitent des combinaisons de touches différentes entre les langages ou sont spécifiques aux paramètres régionaux.
-   **Évitez les combinaisons de touches complexes,** telles que trois clés ou plus (exemple : Ctrl + Alt + barre d’espace) ou des touches éloignées du clavier (par exemple, CTRL + F5). Utilisez les touches de raccourci simples pour les commandes fréquemment utilisées.
-   **N’utilisez pas de combinaisons CTRL + ALT,** car Windows interprète cette combinaison dans certaines versions de langage comme une clé AltGR, qui génère des caractères alphanumériques.

### <a name="keyboard-and-mouse-combinations"></a>Combinaisons clavier/souris

-   Pour les liens, utilisez MAJ + clic pour naviguer à l’aide d’une nouvelle fenêtre et Ctrl + clic pour naviguer à l’aide d’un nouvel onglet. Cette approche est cohérente avec Windows Internet Explorer.

## <a name="documentation"></a>Documentation

Quand vous faites référence au clavier :

-   Utilisez le clavier visuel pour faire référence à une représentation de clavier à l’écran que l’utilisateur touche aux caractères d’entrée.
-   Faites en sorte que les combinaisons de touches commencent par la touche de modification. Présentez les touches de modification dans l’ordre suivant : logo Windows, application, CTRL, Alt, Maj. Si le modificateur de pavé numérique est utilisé, placez-le juste avant la clé qu’il modifie.
-   N’utilisez pas toutes les lettres majuscules pour les touches du clavier. Au lieu de cela, suivez la casse utilisée par les claviers standard ou en minuscules si la touche n’est pas étiquetée sur le clavier.
    -   Pour les combinaisons de touches alphabétiques, utilisez une lettre majuscule.
    -   Épeler la page vers le haut, PG. suiv, Impr. écran et défilement défil.
    -   Le signe plus, le signe moins, le trait d’Union, le point et la virgule.
    -   Pour les touches de direction, utilisez les flèches gauche, droite, haut et bas. N’utilisez pas d’étiquettes graphiques pour les touches de direction.
    -   Utilisez la touche de logo Windows et la touche d’application pour faire référence aux clés étiquetées avec des icônes. N’utilisez pas d’étiquettes graphiques pour ces clés.

**Correct :**

barre d’espace, tabulation, entrée, page précédente, Ctrl + Alt + Suppr, Alt + W, Ctrl + signe plus

**Incorrect :**

BARRE d’espace, tabulation, entrée, PG. préc., Ctrl + Alt + Suppr, alt + w, Ctrl + +

-   Indique les combinaisons de touches avec un signe plus, sans espaces.

**Correct :**

Ctrl + A, Maj + F5

**Incorrect :**

Ctrl-A, Maj + F5

-   Pour afficher une combinaison de touches qui comprend la ponctuation qui requiert l’utilisation de la touche Maj, telle que le point d’interrogation, ajoutez Shift à la combinaison et donnez le nom ou le symbole de la clé décalée. L’utilisation du nom de la clé non décalée, telle que 4 plutôt que $, peut être déroutante pour les utilisateurs ou même incorrecte ; par exemple, le ? les caractères et/ne sont pas toujours décalés vers les touches sur chaque clavier.

**Correct :**

Ctrl + Maj + ?, CTRL + MAJ + \* , Ctrl + Maj + virgule

**Incorrect :**

Ctrl + Maj +/, CTRL + ?, CTRL + MAJ + 8, Ctrl +\*

-   À première vue, utilisez la touche et avec le nom de clé si nécessaire pour plus de clarté, par exemple, la touche F1. À toutes les références suivantes, reportez-vous à la clé uniquement par son nom, par exemple, appuyez sur F1.
-   Consultez spécifiquement les touches d’accès rapide et les touches de raccourci dans programmation et autres documents techniques. N’utilisez pas d’accélérateur, de mnémonique ou de touches d’accès rapide. Partout ailleurs, utilisez le raccourci clavier, en particulier dans la documentation utilisateur.

Lorsque vous faites référence à l’interaction :

-   Utilisez la touche enfoncée, Strike, Strike ou type, quand vous appuyez sur une touche et que vous la relâchez immédiatement, lance une action dans le programme ou navigue dans un document ou une interface utilisateur.
-   Utilisez type, et non entrée, pour indiquer aux utilisateurs de taper du texte.
-   Utilisez dans les situations où la pression peut prêter à confusion, par exemple lorsque vous faites référence à un type de clé comme les touches de direction ou les touches de fonction. Dans ce cas, l’appui sur peut faire en sorte que les utilisateurs pensent avoir besoin d’appuyer sur toutes les clés simultanément.
-   Utilisez la suspension quand vous appuyez sur une touche et maintenez-la enfoncée, par exemple une touche de modification.
-   N’utilisez pas l’enfoncement comme synonyme de clic.

Exemples :

-   Tapez votre nom, puis appuyez sur entrée.
-   Appuyez sur Ctrl + F, puis tapez le texte que vous souhaitez rechercher.
-   Pour enregistrer votre fichier, appuyez sur o.
-   Pour déplacer le point d’insertion, utilisez les touches de direction.

 

