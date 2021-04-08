---
title: À propos des contrôles TrackBar
description: Un TrackBar est une fenêtre qui contient un curseur (parfois appelé curseur de défilement) dans un canal et des graduations facultatives. Lorsque l’utilisateur déplace le curseur, à l’aide de la souris ou des touches de direction, le TrackBar envoie des messages de notification pour indiquer la modification.
ms.assetid: 9fc7bef8-da1d-493b-9a9a-3770873713f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83e364f57a094ed5a29369a00a112150d0282f24
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730492"
---
# <a name="about-trackbar-controls"></a>À propos des contrôles TrackBar

Un TrackBar est une fenêtre qui contient un curseur (parfois appelé curseur de défilement) dans un canal et des graduations facultatives. Lorsque l’utilisateur déplace le curseur, à l’aide de la souris ou des touches de direction, le TrackBar envoie des messages de notification pour indiquer la modification.

-   [Plage de sélection](#selection-range)
-   [Messages TrackBar](#trackbar-messages)
-   [Messages de notification TrackBar](#trackbar-notification-messages)
-   [Traitement du message TrackBar par défaut](#default-trackbar-message-processing)
-   [Info-bulles de TrackBar](#trackbar-tooltips)

Les Trackbars sont utiles lorsque vous souhaitez que l’utilisateur sélectionne une valeur d’entier non signé discret ou un ensemble de valeurs entières non signées consécutives dans une plage. Par exemple, vous pouvez utiliser un TrackBar pour permettre à l’utilisateur de définir la vitesse de répétition du clavier en déplaçant le curseur vers une graduation donnée. L’illustration suivante montre un TrackBar typique.

![capture d’écran d’un TrackBar avec des étiquettes aux extrémités pour une vitesse lente et rapide](images/tkb-simple.png)

Le curseur d’un TrackBar se déplace par incréments que vous spécifiez au moment de sa création. Les valeurs de cette plage sont désignées par le terme « unités logiques ». Par exemple, si vous spécifiez que la barre de défilement doit avoir des unités logiques comprises entre 0 et 5, le curseur ne peut occuper que six positions : une position à gauche du TrackBar et une position pour chaque incrément de la plage. En règle générale, chacune de ces positions est identifiée par une graduation ; Toutefois, le nombre de graduations est arbitraire et peut être inférieur au nombre de positions logiques.

Vous créez un TrackBar à l’aide de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , en spécifiant la classe de fenêtre de la [**\_ classe TrackBar**](common-control-window-classes.md) . Après avoir créé un TrackBar, vous pouvez utiliser des messages TrackBar pour définir et récupérer un grand nombre de ses propriétés. Les modifications que vous pouvez apporter incluent la définition des positions minimale et maximale pour le curseur, le dessin des graduations, la définition d’une plage de sélection et le repositionnement du curseur.

## <a name="selection-range"></a>Plage de sélection

Si vous créez un TrackBar avec le style [**tbs \_ ENABLESELRANGE**](trackbar-control-styles.md) , vous pouvez spécifier une plage de sélection. La barre de défilement met en surbrillance la plage de sélection et affiche des graduations triangulaires au début et à la fin, comme indiqué dans l’illustration suivante.

![capture d’écran d’un TrackBar avec une plage mise en surbrillance](images/tkb-selrange.png)

La plage de sélection du TrackBar n’affecte en aucune manière ses fonctionnalités. C’est à l’application d’implémenter la plage. Vous pouvez effectuer cette opération de l’une des manières suivantes :

-   Utilisez une plage de sélection pour permettre à l’utilisateur de définir des valeurs maximales et minimales pour un paramètre. Par exemple, l’utilisateur peut déplacer le curseur vers une position, puis cliquer sur un bouton intitulé « max ». L’application définit ensuite la plage de sélection pour afficher les valeurs choisies par l’utilisateur.
-   Limitez le déplacement du curseur à une sous-plage prédéterminée dans le contrôle, en gérant la notification [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) et en désautorisant tout mouvement en dehors de la plage de sélection. Vous pouvez effectuer cette opération, par exemple, si la plage de valeurs disponibles pour l’utilisateur peut changer en raison d’autres choix effectués par l’utilisateur ou en fonction des ressources disponibles.

## <a name="trackbar-messages"></a>Messages TrackBar

Les unités logiques d’un TrackBar sont l’ensemble de valeurs contiguës que le TrackBar peut représenter. Elles sont généralement définies en spécifiant la plage de valeurs possibles avec un message [**TBM \_ SetRange**](tbm-setrange.md) dès que le TrackBar a été créé. Les applications peuvent modifier dynamiquement la plage à l’aide de **TBM \_ SetRange**, [**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)ou [**TBM \_ SETRANGEMIN**](tbm-setrangemin.md).

Pour récupérer la position du curseur (autrement dit, la valeur choisie par l’utilisateur), utilisez le message [**TBM \_ GETPOS**](tbm-getpos.md) . Pour définir la position du curseur, utilisez le message [**TBM \_ SetPos**](tbm-setpos.md) .

Un TrackBar affiche automatiquement les graduations au début et à la fin, sauf si vous spécifiez le style [**tbs \_ notiques**](trackbar-control-styles.md) . (Dans l’éditeur de ressources Microsoft Visual Studio, cela signifie affecter la valeur false à la propriété Tick Marks.) Vous pouvez utiliser le style des [**\_ graduations tbs**](trackbar-control-styles.md) pour afficher automatiquement des graduations supplémentaires à intervalles réguliers le long du TrackBar. Par défaut, un suivi de la barre de défilement **tbs \_** affiche une graduation à chaque incrément de la plage du TrackBar. Pour spécifier un intervalle différent pour les graduations automatiques, envoyez le message [**TBM \_ SETTICFREQ**](tbm-setticfreq.md) au TrackBar. Par exemple, vous pouvez utiliser ce message pour afficher uniquement 10 graduations dans une plage comprise entre 1 et 100.

Pour définir la position d’une graduation, envoyez le message [**TBM \_ SETTIC**](tbm-settic.md) . Un TrackBar gère un tableau de valeurs DWORD qui stocke la position de chaque graduation. Le tableau n’inclut pas les première et dernière graduations, que le TrackBar crée automatiquement. Vous pouvez spécifier un index dans ce tableau lorsque vous envoyez le message [**TBM \_ GETTIC**](tbm-gettic.md) pour récupérer la position de la graduation correspondante. Vous pouvez également envoyer le message [**TBM \_ GETPTICS**](tbm-getptics.md) pour récupérer un pointeur vers le tableau. Le nombre d’éléments dans le tableau est égal à deux fois inférieur au nombre de cycles retourné par le message [**TBM \_ GETNUMTICS**](tbm-getnumtics.md) . Cela est dû au fait que le nombre retourné par **TBM \_ GETNUMTICS** inclut la première et la dernière graduations, qui ne sont pas incluses dans le tableau. Pour récupérer la position physique d’une graduation, dans les coordonnées clientes de la fenêtre du TrackBar, envoyez le message [**TBM \_ GETTICPOS**](tbm-getticpos.md) . Le message [**TBM \_ CLEARTICS**](tbm-cleartics.md) supprime toutes les graduations de la barre de progression sauf la première et la dernière.

La taille de ligne d’un TrackBar détermine la distance de déplacement du curseur en réponse à l’entrée au clavier à partir des touches de direction, telles que la flèche droite ou la touche de direction bas. Pour récupérer ou définir la taille de ligne, envoyez les messages [**TBM \_ GETLINESIZE**](tbm-getlinesize.md) et [**TBM \_ SETLINESIZE**](tbm-setlinesize.md) . Le TrackBar envoie également les \_ codes de notification de la programmation to et du \_ point de vue de to à sa fenêtre parente quand l’utilisateur appuie sur les touches de direction.

La taille de page d’un TrackBar détermine le déplacement du curseur en réponse à l’entrée au clavier, telle que la touche PAGE précédente ou PAGE suivante, ou l’entrée de la souris, comme les clics dans le canal TrackBar. Pour récupérer ou définir la taille de la page, envoyez les messages [**TBM \_ GETPAGESIZE**](tbm-getpagesize.md) et [**TBM \_ SETPAGESIZE**](tbm-setpagesize.md) . La barre de défilement envoie également les \_ \_ codes de notification PG. suiv et to PageDown à sa fenêtre parente lorsqu’elle reçoit une entrée de clavier ou de souris qui fait défiler la page. Pour plus d’informations, consultez [messages de notification TrackBar](#trackbar-notification-messages).

Une application peut envoyer des messages pour récupérer les dimensions d’un TrackBar. Le message [**TBM \_ GETTHUMBRECT**](tbm-getthumbrect.md) récupère le rectangle englobant du curseur. Le message [**TBM \_ GETTHUMBLENGTH**](tbm-getthumblength.md) récupère la longueur du curseur. Le message [**TBM \_ GETCHANNELRECT**](tbm-getchannelrect.md) récupère le rectangle englobant pour le canal du TrackBar, qui est la zone sur laquelle le curseur se déplace. Elle contient la surbrillance lorsqu’une plage est sélectionnée. Si un TrackBar a le style [**tbs \_ multiple**](trackbar-control-styles.md) , vous pouvez envoyer le [**message \_ SETTHUMBLENGTH TBM**](tbm-setthumblength.md) pour modifier la longueur du curseur.

Vous pouvez récupérer ou définir la plage de sélection en envoyant des messages au TrackBar. Utilisez le message [**TBM \_ SETSEL**](tbm-setsel.md) pour définir les positions de début et de fin d’une sélection. Pour définir uniquement la position de départ ou simplement la position de fin d’une sélection, envoyez un message [**TBM \_ SETSELSTART**](tbm-setselstart.md) ou [**TBM \_ SETSELEND**](tbm-setselend.md) . Pour récupérer les positions de début et de fin d’une plage de sélection, envoyez un message [**TBM \_ GETSELSTART**](tbm-getselstart.md) ou [**TBM \_ GETSELEND**](tbm-getselend.md) . Pour effacer une plage de sélection et rétablir la plage d’origine du TrackBar, envoyez le message [**TBM \_ CLEARSEL**](tbm-clearsel.md) .

> [!Note]  
> Il incombe à l’application de s’assurer que l’utilisateur ne peut pas sélectionner de valeurs en dehors de la plage de sélection. Le contrôle lui-même n’empêche pas l’utilisateur de déplacer le curseur en dehors de la plage.

 

## <a name="trackbar-notification-messages"></a>Messages de notification TrackBar

Un TrackBar avertit la fenêtre parente des actions de l’utilisateur en lui envoyant un message [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) . Un TrackBar avec le style [**tbs \_ Horiz**](trackbar-control-styles.md) envoie des messages **WM \_ HSCROLL** . Un TrackBar avec le style [**tbs \_ vert**](trackbar-control-styles.md) envoie des messages **WM \_ VSCROLL** . Le mot de poids faible du paramètre *wParam* de **WM \_ HSCROLL** ou **WM \_ VSCROLL** contient le code de notification. Pour les \_ codes de notification to THUMBPOSITION et to \_ THUMBTRACK, le mot de poids fort du paramètre *wParam* spécifie la position du curseur. Pour tous les autres codes de notification, le mot de poids fort est zéro ; Envoyez le message [**TBM \_ GETPOS**](tbm-getpos.md) pour déterminer la position du curseur. Le paramètre *lParam* est le handle du TrackBar.

Le système envoie les \_ codes de notification TB bas, to \_ LINEDOWN, TB \_ et to \_ Top uniquement lorsque l’utilisateur interagit avec un TrackBar à l’aide du clavier. Les \_ codes de notification to THUMBPOSITION et to \_ THUMBTRACK sont envoyés uniquement lorsque l’utilisateur utilise la souris. Les \_ codes de notification to ENDTRACK, to \_ PageDown et to \_ PageUp sont envoyés dans les deux cas. Le tableau suivant répertorie les codes de notification TrackBar et les événements (codes de touches virtuelles ou événements de souris) qui entraînent l’envoi des notifications de [**codes de clé virtuelle**](/windows/desktop/inputdev/virtual-key-codes).



| Code de notification | Raison envoyée                                                                                                                     |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| TO \_ bas        | [**fin de VK \_**](/windows/desktop/inputdev/virtual-key-codes)                                                                         |
| TO \_ ENDTRACK      | [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) (l’utilisateur a publié une clé qui a envoyé un code de clé virtuelle approprié)                              |
| TO \_ LINEDOWN      | [**VK \_ RIGHT**](/windows/desktop/inputdev/virtual-key-codes) ou [ **VK \_**](/windows/desktop/inputdev/virtual-key-codes)     |
| \_programmation to        | [**VK \_ À gauche**](/windows/desktop/inputdev/virtual-key-codes) ou [ **VK \_**](/windows/desktop/inputdev/virtual-key-codes)              |
| TO \_ PageDown      | [**VK \_ SUIVANT**](/windows/desktop/inputdev/virtual-key-codes) (l’utilisateur a cliqué sur le canal en dessous ou à droite du curseur)   |
| TO \_ PG PRÉC        | [**VK \_ AVANT**](/windows/desktop/inputdev/virtual-key-codes) (l’utilisateur a cliqué sur le canal au-dessus ou à gauche du curseur) |
| TO \_ THUMBPOSITION | [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) suivant un \_ Code de notification to THUMBTRACK                                         |
| TO \_ THUMBTRACK    | Déplacement du curseur (l’utilisateur a fait glisser le curseur)                                                                                   |
| TO \_ Top           | [**Page d’VK \_**](/windows/desktop/inputdev/virtual-key-codes)                                                                      |



 

## <a name="default-trackbar-message-processing"></a>Traitement du message TrackBar par défaut

Cette section décrit le traitement des messages de fenêtre effectué par un TrackBar.



| Message                                              | Traitement effectué                                                                                                                                                                                                                                     |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CAPTURECHANGED WM**](/windows/desktop/inputdev/wm-capturechanged) | Arrête le minuteur s’il a été défini lors du traitement du [**\_ LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown) et envoie le \_ Code de notification to THUMBPOSITION, si nécessaire. Il envoie toujours le \_ Code de notification to ENDTRACK.                                     |
| [**création de WM \_**](/windows/desktop/winmsg/wm-create)                   | Effectue une initialisation supplémentaire, telle que la définition de la taille de la ligne, de la taille de la page et de la fréquence des graduations sur les valeurs par défaut.                                                                                                                                 |
| [**\_destructeur WM**](/windows/desktop/winmsg/wm-destroy)                 | Libère des ressources.                                                                                                                                                                                                                                         |
| [**\_activer WM**](/windows/desktop/winmsg/wm-enable)                   | Repeint la fenêtre TrackBar.                                                                                                                                                                                                                            |
| [**\_ERASEBKGND WM**](/windows/desktop/winmsg/wm-erasebkgnd)           | Efface l’arrière-plan de la fenêtre, à l’aide de la couleur d’arrière-plan actuelle du TrackBar.                                                                                                                                                                       |
| [**\_GETDLGCODE WM**](/windows/desktop/dlgbox/wm-getdlgcode)           | Retourne la \_ valeur WANTARROWS DLGC.                                                                                                                                                                                                                      |
| [**WM- \_ touche**](/windows/desktop/inputdev/wm-keydown)               | Traite les touches de direction et envoie, selon le cas, les codes de notification to Top, to Bottom, to \_ \_ \_ PageUp, to \_ PageDown, to PageDown \_ et to \_ LINEDOWN LINEDOWN.                                                                                               |
| [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)                   | Envoie le \_ Code de notification ENDTRACK to si la clé était l’une des touches de direction.                                                                                                                                                                       |
| [**\_KILLFOCUS WM**](/windows/desktop/inputdev/wm-killfocus)           | Repeint la fenêtre TrackBar.                                                                                                                                                                                                                            |
| [**\_LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown)       | Définit le focus et la capture de la souris sur le TrackBar. Le cas échéant, il définit une minuterie qui détermine la vitesse à laquelle le curseur se déplace vers le curseur de la souris lorsque l’utilisateur appuie sur le bouton de la souris dans la fenêtre.                                      |
| [**\_LBUTTONUP WM**](/windows/desktop/inputdev/wm-lbuttonup)           | Libère la capture de la souris et met fin à la minuterie, si celle-ci a été définie lors du traitement [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) . Elle envoie le \_ Code de notification to THUMBPOSITION, si nécessaire. Il envoie toujours le \_ Code de notification to ENDTRACK. |
| [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)           | Déplace le curseur et envoie le code de \_ notification to THUMBTRACK lors du suivi de la souris (consultez [**\_ Timer WM**](/windows/desktop/winmsg/wm-timer)).                                                                                                                          |
| [**\_peinture WM**](/windows/desktop/gdi/wm-paint)                        | Peint le TrackBar. Si le paramètre wParam est non NULL, le contrôle suppose que la valeur est un HDC et peint à l’aide de ce contexte de périphérique.                                                                                                             |
| [**WM \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus)             | Repeint la fenêtre TrackBar.                                                                                                                                                                                                                            |
| [**taille du WM \_**](/windows/desktop/winmsg/wm-size)                       | Définit les dimensions du TrackBar, en supprimant le curseur s’il n’y a pas assez de place pour l’afficher.                                                                                                                                                      |
| [**\_minuteur WM**](/windows/desktop/winmsg/wm-timer)                     | Récupère la position de la souris et met à jour la position du curseur. (Elle est reçue uniquement lorsque l’utilisateur fait glisser le curseur.)                                                                                                                         |
| [**\_WININICHANGE WM**](/windows/desktop/winmsg/wm-wininichange)       | Initialise les dimensions du curseur.                                                                                                                                                                                                                           |



 

## <a name="trackbar-tooltips"></a>Info-bulles de TrackBar

Un TrackBar créé avec le style des [**\_ info-bulles tbs**](trackbar-control-styles.md) a un contrôle ToolTip par défaut. L’info-bulle reste visible et affiche la valeur actuelle au fur et à mesure que l’utilisateur fait glisser le curseur à l’aide de la souris.

Vous pouvez assigner un nouveau contrôle ToolTip à un TrackBar en envoyant le message [**TBM \_ SETTOOLTIPS**](tbm-settooltips.md) . Pour récupérer le handle d’un contrôle ToolTip assigné, utilisez le message [**TBM \_ GETTOOLTIPS**](tbm-gettooltips.md) .

 

 