---
title: À propos de l’entrée de souris
description: Cette rubrique décrit l’entrée de la souris.
ms.assetid: 1f945a31-76d5-4e23-a55a-769ca114dbe9
keywords:
- entrée utilisateur, entrée de la souris
- capture de l’entrée utilisateur, entrée de la souris
- entrées de la souris
- curseur de la souris
- curseurs, entrée de la souris
- capture de la souris
- souris et verrouillage
- XBUTTONs
- configuration de la souris
- messages de la souris
- Message WM_NCHITTEST
- Fonctionnalité d’accessibilité de la souris
- Fonctionnalité d’accessibilité de la souris sonar
- roulette de la souris
- Message WM_MOUSEWHEEL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c4978babd6322102908699dbf88b68e2d3b92f57fa9bfa79b9b8c3eae88931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105788"
---
# <a name="about-mouse-input"></a>À propos de l’entrée de souris

La souris est un appareil d’entrée utilisateur important, mais facultatif pour les applications. Une application bien écrite doit inclure une interface de souris, mais elle ne doit pas dépendre uniquement de la souris pour acquérir une entrée d’utilisateur. L’application doit également fournir une prise en charge complète du clavier.

Une application reçoit l’entrée de la souris sous la forme de messages envoyés ou publiés dans son Windows.

Cette section couvre les sujets suivants :

