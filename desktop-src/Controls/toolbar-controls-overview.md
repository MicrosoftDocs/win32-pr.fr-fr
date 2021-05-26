---
title: À propos des contrôles ToolBar
description: Une barre d’outils est un contrôle qui contient un ou plusieurs boutons.
ms.assetid: b5a00a81-8d23-4844-8b0a-776e7cceced8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f615da972f14bb88c4915504c089dd6b40d9aca
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424149"
---
# <a name="about-toolbar-controls"></a>À propos des contrôles ToolBar

Une barre d’outils est un contrôle qui contient un ou plusieurs boutons. Chaque bouton, lorsque l’utilisateur clique sur un utilisateur, envoie un message de commande à la fenêtre parente. En règle générale, les boutons d’une barre d’outils correspondent aux éléments du menu de l’application, ce qui offre un moyen supplémentaire et plus direct à l’utilisateur d’accéder aux commandes d’une application.

La capture d’écran suivante montre une fenêtre qui contient une barre d’outils simple pour les opérations sur les fichiers. L’application a activé les styles visuels. Le bouton enregistrer est « actif », car le curseur se trouve au-dessus de celui-ci lorsque la capture d’écran a été prise. L’apparence réelle du contrôle varie selon le système d’exploitation et le thème sélectionné par l’utilisateur.

![capture d’écran d’une fenêtre avec une barre d’outils à trois boutons ; un bouton est actif](images/tb-withstyles.png)

La capture d’écran suivante montre le même contrôle dans une application qui a été compilée sans que les styles visuels soient activés.

![capture d’écran d’une fenêtre sans styles visuels : aucun des boutons ne semble chaud](images/tb-wostyles.png)

Les rubriques suivantes décrivent les fonctionnalités à prendre en compte lors de la planification d’une barre d’outils. Pour plus d’informations sur l’implémentation et un exemple de code, consultez [utilisation des contrôles ToolBar](using-toolbar-controls.md).

