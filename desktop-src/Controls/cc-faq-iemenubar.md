---
title: Procédure de création d’une barre de menus Explorer-Style Internet
description: À première vue, la barre de menus dans Microsoft Internet Explorer 5 et versions ultérieures ressemble à un menu standard. Toutefois, il semble très différent lorsque vous commencez à l’utiliser.
ms.assetid: e0fe25f2-3d49-4c5a-a3f9-2f468f2cfef2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b262bc55407d263c97d4bd7e3938a9794d3a58f5
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842773"
---
# <a name="how-to-create-an-internet-explorer-style-menu-bar"></a>Procédure de création d’une barre de menus Explorer-Style Internet

À première vue, la barre de menus dans Microsoft Internet Explorer 5 et versions ultérieures ressemble à un menu standard. Toutefois, il semble très différent lorsque vous commencez à l’utiliser.

La capture d’écran suivante montre la barre de menus de Windows Internet Explorer avec le menu Outils sélectionné.

![capture d’écran qui affiche la barre de menus de Windows Internet Explorer, avec le menu Outils sélectionné](images/howto8.jpg)

La barre de menus est en fait un contrôle de barre d’outils qui ressemble à un menu standard. Au lieu d’éléments de menu de niveau supérieur, une barre de menus contient une série de boutons de texte uniquement qui affichent un menu déroulant lorsque l’utilisateur clique dessus. Toutefois, en tant que type spécialisé de barre d’outils, une barre de menus présente certaines fonctionnalités dont les menus standard sont absents :

-   Il peut être personnalisé à l’aide de techniques de barre d’outils standard, ce qui permet à l’utilisateur de déplacer, supprimer ou ajouter des éléments.
-   Il peut avoir un suivi à chaud, afin que les utilisateurs sachent quand ils se trouvent sur un élément de niveau supérieur sans devoir le cliquer au préalable.

Une barre de menus peut être incorporée dans un contrôle rebar, en lui donnant les fonctionnalités suivantes :

-   Il peut avoir une pince, qui permet à l’utilisateur de déplacer ou de redimensionner la bande.
-   Elle peut partager une bande dans le contrôle rebar avec d’autres bandes, telles que la barre d’outils standard de l’illustration précédente.
-   Il peut afficher un chevron lorsqu’il est couvert par une bande adjacente, ce qui permet à l’utilisateur d’accéder aux éléments masqués.
-   Il peut avoir une image bitmap d’arrière-plan définie par l’application.

Cette rubrique explique comment implémenter une barre de menus. Comme une barre de menus est une implémentation spécialisée d’un contrôle ToolBar, le focus sera sur les rubriques spécifiques aux barres de menus. Pour plus d’informations sur l’incorporation d’une barre d’outils dans un contrôle rebar, consultez [How to Create an Internet Explorer-Style Toolbar](cc-faq-ietoolbar.md) et [about Rebar Controls](rebar-controls.md).