-   [Curseur de la souris](#mouse-cursor)
-   [Capture de la souris](#mouse-capture)
-   [Souris et verrouillage](#mouse-clicklock)
-   [Configuration de la souris](#mouse-configuration)
-   [XBUTTONs](#xbuttons)
-   [Messages de la souris](#mouse-messages)
    -   [Messages de la souris de la zone cliente](#client-area-mouse-messages)
    -   [Messages de souris de la zone non cliente](#nonclient-area-mouse-messages)
    -   [Message WM \_ NCHITTEST](/windows)
-   [Sonar de la souris](#mouse-sonar)
-   [Disparition de la souris](#mouse-vanish)
-   [Roulette de la souris](#the-mouse-wheel)
-   [Activation de la fenêtre](#window-activation)

## <a name="mouse-cursor"></a>Curseur de la souris

Lorsque l’utilisateur déplace la souris, le système déplace un bitmap sur l’écran appelé le *curseur* de la souris. Le curseur de la souris contient un point d’une seule pixel appelée zone *réactive*, un point que le système suit et reconnaît comme position du curseur. Lorsqu’un événement de souris se produit, la fenêtre qui contient la zone réactive reçoit généralement le message de souris résultant de l’événement. La fenêtre n’a pas besoin d’être active ou a le focus clavier pour recevoir un message de souris.

Le système gère une variable qui contrôle la vitesse de la souris, c’est-à-dire la distance de déplacement du curseur lorsque l’utilisateur déplace la souris. Vous pouvez utiliser la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) avec l’indicateur **SPI \_ GETMOUSE** ou **SPI \_ SETMOUSE** pour récupérer ou définir la vitesse de la souris. Pour plus d’informations sur les curseurs de la souris, consultez [curseurs](/windows/desktop/menurc/cursors).

## <a name="mouse-capture"></a>Capture de la souris

Le système publie généralement un message de souris dans la fenêtre qui contient la zone réactive du curseur lorsqu’un événement de souris se produit. Une application peut modifier ce comportement à l’aide de la fonction [**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture) pour acheminer les messages de la souris vers une fenêtre spécifique. La fenêtre reçoit tous les messages de la souris jusqu’à ce que l’application appelle la fonction [**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) ou spécifie une autre fenêtre de capture, ou jusqu’à ce que l’utilisateur clique sur une fenêtre créée par un autre thread.

Lorsque la capture de la souris change, le système envoie un message [**WM \_ CAPTURECHANGED**](wm-capturechanged.md) à la fenêtre qui perd la capture de la souris. Le paramètre *lParam* du message spécifie un handle vers la fenêtre qui obtient la capture de la souris.

Seule la fenêtre de premier plan peut capturer l’entrée de la souris. Quand une fenêtre d’arrière-plan tente de capturer l’entrée de la souris, elle reçoit des messages uniquement pour les événements de souris qui se produisent lorsque la zone réactive du curseur se trouve dans la partie visible de la fenêtre.

La capture de l’entrée de la souris est utile si une fenêtre doit recevoir toutes les entrées de la souris, même lorsque le curseur se déplace à l’extérieur de la fenêtre. Par exemple, une application suit généralement la position du curseur après un événement de pointage de la souris, à la suite du curseur, jusqu’à ce qu’un événement de souris vers le haut se produise. Si une application n’a pas capturé d’entrée de souris et que l’utilisateur relâche le bouton de la souris en dehors de la fenêtre, la fenêtre ne reçoit pas le message de bouton.

Un thread peut utiliser la fonction [**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture) pour déterminer si l’une de ses fenêtres a capturé la souris. Si l’une des fenêtres du thread a capturé la souris, **GetCapture** récupère un handle vers la fenêtre.

## <a name="mouse-clicklock"></a>Souris et verrouillage

La fonctionnalité d’accessibilité du verrouillage de la souris permet à un utilisateur de verrouiller le bouton principal de la souris après un seul clic. Pour une application, le bouton semble toujours enfoncé. Pour déverrouiller le bouton, une application peut envoyer n’importe quel message de souris ou l’utilisateur peut cliquer sur n’importe quel bouton de la souris. Cette fonctionnalité permet à un utilisateur d’effectuer des combinaisons de souris complexes plus simplement. Par exemple, les utilisateurs ayant certaines limitations physiques peuvent mettre en surbrillance du texte, faire glisser des objets ou ouvrir des menus plus facilement. Pour plus d’informations, consultez les indicateurs et les notes suivants dans [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa):

-   **SPI \_ GETMOUSECLICKLOCK**
-   **SPI \_ SETMOUSECLICKLOCK**
-   **SPI \_ GETMOUSECLICKLOCKTIME**
-   **SPI \_ SETMOUSECLICKLOCKTIME**

## <a name="mouse-configuration"></a>Configuration de la souris

Bien que la souris soit un appareil d’entrée important pour les applications, tous les utilisateurs n’ont pas nécessairement une souris. Une application peut déterminer si le système comprend une souris en passant la valeur de **\_ MOUSEPRESENT SM** à la fonction [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) .

Windows prend en charge une souris avec trois boutons au maximum. Sur une souris à trois boutons, les boutons sont désignés comme des boutons gauche, central et droit. Les messages et les constantes nommées associées aux boutons de la souris utilisent les lettres L, M et R pour identifier les boutons. Le bouton d’une souris à bouton unique est considéré comme le bouton gauche. bien que Windows prenne en charge une souris avec plusieurs boutons, la plupart des applications utilisent le bouton gauche principalement et les autres au minimum, si ce n’est du tout.

Les applications peuvent également prendre en charge une roulette de souris. La roulette de la souris peut être appuyée ou pivotée. Lorsque la roulette de la souris est enfoncée, elle agit en tant que bouton central (troisième) et envoie les messages normaux du bouton central à votre application. Lorsqu’il est pivoté, un message de roulette est envoyé à votre application. Pour plus d’informations, consultez [la section roulette de la souris](#the-mouse-wheel) .

Les applications peuvent prendre en charge les boutons de commande d’application. Ces boutons, appelés boutons X, sont conçus pour permettre un accès plus facile à un navigateur Internet, à la messagerie électronique et aux services de média. Quand vous appuyez sur un bouton X, un message [**WM \_ APPCOMMAND**](wm-appcommand.md) est envoyé à votre application. Pour plus d’informations, consultez la description dans le message **WM \_ APPCOMMAND** .

Une application peut déterminer le nombre de boutons sur la souris en passant la valeur de **\_ CMOUSEBUTTONS SM** à la fonction [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) . Pour configurer la souris pour un utilisateur gauche, l’application peut utiliser la fonction [**SwapMouseButton**](/windows/win32/api/winuser/nf-winuser-swapmousebutton) pour inverser la signification des boutons gauche et droit de la souris. Le passage de la valeur **SPI \_ SETMOUSEBUTTONSWAP** à la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) est une autre façon d’inverser la signification des boutons. Notez, cependant, que la souris est une ressource partagée, si bien que l’inversion de la signification des boutons affecte toutes les applications.

## <a name="xbuttons"></a>XBUTTONs

Windows prend en charge une souris avec cinq boutons. Outre les boutons gauche, central et droit, il y a le bouton XButton1 et XBUTTON2, qui fournissent une navigation vers l’avant et vers l’arrière lors de l’utilisation de votre navigateur.

Le gestionnaire de fenêtres prend en charge le bouton XButton1 et XBUTTON2 par le biais des **\_ messages WM XBUTTON \* *_ et _* WM \_ NCXBUTTON \* *_. Le HIWORD du _* wParam** dans ces messages contient un indicateur qui spécifie le bouton X sur lequel l’utilisateur a cliqué. Étant donné que ces messages de souris tiennent également entre les constantes **WM \_ MOUSEFIRST** et **WM \_ MOUSELAST**, une application peut filtrer tous les messages de souris avec [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea).

La prise en charge suivante le bouton XButton1 et XBUTTON2 :

-   [**\_APPCOMMAND WM**](wm-appcommand.md)
-   [**\_NCXBUTTONDBLCLK WM**](wm-ncxbuttondblclk.md)
-   [**\_NCXBUTTONDOWN WM**](wm-ncxbuttondown.md)
-   [**\_NCXBUTTONUP WM**](wm-ncxbuttonup.md)
-   [**\_XBUTTONDBLCLK WM**](wm-xbuttondblclk.md)
-   [**\_XBUTTONDOWN WM**](wm-xbuttondown.md)
-   [**\_XBUTTONUP WM**](wm-xbuttonup.md)
-   [**MOUSEHOOKSTRUCTEX**](/windows/win32/api/winuser/ns-winuser-mousehookstructex)

Les API suivantes ont été modifiées pour prendre en charge les boutons suivants :

-   [**événement de souris \_**](/windows/win32/api/winuser/nf-winuser-mouse_event)
-   [**ShellProc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85))
-   [**MSLLHOOKSTRUCT**](/windows/win32/api/winuser/ns-winuser-msllhookstruct)
-   [**MOUSEINPUT**](/windows/win32/api/winuser/ns-winuser-mouseinput)
-   [**\_PARENTNOTIFY WM**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify)

Il est peu probable qu’une fenêtre enfant dans une application de composant puisse implémenter directement des commandes pour le bouton XButton1 et XBUTTON2. [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envoie donc un message [**WM \_ APPCOMMAND**](wm-appcommand.md) à une fenêtre quand l’utilisateur clique sur un bouton X. **DefWindowProc** envoie également le message **WM \_ APPCOMMAND** à sa fenêtre parente. Cela est similaire à la façon dont les menus contextuels sont appelés par un clic droit :**DefWindowProc** envoie un message [**WM \_ CONTEXTMENU**](/windows/desktop/menurc/wm-contextmenu) au menu et l’envoie également à son parent. En outre, si **DefWindowProc** reçoit un message **WM \_ APPCOMMAND** pour une fenêtre de niveau supérieur, il appelle un hook de Shell avec le code HSHELL \_ APPCOMMAND.

Des claviers supplémentaires sont pris en charge pour les fonctions de navigateur, les fonctions multimédias, le lancement d’applications et la gestion de l’alimentation. Pour plus d’informations, consultez [touches du clavier pour la navigation et d’autres fonctions](about-keyboard-input.md).

## <a name="mouse-messages"></a>Messages de la souris

La souris génère un événement d’entrée lorsque l’utilisateur déplace la souris, ou appuie ou relâche un bouton de la souris. Le système convertit les événements d’entrée de souris en messages et les publie dans la file d’attente de messages du thread approprié. Lorsque les messages de la souris sont publiés plus rapidement qu’un thread ne peut les traiter, le système ignore tous les messages de souris sauf le plus récent.

Une fenêtre reçoit un message de souris lorsqu’un événement de souris se produit alors que le curseur se trouve dans les bordures de la fenêtre ou lorsque la fenêtre a capturé la souris. Les messages de la souris sont divisés en deux groupes : les messages de zone client et les messages de zone non cliente. En règle générale, une application traite les messages de la zone cliente et ignore les messages de la zone non cliente.

Cette section couvre les sujets suivants :

-   [Messages de la souris de la zone cliente](#client-area-mouse-messages)
-   [Messages de souris de la zone non cliente](#nonclient-area-mouse-messages)
-   [Message WM \_ NCHITTEST](/windows)

### <a name="client-area-mouse-messages"></a>Messages de la souris de la zone cliente

Une fenêtre reçoit un message de la souris de la zone cliente lorsqu’un événement de souris se produit dans la zone cliente de la fenêtre. Le système publie le message [**WM \_ MOUSEMOVE**](wm-mousemove.md) dans la fenêtre lorsque l’utilisateur déplace le curseur dans la zone cliente. Il publie l’un des messages suivants lorsque l’utilisateur appuie ou relâche un bouton de la souris alors que le curseur se trouve dans la zone cliente.



| Message                                       | Signification                                     |
|-----------------------------------------------|---------------------------------------------|
| [**\_LBUTTONDBLCLK WM**](wm-lbuttondblclk.md) | Double-clic sur le bouton gauche de la souris.   |
| [**\_LBUTTONDOWN WM**](wm-lbuttondown.md)     | Le bouton gauche de la souris a été enfoncé.          |
| [**\_LBUTTONUP WM**](wm-lbuttonup.md)         | Le bouton gauche de la souris a été relâché.         |
| [**\_MBUTTONDBLCLK WM**](wm-mbuttondblclk.md) | L’utilisateur a double-cliqué sur le bouton central de la souris. |
| [**\_MBUTTONDOWN WM**](wm-mbuttondown.md)     | Le bouton central de la souris a été enfoncé.        |
| [**\_MBUTTONUP WM**](wm-mbuttonup.md)         | Le bouton central de la souris a été relâché.       |
| [**\_RBUTTONDBLCLK WM**](wm-rbuttondblclk.md) | Double-clic sur le bouton droit de la souris.  |
| [**\_RBUTTONDOWN WM**](wm-rbuttondown.md)     | Le bouton droit de la souris a été enfoncé.         |
| [**\_RBUTTONUP WM**](wm-rbuttonup.md)         | Le bouton droit de la souris a été relâché.        |
| [**\_XBUTTONDBLCLK WM**](wm-xbuttondblclk.md) | L’utilisateur a double-cliqué sur un bouton de la souris X.       |
| [**\_XBUTTONDOWN WM**](wm-xbuttondown.md)     | Un bouton X de la souris a été enfoncé.              |
| [**\_XBUTTONUP WM**](wm-xbuttonup.md)         | Un bouton X de la souris a été relâché.             |



 

En outre, une application peut appeler la fonction [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) pour que le système envoie deux autres messages. Il publie le message [**WM \_ MOUSEHOVER**](wm-mousehover.md) quand le curseur pointe sur la zone cliente pendant une certaine période. Il publie le message [**WM \_ MOUSELEAVE**](wm-mouseleave.md) lorsque le curseur quitte la zone cliente.

### <a name="message-parameters"></a>Paramètres du message

Le paramètre *lParam* d’un message de souris de la zone cliente indique la position de la zone réactive du curseur. Le mot de poids faible indique la coordonnée x de la zone réactive, et le mot de poids fort indique la coordonnée y. Les coordonnées sont spécifiées dans les coordonnées clientes. Dans le système de coordonnées client, tous les points de l’écran sont spécifiés par rapport aux coordonnées (0,0) de l’angle supérieur gauche de la zone cliente.

Le paramètre *wParam* contient des indicateurs qui indiquent l’état des autres boutons de la souris et les touches Ctrl et Maj au moment de l’événement de souris. Vous pouvez vérifier ces indicateurs lorsque le traitement des messages de la souris dépend de l’état d’un autre bouton de la souris ou de la touche CTRL ou Maj. Le paramètre *wParam* peut être une combinaison des valeurs suivantes.



| Valeur            | Description                      |
|------------------|----------------------------------|
| **\_contrôle MK**  | La touche CTRL est enfoncée.            |
| **\_LBUTTON MK**  | Le bouton gauche de la souris est enfoncé.   |
| **\_MBUTTON MK**  | Le bouton central de la souris est enfoncé. |
| **\_RBUTTON MK**  | Le bouton droit de la souris est enfoncé.  |
| **\_MAJ MK**    | La touche Maj est enfoncée.           |
| **\_Le bouton XButton1 MK** | Le premier bouton X est enfoncé.      |
| **\_XButton2 MK** | Le deuxième bouton X est enfoncé.     |



 

### <a name="double-click-messages"></a>Messages Double-Click

Le système génère un message de double-clic lorsque l’utilisateur clique deux fois de suite sur un bouton de la souris. Quand l’utilisateur clique sur un bouton, le système établit un rectangle centré autour de la zone réactive du curseur. Il marque également l’heure à laquelle le clic s’est produit. Quand l’utilisateur clique une deuxième fois sur le même bouton, le système détermine si la zone réactive est toujours dans le rectangle et calcule le temps écoulé depuis le premier clic. Si la zone réactive est toujours dans le rectangle et que le temps écoulé ne dépasse pas la valeur du délai d’attente du double-clic, le système génère un message de double-clic.

Une application peut récupérer et définir des valeurs de délai d’attente de double-clic à l’aide des fonctions [**GetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime) et [**SetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime) , respectivement. L’application peut également définir la valeur du délai d’attente du double-clic à l’aide de l’indicateur **SPI \_ SETDOUBLECLICKTIME** avec la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) . Il peut également définir la taille du rectangle utilisé par le système pour détecter les double-clics en passant les indicateurs **SPI \_ SETDOUBLECLKWIDTH** et **SPI \_ SETDOUBLECLKHEIGHT** à **SystemParametersInfo**. Notez, toutefois, que la définition de la valeur et du rectangle du délai d’attente du double-clic affecte toutes les applications.

Par défaut, une fenêtre définie par l’application ne reçoit pas de messages de double-clic. En raison de la surcharge système impliquée dans la génération de messages de double-clic, ces messages sont générés uniquement pour les fenêtres appartenant à des classes qui ont le style de classe **cs \_ DBLCLKS** . Votre application doit définir ce style lors de l’inscription de la classe de fenêtre. Pour plus d’informations, consultez [classes de fenêtre](/windows/desktop/winmsg/window-classes).

Un message de double-clic est toujours le troisième message dans une série de quatre messages. Les deux premiers messages sont les messages Button-Up et Button-Up générés par le premier clic. Le deuxième clic génère le message de double-clic suivi d’un autre message de bouton. Par exemple, double-cliquez sur le bouton gauche de la souris pour générer la séquence de message suivante :

1.  [**\_LBUTTONDOWN WM**](wm-lbuttondown.md)
2.  [**\_LBUTTONUP WM**](wm-lbuttonup.md)
3.  [**\_LBUTTONDBLCLK WM**](wm-lbuttondblclk.md)
4.  [**\_LBUTTONUP WM**](wm-lbuttonup.md)

Étant donné qu’une fenêtre reçoit toujours un message de bouton avant de recevoir un message de double-clic, une application utilise généralement un message de double-clic pour étendre une tâche qu’elle a commencée lors d’un message de bouton. par exemple, quand l’utilisateur clique sur une couleur dans la palette de couleurs de Microsoft Paint, Paint affiche la couleur sélectionnée en regard de la palette. lorsque l’utilisateur double-clique sur une couleur, Paint affiche la couleur et ouvre la boîte de dialogue **modifier les couleurs** .

### <a name="nonclient-area-mouse-messages"></a>Messages de souris de la zone non cliente

Une fenêtre reçoit un message de la souris de la zone non cliente lorsqu’un événement de souris se produit dans n’importe quelle partie d’une fenêtre, à l’exception de la zone cliente. La zone non cliente d’une fenêtre se compose de la bordure, de la barre de menus, de la barre de titre, de la barre de défilement, du menu fenêtre, du bouton réduire et du bouton Agrandir.

Le système génère des messages de zone non cliente principalement pour sa propre utilisation. Par exemple, le système utilise des messages de zone non cliente pour remplacer le curseur par une flèche à deux pointes lorsque la zone réactive du curseur se déplace dans la bordure d’une fenêtre. Une fenêtre doit passer des messages de souris de la zone non cliente à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour tirer parti de l’interface de souris intégrée.

Il y a un message de souris non client correspondant pour chaque message de la souris de la zone cliente. Les noms de ces messages sont similaires, à ceci près que les constantes nommées pour les messages de zone non cliente incluent les lettres NC. Par exemple, le déplacement du curseur dans la zone non cliente génère un message [**WM \_ NCMOUSEMOVE**](wm-ncmousemove.md) . Si vous appuyez sur le bouton gauche de la souris alors que le curseur se trouve dans la zone non cliente, un message [**WM \_ NCLBUTTONDOWN**](wm-nclbuttondown.md) est généré.

Le paramètre *lParam* d’un message de souris non client est une structure qui contient les coordonnées x et y de la zone réactive du curseur. Contrairement aux coordonnées des messages de la souris de la zone cliente, les coordonnées sont spécifiées en coordonnées d’écran plutôt qu’en coordonnées clientes. Dans le système de coordonnées de l’écran, tous les points de l’écran sont relatifs aux coordonnées (0,0) de l’angle supérieur gauche de l’écran.

Le paramètre *wParam* contient une valeur de test de positionnement, valeur qui indique où se trouve l’événement de souris dans la zone non cliente. La section suivante explique l’objectif des valeurs de test de positionnement.

### <a name="the-wm_nchittest-message"></a>Message WM \_ NCHITTEST

Chaque fois qu’un événement de souris se produit, le système envoie un message [**WM \_ NCHITTEST**](wm-nchittest.md) à la fenêtre qui contient la zone réactive du curseur ou à la fenêtre qui a capturé la souris. Le système utilise ce message pour déterminer s’il faut envoyer une zone cliente ou un message de la souris de la zone non cliente. Une application qui doit recevoir les messages de déplacement de la souris et de bouton de la souris doit transmettre le message **WM \_ NCHITTEST** à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .

Le paramètre *lParam* du message [**WM \_ NCHITTEST**](wm-nchittest.md) contient les coordonnées d’écran de la zone réactive du curseur. La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) examine les coordonnées et retourne une valeur de test d’atteinte qui indique l’emplacement de la zone réactive. La valeur du test de positionnement peut être l’une des valeurs suivantes.



| Valeur             | Emplacement de la zone réactive                                                                                                                                                                                |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HTBORDER**      | Dans la bordure d’une fenêtre qui n’a pas de bordure de redimensionnement.                                                                                                                                       |
| **HTBOTTOM**      | Dans la bordure inférieure horizontale d’une fenêtre.                                                                                                                                                         |
| **HTBOTTOMLEFT**  | Dans l’angle inférieur gauche d’une bordure de fenêtre.                                                                                                                                                        |
| **HTBOTTOMRIGHT** | Dans l’angle inférieur droit d’une bordure de fenêtre.                                                                                                                                                       |
| **HTCAPTION**     | Dans une barre de titre.                                                                                                                                                                                     |
| **HTCLIENT**      | Dans une zone cliente.                                                                                                                                                                                   |
| **HTCLOSE**       | Dans un bouton **Fermer** .                                                                                                                                                                              |
| **HTERROR**       | Sur l’arrière-plan de l’écran ou sur une ligne de séparation entre les fenêtres (identique à HTNOWHERE, sauf que la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) génère un bip système pour indiquer une erreur). |
| **HTGROWBOX**     | Dans une zone de taille (identique à **HTSIZE**).                                                                                                                                                                 |
| **HTHELP**        | Dans un bouton **d’aide** .                                                                                                                                                                               |
| **HTHSCROLL**     | Dans une barre de défilement horizontale.                                                                                                                                                                         |
| **HTLEFT**        | Dans la bordure gauche d’une fenêtre.                                                                                                                                                                     |
| **HTMENU**        | Dans un menu.                                                                                                                                                                                          |
| **HTMAXBUTTON**   | Dans un bouton **agrandir** .                                                                                                                                                                           |
| **HTMINBUTTON**   | Dans un bouton **réduire** .                                                                                                                                                                           |
| **HTNOWHERE**     | Sur l’arrière-plan de l’écran ou sur une ligne de séparation entre les fenêtres.                                                                                                                                     |
| **HTREDUCE**      | Dans un bouton **réduire** .                                                                                                                                                                           |
| **HTRIGHT**       | Dans la bordure droite d’une fenêtre.                                                                                                                                                                    |
| **HTSIZE**        | Dans une zone de taille (identique à **HTGROWBOX**).                                                                                                                                                              |
| **HTSYSMENU**     | Dans un menu **système** ou dans un bouton **Fermer** dans une fenêtre enfant.                                                                                                                                    |
| **HTTOP**         | Dans la bordure supérieure horizontale d’une fenêtre.                                                                                                                                                         |
| **HTTOPLEFT**     | Dans l’angle supérieur gauche d’une bordure de fenêtre.                                                                                                                                                        |
| **HTTOPRIGHT**    | Dans l’angle supérieur droit d’une bordure de fenêtre.                                                                                                                                                       |
| **HTTRANSPARENT** | Dans une fenêtre actuellement couverte par une autre fenêtre dans le même thread.                                                                                                                                 |
| **HTVSCROLL**     | Dans la barre de défilement verticale.                                                                                                                                                                         |
| **HTZOOM**        | Dans un bouton **agrandir** .                                                                                                                                                                           |



 

Si le curseur se trouve dans la zone cliente d’une fenêtre, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne la valeur du test de positionnement **HTCLIENT** à la procédure de fenêtre. Lorsque la procédure de fenêtre retourne ce code au système, le système convertit les coordonnées d’écran de la zone réactive du curseur en coordonnées clientes, puis publie le message approprié de la souris de la zone cliente.

La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne l’une des autres valeurs de test de positionnement lorsque la zone réactive du curseur se trouve dans la zone non cliente d’une fenêtre. Lorsque la procédure de fenêtre retourne l’une de ces valeurs de test de positionnement, le système publie un message de souris de la zone non cliente, en plaçant la valeur de test de positionnement dans le paramètre *wParam* du message et les coordonnées du curseur dans le paramètre *lParam* .

## <a name="mouse-sonar"></a>Sonar de la souris

La fonctionnalité d’accessibilité de la souris sonar présente brièvement plusieurs cercles concentriques autour du pointeur lorsque l’utilisateur appuie sur la touche CTRL et la relâche. Cette fonctionnalité permet à un utilisateur de localiser le pointeur de la souris sur un écran encombré ou dont la résolution est élevée, sur un moniteur de qualité médiocre ou pour les utilisateurs ayant une vision altérée. Pour plus d’informations, consultez les indicateurs suivants dans [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa):

**SPI \_ GETMOUSESONAR**

**SPI \_ SETMOUSESONAR**

## <a name="mouse-vanish"></a>Disparition de la souris

La fonctionnalité d’accessibilité de la souris masque le pointeur lorsque l’utilisateur tape. Le pointeur de la souris réapparaît lorsque l’utilisateur déplace la souris. Cette fonctionnalité empêche le pointeur de masquer le texte tapé, par exemple dans un message électronique ou un autre document. Pour plus d’informations, consultez les indicateurs suivants dans [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa):

**SPI \_ GETMOUSEVANISH**

**SPI \_ SETMOUSEVANISH**

## <a name="the-mouse-wheel"></a>Roulette de la souris

La roulette de la souris combine les fonctionnalités d’une roue et le bouton de la souris. La roulette a des crans discrets, uniformément espacés. Lorsque vous faites pivoter la roue, un message de roue est envoyé à votre application à mesure que chaque grugeage est rencontré. le bouton roulette peut également fonctionner comme un bouton normal Windows central (troisième). Le fait d’appuyer sur la roulette de la souris pour envoyer des messages [**WM \_ MBUTTONUP**](wm-mbuttonup.md) et [**WM \_ MBUTTONDOWN**](wm-mbuttondown.md) standard. Le fait de double-cliquer sur le troisième bouton envoie le message [**\_ MBUTTONDBLCLK WM**](wm-mbuttondblclk.md) standard.

La roulette de la souris est prise en charge via le message [**WM \_ MOUSEWHEEL**](wm-mousewheel.md) .

La rotation de la souris envoie le message [**WM \_ MOUSEWHEEL**](wm-mousewheel.md) à la fenêtre Focus. La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) propage le message au parent de la fenêtre. Il ne doit y avoir aucun transfert interne du message, car **DefWindowProc** le propage vers le haut de la chaîne parente jusqu’à ce qu’une fenêtre qui le traite soit trouvée.

### <a name="determining-the-number-of-scroll-lines"></a>Détermination du nombre de lignes de défilement

Les applications doivent utiliser la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) pour récupérer le nombre de lignes qu’un document défile pour chaque opération de défilement (grugeage de roulette). Pour récupérer le nombre de lignes, une application effectue l’appel suivant :


```
SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 0, pulScrollLines, 0)
```



La variable « pulScrollLines » pointe vers une valeur entière non signée qui reçoit le nombre suggéré de lignes à faire défiler lorsque la roulette de la souris pivote sans touches de modification :

-   Si ce nombre est 0, aucun défilement ne doit se produire.
-   Si ce nombre est **\_ PAGESCROLL de roue**, un rouleau de roulette doit être interprété comme un clic unique dans les zones de page suivante ou de page précédente de la barre de défilement.
-   Si le nombre de lignes à faire défiler est supérieur au nombre de lignes affichables, l’opération de défilement doit également être interprétée comme une opération page suivante ou page précédente.

La valeur par défaut du nombre de lignes de défilement est 3. Si un utilisateur modifie le nombre de lignes de défilement, à l’aide de la feuille de propriétés de la souris dans le panneau de configuration, le système d’exploitation diffuse un message [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) à toutes les fenêtres de niveau supérieur pour lesquelles **SPI \_ SETWHEELSCROLLLINES** est spécifié. Quand une application reçoit le **message \_ SETTINGCHANGE WM** , elle peut alors récupérer le nouveau nombre de lignes de défilement en appelant :


```
SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 0, pulScrollLines, 0)
```



### <a name="controls-that-scroll"></a>Contrôles qui défilent

Le tableau ci-dessous répertorie les contrôles avec des fonctionnalités de défilement (y compris les lignes de défilement définies par l’utilisateur). 

| Contrôler                 | Défilement                                                                                                                                                               |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Modifier le contrôle            | Vertical et horizontal.                                                                                                                                                |
| Contrôle zone de liste        | Vertical et horizontal.                                                                                                                                                |
| Combo box               | Lorsqu’ils ne sont pas déplacés, chaque défilement récupère l’élément suivant ou précédent. Lorsqu’elle est déroulée, chaque défilement transmet le message à la zone de liste, qui fait défiler en conséquence. |
| CMD (ligne de commande)      | Vertical.                                                                                                                                                               |
| Arborescence               | Vertical et horizontal.                                                                                                                                                |
| Mode Liste               | Vertical et horizontal.                                                                                                                                                |
| Défilement vers le haut/vers le haut         | Un élément à la fois.                                                                                                                                                     |
| Défilements TrackBar        | Un élément à la fois.                                                                                                                                                     |
| Édition enrichie de Microsoft 1,0 | Vertical. notez que le client Exchange possède ses propres versions des contrôles d’affichage de liste et d’arborescence qui n’offrent pas de prise en charge de roulette.                                        |
| Édition enrichie de Microsoft 2,0 | Vertical.                                                                                                                                                               |



 

### <a name="detecting-a-mouse-with-a-wheel"></a>Détection d’une souris avec une roue

Pour déterminer si une souris avec roulette est connectée, appelez [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) avec le **SM \_ MOUSEWHEELPRESENT**. Une valeur de retour **true** indique que la souris est connectée.

L’exemple suivant est issu de la procédure de fenêtre pour un contrôle d’édition multiligne :


```
BOOL ScrollLines(
     PWNDDATA pwndData,   //scrolls the window indicated
     int cLinesToScroll); //number of times

short gcWheelDelta; //wheel delta from roll
PWNDDATA pWndData; //pointer to structure containing info about the window
UINT gucWheelScrollLines=0;//number of lines to scroll on a wheel rotation

gucWheelScrollLines = SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 
                             0, 
                             pulScrollLines, 
                             0);

case WM_MOUSEWHEEL:
    /*
     * Do not handle zoom and datazoom.
     */
    if (wParam & (MK_SHIFT | MK_CONTROL)) {
        goto PassToDefaultWindowProc;
    }

    gcWheelDelta -= (short) HIWORD(wParam);
    if (abs(gcWheelDelta) >= WHEEL_DELTA && gucWheelScrollLines > 0) 
    {
        int cLineScroll;

        /*
         * Limit a roll of one (1) WHEEL_DELTA to
         * scroll one (1) page.
         */
        cLineScroll = (int) min(
                (UINT) pWndData->ichLinesOnScreen - 1,
                gucWheelScrollLines);

        if (cLineScroll == 0) {
            cLineScroll++;
        }

        cLineScroll *= (gcWheelDelta / WHEEL_DELTA);
        assert(cLineScroll != 0);

        gcWheelDelta = gcWheelDelta % WHEEL_DELTA;
        return ScrollLines(pWndData, cLineScroll);
    }

    break;
```



## <a name="window-activation"></a>Activation de la fenêtre

Quand l’utilisateur clique sur une fenêtre de niveau supérieur inactive ou sur la fenêtre enfant d’une fenêtre de niveau supérieur inactive, le système envoie le message [**WM \_ MOUSEACTIVATE**](wm-mouseactivate.md) (entre autres) à la fenêtre de niveau supérieur ou enfant. Le système envoie ce message après avoir publié le message [**WM \_ NCHITTEST**](wm-nchittest.md) dans la fenêtre, mais avant de publier le message de bouton. Lorsque **WM \_ MOUSEACTIVATE** est passé à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , le système active la fenêtre de niveau supérieur, puis publie le message de bouton vers le haut dans la fenêtre de niveau supérieur ou enfant.

En traitant [**WM \_ MOUSEACTIVATE**](wm-mouseactivate.md), une fenêtre peut contrôler si la fenêtre de niveau supérieur devient la fenêtre active à la suite d’un clic de souris et si la fenêtre sur laquelle l’utilisateur a cliqué reçoit le message de bouton suivant. Pour ce faire, il renvoie l’une des valeurs suivantes après le traitement de **WM \_ MOUSEACTIVATE**.



| Valeur                    | Signification                                                              |
|--------------------------|----------------------------------------------------------------------|
| **\_activation ma**         | Active la fenêtre et n’ignore pas le message de la souris.         |
| **MA \_ NOactivate**       | N’active pas la fenêtre et n’ignore pas le message de la souris. |
| **MA \_ ACTIVATEANDEAT**   | Active la fenêtre et ignore le message de la souris.                 |
| **MA \_ NOACTIVATEANDEAT** | N’active pas la fenêtre mais ignore le message de la souris.         |

## <a name="see-also"></a>Voir aussi

[Tirer parti du High-Definition mouvement de la souris](../dxtecharts/taking-advantage-of-high-dpi-mouse-movement.md)