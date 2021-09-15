---
title: Souris et pointeurs
description: La souris est l’appareil d’entrée principal utilisé pour interagir avec les objets dans Windows.
ms.assetid: 4d99287d-e908-4c8b-b4f6-6e8c91c6c93e
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 6462c69216ee9acb5149a01a805503cea721bb1c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521217"
---
# <a name="mouse-and-pointers"></a>Souris et pointeurs

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

La souris est l’appareil d’entrée principal utilisé pour interagir avec les objets dans Windows. la fonctionnalité de la souris peut également englober d’autres dispositifs de pointage, tels que des trackballs, des pavés tactiles et des memory sticks intégrés à des ordinateurs portables, des stylets utilisés avec technologie Windows Tablet and Touch et, sur des ordinateurs équipés d’écrans tactiles, même le doigt d’un utilisateur.

> [!NOTE]
> Les instructions relatives à l' [accessibilité](inter-accessibility.md), au [stylet](inter-pen.md)et à l' [effleurement](inter-touch.md) sont présentées dans des articles distincts.

Le déplacement physique de la souris déplace le pointeur graphique (également appelé curseur) à l’écran. Le pointeur a plusieurs formes pour indiquer son comportement actuel.

![capture d’écran de cinq pointeurs de souris classiques ](images/inter-mouse-image1.png)

*Pointeurs de souris classiques*

Les périphériques de souris ont souvent un bouton principal (généralement le bouton gauche), un bouton secondaire (généralement le droit) et une roulette de souris entre les deux. En positionnant le pointeur et en cliquant sur les boutons principal et secondaire de la souris, les utilisateurs peuvent sélectionner des objets et effectuer des actions sur ceux-ci. Pour la plupart des interactions, le fait d’appuyer sur un bouton de la souris lorsque le curseur se trouve sur une cible indique la cible sélectionnée et la libération du bouton effectue toute action associée à la cible.

Tous les pointeurs, à l’exception du pointeur Busy, ont une zone réactive de pixel unique qui définit l’emplacement exact de l’écran de la souris. La zone réactive détermine l’objet affecté par les actions de la souris. Les objets définissent une zone réactive, qui est la zone dans laquelle la zone réactive est considérée sur l’objet. En règle générale, la zone d’échange coïncide avec les bordures d’un objet, mais elle peut être plus grande pour faciliter l’exécution de l’utilisateur.

Le signe insertion est la barre verticale clignotante qui s’affiche lorsque l’utilisateur tape dans une zone de texte ou un autre éditeur de texte. le signe insertion est indépendant du pointeur (par défaut, Windows masque le pointeur pendant que l’utilisateur tape).

![capture d’écran de la zone de texte avec le curseur ](images/inter-mouse-image2.png)

*Le signe insertion*

## <a name="design-concepts"></a>Principes de conception

### <a name="the-mouse-is-intuitive"></a>La souris est intuitive

La souris est un appareil d’entrée réussi, car il est facile à utiliser pour une main humaine classique. L’interaction basée sur un pointeur a réussi, car elle est intuitive et permet un large éventail d’expériences.

**Les objets d’interface utilisateur (IU) bien conçus sont dits d’offre, qui sont des propriétés visuelles et comportementales d’un objet qui suggère la manière dont il est utilisé.** Le pointeur agit comme un proxy pour la main, ce qui permet aux utilisateurs d’interagir avec les objets d’écran de la même manière qu’avec des objets physiques. Nous avons une compréhension approfondie de la façon dont la main humaine fonctionne, donc si un événement similaire à celui-ci peut être envoyé, nous essayons de l’envoyer. s’il semble que vous puissiez le saisir, nous essayons de le récupérer. Par conséquent, les utilisateurs peuvent déterminer comment utiliser les objets avec un fort niveau de rentabilité simplement en les examinant et en les essayant.

![capture d’écran d’un bouton et d’un curseur](images/inter-mouse-image3.png)

*Les boutons et les curseurs ont une grande rentabilité*

En revanche, les objets avec un faible niveau de rentabilité sont plus difficiles à deviner. Ces objets requièrent souvent une étiquette ou une instruction pour les expliquer.

![capture d’écran du texte du lien et de l’icône de la terre Internet](images/inter-mouse-image4.png)

*le texte du lien et les icônes ont une rentabilité médiocre*

### <a name="some-aspects-of-mouse-use-are-not-intuitive"></a>Certains aspects de l’utilisation de la souris ne sont pas intuitifs

Le fait de cliquer **avec le bouton droit, de double-cliquer et de cliquer avec les modificateurs touche Maj ou CTRL est trois interactions de la souris qui ne sont pas intuitives**, car elles n’ont pas d’équivalents réalistes. Contrairement aux raccourcis clavier et aux touches d’accès, ces interactions de souris ne sont généralement pas documentées n’importe où dans l’interface utilisateur. Cela suggère que les modificateurs de clic droit, de double-clic et de clavier ne doivent pas être nécessaires pour effectuer des tâches de base, en particulier par les utilisateurs débutants. Elle suggère également que ces interactions avancées doivent avoir un comportement cohérent et prévisible à utiliser efficacement.

