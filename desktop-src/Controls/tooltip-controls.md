---
title: À propos des contrôles ToolTip
description: Les info-bulles s’affichent automatiquement ou s’affichent quand l’utilisateur place le pointeur de la souris sur un outil ou un autre élément d’interface utilisateur.
ms.assetid: 1020cec7-57b4-4463-9419-f80fd14fa12c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9c1042523c86e794865da5d38fb023ee37d60b4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115954"
---
# <a name="about-tooltip-controls"></a>À propos des contrôles ToolTip

Les info-bulles s’affichent automatiquement ou s’affichent quand l’utilisateur place le pointeur de la souris sur un outil ou un autre élément d’interface utilisateur. L’info-bulle apparaît près du pointeur et disparaît lorsque l’utilisateur clique sur un bouton de la souris, éloigne le pointeur de l’outil ou attend simplement quelques secondes.

le contrôle tooltip de l’illustration suivante affiche des informations sur un fichier sur le bureau Windows. Lorsque vous déplacez la souris sur l’illustration, vous devez également voir une info-bulle en direct qui contient du texte descriptif.

![capture d’écran montrant du texte dans une info-bulle qui apparaît sur un fichier sur le Bureau](images/tt-desktop.png)

Cette section décrit le fonctionnement des contrôles ToolTip et la façon dont vous les créez.

