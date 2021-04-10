---
title: Procédure de création d’une barre d’outils Explorer-Style Internet
description: La barre d’outils est l’une des fonctionnalités clés de l’interface utilisateur de Windows Internet Explorer. Il permet non seulement aux utilisateurs d’accéder à une grande variété de fonctionnalités, mais également aux utilisateurs de personnaliser leur disposition en fonction de leurs préférences personnelles.
ms.assetid: d24969ec-4dea-44c6-b045-5611de8f1cce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d32228f941a7c7e1253884ab5d72368f66f25c7f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102428"
---
# <a name="how-to-create-an-internet-explorer-style-toolbar"></a>Procédure de création d’une barre d’outils Explorer-Style Internet

La barre d’outils est l’une des fonctionnalités clés de l’interface utilisateur de Windows Internet Explorer. Il permet non seulement aux utilisateurs d’accéder à une grande variété de fonctionnalités, mais également aux utilisateurs de personnaliser leur disposition en fonction de leurs préférences personnelles.

La capture d’écran suivante montre la barre d’outils d’Internet Explorer et met en évidence certaines des fonctionnalités clés.

![capture d’écran de la barre d’outils Windows Internet Explorer, avec des étiquettes pour huit fonctionnalités](images/howto1a.jpg)

Cette barre d’outils se compose essentiellement d’un contrôle rebar avec quatre bandes : trois barres d’outils et une barre de menus. Comme elle est implémentée avec l’API de contrôles communs, les développeurs peuvent créer des barres d’outils avec tout ou partie de ses fonctionnalités. Cette rubrique décrit les fonctionnalités essentielles de la barre d’outils d’Internet Explorer et comment les implémenter dans votre application.