### <a name="single-click-or-double-click"></a>Un simple clic ou un double-clic ?

le Double-clic est donc utilisé de manière intensive sur le bureau Windows qu’il est possible qu’il ne semble pas être une interaction avancée. par exemple, l’ouverture de dossiers, programmes ou documents dans le volet fichier de Windows Explorer est effectuée en double-cliquant sur. l’ouverture d’un raccourci sur le bureau Windows utilise également un double-clic. en revanche, l’ouverture de dossiers ou de programmes dans le menu Démarrer nécessite un simple clic.

Les objets sélectionnables utilisent un simple clic pour effectuer la sélection. ils nécessitent donc un double-clic pour ouvrir, tandis que les objets non sélectionnables requièrent un seul clic pour s’ouvrir. Cette distinction n’est pas comprise par de nombreux utilisateurs (le fait de cliquer sur une icône de programme est de cliquer sur une icône de programme) et, par conséquent, certains utilisateurs continuent de cliquer sur les icônes jusqu’à ce qu’ils obtiennent ce qu’ils souhaitent.

### <a name="direct-manipulation"></a>Manipulation directe

L’interaction directe avec les objets est appelée manipulation directe. Le pointage, le clic, la sélection, le déplacement, le redimensionnement, le fractionnement, le défilement, le panoramique et le zoom sont des manipulations directes courantes. En revanche, l’interaction avec un objet par le biais de sa fenêtre Propriétés ou d’une autre boîte de dialogue peut être décrite comme manipulation indirecte.

**Toutefois, en cas de manipulation directe, il peut y avoir une manipulation accidentelle et, par conséquent, la nécessité de le faire.** L’effacement est la possibilité d’inverser ou de corriger facilement une action indésirable. Vous créez des manipulations directes indulgent avec en fournissant une annulation, en donnant de bons commentaires visuels et en permettant aux utilisateurs de corriger facilement les erreurs. L’Association d’une annulation permet d’éviter que des actions indésirables ne se produisent en premier lieu, ce que vous pouvez faire en utilisant des contrôles et des confirmations restreints pour des actions ou des commandes risquées qui ont des conséquences inattendues.

### <a name="standard-mouse-button-interactions"></a>Interactions du bouton de la souris standard

Les interactions de la souris standard dépendent de divers facteurs, notamment la touche de la souris sur laquelle l’utilisateur clique, le nombre de clics effectués, sa position pendant les clics et si des modificateurs de clavier ont été activés. Voici un résumé de la façon dont ces facteurs affectent généralement l’interaction :

- Pour la plupart des objets, le double-clic gauche effectue un seul clic gauche et exécute la commande par défaut. La commande par défaut est identifiée dans le menu contextuel.
- Pour certains types d’objets sélectionnables, chaque clic augmente l’effet du clic. Par exemple, un simple clic dans une zone de texte définit l’emplacement d’entrée, le double-clic sélectionne un mot et le triple-clic sélectionne une phrase ou un paragraphe.
- Cliquez avec le bouton droit pour afficher le menu contextuel d’un objet.
- Maintenir la souris toujours en pointant les résultats dans le pointage.
- Le maintien de la souris tout en appuyant sur les boutons de la souris indique un clic et une sélection d’objet unique. Le déplacement de la souris indique le déplacement, le redimensionnement, le fractionnement, le glissement et la sélection de plusieurs objets.
- La touche Maj étend la sélection de façon contiguë.
- La touche Ctrl étend la sélection en basculant l’état de sélection de l’élément cliqué sans affecter la sélection des autres objets.

### <a name="simple-mouse-interactions"></a>Interactions simples avec la souris

Le tableau suivant décrit les interactions et les effets courants de la souris.

| Action simple | Interaction | Effet classique |
|:---|:---|:---|
| Point<br/>          | Placez le pointeur sur un objet spécifique sans cliquer sur aucun bouton de la souris.<br/>                                                                                                                                                                                                                                      | Target affiche son état de survol et tout intuitivité dynamique.<br/>                                                                                                                                                                                                                                                                                                                                                         |
| Pointant<br/>          | Placez le pointeur sur un objet spécifique sans cliquer sur les boutons de la souris et sans vous déplacer pendant au moins une seconde.<br/>                                                                                                                                                                                             | Target affiche son info-bulle, son info-bulle ou son équivalent.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| Activant<br/>          | Placez le pointeur sur un objet spécifique et non sélectionnable, puis appuyez sur le bouton de la souris et relâchez-le sans le déplacer. Cliquer sur prend effet à la sortie du bouton de la souris pour permettre aux utilisateurs d’annuler le clic en déplaçant la souris en dehors de la cible. Par conséquent, la touche souris indique uniquement la cible sélectionnée.<br/> | Pour les clics simples avec le bouton principal, activez l’objet. Pour les double-clics avec le bouton principal, activez l’objet et exécutez la commande par défaut. Pour le bouton secondaire, affichez le menu contextuel de l’objet.<br/>                                                                                                                                                                                         |
| Sélectionnez<br/>         | Placez le pointeur sur un objet spécifique et sélectionnable, puis appuyez sur le bouton de la souris et relâchez-le.<br/>                                                                                                                                                                                                                        | Pour les clics simples avec le bouton principal, sélectionnez l’objet. Si les utilisateurs glissent la souris, sélectionnez une plage contiguë d’objets. Pour les double-clics avec le bouton principal, sélectionnez l’objet et exécutez la commande par défaut.<br/> Pour le texte, le bouton principal droit cliquez sur définit le point d’insertion, le second sélectionne Word au niveau du point d’insertion et le troisième clic sélectionne la phrase ou le paragraphe.<br/> |
| Appuyant sur<br/>          | Placez le pointeur sur un objet spécifique et appuyez sur un bouton de la souris sans le libérer.<br/>                                                                                                                                                                                                                              | Pour les fonctions de répétition automatique (par exemple, en appuyant sur une flèche de défilement pour faire défiler continuellement), activez plusieurs fois. Sinon, indique le début d’un déplacement, d’un redimensionnement, d’un fractionnement ou d’un glissement, sauf s’il est suivi d’une mise en sortie sans déplacement.<br/>                                                                                                                                                                                               |
| Roue<br/>          | Déplacer la roulette de la souris.<br/>                                                                                                                                                                                                                                                                                                  | La fenêtre défile verticalement en direction du mouvement de la roulette de la souris.<br/>                                                                                                                                                                                                                                                                                                                                                      |