-   [Création d’une barre d’outils dans une barre de menus](#making-a-toolbar-into-a-menu-bar)
-   [Gestion de la navigation avec le menu Hot-Tracking désactivé](#handling-navigation-with-menu-hot-tracking-disabled)
    -   [Navigation de la souris](#mouse-navigation)
    -   [Navigation au clavier](#keyboard-navigation)
    -   [Navigation mixte](#mixed-navigation)
-   [Gestion de la navigation avec le Hot-Tracking de menu activé](#handling-navigation-with-menu-hot-tracking-enabled)
    -   [Traitement des messages pour le suivi chaud du menu](#message-processing-for-menu-hot-tracking)
    -   [Navigation de la souris](#mouse-navigation)
    -   [Navigation au clavier](#keyboard-navigation)

## <a name="making-a-toolbar-into-a-menu-bar"></a>Création d’une barre d’outils dans une barre de menus

Pour créer une barre d’outils dans une barre de menus :

-   Créez une barre d’outils plate en incluant [**TBSTYLE \_ Flat**](toolbar-control-and-button-styles.md) avec les autres indicateurs de style de fenêtre. Le **style \_ plat TBSTYLE** active également le suivi à chaud. Avec ce style, la barre de menus ressemble à un menu standard jusqu’à ce que l’utilisateur active un bouton. Ensuite, le bouton apparaît pour s’afficher dans la barre d’outils et appuyez sur la touche enfoncé, tout comme un bouton standard. Étant donné que le suivi à chaud est activé, tout ce qui est nécessaire pour activer un bouton est que le curseur pointe dessus. Si le curseur se déplace vers un autre bouton, il est activé et l’ancien bouton est désactivé.
-   Créer des boutons de style liste en incluant la [**\_ liste TBSTYLE**](toolbar-control-and-button-styles.md) avec les autres indicateurs de style de fenêtre. Ce style crée un bouton plus fin qui ressemble plus à un élément de menu de niveau supérieur standard.
-   Définissez le texte des boutons uniquement en définissant le membre **iBitmap** de la structure [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) du bouton sur I \_ IMAGENONE et le membre **iString** sur le texte du bouton.
-   Donnez à chaque bouton le style de [**\_ liste déroulante BTNS**](toolbar-control-and-button-styles.md) . Lorsque vous cliquez sur le bouton, le contrôle ToolBar envoie à votre application une notification de [ \_ liste déroulante TBN](tbn-dropdown.md) pour lui demander d’afficher le menu du bouton.
-   Incorporez la barre de menus dans une bande rebar. Activez les pinceaux et les chevrons, comme indiqué dans [la rubrique How to Create an Internet Explorer-Style Toolbar](cc-faq-ietoolbar.md).
-   Implémentez un gestionnaire de [ \_ liste déroulante TBN](tbn-dropdown.md) pour afficher le *menu* déroulant du bouton lorsque l’utilisateur clique dessus. Le menu déroulant est un type de menu contextuel. Elle est créée à l’aide de la fonction [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) , dont l’angle supérieur gauche est aligné avec l’angle inférieur gauche du bouton.
-   Implémentez la navigation au clavier, afin que la barre de menus soit entièrement accessible sans souris.
-   Implémenter le suivi à chaud du menu. Avec les menus standard, une fois qu’un menu d’élément de menu de niveau supérieur a été affiché, le déplacement du curseur sur un autre élément de niveau supérieur affiche automatiquement son menu et réduit le menu de l’élément précédent. Le contrôle ToolBar effectue un suivi à chaud du curseur et modifie l’image du bouton, mais il affiche automatiquement le nouveau menu. Votre application doit le faire explicitement.

La plupart de ces éléments sont faciles à implémenter et sont abordés ailleurs. Consultez Guide pratique [pour créer une barre d’outils Internet Explorer-Style](cc-faq-ietoolbar.md), [à propos des contrôles ToolBar](toolbar-controls-overview.md)ou [à propos des contrôles Rebar](rebar-controls.md) pour obtenir une présentation générale de l’utilisation des barres d’outils et des contrôles Rebar. Pour plus d’informations sur la gestion des menus contextuels, consultez [menus](/windows/desktop/menurc/menus) . Les deux derniers éléments, la navigation au clavier et le suivi des menus à chaud, sont décrits dans le reste de cette rubrique.

## <a name="handling-navigation-with-menu-hot-tracking-disabled"></a>Gestion de la navigation avec le menu Hot-Tracking désactivé

Les utilisateurs peuvent choisir de naviguer dans la barre de menus avec la souris, le clavier ou une combinaison des deux. Pour implémenter la navigation dans la barre de menus, votre application doit gérer les notifications de barre d’outils et surveiller la souris et le clavier. Cette tâche peut être divisée en deux parties distinctes : avec et sans suivi chaud du menu. Cette section explique comment gérer la navigation quand aucun menu n’est affiché et que le suivi des menus à chaud n’est pas activé.

### <a name="mouse-navigation"></a>Navigation de la souris

Si le suivi à chaud du menu est désactivé, vous pouvez traiter une barre de menus comme une barre d’outils normale. Si l’utilisateur navigue avec une souris, toute votre application doit effectuer la notification de la [ \_ liste déroulante TBN](tbn-dropdown.md) . Quand cette notification est reçue, affichez le menu déroulant approprié et activez le suivi à chaud du menu. À partir de là, vous êtes dans le menu du régime de suivi à chaud abordé dans [gestion de la navigation avec le menu Hot-Tracking activé](#handling-navigation-with-menu-hot-tracking-enabled).

Comme indiqué dans la [navigation mixte](#mixed-navigation), vous devez également gérer la [notification \_ HOTITEMCHANGE TBN](tbn-hotitemchange.md) pour effectuer le suivi du bouton actif. Cette notification n’est pas pertinente si l’utilisateur navigue uniquement avec la souris, mais elle est nécessaire lorsque la souris et la navigation au clavier sont mélangées.

### <a name="keyboard-navigation"></a>Navigation au clavier

Comme indiqué dans la section précédente, l’utilisateur peut effectuer un certain nombre d’opérations de navigation à l’aide du clavier lorsque le suivi actif du menu est désactivé. Les contrôles ToolBar prennent uniquement en charge la navigation au clavier s’ils ont le focus. Ils ne gèrent pas non plus toutes les touches d’appui nécessaires pour les barres de menus. La solution la plus simple pour gérer la navigation au clavier consiste à traiter explicitement les événements d’appui sur les touches appropriées.

Si le suivi à chaud du menu est désactivé, votre application doit gérer ces événements de pression de touche de la façon suivante :

-   Touche F10. Activez le premier bouton avec [**to \_ SETHOTITEM**](tb-sethotitem.md).
-   Touches de direction gauche et droite. Activez le bouton adjacent avec [**to \_ SETHOTITEM**](tb-sethotitem.md). Si l’utilisateur tente de naviguer à l’extrémité de la barre de menus, activez le premier bouton à l’extrémité opposée.
-   Touche ÉCHAP. Désactivez le bouton actif avec [**to \_ SETHOTITEM**](tb-sethotitem.md). La barre de menus doit être retournée à l’État qu’elle avait avant l’activation du premier bouton.
-   Touche d’accès rapide de *touche* Alt. Utilisez le message [**to \_ MAPACCELERATOR**](tb-mapaccelerator.md) pour déterminer le bouton auquel le caractère *clé* correspond. Affichez le menu déroulant du bouton et activez le suivi à chaud du menu.
-   Touche Bas. Si un bouton est actif mais qu’aucun menu n’a été affiché, affichez le menu du bouton et activez le suivi à chaud du menu.
-   Touche Entrée. Désactivez le bouton actif avec [**to \_ SETHOTITEM**](tb-sethotitem.md). La barre de menus doit être retournée à l’État qu’elle avait avant l’activation du premier bouton.

### <a name="mixed-navigation"></a>Navigation mixte

Les gestionnaires de navigation au clavier décrits dans la section précédente effectuent essentiellement deux tâches : suivre le bouton actif et afficher le menu approprié lorsqu’un bouton est sélectionné. Ces gestionnaires sont suffisants tant que l’utilisateur navigue uniquement avec le clavier. Toutefois, les utilisateurs combinent souvent la navigation au clavier et à la souris. Par exemple, ils peuvent activer le premier bouton avec la touche F10, utiliser la souris pour activer un autre bouton, puis ouvrir son menu avec la touche de direction bas. Si vous analysez uniquement les Appuyez sur les touches pour suivre la clé active, vous affichez le mauvais menu. Vous devez également gérer la [notification \_ HOTITEMCHANGE TBN](tbn-hotitemchange.md) pour suivre avec précision le bouton actif.

## <a name="handling-navigation-with-menu-hot-tracking-enabled"></a>Gestion de la navigation avec le Hot-Tracking de menu activé

Lorsque le suivi des menus à chaud est activé, votre application doit modifier la façon dont elle répond à la navigation de l’utilisateur. Pour répliquer le comportement des menus standard, vous devez implémenter les fonctionnalités suivantes explicitement.

Avec la navigation de la souris :

-   Si l’utilisateur déplace le curseur sur un autre bouton, ce menu s’affiche immédiatement et le menu précédent disparaît.
-   Le suivi à chaud du menu reste actif jusqu’à ce que l’utilisateur sélectionne une commande ou clique sur un point qui ne fait pas partie de la zone de menu. L’une des actions désactive le suivi à chaud du menu jusqu’à ce que vous cliquiez sur un autre bouton.
-   Si le curseur est déplacé en dehors du menu, le menu déroulant actuel reste jusqu’à ce que le curseur repasse sur, ou lorsque l’utilisateur clique sur un point extérieur, la zone couverte par le menu. Si le curseur retourne à un autre bouton que celui actuellement affiché, l’ancien menu est réduit et le nouveau menu s’affiche.

Avec la navigation à l’aide du clavier :

-   La touche de direction droite déplace le focus vers la droite. Si l’élément a un sous-menu, affichez le sous-menu. Si l’élément n’a pas de sous-menu, réduisez le menu et tous les sous-menus, activez le bouton suivant avec [**to \_ SETHOTITEM**](tb-sethotitem.md)et affichez le menu du bouton adjacent. Si le dernier bouton est actif lors de la réception de ce message, affichez le menu du premier bouton.
-   La touche de direction gauche déplace le focus vers la gauche. Si l’élément est un sous-menu, réduisez-le et déplacez le focus vers son menu parent. Si l’élément n’est pas un sous-menu, réduisez le menu, activez le bouton suivant avec [**to \_ SETHOTITEM**](tb-sethotitem.md)et affichez le menu du bouton.

<!-- -->

-   La touche Échap rétablit l’affichage d’une étape.
    -   Si un sous-menu est affiché, il est réduit et le focus se déplace vers le menu parent.
    -   Si le menu d’un bouton est affiché, il est réduit et le suivi à chaud du menu est désactivé. Le bouton de l’élément reste actif.
    -   Si aucun menu n’est affiché, mais qu’un bouton est actif, le bouton est désactivé et le suivi de menu actif est désactivé.
-   Les touches de direction haut et bas permettent uniquement de naviguer dans un menu particulier.
-   La touche entrée lance la commande associée à un élément de menu. Si l’élément de menu a un sous-menu, la touche entrée l’affiche.

Comme avec le cas où le suivi des menus est désactivé, votre application doit être en mesure de gérer la souris, le clavier et la navigation mixte. Toutefois, le fait qu’un menu s’affiche signifie que la messagerie doit être traitée un peu différemment.

### <a name="message-processing-for-menu-hot-tracking"></a>Traitement des messages pour les Hot-Tracking de menu

Le suivi à chaud du menu requiert qu’un menu s’affiche en permanence, à l’exception du bref intervalle requis pour basculer vers un nouveau menu. Toutefois, le menu déroulant qui s’affiche par [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) est modal. Votre application continuera à recevoir des messages directement, y compris les messages de [**\_ commande WM**](/windows/desktop/menurc/wm-command), [TBN \_ HOTITEMCHANGE](tbn-hotitemchange.md)et normal, tels que [**WM \_ MENUSELECT**](/windows/desktop/menurc/wm-menuselect). Toutefois, il ne recevra pas directement les messages de clavier ou de souris de bas niveau. Pour gérer les messages tels que [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove), vous devez définir un raccordement de message pour intercepter les messages qui sont dirigés vers le menu.

Quand un menu déroulant s’affiche, définissez le hook de message en appelant la fonction [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa) avec le paramètre *IDHOOK* défini sur WH \_ msgfilter. Tous les messages destinés au menu seront transmis à votre [procédure de raccordement](/previous-versions/windows/desktop/legacy/ms644987(v=vs.85)). Par exemple, le fragment de code suivant définit un hook de message qui intercepte les messages qui vont dans un menu déroulant. `MsgHook` nom de la procédure de raccordement et `hhookMsg` est le handle de la procédure.


```
hhookMsg = SetWindowsHookEx(WH_MSGFILTER, MsgHook, HINST_THISDLL, 0);
```



Les messages de menu sont identifiés en définissant le paramètre *nCode* de la procédure de hook sur le \_ menu MSGF. Le paramètre *lParam* pointera vers une structure [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) avec le message. Les détails des messages qui doivent être gérés, et comment, sont décrits dans le reste de cette rubrique.

Votre application doit transmettre tous les messages au hook de message suivant en appelant la fonction [**CallNextHookEx**](/windows/desktop/api/winuser/nf-winuser-callnexthookex) . Vous devez également envoyer des messages de souris directement au contrôle ToolBar, en veillant à convertir toutes les coordonnées de point dans l’espace de coordonnées client de la barre d’outils. L’envoi des messages permet de s’assurer que le contrôle de barre d’outils reçoit les messages de souris appropriés. Par exemple, la barre d’outils doit recevoir les messages de la [**\_ souris WM**](/windows/desktop/inputdev/wm-mousemove) pour effectuer un suivi à chaud de ses boutons.

Quand un nouveau bouton est activé, votre application doit réduire l’ancien menu déroulant avec un message [**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) et afficher un nouveau menu. Il doit également réduire le menu déroulant lorsque le focus est effectué à partir de la barre de menus avec la navigation au clavier ou en cliquant à l’extérieur de la zone de menu. Chaque fois que vous réduisez un menu, vous devez libérer son hook de message à l’aide de la fonction [**UnhookWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-unhookwindowshookex) . Si vous avez besoin d’afficher un autre menu déroulant, créez un nouveau hook de message. Quand une commande est lancée, le menu est réduit automatiquement, mais vous devez libérer explicitement le hook de message.

L’exemple de code suivant libère le hook de message qui a été défini dans l’exemple précédent.


```
UnhookWindowsHookEx(hhookMsg);
```



### <a name="mouse-navigation"></a>Navigation de la souris

Lorsqu’un contrôle de barre d’outils normal effectue le suivi des boutons à chaud, il met en surbrillance le bouton actif et envoie une notification [TBN \_ HOTITEMCHANGE](tbn-hotitemchange.md) à l’application chaque fois qu’un nouveau bouton est activé. Votre application est chargée d’afficher le menu déroulant approprié. Elle doit :

-   Gérez la [notification \_ HOTITEMCHANGE TBN](tbn-hotitemchange.md) pour effectuer le suivi du bouton actif. Lorsque le bouton actif change, réduisez l’ancien menu et créez-en un nouveau.
-   Gérez la notification de [ \_ liste déroulante TBN](tbn-dropdown.md) qui est envoyée lorsque l’utilisateur clique sur un bouton. Il doit ensuite réduire le menu et désactiver le suivi à chaud du menu. Le bouton reste actif.
-   Gérez les messages [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown), [**WM \_ RBUTTONDOWN**](/windows/desktop/inputdev/wm-rbuttondown)et [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) dans votre procédure de raccordement de message, afin d’assurer le suivi de la position de la souris. Si l’utilisateur clique sur le bouton de la souris en dehors de la zone de menu, réduisez le menu déroulant actuel, désactivez le suivi à chaud du menu et replacez la barre de menus à son état de préactivation.
-   Quand une commande de menu est lancée, désactiver le suivi à chaud du menu. Le menu est réduit automatiquement, mais vous devez libérer explicitement le hook de message.

Vous devez également gérer la messagerie liée au menu, telle que le message [**WM \_ INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) envoyé lorsqu’un élément de menu doit afficher un sous-menu. Pour plus d’informations sur la gestion de ces messages, consultez [menus](/windows/desktop/menurc/menus).

### <a name="keyboard-navigation"></a>Navigation au clavier

Votre application doit traiter les messages de clavier dans la procédure de hook de message et agir sur ceux qui affectent le suivi chaud du menu. Les pressions sur les touches suivantes doivent être gérées :

-   Touche ÉCHAP. La touche Échap rétablit l’affichage d’un niveau. Si un sous-menu est affiché, il doit être réduit. Si le menu principal d’un bouton s’affiche, réduisez-le et désactivez le suivi à chaud du menu. Le bouton reste actif.
-   Touche Droite. Si l’élément a un sous-menu, affichez-le. Si l’élément n’a pas de sous-menu, réduisez le menu et tous les sous-menus, activez le bouton suivant avec [**to \_ SETHOTITEM**](tb-sethotitem.md)et Affichez son menu. Si le dernier bouton était actif au moment de la réception de cette notification, affichez le menu du premier bouton.
-   Touche Gauche. Si l’élément se trouve dans un sous-menu, réduisez-le et déplacez le focus vers son menu parent. Si l’élément n’est pas un sous-menu, réduisez le menu, activez le bouton adjacent avec [**to \_ SETHOTITEM**](tb-sethotitem.md)et Affichez son menu. Si le premier bouton était actif au moment de la réception de cette notification, affichez le menu du dernier bouton.
-   Les flèches haut et bas. Ces clés sont utilisées pour naviguer dans un menu, mais n’affectent pas directement le suivi à chaud du menu.
-   Touche d’accès rapide de *touche* Alt. Utilisez le message [**to \_ MAPACCELERATOR**](tb-mapaccelerator.md) pour déterminer le bouton auquel le caractère *clé* correspond. Si elle correspond à un autre bouton que celui actuellement actif, réduisez le menu déroulant actuel, activez le nouveau bouton avec [**to \_ SETHOTITEM**](tb-sethotitem.md)et affichez le menu du bouton adjacent. Si le *caractère clé* correspond au bouton actuellement affiché, réduisez le menu déroulant et désactivez le suivi à chaud du menu. Le bouton doit rester actif.

 

 