-   [Contrôle rebar](#the-rebar-control)
    -   [Implémentation du contrôle rebar](#implementing-the-rebar-control)
-   [Les barres d’outils](#how-to-create-an-internet-explorer-style-toolbar)
    -   [Boutons déroulants](#drop-down-buttons)
    -   [Boutons de style liste](#list-style-buttons)
    -   [Chevrons](#handling-chevrons)
    -   [Suivi à chaud](#hot-tracking)
-   [Rubriques connexes](#related-topics)

## <a name="the-rebar-control"></a>Contrôle rebar

La structure sous-jacente de la barre d’outils d’Internet Explorer est fournie par un [contrôle rebar](rebar-controls.md). Ce contrôle permet aux utilisateurs de personnaliser la disposition d’une collection d’outils. Chaque Rebar contient une ou plusieurs *bandes*, qui sont généralement des rectangles étroits longs qui contiennent une fenêtre enfant, généralement un contrôle ToolBar.

Le contrôle rebar affiche ses bandes dans une zone rectangulaire, en général en haut de la fenêtre. Ce rectangle est subdivisé en une ou plusieurs bandes qui correspondent à la hauteur d’une bande. Chaque bande peut se trouver sur une bande distincte, ou plusieurs bandes peuvent être placées sur la même bande.

Un contrôle rebar offre aux utilisateurs deux moyens de réorganiser leurs outils :

-   Chaque bande possède généralement une *pince* sur son bord gauche. Les pinceaux sont utilisés lorsque deux ou plusieurs bandes sur une seule bande dépassent la largeur de la fenêtre. En faisant glisser la pince vers la gauche ou la droite, les utilisateurs peuvent contrôler la quantité d’espace allouée à chaque bande.
-   Les utilisateurs peuvent déplacer les bandes dans le rectangle d’affichage du Rebar en les faisant glisser. Le contrôle rebar change ensuite l’affichage pour s’adapter à la nouvelle disposition des bandes. Si toutes les bandes sont retirées d’une bande, la hauteur du Rebar sera réduite, ce qui augmentera la zone d’affichage.

Une application peut ajouter ou supprimer des bandes en fonction des besoins. En règle générale, les applications permettent aux utilisateurs de sélectionner les bandes qu’ils souhaitent afficher via le menu Affichage ou un menu contextuel.

Si la largeur combinée des bandes sur une bande dépasse la largeur de la fenêtre, le contrôle rebar ajuste leur largeur en fonction des besoins. Certains des outils peuvent être couverts par la bande adjacente.

La [Version 5,80](common-control-versions.md) des contrôles communs offre un moyen de rendre les outils couverts par une autre bande accessible à l’utilisateur. Si vous définissez l' \_ indicateur RBBS USECHEVRON dans le membre **fStyle** de la structure [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) de la bande, un *Chevron* s’affiche pour les barres d’outils qui ont été couvertes. Lorsqu’un utilisateur clique sur le Chevron, un menu s’affiche pour lui permettre d’utiliser les outils cachés. La capture d’écran suivante de Microsoft Internet Explorer 6 affiche le menu qui s’affiche lorsqu’une partie de la barre d’outils standard est couverte.

![capture d’écran qui montre le menu affiché en cliquant sur le Chevron](images/howto2.jpg)

Étant donné que chaque bande contient un contrôle, vous pouvez fournir une flexibilité supplémentaire par le biais de l’API du contrôle. Par exemple, vous pouvez implémenter la personnalisation de la barre d’outils pour permettre à l’utilisateur d’ajouter, de déplacer ou de supprimer des boutons sur une barre d’outils.

### <a name="implementing-the-rebar-control"></a>Implémentation du contrôle rebar

La plupart des fonctionnalités de la barre d’outils Internet Explorer sont réellement implémentées dans les bandes individuelles. L’implémentation du contrôle rebar lui-même est simple et est indiquée ci-dessous.

1.  Créez le contrôle rebar avec [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Définissez *dwExStyle* sur [**WS \_ ex \_ TOOLWINDOW**](/windows/desktop/winmsg/extended-window-styles) et *lpClassName* sur [**REBARCLASSNAME**](common-control-window-classes.md). Internet Explorer utilise les styles de fenêtre suivants :

    -   [**\_BANDBORDERS RBS**](rebar-control-styles.md)
    -   [**\_DBLCLKTOGGLE RBS**](rebar-control-styles.md)
    -   [**\_REGISTERDROP RBS**](rebar-control-styles.md)
    -   [**\_VARHEIGHT RBS**](rebar-control-styles.md)
    -   [**CCS \_ diviseur**](common-control-styles.md)
    -   [**CCS \_ NOPARENTALIGN**](common-control-styles.md)
    -   [**\_bordure WS**](/windows/desktop/winmsg/window-styles)
    -   [**\_enfant WS**](/windows/desktop/winmsg/window-styles)
    -   [**\_CLIPCHILDREN WS**](/windows/desktop/winmsg/window-styles)
    -   [**\_CLIPSIBLINGS WS**](/windows/desktop/winmsg/window-styles)
    -   [**WS \_ visible**](/windows/desktop/winmsg/window-styles)

    Définissez les autres paramètres en fonction de votre application.

2.  Créez un contrôle avec [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou une fonction de création de contrôle spécialisée telle que [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex).
3.  Initialisez une bande pour le contrôle en remplissant les membres de [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa). Incluez le \_ style RBBS USECHEVRON avec le membre **fStyle** pour activer les chevrons.
4.  Ajoutez la bande au contrôle rebar avec un message [**RB \_ INSERTBAND**](rb-insertband.md) .
5.  Répétez les étapes 2-4 pour les bandes restantes.
6.  Implémentez des gestionnaires pour les notifications Rebar. En particulier, vous devez gérer [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) pour afficher un menu déroulant lorsque l’utilisateur clique sur un chevron. Pour plus d’informations, consultez [gestion des chevrons](#handling-chevrons).

Les pinces sont incluses par défaut. Pour omettre la pince d’une bande, définissez l' \_ indicateur NOHENSION RBBS dans le membre **fStyle** de la structure [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) de la bande. Pour plus d’informations sur l’implémentation des contrôles rebar, consultez [à propos des contrôles Rebar](rebar-controls.md).

### <a name="handling-chevrons"></a>Gestion des chevrons

Lorsqu’un utilisateur clique sur un chevron, le contrôle rebar envoie une notification [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) à votre application. La structure [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) transmise avec la notification contient l’identificateur de la bande et une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) avec le rectangle occupé par le Chevron. Votre gestionnaire doit déterminer les boutons qui sont masqués et afficher les commandes associées dans un menu contextuel.

La procédure suivante décrit comment gérer une notification [ \_ CHEVRONPUSHED RBN](rbn-chevronpushed.md) :

1.  Récupérez le rectangle englobant actuel pour la bande sélectionnée en envoyant le contrôle rebar à un message [**RB \_ GETRECT**](rb-getrect.md) .
2.  Récupérez le nombre total de boutons en envoyant la barre d’outils du contrôle de la bande à un message [**\_ BUTTONCOUNT to**](tb-buttoncount.md) .
3.  En commençant par le bouton le plus à gauche, récupérez le rectangle englobant du bouton en envoyant au contrôle de barre d’outils un message [**\_ GETITEMRECT to**](tb-getitemrect.md) .
4.  Transmettez les rectangles de la bande et du bouton à la fonction [**IntersectRect**](/windows/desktop/api/winuser/nf-winuser-intersectrect) . Cette fonction retourne une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui correspond à la partie visible du bouton.
5.  Transmettez le rectangle du bouton et le rectangle de la partie visible du bouton à la fonction [**EqualRect**](/windows/desktop/api/winuser/nf-winuser-equalrect) .
6.  Si [**EqualRect**](/windows/desktop/api/winuser/nf-winuser-equalrect) retourne la **valeur true**, le bouton entier est visible. Répétez les étapes 3-5 pour le bouton suivant dans la barre d’outils. Si **EqualRect** retourne la **valeur false**, le bouton est au moins partiellement masqué et tous les autres boutons sont complètement masqués. Passez à l’étape suivante.
7.  Créez un menu contextuel contenant les éléments de chaque bouton masqué.
8.  Affichez le menu contextuel à l’aide de la fonction [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) . Utilisez le rectangle à chevrons qui a été transmis avec la notification [ \_ CHEVRONPUSHED RBN](rbn-chevronpushed.md) pour positionner le menu. Le menu doit être immédiatement sous le Chevron, avec les bords gauches alignés.
9.  Gérer les commandes de menu.

## <a name="the-toolbars"></a>Les barres d’outils

La majeure partie de la complexité de la barre d’outils d’Internet Explorer réside dans l’implémentation des contrôles qui composent les bandes rebar. Internet Explorer affiche généralement quatre bandes :

-   Barre de menus
-   Barre d’outils standard
-   Barre d’outils liens
-   Barre d’outils adresse

Toutes ces bandes, y compris la barre de menus, comportent en fait des contrôles ToolBar. Cette section décrit l’implémentation des barres d’outils standard et links. La barre de menus est un peu plus compliquée et est décrite séparément dans Guide pratique [pour créer une barre de menus Explorer-Style Internet](cc-faq-iemenubar.md).

Les procédures de base pour l’implémentation des contrôles ToolBar sont décrites dans [à propos des contrôles ToolBar](toolbar-controls-overview.md). Cette section se concentre sur certaines des nouvelles fonctionnalités de la barre d’outils utilisées par Internet Explorer pour améliorer la convivialité du contrôle.

-   [Boutons déroulants](#drop-down-buttons)
-   [Boutons de style liste](#list-style-buttons)
-   [Chevrons](#handling-chevrons)
-   [Suivi à chaud](#hot-tracking)

### <a name="drop-down-buttons"></a>Boutons déroulants

Les boutons déroulants prennent en charge plusieurs commandes. Quand l’utilisateur clique sur un bouton déroulant, le bouton affiche un menu contextuel au lieu de lancer une commande. L’utilisateur lance une commande en la sélectionnant dans le menu. La capture d’écran suivante montre un bouton et un menu déroulants à partir de la barre d’outils standard d’Internet Explorer.

![capture d’écran montrant le menu déroulant courrier](images/howto3.jpg)

La fonctionnalité de liste déroulante peut être ajoutée à n’importe quel style de bouton en ajoutant un indicateur de style au membre **fStyle** de la structure [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) du bouton. Il existe trois styles de bouton déroulant, tous utilisés par Internet Explorer :

-   Les boutons déroulants bruts ont le style de [**\_ liste déroulante BTNS**](toolbar-control-and-button-styles.md) . Ils ressemblent à des boutons normaux, mais ils affichent un menu lorsque vous cliquez dessus au lieu de lancer une commande.
-   Les boutons fléchés déroulants simples ont le style [**BTNS \_ WHOLEDROPDOWN**](toolbar-control-and-button-styles.md) . Elles ont une flèche affichée en regard de l’image ou du texte du bouton. À part la différence de l’apparence, elles sont identiques aux boutons déroulants bruts. Le bouton courrier utilisé comme exemple dans l’illustration précédente est un bouton de flèche déroulante.
-   Les boutons de liste déroulante qui ajoutent le style étendu [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) à la [**\_ liste déroulante BTNS**](toolbar-control-and-button-styles.md) comportent une flèche séparée du texte ou de l’image. Ce style de bouton combine les fonctionnalités des boutons déroulants et standard. Si l’utilisateur clique sur la flèche, un menu s’affiche et l’utilisateur peut choisir parmi plusieurs commandes. Si l’utilisateur clique sur le bouton adjacent, il lance une commande par défaut. La capture d’écran suivante montre le bouton **précédent** d’Internet Explorer, qui utilise une flèche séparée.

    ![capture d’écran qui montre le menu du bouton de fractionnement précédent](images/howto4.jpg)

Quand l’utilisateur clique sur un bouton déroulant avec les styles de flèche simple ou simple, le contrôle de barre d’outils envoie une notification de [ \_ liste déroulante TBN](tbn-dropdown.md) à votre application. Lorsque votre application reçoit ce message, elle est responsable de la création et de l’affichage du menu, ainsi que de la gestion de la commande sélectionnée.

Quand l’utilisateur clique sur une flèche séparée, le contrôle de barre d’outils envoie une notification de [ \_ liste déroulante TBN](tbn-dropdown.md) à votre application. Votre application doit la gérer de la même façon qu’elle gère les deux autres types de boutons déroulants. Si l’utilisateur clique sur le bouton principal, votre application reçoit un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) avec l’ID de commande du bouton, comme s’il s’agissait d’un bouton standard. Les applications répondent généralement en lançant la commande top dans le menu déroulant, mais vous êtes libre de répondre de manière appropriée.

### <a name="list-style-buttons"></a>Boutons List-Style

Avec les boutons standard, si vous ajoutez du texte, il est affiché sous l’image bitmap. La capture d’écran suivante montre les boutons **recherche** et **favoris** d’Internet Explorer avec un texte de bouton standard.

![capture d’écran montrant la barre d’outils Rechercher et favoris avec des boutons standard](images/howto6.jpg)

Microsoft Internet Explorer 5 et versions ultérieures utilisent le style de [**\_ liste TBSTYLE**](toolbar-control-and-button-styles.md) . Le texte se trouve à droite de l’image bitmap, ce qui réduit la hauteur du bouton et l’agrandissement de la zone d’affichage. L’illustration suivante montre les boutons de **recherche** et de **favoris** d’Internet Explorer 6 avec le style de **\_ liste TBSTYLE** .

![capture d’écran montrant la barre d’outils Rechercher et favoris à l’aide des boutons de style liste](images/howto5.jpg)

### <a name="chevrons"></a>Chevrons

Lorsque l’utilisateur réorganise les bandes dans le contrôle rebar, une partie d’une barre d’outils peut être couverte. Si la bande a été créée avec le \_ style RBBS USECHEVRON, le contrôle rebar affiche un chevron sur le bord droit de la barre d’outils. L’utilisateur clique sur le Chevron pour afficher un menu avec les outils masqués.

### <a name="hot-tracking"></a>Hot-Tracking

Lorsque le suivi à chaud est activé, un bouton devient *actif* lorsque le curseur se trouve sur celui-ci. Le bouton chaud se distingue normalement des autres boutons de la barre d’outils par une image distincte. Par défaut, un bouton actif semble être déclenché au-dessus du reste de la barre d’outils. Quand un nouveau bouton devient actif, votre application reçoit une notification [TBN \_ HOTITEMCHANGE](tbn-hotitemchange.md) . L’illustration suivante montre les boutons **recherche** et **favoris** d’Internet Explorer 5, avec un bouton de **recherche** à chaud. En plus d’avoir une apparence en relief, la bitmap grise du bouton a été remplacée par une image en couleur.

![capture d’écran montrant les boutons Rechercher et favoris, avec un bouton de recherche à chaud](images/howto7.jpg)

Pour activer le suivi à chaud, créez un contrôle de barre d’outils avec le style de [**\_ liste**](toolbar-control-and-button-styles.md) [**TBSTYLE \_ plat**](toolbar-control-and-button-styles.md) ou TBSTYLE. Celles-ci sont appelées barres d’outils *plates* , car les boutons individuels ne sont généralement pas mis en surbrillance de quelque manière que ce soit. Les bitmaps sont simplement affichées les unes à côté des autres. Ils prennent une apparence de type bouton uniquement lorsqu’ils sont à chaud. Ces deux styles sont également transparents, ce qui signifie que l’arrière-plan des icônes sera la couleur de la fenêtre du client sous-jacent.

Pour afficher une autre bitmap lorsque le bouton est actif, créez une deuxième [liste d’images](image-lists.md) qui contient des images réactives pour tous les boutons de la barre d’outils. La taille et l’ordre de ces images doivent être les mêmes que dans la liste d’images par défaut. Envoyer le contrôle de barre d’outils à un message [**\_ SETHOTIMAGELIST to**](tb-sethotimagelist.md) pour définir la liste d’images réactives.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Procédure de création d’une barre de menus Explorer-Style Internet](cc-faq-iemenubar.md)
</dt> </dl>

 

 