### <a name="pointer-shapes"></a>Formes de pointeur

Le tableau suivant décrit les formes et les utilisations courantes des pointeurs.

| Graphique à base de formes | Nom | Quand l’utiliser |
|:---|:---|:---|
| ![capture d’écran d’un pointeur avec une forme de flèche ](images/inter-mouse-image5.png)<br/>           | Sélection normale<br/>    | Utilisé pour la plupart des objets.<br/>                                             |
| ![capture d’écran de main avec point d’index pointant vers le doigt ](images/inter-mouse-image6.png)<br/>    | Sélectionner un lien<br/>      | Utilisé pour les liens textuels et graphiques en raison de leur faible rentabilité.<br/> |
| ![capture d’écran du pointeur avec la forme i-Beam ](images/inter-mouse-image7.png)<br/>          | Sélection de texte<br/>      | Utilisé pour le texte pour indiquer un emplacement entre les caractères.<br/>           |
| ![capture d’écran d’un pointeur avec une grande forme de signe plus ](images/inter-mouse-image8.png)<br/> | Précision, sélectionner<br/> | Utilisé pour les interactions graphiques et autres interactions à deux dimensions.<br/>            |

### <a name="compound-mouse-interactions"></a>Interactions de souris composées

Le tableau suivant décrit les interactions courantes de la souris.

| Action composée | Interaction | Effet classique | Pointeurs |
|:---|:---|:---|:---|
| Déplacement<br/>                | Si le déplacement est un mode (entré en donnant une commande), entrez le mode, placez le pointeur sur un objet mobile, appuyez sur le bouton et déplacez la souris, relâchez le bouton de la souris. dans ce cas, le pointeur change Shape pour indiquer le mode.<br/> Sinon, placez le pointeur sur la accroche d’un objet mobile, appuyez sur le bouton et déplacez la souris, puis cliquez sur le bouton de la souris. dans ce cas, le pointeur n’a pas besoin de modifier la forme.<br/> | l’objet se déplace dans le sens du mouvement du pointeur.<br/>            | déplacer<br/> ![capture d’écran d’un pointeur avec quatre flèches ](images/inter-mouse-image9.png)<br/> utilisé pour déplacer une fenêtre dans n’importe quelle direction.<br/> panoramique<br/> ![capture d’écran d’un pointeur avec une forme main ](images/inter-mouse-image10.png)<br/> Utilisé pour déplacer un objet dans une fenêtre dans n’importe quelle direction.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Redimensionnement<br/>              | Placez le pointeur sur une bordure redimensionnable ou une poignée de redimensionnement, appuyez sur un bouton de la souris et déplacez la souris, puis relâchez le bouton de la souris.<br/>                                                                                                                                                                                                                                                                                 | le redimensionnement de l’objet dans le sens du mouvement du pointeur.<br/>          | redimensionnement vertical et horizontal<br/> ![Capture d’écran montrant des pointeurs vers le haut.](images/inter-mouse-image11.png)![capture d’écran des pointeurs vers le haut et vers la gauche ](images/inter-mouse-image12.png)<br/> utilisé pour redimensionner une seule dimension.<br/> Redimensionnement diagonal<br/> ![bb545459. mouse13 (en-US, MSDN. 10) .png](images/inter-mouse-image13.png)![capture d’écran des pointeurs en diagonale avec des flèches](images/inter-mouse-image14.png)<br/> utilisé pour redimensionner deux dimensions simultanément.<br/> redimensionnement des lignes et des colonnes<br/> ![bb545459. mouse15 (en-US, MSDN. 10) .png](images/inter-mouse-image15.png)![capture d’écran des pointeurs de flèche avec la barre ](images/inter-mouse-image16.png)<br/> Utilisé pour redimensionner une ligne ou une colonne dans une grille.<br/> |
| Fractionnement<br/>             | Placez le pointeur sur un séparateur, appuyez sur un bouton de la souris et déplacez la souris, puis relâchez le bouton de la souris.<br/>                                                                                                                                                                                                                                                                                                          | la bordure du volet de fractionnement se déplace dans le sens du mouvement du pointeur.<br/> | séparateurs de fenêtres<br/> ![bb545459. mouse17 (en-US, MSDN. 10) .png](images/inter-mouse-image17.png)![capture d’écran des pointeurs de flèche avec double-croix ](images/inter-mouse-image18.png)<br/> Utilisé pour redimensionner un volet fractionné verticalement ou horizontalement.<br/> |
| déplaçant des données avec la méthode glisser-déposer.<br/> | Placez le pointeur sur un objet valide pour le faire glisser, appuyez sur un bouton de la souris et déplacez la souris sur une cible de déplacement, puis relâchez le bouton de la souris.<br/> | l’objet est déplacé ou copié vers la cible de déplacement.<br/>             | sélection normale<br/> ![capture d’écran de la photo, du pointeur standard et de l’info-bulle ](images/inter-mouse-image19.png)<br/> utilisé sur des cibles de glissement valides. peut également avoir une info-bulle pour indiquer un effet spécifique.<br/> non disponible<br/> ![capture d’écran de la petite icône bloquée/hors connexion ](images/inter-mouse-image20.png)<br/> Permet d’indiquer qu’une surface n’est pas une cible de dépôt valide.<br/> |

