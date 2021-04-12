---
title: À propos des menus
description: Cette rubrique traite des menus.
ms.assetid: fd0b26f1-93cd-421b-9097-8502ab7681e9
keywords:
- ressources, menus
- menus, à propos de
- sous-menus
- barres de menus
- menus de niveau supérieur
- menus contextuels
- menus déroulants
- menus, niveau supérieur
- menus, fenêtres contextuelles
- menus, liste déroulante
- noms de menu
- menus, raccourci
- menus, fenêtre
- menus, système
- menus, contrôle
- menus contextuels
- Menu Fenêtre
- Menu système
- Menu de contrôle
- identificateurs d’aide
- poignées de menu
- éléments de menu
- éléments de commande
- identificateurs d’élément de menu
- position de l’élément de menu
- sélection d’éléments de menu
- effacement des éléments de menu
- menus owner-drawn
- menus, owner-drawn
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed5d42eb42aaaaa16eef0b5b118adcfe0f91156e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381852"
---
# <a name="about-menus"></a>À propos des menus

Un *menu* est une liste d’éléments qui spécifient des options ou des groupes d’options (un sous-menu) pour une application. Le fait de cliquer sur un élément de menu ouvre un sous-menu ou provoque l’exécution d’une commande par l’application. Cette section fournit des informations sur les rubriques suivantes :