-   [Comportement et apparence de l’info-bulle](#tooltip-behavior-and-appearance)
-   [Création de contrôles ToolTip](#creating-tooltip-controls)
-   [Activation des contrôles ToolTip](#activating-tooltip-controls)
-   [Outils de prise en charge](#supporting-tools)
-   [Affichage du texte](#displaying-text)
-   [Messagerie et notification](#messaging-and-notification)
-   [Test des résultats](#hit-testing)
-   [Traitement des messages par défaut](#default-message-processing)

## <a name="tooltip-behavior-and-appearance"></a>Comportement et apparence de l’info-bulle

Les contrôles ToolTip peuvent afficher une seule ligne de texte ou plusieurs lignes. Leurs angles peuvent être arrondis ou carrés. Ils peuvent avoir ou non une tige qui pointe vers les outils comme une bulle d’outils de synthèse vocale. Le texte d’info-bulle peut être stationnaire ou peut se déplacer avec le pointeur de la souris, appelé suivi. Le texte fixe peut être affiché à côté d’un outil ou il peut être affiché sur un outil, appelé sur place. Les info-bulles standard sont fixes, affichent une seule ligne de texte, ont des angles carrés et n’ont pas de tige pointant sur l’outil.

Les info-bulles de suivi, qui sont prises en charge par la [version 4,70](common-control-versions.md) des contrôles communs, modifient la position sur l’écran dynamiquement. En mettant à jour rapidement la position, ces contrôles ToolTip semblent se déplacer correctement ou « suivre ». Elles sont utiles lorsque vous souhaitez que le texte info-bulle suive la position du pointeur de la souris à mesure qu’il se déplace. Pour plus d’informations sur le suivi des info-bulles et un exemple de code qui montre comment les créer, consultez [suivi des info-bulles](using-tooltip-contro.md).

Les info-bulles multilignes, qui sont également prises en charge par la version 4,70 des contrôles communs, affichent du texte sur plusieurs lignes. Ils sont utiles pour afficher des messages longs. Pour plus d’informations et pour obtenir un exemple qui montre comment créer des info-bulles multilignes, consultez [info-bulles multilignes](using-tooltip-contro.md).

Les info-bulles sont affichées dans une zone avec des angles arrondis et une tige pointant sur l’outil. Il peut s’agir d’une ligne ou d’une ligne multiligne. L’illustration suivante montre une info-bulle avec la tige et le rectangle dans leurs positions par défaut. Pour plus d’informations sur les info-bulles et un exemple qui montre comment les créer, consultez [utilisation de contrôles ToolTip](using-tooltip-contro.md).

![capture d’écran montrant une info-bulle contenant une ligne de texte, positionnée au-dessus d’un bouton sur une boîte de dialogue](images/tt-balloon.png)

Une info-bulle peut également comporter un texte de titre et une icône, comme indiqué dans l’illustration suivante. Notez que l’info-bulle doit contenir du texte. s’il n’a qu’un texte de titre, l’info-bulle ne s’affiche pas. De même, l’icône n’apparaît pas, sauf s’il existe un titre.

![capture d’écran montrant une info-bulle avec une icône, un titre et un texte, positionné sous un bouton dans une boîte de dialogue](images/tt-titled.png)

Parfois, les chaînes de texte sont découpées, car elles sont trop longues pour s’afficher complètement dans une petite fenêtre. Les info-bulles sur place sont utilisées pour afficher des chaînes de texte pour les objets qui ont été découpés, tels que le nom de fichier dans l’illustration suivante. Pour obtenir un exemple qui montre comment créer des info-bulles sur place, consultez [info-bulles sur place](using-tooltip-contro.md).

![capture d’écran montrant une info-bulle contenant un nom de fichier positionné en regard d’une icône de fichier dans un contrôle d’arborescence](images/tt-inplace.png)

Le curseur doit pointer sur un outil pendant une période de temps avant que l’info-bulle ne s’affiche. La durée par défaut de ce délai est contrôlée par le double-clic de l’utilisateur et correspond généralement à environ une demi-seconde. Pour spécifier une valeur de délai d’attente non définie par défaut, envoyez au contrôle ToolTip un message [**atténuation \_ SETDELAYTIME**](ttm-setdelaytime.md) .

## <a name="creating-tooltip-controls"></a>Création de contrôles ToolTip

Pour créer un contrôle ToolTip, appelez [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) et spécifiez la classe de fenêtre d' [**info-bulle \_ Class**](common-control-window-classes.md) . Cette classe est inscrite lors du chargement de la DLL de contrôles communs. Pour vous assurer que cette DLL est chargée, incluez la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) dans votre application. Vous devez définir explicitement un contrôle ToolTip comme étant le plus haut. Dans le cas contraire, elle peut être couverte par la fenêtre parente. Le fragment de code suivant montre comment créer un contrôle ToolTip.


```
HWND hwndTip = CreateWindowEx(NULL, TOOLTIPS_CLASS, NULL,
                            WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP,
                            CW_USEDEFAULT, CW_USEDEFAULT,
                            CW_USEDEFAULT, CW_USEDEFAULT,
                            hwndParent, NULL, hinstMyDll,
                            NULL);

SetWindowPos(hwndTip, HWND_TOPMOST,0, 0, 0, 0,
             SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE);
```



La procédure de fenêtre pour le contrôle ToolTip définit automatiquement la taille, la position et la visibilité du contrôle. La hauteur de la fenêtre d’info-bulle est basée sur la hauteur de la police actuellement sélectionnée dans le contexte de périphérique pour le contrôle ToolTip. La largeur varie en fonction de la longueur de la chaîne actuellement dans la fenêtre d’info-bulle.

## <a name="activating-tooltip-controls"></a>Activation des contrôles ToolTip

Un contrôle ToolTip peut être actif ou inactif. Lorsqu’il est actif, le texte d’info-bulle s’affiche lorsque le pointeur de la souris se trouve sur un outil. Lorsqu’il est inactif, le texte d’info-bulle ne s’affiche pas, même si le pointeur se trouve sur un outil. Le message d' [**\_ activation atténuation**](ttm-activate.md) active et désactive un contrôle ToolTip.

## <a name="supporting-tools"></a>Outils de prise en charge

Un contrôle ToolTip peut prendre en charge n’importe quel nombre d’outils. Pour prendre en charge un outil particulier, vous devez inscrire l’outil avec le contrôle ToolTip en envoyant le contrôle au message [**atténuation \_ ADDTOOL**](ttm-addtool.md) . Le message inclut l’adresse d’une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , qui fournit les informations dont le contrôle ToolTip a besoin pour afficher le texte de l’outil. Le membre **uID** de la structure **TOOLINFO** est défini par l’application. Chaque fois que vous ajoutez un outil, votre application fournit un identificateur unique. Le membre **cbSize** de la structure **TOOLINFO** est requis et doit spécifier la taille de la structure.

Un contrôle ToolTip prend en charge les outils implémentés en tant que fenêtres (telles que les fenêtres enfants ou les fenêtres de contrôle) et en tant que zones rectangulaires dans la zone cliente d’une fenêtre. Lorsque vous ajoutez un outil implémenté en tant que zone rectangulaire, le membre **HWND** de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) doit spécifier le handle de la fenêtre qui contient la zone, et le membre **Rect** doit spécifier les coordonnées clientes du rectangle englobant de la zone. En outre, le membre **uID** doit spécifier l’identificateur défini par l’application pour l’outil.

Lorsque vous ajoutez un outil implémenté en tant que fenêtre, le membre **uID** de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) doit contenir le handle de fenêtre de l’outil. En outre, le membre **uFlags** doit spécifier la valeur **ttf \_ IDISHWND** , qui indique au contrôle ToolTip d’interpréter le membre **uID** comme un handle de fenêtre.

## <a name="displaying-text"></a>Affichage du texte

Lorsque vous ajoutez un outil à un contrôle ToolTip, le membre **lpszText** de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) doit spécifier l’adresse de la chaîne à afficher pour l’outil. Après avoir ajouté un outil, vous pouvez modifier le texte à l’aide du message [**atténuation \_ UPDATETIPTEXT**](ttm-updatetiptext.md) .

Si le mot de poids fort de **lpszText** est égal à zéro, le mot de poids faible doit être l’identificateur d’une ressource de type chaîne. Lorsque le contrôle ToolTip a besoin du texte, le système charge la ressource de chaîne spécifiée à partir de l’instance d’application identifiée par le membre **HINST** de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .

Si vous spécifiez la \_ valeur LPSTR TEXTCALLBACK dans le membre **lpszText** , le contrôle ToolTip notifie la fenêtre spécifiée dans le membre **HWND** de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)chaque fois que le contrôle ToolTip a besoin d’afficher du texte pour l’outil. Le contrôle ToolTip envoie le code de notification [ttn \_ GETDISPINFO](ttn-getdispinfo.md) à la fenêtre. Le message inclut l’adresse d’une structure [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) , qui contient le handle de fenêtre ainsi que l’identificateur défini par l’application pour l’outil. La fenêtre examine la structure pour déterminer l’outil pour lequel le texte est nécessaire, et remplit les membres de structure appropriés avec les informations dont le contrôle ToolTip a besoin pour afficher la chaîne.

> [!Note]  
> La longueur maximale du texte d’info-bulle standard est de 80 caractères. Pour plus d’informations, consultez la structure [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) . Le texte info-bulle multiligne peut être plus long.

 

De nombreuses applications créent des barres d’outils qui contiennent des outils qui correspondent à des commandes de menu. Pour ces outils, il est pratique que le contrôle ToolTip affiche le même texte que l’élément de menu correspondant. Le système supprime automatiquement les caractères d’accélérateur esperluette (&) de toutes les chaînes passées à un contrôle ToolTip, puis met fin à la chaîne au premier caractère de tabulation ( \\ t), à moins que le contrôle n’ait le style de [**\_ préfixe TTS**](tooltip-styles.md) .

Pour récupérer le texte d’un outil, utilisez le message [**atténuation \_ GETTEXT**](ttm-gettext.md) .

## <a name="messaging-and-notification"></a>Messagerie et notification

Le texte info-bulle s’affiche normalement lorsque le pointeur de la souris est placé sur une zone, généralement le rectangle défini par un outil tel qu’un contrôle bouton. toutefois, Microsoft Windows envoie uniquement des messages liés à la souris à la fenêtre qui contient le pointeur, pas le contrôle tooltip lui-même. Les informations relatives à la souris doivent être relayées vers le contrôle ToolTip afin qu’il affiche le texte d’info-bulle à l’heure et au lieu appropriés.

Vous pouvez avoir des messages relayés automatiquement dans les cas suivants :

-   L’outil est un contrôle ou est défini comme un rectangle dans la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) de l’outil.
-   La fenêtre associée à l’outil se trouve dans le même thread que le contrôle ToolTip.

Si ces deux conditions sont remplies, définissez l’indicateur de **\_ sous-classe ttf** dans le membre **UFlags** de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) de l’outil lorsque vous ajoutez l’outil au contrôle ToolTip avec [**atténuation \_ ADDTOOL**](ttm-addtool.md). Les messages de souris nécessaires sont ensuite relayés automatiquement vers le contrôle ToolTip.

La définition de la **\_ sous-classe ttf** pour que les messages de souris relayés vers le contrôle soient suffisants dans la plupart des cas. Toutefois, il ne fonctionne pas dans les cas où il n’existe aucune connexion directe entre le contrôle ToolTip et la fenêtre de l’outil. Par exemple, si un outil est implémenté en tant que zone rectangulaire dans une fenêtre définie par l’application, la procédure de fenêtre reçoit les messages de la souris. La définition de la **\_ sous-classe ttf** suffit pour s’assurer qu’elle est passée au contrôle. Toutefois, si un outil est implémenté en tant que fenêtre définie par le système, les messages de la souris sont envoyés à cette fenêtre et ne sont pas directement disponibles pour l’application. Dans ce cas, vous devez sous-classer la fenêtre ou utiliser un raccordement de message pour accéder aux messages de la souris. Vous devez ensuite relayer explicitement les messages de la souris vers le contrôle ToolTip avec [**atténuation \_ RELAYEVENT**](ttm-relayevent.md). Pour obtenir un exemple d’utilisation de **atténuation \_ RELAYEVENT**, consultez [suivi des info-bulles](using-tooltip-contro.md).

Lorsqu’un contrôle ToolTip reçoit un message [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) , il détermine si le pointeur de la souris se trouve dans le rectangle englobant d’un outil. Si c’est le cas, le contrôle ToolTip définit un minuteur. À la fin de l’intervalle de délai d’attente, le contrôle ToolTip vérifie la position du pointeur pour voir s’il a été déplacé. Si ce n’est pas le cas, le contrôle ToolTip récupère le texte de l’outil et affiche l’info-bulle. Le contrôle ToolTip continue d’afficher la fenêtre jusqu’à ce qu’il reçoive un message de bouton ou de bouton vers le haut relayé ou jusqu’à ce qu’un message **WM \_ MOUSEMOVE** indique que le pointeur a été déplacé en dehors du rectangle englobant de l’outil.

Un contrôle ToolTip a en fait trois durées d’expiration associées. La durée initiale est l’heure à laquelle le pointeur de la souris doit rester immobile dans le rectangle englobant d’un outil avant que la fenêtre d’info-bulle ne s’affiche. La durée du réaffichage correspond à la longueur du délai avant l’affichage des fenêtres d’info-bulle suivantes lorsque le pointeur se déplace d’un outil à un autre. La durée contextuelle est l’heure à laquelle la fenêtre d’info-bulle reste affichée avant d’être masquée. Autrement dit, si le pointeur reste immobile dans le rectangle englobant après l’affichage de la fenêtre d’info-bulle, la fenêtre d’info-bulle est automatiquement masquée à la fin de la durée de la fenêtre contextuelle. Vous pouvez ajuster toutes les durées de délai d’attente à l’aide du message [**atténuation \_ SETDELAYTIME**](ttm-setdelaytime.md) .

Si une application comprend un outil implémenté comme zone rectangulaire et que la taille ou la position du contrôle change, l’application peut utiliser le message [**atténuation \_ NEWTOOLRECT**](ttm-newtoolrect.md) pour signaler la modification au contrôle ToolTip. Une application n’a pas besoin de signaler les modifications de taille et de position pour un outil implémenté en tant que fenêtre, car le contrôle ToolTip utilise le handle de fenêtre de l’outil pour déterminer si le pointeur de la souris se trouve sur l’outil, et non sur le rectangle englobant de l’outil.

Quand une info-bulle va être affichée, le contrôle ToolTip envoie à la fenêtre propriétaire un code de notification [ttn \_ Show](ttn-show.md) . La fenêtre propriétaire reçoit un code de notification [ \_ pop ttn](ttn-pop.md) quand une info-bulle va être masquée. Chaque code de notification est envoyé dans le contexte d’un message [**WM \_ Notify**](wm-notify.md) .

## <a name="hit-testing"></a>Test des résultats

Le message [**atténuation \_ HITTEST**](ttm-hittest.md) vous permet de récupérer des informations qu’un contrôle ToolTip gère à propos de l’outil occupant un point particulier. Le message inclut une structure [**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) qui contient un handle de fenêtre, les coordonnées d’un point et l’adresse d’une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . Le contrôle ToolTip détermine si un outil occupe le point et, si c’est le cas, remplit **TOOLINFO** avec des informations sur l’outil.

## <a name="default-message-processing"></a>Traitement des messages par défaut

Le tableau suivant décrit les messages traités par la procédure de fenêtre pour le contrôle ToolTip.



| Message                                        | Description                                                                                                                                                                                                                                                       |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**création de WM \_**](/windows/desktop/winmsg/wm-create)             | Garantit que le contrôle ToolTip a les styles de fenêtre [**\_ contextuelle**](/windows/desktop/winmsg/window-styles) [**WS \_ ex \_ TOOLWINDOW**](/windows/desktop/winmsg/window-styles) et WS. Elle alloue également de la mémoire et initialise des variables internes. |
| [**\_destructeur WM**](/windows/desktop/winmsg/wm-destroy)           | Libère les ressources allouées pour le contrôle ToolTip.                                                                                                                                                                                                                |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)           | Retourne le handle de la police que le contrôle ToolTip utilisera pour dessiner du texte.                                                                                                                                                                                    |
| [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)     | Masque la fenêtre d’info-bulle.                                                                                                                                                                                                                                         |
| [**\_peinture WM**](/windows/desktop/gdi/wm-paint)                  | Dessine la fenêtre d’info-bulle.                                                                                                                                                                                                                                         |
| [**\_SetFont WM**](/windows/desktop/winmsg/wm-setfont)           | Définit le handle de la police que le contrôle ToolTip utilisera pour dessiner du texte.                                                                                                                                                                                       |
| [**\_minuteur WM**](/windows/desktop/winmsg/wm-timer)               | Masque la fenêtre d’info-bulle si l’outil a changé de position ou si le pointeur de la souris est déplacé en dehors de l’outil. Dans le cas contraire, elle affiche la fenêtre d’info-bulle.                                                                                                             |
| [**\_WININICHANGE WM**](/windows/desktop/winmsg/wm-wininichange) | Réinitialise les variables internes qui sont basées sur les métriques du système.                                                                                                                                                                                                       |



 

 

 