### <a name="activity-indicators"></a>Indicateurs d’activité

Le tableau suivant montre les pointeurs que les utilisateurs voient lorsqu’ils effectuent une action qui prend plus de quelques secondes.

| Graphique à base de formes | Nom | Quand l’utiliser |
|:---|:---|:---|
| ![Capture d’écran montrant un pointeur « occupé » en forme d’anneau.](images/inter-mouse-image21.png)<br/>          | Pointeur occupé<br/>                  | Utilisé pour attendre qu’une fenêtre devienne réactive.<br/>                                  |
| ![capture d’écran d’un pointeur et d’une flèche en forme d’anneau](images/inter-mouse-image22.png)<br/> | Utilisation du pointeur d’arrière-plan<br/> | Utilisé pour pointer, cliquer, appuyer ou sélectionner pendant qu’une tâche se termine en arrière-plan.<br/> |

### <a name="hand-pointers"></a>Pointeurs de main

Les liens Text et Graphics utilisent un pointeur main ou « Link Select » (une main avec l’index pointant vers le doigt) ![capture d’écran de main avec point d’index pointant vers le doigt ](images/inter-mouse-image6.png)) en raison de leur faible rentabilité. Alors que les liens peuvent avoir d’autres indices visuels pour indiquer qu’il s’agit de liens (tels que les traits de soulignement et le placement spécial), l’affichage du pointeur en forme de main sur Hover est l’indication définitive d’un lien.

**Pour éviter toute confusion, il est impératif de ne pas utiliser le pointeur main à d’autres fins.** Par exemple, les boutons de commande ont déjà un haut niveau de rentabilité, donc ils n’ont pas besoin d’un pointeur main. Le pointeur main doit signifier « cette cible est un lien » et rien d’autre.

### <a name="custom-pointers"></a>Pointeurs personnalisés

Windows prend en charge la création de pointeurs personnalisés. Pour plus d’informations, consultez [définition de l’image de curseur](../learnwin32/setting-the-cursor-image.md) et [entrée utilisateur : exemple étendu](../learnwin32/user-input--extended-example.md).

De nombreuses applications fournissent une palette de contrôles avec des pointeurs personnalisés pour prendre en charge les fonctionnalités de l’application.

![capture d’écran de la palette avec un pointeur de pulvérisation ](images/inter-mouse-image23.png)

*Microsoft Paint comprend une palette de fonctions différentes, chacune avec un pointeur unique*

### <a name="fitts-law"></a>Loi de Fitts

La Loi de Fitts est un principe bien connu dans l’ergonomie de la conception d’interface utilisateur graphique qui indique essentiellement :

- Plus une cible est éloignée, plus il faut de temps pour l’acquérir avec la souris.
- Plus une cible est petite, plus il faut de temps pour l’acquérir avec la souris.

Par conséquent, les cibles volumineuses sont correctes. Veillez à rendre l’ensemble de la zone cible cliquable.

| Incorrect. | Correct (la cible entière est cliquable) |
|:---|:---|
| ![capture d’écran de l’icône avec un clic sur l’étiquette uniquement ](images/inter-mouse-image24.png) | ![capture d’écran de l’icône cliquable et de l’étiquette cliquable ](images/inter-mouse-image25.png) |

Vous pouvez modifier dynamiquement la taille d’une cible en pointant pour la rendre plus facile à acquérir.

![capture d’écran de la carte de caractères avec un nombre agrandi ](images/inter-mouse-image26.png)

*Une cible devient plus grande lorsque l’utilisateur pointe pour faciliter son acquisition*

Et les cibles de fermeture sont également correctes. Recherchez les éléments intervisibles proches de l’emplacement où ils vont probablement être utilisés. Dans l’image suivante, la palette de couleurs est trop éloignée du sélecteur d’outils.

![capture d’écran de la palette de couleurs séparée des outils ](images/inter-mouse-image27.png)