-   [Menus et barres de menus](#menu-bars-and-menus)
    -   [Menus contextuels](#shortcut-menus)
    -   [Menu fenêtre](#the-window-menu)
    -   [Identificateur d’aide](#help-identifier)
-   [Accès au clavier à des menus](#keyboard-access-to-menus)
    -   [Interface clavier standard](#standard-keyboard-interface)
    -   [Touches d’accès au menu](#menu-access-keys)
    -   [Touches de raccourci du menu](#menu-shortcut-keys)
-   [Création de menu](#menu-creation)
    -   [Ressources de modèle de menu](#menu-template-resources)
    -   [Modèle de menu en mémoire](#menu-template-in-memory)
    -   [Poignées de menu](#menu-handles)
    -   [Fonctions de création de menu](#menu-creation-functions)
    -   [Affichage du menu](#menu-display)
    -   [Menus de la classe de fenêtre](#window-class-menus)
-   [Éléments de menu](#menu-items)
    -   [Éléments de commande et éléments qui ouvrent des sous-menus](#command-items-and-items-that-open-submenus)
    -   [Identificateur d’élément de menu](#menu-item-identifier)
    -   [Position de l’élément de menu](#menu-item-position)
    -   [Accès par programmation aux éléments de menu](#accessing-menu-items-programmatically)
    -   [Éléments de menu par défaut](#default-menu-items)
    -   [Éléments de menu sélectionnés et désactivés](#selected-and-clear-menu-items)
    -   [Éléments de menu activé, grisé et désactivé](#enabled-grayed-and-disabled-menu-items)
    -   [Éléments de menu en surbrillance](#highlighted-menu-items)
    -   [Éléments de menu owner-drawn](#owner-drawn-menu-items)
    -   [Séparateurs d’éléments de menu et sauts de ligne](#menu-item-separators-and-line-breaks)
-   [Messages utilisés avec les menus](#messages-used-with-menus)
-   [Destruction de menu](#menu-destruction)

## <a name="menu-bars-and-menus"></a>Menus et barres de menus

Un menu est organisé dans une hiérarchie. Au niveau supérieur de la hiérarchie se trouve la *barre de menus*. qui contient une liste de *menus*, qui peuvent à leur tour contenir des *sous-menus*. Une barre de menus est parfois appelée *menu de niveau supérieur*, tandis que les menus et les sous-menus sont également appelés *menus contextuels*.

Un élément de menu peut soit exécuter une commande, soit ouvrir un sous-menu. Un élément qui exécute une commande est appelé un *élément de commande* ou une *commande*.

Un élément de la barre de menus ouvre presque toujours un menu. Les barres de menus contiennent rarement des éléments de commande. Un menu ouvert à partir de la barre de menus descend de la barre de menus et est parfois appelé un *menu déroulant*. Lorsqu’un menu déroulant s’affiche, il est attaché à la barre de menus. Un élément de menu de la barre de menus qui ouvre un menu déroulant est également appelé un *nom de menu*.

Les noms de menu d’une barre de menus représentent les principales catégories de commandes fournies par une application. La sélection d’un nom de menu dans la barre de menus ouvre généralement un menu dont les éléments de menu correspondent aux commandes d’une catégorie. Par exemple, une barre de menus peut contenir un nom de menu de **fichier** qui, lorsque l’utilisateur clique dessus, active un menu avec des éléments de menu tels que **nouveau**, **ouvrir** et **Enregistrer**. Pour obtenir des informations sur une barre de menus, appelez [**GetMenuBarInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenubarinfo).

Seule une fenêtre superposée ou contextuelle peut contenir une barre de menus ; une fenêtre enfant ne peut pas en contenir une. Si la fenêtre a une barre de titre, le système positionne la barre de menus juste en dessous. Une barre de menus est toujours visible. Toutefois, un sous-menu n’est pas visible jusqu’à ce que l’utilisateur sélectionne un élément de menu qui l’active. Pour plus d’informations sur les fenêtres superposées et les fenêtres indépendantes, consultez [types de fenêtre](/windows/desktop/winmsg/window-features).

Chaque menu doit avoir une fenêtre propriétaire. Le système envoie des messages à la fenêtre propriétaire d’un menu lorsque l’utilisateur sélectionne le menu ou choisit un élément dans le menu.

Cette section décrit les rubriques suivantes.

-   [Menus contextuels](#shortcut-menus)
-   [Menu fenêtre](#the-window-menu)
-   [Identificateur d’aide](#help-identifier)

### <a name="shortcut-menus"></a>Menus contextuels

Le système fournit également des *menus contextuels*. Un menu contextuel n’est pas attaché à la barre de menus ; elle peut apparaître n’importe où sur l’écran. Une application associe généralement un menu contextuel à une partie d’une fenêtre, telle que la zone cliente, ou à un objet spécifique, tel qu’une icône. C’est la raison pour laquelle ces menus sont également appelés *menus contextuels*.

Un menu contextuel reste masqué jusqu’à ce que l’utilisateur l’active, en général en cliquant avec le bouton droit sur une sélection, une barre d’outils ou un bouton de la barre des tâches. Le menu s’affiche généralement à la position du point d’insertion ou du curseur de la souris.

### <a name="the-window-menu"></a>Menu fenêtre

Le menu **fenêtre** (également appelé menu **système** ou menu **contrôle** ) est un menu contextuel défini et géré presque exclusivement par le système d’exploitation. L’utilisateur peut ouvrir le menu fenêtre en cliquant sur l’icône d’application dans la barre de titre ou en cliquant avec le bouton droit n’importe où dans la barre de titre.

Le menu **fenêtre** fournit un ensemble standard d’éléments de menu que l’utilisateur peut choisir pour modifier la taille ou la position d’une fenêtre, ou fermer l’application. Les éléments du menu fenêtre peuvent être ajoutés, supprimés et modifiés, mais la plupart des applications utilisent simplement l’ensemble standard d’éléments de menu. Une fenêtre superposée, contextuelle ou enfant peut avoir un menu fenêtre. Il est rare qu’une fenêtre Overlapped ou contextuelle n’inclue pas de menu fenêtre.

Quand l’utilisateur choisit une commande dans le menu **fenêtre** , le système envoie un message [**WM \_ SYSCOMMAND**](wm-syscommand.md) à la fenêtre propriétaire du menu. Dans la plupart des applications, la procédure de fenêtre ne traite pas les messages du menu fenêtre. Au lieu de cela, il transmet simplement les messages à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour le traitement par défaut du message par le système. Si une application ajoute une commande au menu fenêtre, la procédure de fenêtre doit traiter la commande.

Une application peut utiliser la fonction [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu) pour créer une copie du menu de la fenêtre par défaut à modifier. Toute fenêtre qui n’utilise pas la fonction **GetSystemMenu** pour faire de sa propre copie du menu fenêtre reçoit le menu fenêtre standard.

### <a name="help-identifier"></a>Identificateur d’aide

Le menu, le menu, le sous-menu et le menu contextuel associés à chaque barre de menus sont des identificateurs d’aide. Si l’utilisateur appuie sur la touche F1 alors que le menu est actif, cette valeur est envoyée à la fenêtre propriétaire dans le cadre d’un message d' [**\_ aide WM**](../shell/wm-help.md) .

## <a name="keyboard-access-to-menus"></a>Accès au clavier à des menus

Le système fournit une interface clavier standard pour les menus. Vous pouvez améliorer cette interface en fournissant des clés d’accès mnémoniques et des touches de raccourci (Accélérateur) pour vos éléments de menu.

Les rubriques suivantes décrivent l’interface clavier standard, les touches d’accès rapide et les touches de raccourci :

-   [Interface clavier standard](#standard-keyboard-interface)
-   [Touches d’accès au menu](#menu-access-keys)
-   [Touches de raccourci du menu](#menu-shortcut-keys)

### <a name="standard-keyboard-interface"></a>Interface clavier standard

Le système est conçu pour fonctionner avec ou sans souris ou autre dispositif de pointage. Étant donné que le système fournit une interface clavier standard, l’utilisateur peut utiliser le clavier pour sélectionner les éléments de menu. Cette interface de clavier n’a pas besoin de code spécial. Une application reçoit un message de commande si l’utilisateur sélectionne un élément de menu par le biais du clavier ou à l’aide d’une souris. L’interface clavier standard traite les séquences de touches suivantes.



| Séquence de touches              | Action                                                                                                                                                                                                                                   |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Caractère alphabétique | Sélectionne le premier élément de menu avec le caractère spécifié comme clé d’accès. Si l’élément sélectionné appelle un menu, le menu s’affiche et le premier élément est mis en surbrillance. Dans le cas contraire, l’élément de menu est choisi.                            |
| Alt                    | Active ou désactive le mode de barre de menus.                                                                                                                                                                                                     |
| ALT + BARRE D’ESPACE           | Affiche le menu fenêtre.                                                                                                                                                                                                                |
| ENTRÉE                  | Active un menu et sélectionne le premier élément de menu si un menu est associé à un élément. Dans le cas contraire, cette séquence de touches choisit l’élément comme si l’utilisateur avait relâché le bouton de la souris pendant que l’élément était sélectionné.                              |
| ÉCHAP                    | Quitte le mode de menu.                                                                                                                                                                                                                         |
| Gauche             | Effectue un cycle vers l’élément de menu de niveau supérieur précédent. Les éléments de menu de niveau supérieur incluent les noms de menu et le menu fenêtre. Si l’élément sélectionné est dans un menu, la colonne précédente du menu est sélectionnée ou l’élément de menu de niveau supérieur précédent est sélectionné. |
| Flèche droite            | Fonctionne comme la touche de direction gauche, sauf dans la direction opposée. Dans les menus, cette séquence de touches avance d’une colonne ; Lorsque l’élément actuellement sélectionné se trouve dans la colonne située à l’extrême droite, le menu suivant est sélectionné.                              |
| FLÈCHES haut ou bas      | Active un menu quand vous appuyez sur un nom de menu. Quand vous appuyez sur un menu, la touche de direction haut sélectionne l’élément précédent. la touche de direction bas sélectionne l’élément suivant.                                                                  |



 

### <a name="menu-access-keys"></a>Touches d’accès au menu

L’interface clavier standard pour les menus peut être améliorée en ajoutant des touches d’accès (mnémoniques) aux éléments de menu. Une touche d’accès est une lettre soulignée dans le texte d’un élément de menu. Lorsqu’un menu est actif, l’utilisateur peut sélectionner un élément de menu en appuyant sur la touche qui correspond à la lettre soulignée de l’élément. L’utilisateur rend la barre de menus active en appuyant sur la touche ALT pour mettre en surbrillance le premier élément de la barre de menus. Un menu est actif lorsqu’il est affiché.

Pour créer une touche d’accès pour un élément de menu, faites précéder tout caractère de la chaîne de texte de l’élément d’une esperluette. Par exemple, la chaîne de texte « &Move » amène le système à souligner la lettre « M ».

### <a name="menu-shortcut-keys"></a>Touches de raccourci du menu

En plus de disposer d’une touche d’accès rapide, un élément de menu peut être associé à une touche de raccourci. Une touche de raccourci est différente d’une touche d’accès rapide, car il n’est pas nécessaire que le menu soit actif pour que la touche de raccourci fonctionne. En outre, une touche d’accès rapide est *toujours* associée à un élément de menu, tandis qu’une touche de raccourci est *généralement* (mais n’a pas besoin d’être) associée à un élément de menu.

Le texte qui identifie la touche de raccourci est ajouté à la chaîne de texte de l’élément de menu. Le texte du raccourci s’affiche à droite du nom de l’élément de menu, après une barre oblique inverse et un caractère de tabulation ( \\ t). Par exemple, « &fermer \\ tAlt + F4 » représente une commande close avec la combinaison de touches ALT + F4 comme touche de raccourci et avec la lettre « C » comme clé d’accès. Pour plus d’informations, consultez [accélérateurs clavier](keyboard-accelerators.md).

## <a name="menu-creation"></a>Création de menu

Vous pouvez créer un menu à l’aide d’un modèle de menu ou de fonctions de création de menu. Les modèles de menu sont généralement définis en tant que ressources. Les ressources de modèle de menu peuvent être chargées explicitement ou affectées comme menu par défaut pour une classe de fenêtre. Vous pouvez également créer dynamiquement des ressources de modèle de menu dans la mémoire.

Les rubriques suivantes décrivent la création de menus en détail :

-   [Ressources de modèle de menu](#menu-template-resources)
-   [Modèle de menu en mémoire](#menu-template-in-memory)
-   [Poignées de menu](#menu-handles)
-   [Fonctions de création de menu](#menu-creation-functions)
-   [Affichage du menu](#menu-display)
-   [Menus de la classe de fenêtre](#window-class-menus)

### <a name="menu-template-resources"></a>Ressources de modèle de menu

La plupart des applications créent des menus à l’aide des ressources de modèle de menu. Un *modèle de menu* définit un menu, y compris les éléments de la barre de menus et tous les menus. Pour plus d’informations sur la création d’une ressource de modèle de menu, consultez la documentation fournie avec vos outils de développement.

Après avoir créé une ressource de modèle de menu et l’avoir ajoutée au fichier exécutable (. exe) de votre application, vous pouvez utiliser la fonction [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) pour charger la ressource en mémoire. Cette fonction retourne un handle au menu, que vous pouvez ensuite assigner à une fenêtre à l’aide de la fonction [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) . Vous pouvez assigner un menu à n’importe quelle fenêtre qui n’est pas une fenêtre enfant.

L’implémentation de menus en tant que ressources rend une application plus facile à localiser pour une utilisation dans plusieurs pays/régions. Seul le fichier de définition de ressource doit être localisé pour chaque langue, et non le code source de l’application.

### <a name="menu-template-in-memory"></a>Modèle de menu en mémoire

Un menu peut être créé à partir d’un modèle de menu qui est généré en mémoire au moment de l’exécution. Par exemple, une application qui permet à un utilisateur de personnaliser son menu peut créer un modèle de menu en mémoire basé sur les préférences de l’utilisateur. L’application peut ensuite enregistrer le modèle dans un fichier ou dans le registre pour une utilisation ultérieure. Pour créer un menu à partir d’un modèle en mémoire, utilisez la fonction [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) . Pour obtenir une description des formats de modèle de menu, consultez [ressources de modèle de menu](#menu-template-resources).

Un modèle de menu standard se compose d’une structure [**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) suivie d’une ou de plusieurs structures [**MENUITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate) .

Un modèle de menu étendu se compose d’une structure d' [**\_ \_ en-tête de modèle menuex**](menuex-template-header.md) suivie d’une ou de plusieurs structures d' [**\_ \_ élément de modèle menuex**](menuex-template-item.md) .

### <a name="menu-handles"></a>Poignées de menu

Le système génère un handle unique pour chaque menu. Un *descripteur de menu* est une valeur du type **HMENU** . Une application doit spécifier un handle de menu dans la plupart des fonctions de menu. Vous recevez un handle vers une barre de menus lorsque vous créez le menu ou chargez une ressource de menu.

Pour récupérer un handle vers la barre de menus d’un menu qui a été créé ou chargé, utilisez la fonction [**GetMenu**](/windows/desktop/api/Winuser/nf-winuser-getmenu) . Pour récupérer un handle du sous-menu associé à un élément de menu, utilisez la fonction [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) ou [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) . Pour récupérer un handle d’un menu fenêtre, utilisez la fonction [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu) .

### <a name="menu-creation-functions"></a>Fonctions de création de menu

À l’aide des fonctions de création de menu, vous pouvez créer des menus au moment de l’exécution ou ajouter des éléments de menu à des menus existants. Vous pouvez utiliser la fonction [**CreateMenu**](/windows/desktop/api/Winuser/nf-winuser-createmenu) pour créer une barre de menus vide et la fonction [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) pour créer un menu vide. Vous pouvez enregistrer certaines informations de paramètres pour un menu à l’aide de la structure [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) . Pour obtenir ou récupérer les paramètres d’un menu, utilisez [**GetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuinfo) ou [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo). Pour ajouter des éléments à un menu, utilisez la fonction [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) . Les anciennes fonctions [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) et [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua) sont toujours prises en charge, mais **InsertMenuItem** doit être utilisé pour les nouvelles applications.

### <a name="menu-display"></a>Affichage du menu

Une fois qu’un menu a été chargé ou créé, il doit être assigné à une fenêtre pour que le système puisse l’afficher. Vous pouvez assigner un menu en définissant un menu de classe. Pour plus d’informations, consultez menus de la [classe de fenêtre](#window-class-menus). Vous pouvez également assigner un menu à une fenêtre en spécifiant un handle vers le menu comme paramètre *HMENU* de la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , ou en appelant la fonction [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) .

Pour afficher un menu contextuel, utilisez la fonction [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) . Les menus contextuels, également appelés menus contextuels flottants ou menus contextuels, s’affichent généralement lorsque le message [**WM \_ CONTEXTMENU**](wm-contextmenu.md) est traité.

Vous pouvez assigner un menu à n’importe quelle fenêtre qui n’est pas une fenêtre enfant.

L’ancienne fonction [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) est toujours prise en charge, mais les nouvelles applications doivent utiliser la fonction [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) .

### <a name="window-class-menus"></a>Menus de la classe de fenêtre

Vous pouvez spécifier un menu par défaut, appelé *menu de classe,* quand vous inscrivez une classe de fenêtre. Pour ce faire, vous assignez le nom de la ressource de modèle de menu au membre **lpszMenuName** de la structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) utilisée pour inscrire la classe.

Par défaut, chaque fenêtre est assignée au menu classe pour sa classe de fenêtre. vous n’avez donc pas besoin de charger explicitement le menu et de l’assigner à chaque fenêtre. Vous pouvez remplacer le menu classe en spécifiant un autre handle de menu dans un appel à la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) . Vous pouvez également modifier le menu d’une fenêtre après qu’il a été créé à l’aide de la fonction [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) . Pour plus d’informations, consultez [classes de fenêtre](/windows/desktop/winmsg/window-classes).

## <a name="menu-items"></a>Éléments de menu

Les rubriques suivantes décrivent ce que fait le système lorsque l’utilisateur choisit un élément de menu et comment une application peut contrôler l’apparence et les fonctionnalités d’un élément :

-   [Éléments de commande et éléments qui ouvrent des sous-menus](#command-items-and-items-that-open-submenus)
-   [Identificateur d’élément de menu](#menu-item-identifier)
-   [Position de l’élément de menu](#menu-item-position)
-   [Accès par programmation aux éléments de menu](#accessing-menu-items-programmatically)
-   [Éléments de menu par défaut](#default-menu-items)
-   [Éléments de menu sélectionnés et désactivés](#selected-and-clear-menu-items)
-   [Éléments de menu activé, grisé et désactivé](#enabled-grayed-and-disabled-menu-items)
-   [Éléments de menu en surbrillance](#highlighted-menu-items)
-   [Éléments de menu owner-drawn](#owner-drawn-menu-items)
-   [Séparateurs d’éléments de menu et sauts de ligne](#menu-item-separators-and-line-breaks)

### <a name="command-items-and-items-that-open-submenus"></a>Éléments de commande et éléments qui ouvrent des sous-menus

Quand l’utilisateur choisit un élément de commande, le système envoie un message de commande à la fenêtre qui possède le menu. Si l’élément de commande se trouve dans le menu fenêtre, le système envoie le message [**WM \_ SYSCOMMAND**](wm-syscommand.md) . Dans le cas contraire, il envoie le message de [**\_ commande WM**](wm-command.md) .

Associé à chaque élément de menu qui ouvre un sous-menu est un handle vers le sous-menu correspondant. Lorsque l’utilisateur pointe sur ce type d’élément, le système ouvre le sous-menu. Aucun message de commande n’est envoyé à la fenêtre propriétaire. Toutefois, le système envoie un message [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) à la fenêtre propriétaire avant d’afficher le sous-menu. Vous pouvez obtenir un handle vers le sous-menu associé à un élément à l’aide de la fonction [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) ou [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) .

Une barre de menus contient généralement des noms de menu, mais elle peut également contenir des éléments de commande. Un sous-menu contient généralement des éléments de commande, mais il peut également contenir des éléments qui ouvrent des sous-menus imbriqués. En ajoutant ces éléments aux sous-menus, vous pouvez imbriquer des menus à n’importe quelle profondeur. Pour fournir une indication visuelle pour l’utilisateur, le système affiche automatiquement une petite flèche à droite du texte d’un élément de menu qui ouvre un sous-menu.

### <a name="menu-item-identifier"></a>Identificateur de Menu-Item

Le associé à chaque élément de menu est un entier unique défini par l’application, appelé *identificateur d’élément de menu*. Quand l’utilisateur choisit un élément de commande dans un menu, le système envoie l’identificateur de l’élément à la fenêtre propriétaire dans le cadre d’un message de [**\_ commande WM**](wm-command.md) . La procédure de fenêtre examine l’identificateur pour déterminer la source du message et traite le message en conséquence. En outre, vous pouvez spécifier un élément de menu à l’aide de son identificateur lorsque vous appelez des fonctions de menu. par exemple, pour activer ou désactiver un élément de menu.

Les éléments de menu qui ouvrent des sous-menus ont des identificateurs de la même façon que les éléments de commande. Toutefois, le système n’envoie pas de message de commande quand un tel élément est sélectionné à partir d’un menu. Au lieu de cela, le système ouvre le sous-menu associé à l’élément de menu.

Pour récupérer l’identificateur de l’élément de menu à une position spécifiée, utilisez la fonction [**GetMenuItemID**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemid) ou [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) .

### <a name="menu-item-position"></a>Position Menu-Item

En plus d’avoir un identificateur unique, chaque élément de menu dans une barre de menus ou un menu a une valeur de position unique. L’élément le plus à gauche dans une barre de menus, ou l’élément supérieur d’un menu, a la position zéro. La valeur de position est incrémentée pour les éléments de menu suivants. Le système assigne une valeur de position à tous les éléments d’un menu, y compris les séparateurs. L’illustration suivante montre les valeurs de position des éléments dans une barre de menus et dans un menu.

![barre de menus et menu](images/csemn-01.png)

Lors de l’appel d’une fonction de menu qui modifie ou récupère des informations sur un élément de menu spécifique, vous pouvez spécifier l’élément à l’aide de son identificateur ou de sa position. Pour plus d'informations, consultez la section suivante.

### <a name="accessing-menu-items-programmatically"></a>Accès par programmation aux éléments de menu

La plupart des fonctions de menu vous permettent de spécifier un élément de menu par position ou par commande. Certaines fonctions utilisent les indicateurs **MF \_ BYPOSITION** et **MF \_ BYCOMMAND** pour indiquer l’algorithme de recherche ; d’autres ont un paramètre *fByPosition* explicite. Si vous spécifiez l’élément de menu par position, le numéro d’élément est un index de base zéro dans le menu. Si vous spécifiez l’élément de menu par commande, le menu et ses sous-menus font l’objet d’une recherche sur un élément dont l’identificateur de menu est égal au numéro d’élément fourni. Si plusieurs éléments de la hiérarchie de menus correspondent au numéro d’élément, il n’est pas spécifié, lequel est utilisé. Si vos menus contiennent des identificateurs de menu en double, vous devez utiliser des opérations de menu basées sur la position pour éviter cette ambiguïté.

### <a name="default-menu-items"></a>Éléments de menu par défaut

Un sous-menu peut contenir un élément de menu par défaut. Quand l’utilisateur ouvre un sous-menu en double-cliquant sur, le système envoie un message de commande à la fenêtre propriétaire du menu et ferme le menu comme si l’élément de commande par défaut avait été choisi. S’il n’y a pas d’élément de commande par défaut, le sous-menu reste ouvert. Pour récupérer et définir l’élément par défaut d’un sous-menu, utilisez les fonctions [**GetMenuDefaultItem**](/windows/desktop/api/Winuser/nf-winuser-getmenudefaultitem) et [**SetMenuDefaultItem**](/windows/desktop/api/Winuser/nf-winuser-setmenudefaultitem) .

### <a name="selected-and-clear-menu-items"></a>Éléments de menu sélectionnés et désactivés

Un élément de menu peut être sélectionné ou désactivé. Le système affiche une bitmap à côté des éléments de menu sélectionnés pour indiquer leur état sélectionné. Le système n’affiche pas de bitmap en regard des éléments clairs, sauf si une image bitmap « Clear » définie par l’application est spécifiée. Seuls les éléments de menu d’un menu peuvent être sélectionnés ; les éléments d’une barre de menus ne peuvent pas être sélectionnés.

En règle générale, les applications vérifient ou décochent un élément de menu pour indiquer si une option est activée. Par exemple, supposons qu’une application possède une barre d’outils que l’utilisateur peut afficher ou masquer à l’aide d’une commande de **barre d’outils** dans un menu. Quand la barre d’outils est masquée, l’élément de menu de la **barre d’outils** est vide. Lorsque l’utilisateur choisit la commande, l’application vérifie l’élément de menu et affiche la barre d’outils.

Un attribut coche détermine si un élément de menu est sélectionné. Vous pouvez définir l’attribut de coche d’un élément de menu à l’aide de la fonction [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) . Vous pouvez utiliser la fonction [**GetMenuState**](/windows/desktop/api/Winuser/nf-winuser-getmenustate) pour déterminer si un élément de menu est actuellement sélectionné ou effacé.

Au lieu de [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) et [**GetMenuState**](/windows/desktop/api/Winuser/nf-winuser-getmenustate), vous pouvez utiliser les fonctions [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) et [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) pour récupérer et définir l’état d’activation d’un élément de menu.

Parfois, un groupe d’éléments de menu correspond à un ensemble d’options s’excluant mutuellement. Dans ce cas, vous pouvez indiquer l’option sélectionnée à l’aide d’un élément de menu Radio sélectionné (semblable à un contrôle de case d’option). Les éléments de radio sélectionnés sont affichés avec une image bitmap au lieu d’une bitmap de coche. Pour vérifier un élément de menu et en faire un élément radio, utilisez la fonction [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) .

Par défaut, le système affiche une image bitmap en regard des éléments de menu sélectionnés et aucune bitmap en regard de éléments de menu effacés. Toutefois, vous pouvez utiliser la fonction [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) pour associer des bitmaps sélectionnées et effacées définies par l’application à un élément de menu. Le système utilise ensuite les bitmaps spécifiées pour indiquer l’état sélectionné ou effacé de l’élément de menu.

Les bitmaps définies par l’application associées à un élément de menu doivent avoir la même taille que la bitmap de coche par défaut, dont les dimensions peuvent varier en fonction de la résolution de l’écran. Pour récupérer les dimensions correctes, utilisez la fonction [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) . Vous pouvez créer plusieurs ressources bitmap pour différentes résolutions d’écran. Créez une ressource bitmap et mettez-la à l’échelle, si nécessaire ; ou créez une bitmap au moment de l’exécution et dessinez-y une image. Les bitmaps peuvent être de type monochrome ou couleur. Toutefois, étant donné que les éléments de menu sont inversés lorsqu’ils sont mis en surbrillance, l’apparence de certaines bitmaps de couleurs inversées peut être indésirable. Pour plus d’informations, consultez [bitmaps](/windows/desktop/gdi/bitmaps).

### <a name="enabled-grayed-and-disabled-menu-items"></a>Éléments de menu activé, grisé et désactivé

Un élément de menu peut être activé, grisé ou désactivé. Par défaut, un élément de menu est activé. Quand l’utilisateur choisit un élément de menu activé, le système envoie un message de commande à la fenêtre propriétaire ou affiche le sous-menu correspondant, selon le type d’élément de menu.

Lorsque les éléments de menu ne sont pas disponibles pour l’utilisateur, ils doivent être grisés ou désactivés. Les éléments de menu grisés et désactivés ne peuvent pas être choisis. Un élément désactivé se présente comme un élément activé. Lorsque l’utilisateur clique sur un élément désactivé, l’élément n’est pas sélectionné et rien ne se produit. Les éléments désactivés peuvent être utiles dans, par exemple, un didacticiel qui présente un menu qui semble actif mais non.

Une application grise un élément de menu non disponible pour fournir à l’utilisateur un signal visuel indiquant qu’une commande n’est pas disponible. Vous pouvez utiliser un élément grisé quand une action n’est pas appropriée (par exemple, vous pouvez griser la commande **Imprimer** dans le menu **fichier** quand aucune imprimante n’est installée sur le système).

La fonction [**EnableMenuItem**](/windows/desktop/api/Winuser/nf-winuser-enablemenuitem) active, grise ou désactive un élément de menu. Pour déterminer si un élément de menu est activé, grisé ou désactivé, utilisez la fonction [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) .

Au lieu de [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa), vous pouvez également utiliser la fonction [**GetMenuState**](/windows/desktop/api/Winuser/nf-winuser-getmenustate) pour déterminer si un élément de menu est activé, grisé ou désactivé.

### <a name="highlighted-menu-items"></a>Éléments de menu en surbrillance

Le système met automatiquement en surbrillance les éléments de menu des menus lorsque l’utilisateur les sélectionne. Toutefois, la mise en surbrillance peut être ajoutée ou supprimée explicitement d’un nom de menu dans la barre de menus à l’aide de la fonction [**HiliteMenuItem**](/windows/desktop/api/Winuser/nf-winuser-hilitemenuitem) . Cette fonction n’a aucun effet sur les éléments de menu des menus. Quand **HiliteMenuItem** est utilisé pour mettre en surbrillance un nom de menu, le nom apparaît uniquement comme étant sélectionné. Si l’utilisateur appuie sur la touche entrée, l’élément mis en surbrillance n’est pas sélectionné. Cette fonctionnalité peut être utile dans, par exemple, une application de formation qui illustre l’utilisation de menus.

### <a name="owner-drawn-menu-items"></a>Owner-Drawn les éléments de menu

Une application peut contrôler complètement l’apparence d’un élément de menu à l’aide d’un *élément owner-drawn*. Les éléments owner-drawn nécessitent une application pour assumer la responsabilité totale pour le dessin des États sélectionnés (en surbrillance), sélectionnés et désélectionnés. Par exemple, si une application a fourni un menu police, elle peut dessiner chaque élément de menu à l’aide de la police correspondante ; l’élément pour roman est dessiné avec le chiffre romain, l’élément en italique est dessiné en italique, et ainsi de suite. Pour plus d’informations, consultez [création d' Owner-Drawn éléments de menu](using-menus.md).

### <a name="menu-item-separators-and-line-breaks"></a>Séparateurs d’éléments de menu et sauts de ligne

Le système fournit un type spécial d’élément de menu, appelé *séparateur*, qui apparaît sous forme de ligne horizontale. Vous pouvez utiliser un séparateur pour diviser un menu en groupes d’éléments associés. Un séparateur ne peut pas être utilisé dans une barre de menus et l’utilisateur ne peut pas sélectionner de séparateur.

Quand une barre de menus contient plus de noms de menu qu’une seule ligne, le système encapsule la barre de menus en la divisant automatiquement en deux lignes ou plus. Vous pouvez faire en sorte qu’un saut de ligne se produise au niveau d’un élément spécifique d’une barre de menus en affectant l’indicateur de type **\_ MENUBREAK MFT** à l’élément. Le système place cet élément et tous les éléments suivants sur une nouvelle ligne.

Quand un menu contient plus d’éléments que ne peut en contenir une colonne, le menu est tronqué. Vous pouvez faire en sorte qu’un saut de colonne se produise au niveau d’un élément spécifique d’un menu en affectant l’indicateur de type **\_ MENUBREAK MFT** à l’élément ou en utilisant l’option MENUBREAK dans l’instruction [MenuItem](/windows/desktop/menurc/menuitem-statement) . Le système place cet élément et tous les éléments suivants dans une nouvelle colonne. L’indicateur de type **\_ MENUBARBREAK MFT** a le même effet, sauf qu’une ligne verticale apparaît entre la nouvelle colonne et l’ancien.

Si vous utilisez les fonctions [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)ou [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) pour assigner des sauts de ligne, vous devez assigner les indicateurs de type **MF \_ MENUBREAK** ou **MF \_ MENUBARBREAK**.

## <a name="messages-used-with-menus"></a>Messages utilisés avec les menus

Le système signale une activité liée au menu en envoyant des messages à la procédure de fenêtre de la fenêtre qui possède le menu. Le système envoie une série de messages lorsque l’utilisateur sélectionne des éléments dans la barre de menus ou clique avec le bouton droit de la souris pour afficher un menu contextuel.

Lorsque l’utilisateur active un élément dans la barre de menus, la fenêtre propriétaire reçoit d’abord un message [**WM \_ SYSCOMMAND**](wm-syscommand.md) . Ce message comprend un indicateur qui indique si l’utilisateur a activé le menu à l’aide du clavier ( \_ menu SC) ou de la souris (SC \_ MOUSEMENU). Pour plus d’informations, consultez [accès clavier aux menus](#keyboard-access-to-menus).

Ensuite, avant d’afficher des menus, le système envoie le message [**WM \_ INITMENU**](wm-initmenu.md) à la procédure de fenêtre afin qu’une application puisse modifier les menus avant que l’utilisateur ne les voit. Le système envoie le message **WM \_ INITMENU** une seule fois par activation de menu.

Quand l’utilisateur pointe sur un élément de menu qui ouvre un sous-menu, le système envoie la fenêtre propriétaire du message [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) avant d’afficher le sous-menu. Ce message donne à l’application la possibilité de modifier le sous-menu avant qu’il ne s’affiche.

Chaque fois que l’utilisateur déplace la mise en surbrillance d’un élément à un autre, le système envoie un message [**WM \_ MENUSELECT**](wm-menuselect.md) à la procédure de fenêtre de la fenêtre propriétaire du menu. Ce message identifie l’élément de menu actuellement sélectionné. De nombreuses applications fournissent une zone d’informations en bas de leurs fenêtres principales et utilisent ce message pour afficher des informations supplémentaires sur l’élément de menu sélectionné.

Quand l’utilisateur choisit un élément de commande dans un menu, le système envoie un message de [**\_ commande WM**](wm-command.md) à la procédure de fenêtre. Le mot de poids faible du paramètre *wParam* du message de **\_ commande WM** contient l’identificateur de l’élément choisi. La procédure de fenêtre doit examiner l’identificateur et traiter le message en conséquence.

Vous pouvez enregistrer les informations d’un menu à l’aide de la structure [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) . Si le menu est défini avec un **MENUINFO**. **dwStyle** valeur de MNS \_ NOTIFYBYPOS, le système envoie [**WM \_ MENUCOMMAND**](wm-menucommand.md) à la place de la [**\_ commande WM**](wm-command.md) lorsqu’un élément est sélectionné. Cela vous permet d’accéder aux informations contenues dans la structure **MENUINFO** et de fournir l’index de l’élément sélectionné directement.

Tous les menus ne sont pas accessibles par le biais de la barre de menus d’une fenêtre. De nombreuses applications affichent des menus contextuels lorsque l’utilisateur clique avec le bouton droit de la souris à un emplacement spécifique. De telles applications doivent traiter le message [**WM \_ CONTEXTMENU**](wm-contextmenu.md) et afficher un menu contextuel, le cas échéant. Si une application n’affiche pas de menu contextuel, elle doit passer le message **WM \_ CONTEXTMENU** à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour le traitement par défaut.

Le message [**WM \_ MENURBUTTONUP**](wm-menurbuttonup.md) est envoyé lorsque l’utilisateur relâche le bouton droit de la souris alors que le curseur se trouve sur un élément de menu. Ce message est fourni afin que les applications puissent afficher un menu contextuel ou un menu contextuel pour un élément de menu.

Il y a quelques messages qui impliquent uniquement des menus de glisser-déplacer. Le [**\_ MENUGETOBJECT WM**](wm-menugetobject.md) est envoyé au propriétaire d’un menu glisser-déplacer lorsque le curseur de la souris entre dans un élément de menu ou se déplace du centre d’un élément vers le haut ou le bas d’un élément. Le message [**WM \_ MENUDRAG**](wm-menudrag.md) est envoyé lorsque l’utilisateur fait glisser un élément de menu.

Lorsqu’un menu déroulant ou un sous-menu a été détruit, le système envoie un message [**WM \_ UNINITMENUPOPUP**](wm-uninitmenupopup.md) .

## <a name="menu-destruction"></a>Destruction de menu

Si un menu est affecté à une fenêtre et que cette fenêtre est détruite, le système détruit automatiquement le menu et ses sous-menus, libérant ainsi la poignée du menu et la mémoire occupée par le menu. Le système ne détruit pas automatiquement un menu qui n’est pas assigné à une fenêtre. Une application doit détruire le menu non assigné en appelant la fonction [**DestroyMenu**](/windows/desktop/api/Winuser/nf-winuser-destroymenu) . Dans le cas contraire, le menu continue d’exister en mémoire même après la fermeture de l’application. Pour terminer le menu actif du thread appelant, utilisez [**EndMenu**](/windows/desktop/api/Winuser/nf-winuser-endmenu). Si une plateforme ne prend pas en charge **EndMenu**, envoyez au propriétaire du menu actif un message [**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) .

 

 