-   [Spécifier la taille et la position de la barre d’outils](#specifying-toolbar-size-and-position)
-   [Barres d’outils transparentes](#transparent-toolbars)
-   [Barres d’outils de style liste](#list-style-toolbars)
-   [Définition des images de bouton](#defining-button-images)
    -   [Définition d’images de bouton à l’aide de bitmaps](#defining-button-images-by-using-bitmaps)
    -   [Définition d’images de bouton à l’aide de listes d’images](#defining-button-images-by-using-image-lists)
-   [Définition du texte pour les boutons](#defining-text-for-buttons)
-   [Ajout de boutons de barre d’outils](#adding-toolbar-buttons)
    -   [Styles de boutons de barre d’outils](#toolbar-button-styles)
    -   [États des boutons de barre d’outils](#toolbar-button-states)
    -   [Identificateur de commande](#command-identifier)
    -   [Taille et position des boutons](#button-size-and-position)
-   [Activation de la personnalisation](#enabling-customization)
-   [Activation du suivi actif](#enabling-hot-tracking)

## <a name="specifying-toolbar-size-and-position"></a>Spécifier la taille et la position de la barre d’outils

Si vous créez une barre d’outils à l’aide de [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), la fonction vous permet de spécifier, en pixels, la hauteur et la largeur de la barre d’outils.

> [!Note]  
> L’utilisation de [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) n’est pas recommandée, car elle ne prend pas en charge les nouvelles fonctionnalités des barres d’outils, y compris les listes d’images. Pour plus d’informations sur la création de barres d’outils, consultez [utilisation des contrôles ToolBar](using-toolbar-controls.md).

 

La fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) n’a pas de paramètres pour spécifier la taille de la barre d’outils. La procédure de fenêtre de barre d’outils définit automatiquement la taille et la position de la fenêtre de la barre d’outils. La hauteur est basée sur la hauteur des boutons dans la barre d’outils. La largeur est identique à la largeur de la zone cliente de la fenêtre parente. Pour modifier les paramètres de taille automatique, envoyez un message [**to \_ SETBUTTONSIZE**](tb-setbuttonsize.md) . Les styles de contrôle communs [**CCS \_ Top**](common-control-styles.md) et [**CCS \_ Bottom**](common-control-styles.md) déterminent si la barre d’outils est positionnée le long du bord supérieur ou inférieur de la zone cliente. Par défaut, une barre d’outils a le style **CCS \_ Top** .

En outre, la procédure de fenêtre de barre d’outils ajuste automatiquement la taille de la barre d’outils chaque fois qu’elle reçoit un message de taille [**WM \_**](/windows/desktop/winmsg/wm-size) ou [**to \_ AutoSize**](tb-autosize.md) . Une application doit envoyer l’un de ces messages chaque fois que la taille de la fenêtre parente change ou après l’envoi d’un message nécessitant l’ajustement de la taille de la barre d’outils (par exemple, un message de [**\_ SETBUTTONSIZE to**](tb-setbuttonsize.md) ).

Les comportements de dimensionnement et de positionnement par défaut de la barre d’outils peuvent être désactivés en définissant les styles de contrôle communs [**CCS \_ NORESIZE**](common-control-styles.md) et [**CCS \_ NOPARENTALIGN**](common-control-styles.md) . Les contrôles Toolbar qui sont hébergés par les contrôles Rebar doivent définir ces styles, car le contrôle rebar contrôle la taille et la position de la barre d’outils.

## <a name="transparent-toolbars"></a>Barres d’outils transparentes

Les contrôles ToolBar prennent en charge une apparence transparente qui permet d’afficher la zone cliente sous la barre d’outils. Il existe deux types de barres d’outils transparentes, celles avec des boutons plats et des boutons à trois dimensions. Si vous souhaitez que votre application corresponde à l’interface Windows, utilisez la barre d’outils style transparent transparent.

La capture d’écran suivante montre les deux types de barres d’outils transparentes, sans utiliser les styles visuels.

![capture d’écran de deux fenêtres avec différents styles de barres d’outils, mais les deux barres d’outils sont transparentes](images/toolbartrans.jpg)

La capture d’écran suivante montre une barre d’outils transparente telle qu’elle peut apparaître dans Windows Vista, avec les styles visuels activés. La couleur d’arrière-plan de la boîte de dialogue a été modifiée pour rendre la transparence plus évidente.

![capture d’écran d’une fenêtre dans Windows Vista avec une barre d’outils transparente](images/tb-transparent.png)

Pour créer une barre d’outils transparente, il vous suffit d’ajouter [**TBSTYLE \_ Flat**](toolbar-control-and-button-styles.md) ou [**TBSTYLE \_ transparent**](toolbar-control-and-button-styles.md) au paramètre de style Window de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Si vous ne souhaitez pas qu’une ligne apparaisse pour indiquer le bas de la barre d’outils, n’utilisez pas le style de fenêtre [**WS \_ Border**](/windows/desktop/winmsg/window-styles) .

> [!Note]  
> Lorsque vous utilisez des styles visuels, les barres d’outils peuvent être plates par défaut.

 

## <a name="list-style-toolbars"></a>Barres d’outils de style liste

Les boutons de la barre d’outils vous permettent d’afficher à la fois le texte et les bitmaps. Les boutons d’une barre d’outils créée à l’aide du style de [**\_ liste TBSTYLE**](toolbar-control-and-button-styles.md) placent le texte à droite de l’image bitmap au lieu de le placer sous celui-ci.

La capture d’écran suivante montre une barre d’outils avec le style de liste.

![capture d’écran d’une barre d’outils avec le texte à droite de chaque icône](images/tb-liststyle.png)

Vous pouvez utiliser le style de barre d’outils de [**\_ liste TBSTYLE**](toolbar-control-and-button-styles.md) en combinaison avec le style [**TBSTYLE \_ Flat**](toolbar-control-and-button-styles.md) style pour créer une barre d’outils avec des boutons à deux dimensions.

## <a name="defining-button-images"></a>Définition des images de bouton

Il existe deux façons de spécifier les images pour les boutons, par images bitmap ou par listes d’images. Une application doit choisir la méthode à utiliser. Elle ne peut pas utiliser les deux méthodes avec le même contrôle ToolBar. Notez que la fonction [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) utilise la méthode bitmap. Les applications qui souhaitent utiliser la méthode de liste d’images doivent utiliser la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) pour créer le contrôle de barre d’outils.

### <a name="defining-button-images-by-using-bitmaps"></a>Définition d’images de bouton à l’aide de bitmaps

Chaque bouton d’une barre d’outils peut inclure une image bitmap. Une barre d’outils utilise une liste interne pour stocker les informations dont elle a besoin pour dessiner les images. Quand vous appelez la fonction [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) , vous spécifiez une image bitmap monochrome ou couleur qui contient les images initiales, et la barre d’outils ajoute les informations à la liste interne d’images. Vous pouvez ajouter des images supplémentaires ultérieurement à l’aide du message [**to \_ ADDBITMAP**](tb-addbitmap.md) .

Chaque image a un index de base zéro. La première image ajoutée à la liste interne a un index égal à 0, la deuxième image l’index 1, et ainsi de suite. [**To \_ ADDBITMAP**](tb-addbitmap.md) ajoute des images à la fin de la liste et retourne l’index de la première nouvelle image ajoutée. Pour associer l’image à un bouton, vous devez envoyer un message [**to \_ ADDBUTTONS**](tb-addbuttons.md) et spécifier l’index de l’image après avoir ajouté des bitmaps à la liste d’images internes.

Windows suppose que toutes les images bitmap d’une barre d’outils ont la même taille. Vous spécifiez la taille lors de la création de la barre d’outils à l’aide de [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex). Si vous utilisez la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) pour créer une barre d’outils, la taille des images est définie sur les dimensions par défaut de 16 par 15 pixels. Vous pouvez utiliser le message [**to \_ SETBITMAPSIZE**](tb-setbitmapsize.md) pour modifier les dimensions des images bitmap, mais vous devez le faire avant d’ajouter des images à la liste interne.

### <a name="defining-button-images-by-using-image-lists"></a>Définition d’images de bouton à l’aide de listes d’images

Vous pouvez également stocker des images de bouton dans un ensemble de [listes d’images](image-lists.md). Une liste d’images est une collection d’images de même taille, dont chacune peut être référencée par son index. Les listes d’images sont utilisées pour gérer de grands ensembles d’icônes ou de bitmaps. Vous pouvez utiliser jusqu’à trois listes d’images différentes pour afficher les boutons dans différents États, comme indiqué dans le tableau suivant.



|  État        |  Description                                                                                                                                                                                            |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Normal   | Boutons dans leur état par défaut.                                                                                                                                                              |
| À chaud      | Boutons situés sous le pointeur ou appuyés. Les éléments à chaud sont pris en charge uniquement dans les contrôles Toolbar qui ont le style à [**\_ deux dimensions TBSTYLE**](toolbar-control-and-button-styles.md) . |
| Désactivé | Boutons désactivés.                                                                                                                                                                   |



 

Une fois la barre d’outils détruite, les applications doivent libérer toutes les listes d’images qu’elles ont créées.

## <a name="defining-text-for-buttons"></a>Définition du texte pour les boutons

Chaque bouton peut afficher une chaîne en plus de, ou à la place d’une image. Une barre d’outils gère une liste interne qui contient toutes les chaînes disponibles pour les boutons de la barre d’outils. Vous ajoutez des chaînes à la liste interne à l’aide du message de [**to \_ ADDSTRING**](tb-addstring.md) , en spécifiant l’adresse de la mémoire tampon contenant les chaînes à ajouter. Chaque chaîne doit se terminer par un caractère null, et la dernière chaîne doit se terminer par deux caractères null.

Chaque chaîne a un index de base zéro. La première chaîne ajoutée à la liste interne des chaînes a un index égal à 0, la deuxième chaîne l’index 1, et ainsi de suite. [**To \_ ADDSTRING**](tb-addstring.md) ajoute des chaînes à la fin de la liste et retourne l’index de la première nouvelle chaîne. Vous utilisez l’index d’une chaîne pour associer la chaîne à un bouton.

L’utilisation de [**to \_ ADDSTRING**](tb-addstring.md) n’est pas la seule manière d’ajouter des chaînes à une barre d’outils. Vous pouvez afficher une chaîne dans un bouton en passant un pointeur de chaîne dans le membre **iString** de la structure [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) qui est passée à [**to \_ ADDBUTTONS**](tb-addbuttons.md). En outre, vous pouvez utiliser [**to \_ SETBUTTONINFO**](tb-setbuttoninfo.md) pour affecter du texte à un bouton de barre d’outils.

## <a name="adding-toolbar-buttons"></a>Ajout de boutons de barre d’outils

Si vous utilisez la fonction [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) pour créer une barre d’outils, vous pouvez ajouter des boutons à la barre d’outils en remplissant un tableau de structures [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) et en spécifiant l’adresse du tableau dans l’appel de fonction. Toutefois, la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) n’a pas de paramètre pour passer une structure **TBBUTTON** . **CreateWindowEx** crée une barre d’outils vide que vous remplissez en envoyant un message [**to \_ ADDBUTTONS**](tb-addbuttons.md) , en spécifiant l’adresse d’une structure **TBBUTTON** .

Après la création d’une barre d’outils, vous pouvez ajouter des boutons en envoyant un message [**to \_ INSERTBUTTON**](tb-insertbutton.md) ou [**to \_ ADDBUTTONS**](tb-addbuttons.md) . Chaque bouton est décrit par une structure [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) , qui définit les attributs du bouton, y compris les index de sa chaîne et de sa bitmap, ainsi que son style, État, identificateur de commande et valeur 32 bits définie par l’application.

> [!Note]  
> Si vous utilisez la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) pour créer une barre d’outils, vous devez envoyer le message [**to \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) avant d’ajouter des boutons. Le message transmet la taille de la structure [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) à la barre d’outils.

 

### <a name="toolbar-button-styles"></a>Styles de boutons de barre d’outils

Le style d’un bouton détermine la façon dont le bouton apparaît et comment il répond aux entrées d’utilisateur. Par exemple, le style de [**\_ bouton BTNS**](toolbar-control-and-button-styles.md) crée un bouton de barre d’outils qui se comporte comme un bouton de commande standard. Un bouton dont le style [**de \_ contrôle BTNS**](toolbar-control-and-button-styles.md) est similaire à un bouton de commande standard, à ceci près qu’il bascule entre les États enfoncé et non enfoncé chaque fois que l’utilisateur clique dessus.

Vous pouvez créer des groupes de boutons de barre d’outils qui agissent comme des cases d’option à l’aide du style [**BTNS \_**](toolbar-control-and-button-styles.md) ou [**BTNS \_ CHECKGROUP**](toolbar-control-and-button-styles.md) . Un bouton est alors maintenu enfoncé jusqu’à ce que l’utilisateur choisisse un autre bouton dans le groupe. Un groupe est défini en tant que collection contiguë de boutons, le tout avec le **BTNS \_ groupe** ou le style **BTNS \_ CHECKGROUP** .

Le [**style \_ Sep BTNS**](toolbar-control-and-button-styles.md) crée un petit intervalle entre les boutons ou dessine une gravure entre les boutons des barres d’outils plates. Un bouton avec le **style \_ Sep BTNS** ne reçoit pas d’entrée utilisateur.

La version 5,80 des contrôles communs a introduit de nouveaux styles de boutons de barre d’outils et renommé certains des anciens styles. Tous les indicateurs de style de bouton commencent désormais par BTNS \_ xxx au lieu de TBSTYLE \_ xxx. Pour obtenir une liste et une description des styles de bouton, consultez [barre d’outils et styles de bouton](toolbar-control-and-button-styles.md).

### <a name="toolbar-button-states"></a>États des boutons de barre d’outils

Chaque bouton dans une barre d’outils a un État. La barre d’outils met à jour l’état d’un bouton pour refléter les actions de l’utilisateur, par exemple en cliquant sur le bouton. L’état indique si le bouton est actuellement enfoncé ou non enfoncé, activé ou désactivé, masqué ou visible. Bien qu’une application définisse l’état initial d’un bouton lors de l’ajout du bouton à la barre d’outils, elle peut modifier et récupérer l’État en envoyant des messages [**to \_ GETSTATE to**](tb-getstate.md) et [**to \_ SETSTATE**](tb-setstate.md) à la barre d’outils. Pour obtenir la liste des États des boutons de barre d’outils, consultez États de la [barre d’outils](toolbar-button-states.md).

### <a name="command-identifier"></a>Identificateur de commande

Chaque bouton est associé à un identificateur de commande défini par l’application. Les identificateurs de bouton sont généralement définis dans un fichier d’en-tête d’application. Par exemple, un bouton Coller peut être défini comme suit :


```
#define ID_PASTE 100
```



Lorsque l’utilisateur sélectionne un bouton, la barre d’outils envoie la fenêtre parente à une [**\_ commande WM**](/windows/desktop/menurc/wm-command) ou à un message [**WM \_ Notify**](wm-notify.md) qui comprend l’identificateur de commande du bouton. La fenêtre parente examine l’identificateur de commande et exécute la commande associée au bouton. Pour plus d’informations sur le moment où les contrôles envoient des messages de **\_ commande WM** et lorsqu’ils envoient la **\_ notification WM**, consultez la section Notes de la documentation sur [**WM \_ Notify**](wm-notify.md) .

### <a name="button-size-and-position"></a>Taille et position des boutons

Une barre d’outils effectue le suivi de ses boutons en attribuant à chaque bouton un index de position. L’index est de base zéro ; autrement dit, le bouton le plus à gauche a un index égal à 0, le bouton suivant à droite a un index de 1, et ainsi de suite. Une application doit spécifier l’index d’un bouton lors de l’envoi de messages pour récupérer des informations sur le bouton ou pour définir les attributs du bouton.

Une barre d’outils met à jour les index de position lors de l’insertion et de la suppression de boutons. Une application peut récupérer l’index de position actuel d’un bouton en utilisant le message [**to \_ COMMANDTOINDEX**](tb-commandtoindex.md) . Le message spécifie l’identificateur de commande d’un bouton, et la fenêtre de la barre d’outils utilise l’identificateur pour localiser le bouton et retourner son index de position.

Tous les boutons d’une barre d’outils ont la même taille. La fonction [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) vous oblige à définir la taille initiale des boutons lorsque vous créez la barre d’outils. Lorsque vous utilisez la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , la taille initiale est définie sur les dimensions par défaut 24 par 22 pixels. Vous pouvez utiliser le message [**to \_ SETBUTTONSIZE**](tb-setbuttonsize.md) pour modifier la taille du bouton, mais vous devez le faire avant d’ajouter des boutons à la barre d’outils. Le message [**to \_ GETITEMRECT**](tb-getitemrect.md) récupère les dimensions actuelles des boutons.

Lorsque vous ajoutez une chaîne plus longue que n’importe quelle chaîne actuellement dans la barre d’outils, la barre d’outils réinitialise automatiquement la largeur de ses boutons. La largeur est définie pour s’adapter à la chaîne la plus longue dans la barre d’outils.

## <a name="enabling-customization"></a>Activation de la personnalisation

Une barre d’outils offre des fonctionnalités de personnalisation intégrées que vous pouvez mettre à la disposition de l’utilisateur en donnant à la barre d’outils le style de contrôle commun [**\_ ajustable CCS**](common-control-styles.md) . Les fonctionnalités de personnalisation permettent à l’utilisateur de faire glisser un bouton à un nouvel emplacement ou de supprimer un bouton en le faisant glisser en dehors de la barre d’outils. En outre, l’utilisateur peut double-cliquer sur la barre d’outils pour afficher la boîte de dialogue Personnaliser la barre d’outils, qui lui permet d’ajouter, de supprimer et de réorganiser les boutons de barre d’outils. Pour afficher la boîte de dialogue, utilisez le message de [**\_ personnalisation to**](tb-customize.md) . Une application détermine si les fonctionnalités de personnalisation sont disponibles pour l’utilisateur et contrôle l’étendue dans laquelle l’utilisateur peut personnaliser la barre d’outils.

Dans le cadre du processus de personnalisation, les applications doivent souvent enregistrer et restaurer l’état d’une barre d’outils. Par exemple, de nombreuses applications stockent l’état de la barre d’outils avant que l’utilisateur ne commence à personnaliser la barre d’outils au cas où l’utilisateur souhaiterait restaurer l’état d’origine de la barre d’outils. Le contrôle ToolBar ne conserve pas automatiquement un enregistrement de son état de prépersonnalisation. Votre application doit enregistrer l’état de la barre d’outils afin de la restaurer. Pour plus d’informations, consultez [utilisation des contrôles ToolBar](using-toolbar-controls.md).

## <a name="enabling-hot-tracking"></a>Activation du suivi actif

Le suivi à chaud signifie que lorsque le pointeur se déplace sur un élément, l’apparence du bouton change. Lorsque les styles visuels sont activés, les barres d’outils prennent en charge le suivi à chaud par défaut. Sinon, seuls les contrôles de barre d’outils créés avec le style à [**\_ deux dimensions TBSTYLE**](toolbar-control-and-button-styles.md) prennent en charge le suivi à chaud. Vous pouvez utiliser d’autres styles de fenêtres en combinaison avec **TBSTYLE \_ Flat** pour produire des barres d’outils qui permettent le suivi à chaud, mais qui ont une apparence différente de celle d’une barre d’outils plate. Pour plus d’informations, consultez [utilisation des contrôles ToolBar](using-toolbar-controls.md).

 

 