*La palette de couleurs est trop éloignée de l’endroit où elle est susceptible d’être utilisée*

Considérez le fait que l’emplacement du pointeur actuel de l’utilisateur est aussi proche qu’une cible peut être, ce qui le rend facile à acquérir. Ainsi, les menus contextuels tirent pleinement parti de la Loi de Fitts, tout comme les mini-barres d’outils utilisées par Microsoft Office.

![capture d’écran des pointeurs près de la liste déroulante ](images/inter-mouse-image28.png)

*L’emplacement du pointeur actuel est toujours le plus facile à acquérir*

Envisagez également d’autres périphériques d’entrée lors de la détermination de la taille des objets. Par exemple, la taille de cible minimale recommandée pour Touch est 23x23 pixels (13x13).

### <a name="environments-without-a-mouse"></a>Environnements sans souris

tous les environnements Windows ne disposent pas d’une souris. Par exemple, les bornes disposent rarement d’une souris et ont généralement un écran tactile à la place. Cela signifie que les utilisateurs peuvent effectuer des interactions simples, telles qu’un clic gauche et peut-être glisser-déplacer. Toutefois, ils ne peuvent pas pointer, cliquer avec le bouton droit ou double-cliquer. Cette situation est facile à concevoir pour, car ces limitations sont généralement connues à l’avance.

L’utilisation d’une souris nécessite des compétences de moteur précises et, par conséquent, tous les utilisateurs ne peuvent pas utiliser de souris. Pour rendre votre logiciel accessible au plus grand nombre d’audiences, assurez-vous que toutes les interactions pour lesquelles des compétences de moteur fine ne sont pas essentielles peuvent être effectuées à l’aide du clavier.

Pour plus d’informations et des instructions, consultez [accessibilité](inter-accessibility.md).

**Si vous ne faites que quatre choses...**

1.  Donnez des comportements d’interaction de la souris à leurs effets standard, en utilisant les pointeurs standard chaque fois que nécessaire.
2.  Limitez les interactions avancées de la souris (celles nécessitant des clics droits, des clics multiples ou des touches de modification) aux tâches avancées destinées aux utilisateurs expérimentés.
3.  Affectez des comportements prévisibles et cohérents pour les interactions de souris avancées afin qu’elles puissent être utilisées efficacement.
4.  Assurez-vous que votre programme offre la possibilité d’inverser ou de corriger des actions indésirables, en particulier pour les commandes destructrices. Les actions accidentelles sont plus probables lors de l’utilisation de la manipulation directe.

## <a name="guidelines"></a>Consignes

### <a name="click-affordance"></a>Cliquer sur le prix de l’offre

- **Ne demandez jamais aux utilisateurs de cliquer sur un objet pour déterminer s’il est cliquable.** Les utilisateurs doivent être en mesure de déterminer la possibilité de clic par le biais de l’inspection visuelle seule.
  - L’interface utilisateur principale (comme les boutons de validation) doit avoir une offre de clic statique. Les utilisateurs ne doivent pas avoir à POINTER pour découvrir l’interface utilisateur principale.
  - L’interface utilisateur secondaire (par exemple, les commandes secondaires ou les contrôles de divulgation progressive) peut afficher sa possibilité de clic au pointage.
  - Les [liens de texte](ctrl-links.md) doivent suggérer statiquement du texte de lien, puis afficher leur caractère de clic (souligné ou autre modification de présentation, à l’aide d’un pointeur en forme de [main](#hand-pointers)) au pointage.
  - Les [liens graphiques](ctrl-links.md) affichent uniquement un pointeur vers la main au pointage.
- **Utilisez le pointeur main (ou « Link Select ») uniquement pour les liens textuels et de texte.** Dans le cas contraire, les utilisateurs doivent cliquer sur les objets pour déterminer s’ils sont des liens.

### <a name="standard-mouse-button-interactions"></a>Interactions du bouton de la souris standard

Le tableau suivant récapitule les interactions de bouton de la souris qui s’appliquent dans la plupart des cas :



| Interaction                                    | Résultat                                                                                                                                                                                                                                                          |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pointage<br/>                    | Target affiche son info-bulle, son info-bulle ou son équivalent.<br/>                                                                                                                                                                                           |
| Clic simple à gauche<br/>        | Active ou sélectionne l’objet. Pour le texte, définit le point d’insertion.<br/>                                                                                                                                                                           |
| Clic simple avec le bouton droit<br/>       | Sélectionne l’objet et affiche son menu contextuel.<br/>                                                                                                                                                                                              |
| Double-cliquez sur<br/>        | Active ou sélectionne l’objet et exécute la commande par défaut. Pour Text, sélectionne Word au niveau du point d’insertion (un troisième clic sélectionne la phrase ou le paragraphe).<br/>                                                                            |
| Double-clic avec le bouton droit<br/>       | Identique au simple clic droit.<br/>                                                                                                                                                                                                                    |
| Shift simple-clic gauche<br/>  | Pour les objets sélectionnables, étend la sélection de manière contiguë. Sinon, même comme un clic unique avec les modifications possibles. par exemple, dans Paint, le dessin d’un ovale avec le modificateur de touche maj entraîne le dessin d’un cercle.<br/>                  |
| Shift simple-clic avec le bouton droit<br/> | Identique au décalage simple d’un clic gauche.<br/>                                                                                                                                                                                                               |
| Maj double-clic gauche<br/>  | Identique au décalage simple d’un clic gauche et exécute la commande par défaut sur l’ensemble de la sélection.<br/>                                                                                                                                                     |
| Maj double clic droit<br/> | Identique au décalage simple d’un clic gauche.<br/>                                                                                                                                                                                                               |
| Ctrl simple-clic gauche<br/>   | Pour les objets sélectionnables, étend la sélection en faisant basculer l’état de sélection de l’élément sur lequel vous avez cliqué sans affecter la sélection d’autres objets (permettant ainsi une sélection qui n’est pas contiguë). Sinon, identique à un clic unique.<br/> |
| Ctrl simple clic droit<br/>  | Identique à Ctrl simple clic gauche.<br/>                                                                                                                                                                                                                |
| Ctrl double clic gauche<br/>   | Identique à l’option Ctrl simple-clic gauche et exécute la commande par défaut sur l’ensemble de la sélection.<br/>                                                                                                                                                      |
| Ctrl double clic droit<br/>  | Identique à Ctrl simple clic gauche.<br/>                                                                                                                                                                                                                |



 

### <a name="mouse-interaction"></a>Interaction avec la souris

- **Faites en sorte que le clic cible au moins 16x16 pixels afin de pouvoir cliquer facilement sur n’importe quel appareil d’entrée.** Pour les [fonctions tactiles](inter-touch.md), la taille de contrôle minimale recommandée est de 23x23 pixels (13x13). Envisagez de modifier dynamiquement la taille des petites cibles lorsque l’utilisateur pointe pour les rendre plus faciles à acquérir.

    Dans cet exemple, les boutons de contrôle spin sont trop petits pour être utilisés efficacement avec Touch ou un stylet.

    ![capture d’écran du contrôle spin avec de petites flèches ](images/inter-mouse-image29.png) 

- **Effectuez des fractionnements d’au moins cinq pixels de largeur pour qu’ils puissent cliquer facilement sur n’importe quel appareil d’entrée.** Envisagez de modifier dynamiquement la taille des petites cibles lorsque l’utilisateur pointe pour les rendre plus faciles à acquérir.

    dans cet exemple, le séparateur dans le volet de navigation Windows Explorer est trop étroit pour être utilisé efficacement avec une souris ou un stylet.

    ![capture d’écran d’un séparateur étroit et presque invisible ](images/inter-mouse-image30.png)

- **Fournissez aux utilisateurs une marge d’erreur spatiale.** Autoriser le déplacement de la souris (par exemple, trois pixels) lorsque les utilisateurs relâchent le bouton de la souris. Parfois, les utilisateurs déplacent légèrement la souris lorsqu’ils relâchent le bouton de la souris, de sorte que la position de la souris juste avant la version du bouton reflète mieux l’intention de l’utilisateur que la position juste après.
- **Fournir aux utilisateurs une marge d’erreur temporelle.** Utilisez la vitesse du double-clic système pour faire la distinction entre les double-clics.
- **Les clics prennent effet lorsque le bouton de la souris est enfoncé.** Autorisez les utilisateurs à abandonner les actions de la souris en supprimant la souris des cibles valides avant de relâcher le bouton de la souris. Pour la plupart des interactions de la souris, l’utilisation d’un bouton de la souris indique uniquement la cible sélectionnée et le relâchement du bouton active l’action. Les fonctions de répétition automatique (par exemple, en appuyant sur une flèche de défilement pour faire défiler continuellement) sont une exception.
- [Capturer la souris](/windows/win32/api/winuser/nf-winuser-setcapture) pour sélectionner, déplacer, redimensionner, fractionner et faire glisser.
- Utilisez la touche ÉCHAP pour permettre aux utilisateurs d’abandonner les interactions composées avec la souris, telles que le déplacement, le redimensionnement, le fractionnement et le glissement.
- **Si un objet ne prend pas en charge les doubles clics, mais que les utilisateurs sont susceptibles de supposer qu’il le fait, interprétez un « double-clic » comme un seul clic.** Supposons que l’utilisateur ait prévu une action unique au lieu de deux.

    Étant donné que les utilisateurs sont susceptibles de supposer que les boutons de la barre des tâches prennent en charge les doubles clics, un double-clic doit être traité comme un simple clic.

    ![capture d’écran du bouton de la barre des tâches et du pointeur standard ](images/inter-mouse-image31.png)

- **Ignorer les clics de souris redondants lorsque votre programme est inactif.** Par exemple, si l’utilisateur clique sur un bouton 10 fois alors qu’un programme est inactif, interprétez-le comme un simple clic.
- **N’utilisez pas de doubles ou de cordes.** Un double-glissement est une action de glissement commencée par un double-clic, et une corde est lorsque plusieurs boutons de la souris sont appuyés simultanément. Ces interactions ne sont pas standard, ne sont pas détectables, sont difficiles à exécuter et sont probablement effectuées par inadvertance.
- **N’utilisez pas Alt comme modificateur pour les interactions de la souris.** La touche Alt est réservée à l’accès à la barre d’outils et aux touches d’accès.
- **N’utilisez pas Maj + Ctrl comme modificateur pour les interactions de la souris.** Cela serait trop difficile à utiliser.
- **Rendez le point de suspension redondant.** Pour rendre votre programme touchable, tirez pleinement parti du pointage, mais uniquement de la manière dont il n’est pas nécessaire d’effectuer une action. Cela signifie généralement qu’une action peut également être effectuée en cliquant, mais pas nécessairement exactement de la même façon. Le survol n’est pas pris en charge par la plupart des technologies tactiles, de sorte que les utilisateurs avec des écrans tactiles ne peuvent effectuer aucune tâche nécessitant un pointage.

### <a name="mouse-wheel"></a>Roulette de la souris

- **Faites en sorte que la roulette de la souris affecte le contrôle, le volet ou la fenêtre sur lequel le pointeur est actuellement.** Cela permet d’éviter les résultats inattendus.
- **Rendez la roulette de la souris prise en compte sans cliquer ou avoir le focus d’entrée.** Le pointage est suffisant.
- **Faites en sorte que la roulette de la souris affecte l’objet avec l’étendue la plus spécifique.** Par exemple, si le pointeur se trouve sur un contrôle de zone de liste déroulante dans un volet défilant dans une fenêtre déroulante, la roulette de la souris affecte le contrôle de zone de liste.
- **Ne modifiez pas le focus d’entrée lorsque vous utilisez la roulette de la souris.**
- Donnez les effets suivants à la roulette de la souris :
  - Pour les fenêtres, les volets et les contrôles défilant :
    - **La rotation de la roulette de la souris permet de faire défiler verticalement l’objet vers le haut.** Pour que la roulette ait un mappage naturel, la rotation de la roulette de la souris ne doit jamais faire défiler horizontalement, car elle est désorientée et inattendue.
      - **Si la touche CTRL est enfoncée, la rotation** de la roulette de la souris permet de faire un zoom avant et de faire pivoter vers le haut.
      - **L’inclinaison de la roulette de la souris fait défiler l’objet horizontalement.**
  - Pour les fenêtres et les volets zoomables (sans barres de défilement) :
    - **La rotation de la Roulette** de la souris permet de faire un zoom avant et de faire pivoter vers le haut.
    - L’inclinaison de la roulette de la souris n’a aucun effet.
  - Pour les onglets :
    - La **rotation de la roulette de la souris peut modifier l’onglet actuel,** quelle que soit l’orientation des onglets.
    - L’inclinaison de la roulette de la souris n’a aucun effet.
  - Si les touches Maj et Alt sont enfoncées, la roulette de la souris n’a aucun effet.
- **utilisez les paramètres système Windows pour la taille de défilement vertical (pour la rotation) et la taille de défilement horizontal (pour l’inclinaison).** Ces paramètres sont configurables par le biais de l’élément du panneau de configuration de la souris.
- **Faites pivoter la roulette de la souris plus rapidement pour accélérer le défilement.** Cela permet aux utilisateurs de faire défiler les documents volumineux de manière plus efficace.
- **Pour les fenêtres défilantes, envisagez de cliquer sur le bouton roulette de la souris pour mettre la fenêtre en « mode lecteur ».** Le mode lecteur plante une icône d’origine de défilement spéciale et fait défiler la fenêtre dans une direction et une vitesse par rapport à l’origine du défilement.

![capture d’écran de la page avec l’icône d’origine de défilement ](images/inter-mouse-image32.png)

*Internet Explorer prend en charge le mode lecteur, qui comporte l’icône d’origine du défilement.*

### <a name="hiding-the-pointer"></a>Masquage du pointeur

- **Ne masquez pas le pointeur.** Exceptions :
  - Les applications de présentation s’exécutant en mode de présentation plein écran peuvent masquer le pointeur. Toutefois, le pointeur doit être restauré immédiatement lorsque les utilisateurs déplacent la souris et peut être remasqué après deux secondes d’inactivité.
  - Les environnements sans souris (tels que les bornes) peuvent masquer définitivement le pointeur.
- par défaut, Windows masque le pointeur pendant que l’utilisateur tape dans une zone de texte. ce paramètre système Windows peut être configuré à l’aide de l’élément du panneau de configuration de la souris.

### <a name="activity-pointers"></a>Pointeurs d’activité

les pointeurs d’activité dans Windows sont le pointeur occupé (![capture d’écran d’un pointeur en forme d’anneau ](images/inter-mouse-image33.png)) et le pointeur de travail en arrière-plan (![capture d’écran d’un pointeur et d’une flèche en forme d’anneau ](images/inter-mouse-image34.png)).

- Affichez le pointeur occupé lorsque les utilisateurs doivent attendre plus d’une seconde pour qu’une action se termine. Notez que le pointeur occupé n’a pas de zone réactive, afin que les utilisateurs ne puissent rien cliquer pendant qu’il est affiché.
- Afficher le pointeur de travail en arrière-plan lorsque les utilisateurs doivent attendre plus d’une seconde pour qu’une action se termine, mais que le programme est réactif et qu’il n’y a pas d’autre commentaire visuel indiquant que l’action n’est pas terminée.
- Ne combinez pas les pointeurs d’activité avec des barres de progression ou des animations de progression.

### <a name="caret"></a>Signe insertion

- **N’affiche pas le signe insertion tant que la fenêtre ou le contrôle d’entrée de texte n’a pas le focus d’entrée.** Le signe insertion suggère le focus d’entrée pour les utilisateurs, mais une fenêtre ou un contrôle peut afficher le signe insertion sans le focus d’entrée. Bien entendu, ne dérobez pas le focus d’entrée pour qu’une boîte de dialogue hors contexte puisse afficher le signe insertion.

    le gestionnaire d’informations d’identification Windows est affiché hors contexte avec le signe insertion mais sans le focus d’entrée. Par conséquent, les utilisateurs finissent par taper leur mot de passe dans des emplacements inattendus.

    ![capture d’écran du gestionnaire d’informations d’identification sans le focus ](images/inter-mouse-image35.png)

- **Placez le signe insertion à l’endroit où les utilisateurs sont le plus susceptibles de taper en premier.** En général, il s’agit du dernier emplacement que l’utilisateur a tapé ou à la fin du texte.

### <a name="accessibility"></a>Accessibilité

- Pour les utilisateurs qui ne peuvent pas utiliser la souris du tout, rendez la souris redondante avec le clavier.
  - Les utilisateurs doivent être en mesure d’effectuer toutes les opérations à l’aide du clavier qu’ils peuvent utiliser avec la souris, à l’exception des actions pour lesquelles des compétences de moteur précises sont essentielles, telles que le dessin et la diffusion de jeux.
  - Les utilisateurs doivent pouvoir tout faire avec la souris qu’ils peuvent utiliser avec le clavier, à l’exception de la saisie de texte efficace.
- Pour les utilisateurs disposant d’une capacité limitée à utiliser la souris :
  - N’effectuez pas de double-clic et en faisant glisser le seul moyen d’effectuer une action.

Pour plus d’informations et des instructions, consultez [accessibilité](inter-accessibility.md).

## <a name="documentation"></a>Documentation

Quand vous faites référence à la souris :

- Évitez d’utiliser la plupart des souris ; Si vous devez faire référence à plusieurs souris, utilisez les souris.
- Utilisez le bouton de la souris pour indiquer le bouton gauche de la souris. N’utilisez pas le bouton principal de la souris. De même, utilisez le bouton droit de la souris au lieu du bouton secondaire de la souris. Quelle que soit la précision, les utilisateurs comprennent les termes et les utilisateurs qui reprogramment les boutons qui font le changement mental.
- Utilisez Wheel pour la partie en rotation de la roulette de la souris et le bouton roulette pour faire référence à la partie cliquable.
- Utilisez des verbes tels que Click, point et Drag pour faire référence aux actions de la souris. Les utilisateurs font pivoter la molette verticalement, l’incliner horizontalement et cliquent sur le bouton roulette.
- Utilisez l’opération glisser-déplacer pour déplacer un document ou un dossier. Il est acceptable d’utiliser le glisser-déplacer comme un adjectif, comme dans « le déplacement du dossier est une opération de glisser-déplacer ».
- Coupez toujours le double-clic et cliquez avec le bouton droit en tant que verbes.
- Cliquez sur, et non sur. Cliquez sur in (comme dans « cliquez dans la fenêtre ») est acceptable.

Lorsque vous faites référence aux pointeurs de souris :

- Reportez-vous au pointeur de la souris comme pointeur. Utilisez curseur uniquement dans la documentation technique.
- Pour les pointeurs avec des indicateurs d’activité, utilisez un pointeur occupé pour le pointeur qui se compose uniquement d’un indicateur d’activité, et qui fonctionne dans le pointeur d’arrière-plan pour le pointeur de combinaison et l’indicateur d’activité.
- Pour les autres types de pointeurs, n’utilisez pas d’étiquettes descriptives pour faire référence au pointeur. Si nécessaire, utilisez un graphique pour décrire comment le pointeur de la souris peut s’afficher à l’écran.

**Exemples :**

- Pointez sur la bordure de la fenêtre.
- À l’aide de la souris, cliquez sur le bouton **réduire** .
- Maintenez la touche Maj enfoncée et cliquez sur le bouton droit de la souris.
- Lorsque le pointeur devient ![capture d’écran de la flèche avec deux croix](images/inter-mouse-image18.png), faites glisser le pointeur pour déplacer la ligne de fractionnement.

## <a name="see-also"></a>Voir aussi

- [Instructions relatives à l’interaction d’accessibilité](inter-accessibility.md)
- [Instructions tactiles d’interaction](inter-touch.md)
- [Instructions relatives à l’interaction avec le stylet](inter-pen.md)
- [Liens de texte](ctrl-links.md)
- [Liens graphiques](ctrl-links.md)
- [Capturer la souris](/windows/win32/api/winuser/nf-winuser-setcapture)
- [Définition de l’image de curseur](../learnwin32/setting-the-cursor-image.md)
- [Entrée utilisateur : exemple étendu](../learnwin32/user-input--extended-example.md)