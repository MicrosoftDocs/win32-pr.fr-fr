---
title: Messages de bouton
description: Un bouton peut envoyer des messages à sa fenêtre parente et une fenêtre parente peut envoyer des messages à un bouton.
ms.assetid: 2d2358fb-b17d-48a9-8def-15ae8bad9162
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1601f269ec1242a10579d2ace812723d3ead7f84
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103734044"
---
# <a name="button-messages"></a>Messages de bouton

Un bouton peut envoyer des messages à sa fenêtre parente et une fenêtre parente peut envoyer des messages à un bouton.

Les rubriques suivantes sont présentées dans cette section.

-   [Envoi de messages à des boutons](#sending-messages-to-buttons)
-   [Gestion des messages à partir d’un bouton](#handling-messages-from-a-button)
-   [Messages de notification à partir de boutons](#notification-messages-from-buttons)
-   [Messages de couleur de bouton](#button-color-messages)
-   [Traitement du message par défaut du bouton](#button-default-message-processing)
-   [Rubriques connexes](#related-topics)

## <a name="sending-messages-to-buttons"></a>Envoi de messages à des boutons

Une fenêtre parente peut envoyer des messages à un bouton dans une fenêtre superposée ou enfant à l’aide de la fonction [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , ou elle peut envoyer des messages à un bouton dans une boîte de dialogue à l’aide des fonctions [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea), [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton), [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton)et [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) .

Une application peut utiliser le [**message \_ GETCHECK BM**](bm-getcheck.md) pour récupérer l’état d’activation d’une case à cocher ou d’une case d’option. Une application peut également utiliser le [**message \_ GETSTATE BM**](bm-getstate.md) pour récupérer les États actuels du bouton (l’état d’activation, de transmission et de focus). Pour obtenir des informations sur un état spécifique, utilisez un masque de données sur la valeur d’État retournée.

Le message [**BM \_ SETCHECK**](bm-setcheck.md) définit l’état d’activation d’une case à cocher ou d’une case d’option ; le message retourne la valeur zéro. Le message de [**BM \_ SETSTATE**](bm-setstate.md) définit l’état de transmission d’un bouton ; ce message retourne également zéro. Le message [**BM \_ SETSTYLE**](bm-setstyle.md) change le style d’un bouton. Il est conçu pour modifier les styles de bouton dans un type (par exemple, en remplaçant une case à cocher par une case à cocher automatique). Elle n’est pas conçue pour changer entre les types (par exemple, en remplaçant une case à cocher par une case d’option). Une application ne doit pas modifier un bouton d’un type à un autre.

Un bouton du style de la [**\_ bitmap BS**](button-styles.md) ou de l' [**\_ icône BS**](button-styles.md) affiche une bitmap ou une icône au lieu de texte. Le [**message \_ SETIMAGE BM**](bm-setimage.md) associe un handle à une image bitmap ou à une icône avec un bouton. Le [**message \_ GETIMAGE de BM**](bm-getimage.md) récupère un handle vers l’image bitmap ou l’icône associée à un bouton.

Une application peut également utiliser le message [**DM \_ GETDEFID**](/windows/desktop/dlgbox/dm-getdefid) pour récupérer l’identificateur du contrôle bouton de commande par défaut dans une boîte de dialogue. Une application peut utiliser le message [**DM \_ SETDEFID**](/windows/desktop/dlgbox/dm-setdefid) pour définir le bouton de commande par défaut d’une boîte de dialogue.

L’appel de la fonction [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) ou [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton) équivaut à l’envoi d’un message [**\_ SETCHECK BM**](bm-setcheck.md) . L’appel de la fonction [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) revient à envoyer un message [**\_ GETCHECK BM**](bm-getcheck.md) .

## <a name="handling-messages-from-a-button"></a>Gestion des messages à partir d’un bouton

Les notifications d’un bouton sont envoyées en tant que [**\_ commandes WM**](/windows/desktop/menurc/wm-command) ou messages de [**\_ notification WM**](wm-notify.md) . Vous trouverez des informations sur le message qui est utilisé dans la page de référence de chaque notification.

Pour plus d’informations sur la gestion des messages, consultez [contrôle des messages](control-messages.md). Voir aussi messages de bouton.

## <a name="notification-messages-from-buttons"></a>Messages de notification à partir de boutons

Lorsque l’utilisateur clique sur un bouton, son état change et le bouton envoie des codes de notification, sous la forme de messages de [**\_ commande WM**](/windows/desktop/menurc/wm-command) , à sa fenêtre parente. Par exemple, un contrôle de bouton de commande envoie le code de notification sur lequel l’utilisateur a [ \_ cliqué](bn-clicked.md) chaque fois que l’utilisateur choisit le bouton. Dans tous les cas (à l’exception de [BCN \_ HOTITEMCHANGE](bcn-hotitemchange.md)), le mot de poids faible du paramètre *wParam* contient l’identificateur de contrôle, le mot de poids fort de *wParam* contient le code de notification et le paramètre *lParam* contient le handle de fenêtre de contrôle.

Le message et la réponse de la fenêtre parente dépendent du type, du style et de l’état actuel du bouton. Voici les codes de notification de bouton qu’une application doit surveiller et traiter.



| Code de notification                                                        | Description                                            |
|--------------------------------------------------------------------------|--------------------------------------------------------|
| [BCN \_ HOTITEMCHANGE](bcn-hotitemchange.md)                              | Souris entrée ou gauche de la zone cliente d’un bouton. |
| [sur lequel l' \_ utilisateur a cliqué](bn-clicked.md)                                            | L’utilisateur a cliqué sur un bouton.                             |
| De la [ \_ DBLCLK](bn-dblclk.md) ou [un \_ ](bn-doubleclicked.md) | L’utilisateur a double-cliqué sur un bouton.                      |
| [désactivation de la \_ coche](bn-disable.md)                                            | Un bouton est désactivé.                                  |
| De la [ \_ Push](bn-pushed.md) ou [ \_ HiLite](bn-hilite.md)               | L’utilisateur a appuyé sur un bouton.                              |
| [\_KILLFOCUS.](bn-killfocus.md)                                        | Le bouton a perdu le focus clavier.                    |
| [peinture de la \_ bosse](bn-paint.md)                                                | Le bouton doit être peint.                          |
| [-e \_ SetFocus](bn-setfocus.md)                                          | Le bouton a obtenu le focus clavier.                  |
| De la [ \_ ](bn-unpushed.md) [ \_ UNHILITE](bn-unhilite.md) de type push       | Le bouton n’est plus poussé.                        |



 

Un bouton envoie les codes de notification de la part de [ \_ désactivation](bn-disable.md), de la cale, de l' [ \_ KILLFOCUS](bn-killfocus.md) [, \_ du](bn-pushed.md)type de ligne et de la ligne de commande [**de la part de la ligne \_**](button-styles.md) de [ \_ commande](bn-unpushed.md) . [ \_](bn-paint.md) [ \_](bn-setfocus.md) De la [ \_](bn-dblclk.md)Les codes de notification DBLCLK sont automatiquement envoyés pour les boutons [**BS \_ UserButton**](button-styles.md), [**BS \_ RadioButton**](button-styles.md)et [**BS \_ OwnerDraw**](button-styles.md) . Les autres types de bouton envoient \_ l’DBLCLK de l’adresse de l’utilisateur uniquement s’ils ont le style **BS \_ Notify** . Tous les boutons envoient le code de notification [ \_ sur lequel vous avez cliqué](bn-clicked.md) , quels que soient les styles de bouton.

Pour les boutons automatiques, le système modifie l’état de transmission et peint le bouton. Dans ce cas, l’application traite généralement uniquement les codes de notification « en [ \_ un clic](bn-clicked.md) » et « [ \_ DBLCLK](bn-dblclk.md) ». Pour les boutons qui ne sont pas automatiques, l’application répond généralement au code de notification en envoyant un message pour modifier l’état du bouton. Pour plus d’informations sur l’envoi de messages à des boutons, consultez [envoi de messages à des boutons](#sending-messages-to-buttons).

Lorsque l’utilisateur sélectionne un bouton owner-drawn, le bouton envoie à sa fenêtre parente un message [**WM \_ DRAWITEM**](wm-drawitem.md) contenant l’identificateur du contrôle à dessiner et des informations sur ses dimensions et son état.

## <a name="button-color-messages"></a>Messages de couleur de bouton

Le système fournit des valeurs de couleur par défaut pour les boutons. Une application peut récupérer les valeurs par défaut de ces couleurs en appelant la fonction [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) ou définir les valeurs en appelant la fonction [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) . Le tableau suivant indique les valeurs de couleur de bouton par défaut.



| Valeur               | Élément coloré                                                                                                            |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| BTNFACE de couleurs \_      | Visages de bouton.                                                                                                              |
| BTNHIGHLIGHT de couleurs \_ | Zone de surbrillance (bords supérieur et gauche) d’un bouton.                                                                       |
| BTNSHADOW de couleurs \_    | Zone ombrée (bords inférieur et droit) d’un bouton.                                                                      |
| BTNTEXT de couleurs \_      | Texte normal (qui n’est pas grisé) dans les boutons.                                                                                       |
| GRAYTEXT de couleurs \_     | Texte désactivé (gris) dans les boutons. Cette couleur est définie sur 0 si le pilote d’affichage actuel ne prend pas en charge une couleur grise unie. |
| fenêtre de couleur \_       | Arrière-plan des fenêtres.                                                                                                        |
| WINDOWFRAME de couleurs \_  | Frames de fenêtre.                                                                                                             |
| WINDOWTEXT de couleurs \_   | Texte dans Windows.                                                                                                           |



 

Toutefois, l’appel de [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) affecte toutes les applications. par conséquent, vous ne devez pas appeler cette fonction pour personnaliser des boutons pour votre application.

Le système envoie un message [**WM \_ CTLCOLORBTN**](wm-ctlcolorbtn.md) à la fenêtre parente d’un bouton avant de dessiner un bouton. Ce message contient un handle vers le contexte de périphérique du bouton et un handle vers la fenêtre enfant. La fenêtre parente peut utiliser ces poignées pour modifier le texte du bouton et les couleurs d’arrière-plan. Toutefois, seuls les boutons owner-drawn répondent à la fenêtre parente qui traite le message.

## <a name="button-default-message-processing"></a>Traitement du message par défaut du bouton

La procédure de fenêtre pour la classe de fenêtre de contrôle de bouton prédéfinie effectue le traitement par défaut pour tous les messages que la procédure de contrôle de bouton ne traite pas. Lorsque la procédure de contrôle Button retourne la **valeur false** pour un message, la procédure de fenêtre prédéfinie vérifie les messages et exécute les actions par défaut indiquées dans le tableau suivant.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Message</th>
<th>Action par défaut</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="bm-click.md"><strong>BM_CLICK</strong></a></td>
<td>Envoie le bouton une <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> et un message <a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a> , puis envoie la fenêtre parente à un code de notification <a href="bn-clicked.md">BN_CLICKED</a> .</td>
</tr>
<tr class="even">
<td><a href="bm-getcheck.md"><strong>BM_GETCHECK</strong></a></td>
<td>Retourne l’état d’activation du bouton.</td>
</tr>
<tr class="odd">
<td><a href="bm-getimage.md"><strong>BM_GETIMAGE</strong></a></td>
<td>Retourne un handle vers la bitmap ou l’icône associée au bouton, ou <strong>null</strong> si le bouton n’a aucune bitmap ou icône.</td>
</tr>
<tr class="even">
<td><a href="bm-getstate.md"><strong>BM_GETSTATE</strong></a></td>
<td>Retourne l’état d’activation actuel, l’état de push et l’état de focus du bouton.</td>
</tr>
<tr class="odd">
<td><a href="bm-setcheck.md"><strong>BM_SETCHECK</strong></a></td>
<td>Définit l’état d’activation de tous les styles des cases d’option et des cases à cocher. Si le paramètre <em>wParam</em> est supérieur à zéro pour les cases d’option, le bouton se voit attribuer le style <a href="/windows/desktop/winmsg/window-styles"><strong>WS_TABSTOP</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="bm-setimage.md"><strong>BM_SETIMAGE</strong></a></td>
<td>Associe la bitmap ou la poignée d’icône spécifiée au bouton et retourne un handle vers la bitmap ou l’icône précédente.</td>
</tr>
<tr class="odd">
<td><a href="bm-setstate.md"><strong>BM_SETSTATE</strong></a></td>
<td>Définit l’état de transmission (push) du bouton. Pour les boutons owner-drawn, un <a href="wm-drawitem.md"><strong>WM_DRAWITEM</strong></a> message est envoyé à la fenêtre parente si l’état du bouton a changé.</td>
</tr>
<tr class="even">
<td><a href="bm-setstyle.md"><strong>BM_SETSTYLE</strong></a></td>
<td>Définit le style du bouton. Si le mot de poids faible du paramètre <em>lParam</em> a la <strong>valeur true</strong>, le bouton est redessiné.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a></td>
<td>Active une case à cocher ou une case à cocher automatique lorsque l’utilisateur appuie sur les touches plus (+) ou égales (=). Désactive une case à cocher ou une case à cocher automatique lorsque l’utilisateur appuie sur la touche moins (–).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a></td>
<td>Peint le bouton.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-erasebkgnd"><strong>WM_ERASEBKGND</strong></a></td>
<td>Efface l’arrière-plan des boutons owner-drawn. Les arrière-plans des autres boutons sont effacés dans le cadre de la <a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a> et <a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a> traitement.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/dlgbox/wm-getdlgcode"><strong>WM_GETDLGCODE</strong></a></td>
<td>Retourne des valeurs qui indiquent le type d’entrée traité par la procédure de bouton par défaut, comme indiqué dans le tableau suivant. 
<table>
<thead>
<tr class="header">
<th>Style de bouton</th>
<th>Retours</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_AUTOCHECKBOX</strong></a></td>
<td>DLGC_WANTCHARS | DLGC_BUTTON</td>
</tr>
<tr class="even">
<td><a href="button-styles.md"><strong>BS_AUTORADIOBUTTON</strong></a></td>
<td>DLGC_RADIOBUTTON | DLGC_BUTTON</td>
</tr>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_CHECKBOX</strong></a></td>
<td>DLGC_WANTCHARS | DLGC_BUTTON</td>
</tr>
<tr class="even">
<td><a href="button-styles.md"><strong>BS_DEFPUSHBUTTON</strong></a></td>
<td>DLGC_DEFPUSHBUTTON | DLGC_BUTTON</td>
</tr>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_GROUPBOX</strong></a></td>
<td>DLGC_STATIC</td>
</tr>
<tr class="even">
<td><a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a></td>
<td>DLGC_UNDEFPUSHBUTTON | DLGC_BUTTON</td>
</tr>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a></td>
<td>DLGC_RADIOBUTTON | DLGC_BUTTON</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-getfont"><strong>WM_GETFONT</strong></a></td>
<td>Retourne un handle vers la police actuelle.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-keydown"><strong>WM_KEYDOWN</strong></a></td>
<td>Exécute un push du bouton si l’utilisateur appuie sur la barre d’espace.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-keyup"><strong>WM_KEYUP</strong></a></td>
<td>Libère la capture de la souris pour tous les cas, à l’exception de la touche TAB.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-killfocus"><strong>WM_KILLFOCUS</strong></a></td>
<td>Supprime le rectangle de focus d’un bouton. Pour les boutons de commande et les boutons de commande par défaut, le rectangle de focus est invalidé. Si le bouton a la capture de la souris, la capture est libérée, le bouton n’est pas cliqué et tout état de transmission est supprimé.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-lbuttondblclk"><strong>WM_LBUTTONDBLCLK</strong></a></td>
<td>Envoie un <a href="bn-dblclk.md">BN_DBLCLK</a> code de notification à la fenêtre parente pour les cases d’option et les boutons owner-drawn. Pour les autres boutons, un double-clic est traité comme un message de <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a></td>
<td>Met en surbrillance le bouton si la position du curseur de la souris se trouve dans le rectangle client du bouton.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a></td>
<td>Libère la capture de la souris si le bouton avait la capture de la souris.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-mousemove"><strong>WM_MOUSEMOVE</strong></a></td>
<td>Effectue la même action que <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a>, si le bouton a la capture de la souris. Dans le cas contraire, aucune action n’est effectuée.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-nccreate"><strong>WM_NCCREATE</strong></a></td>
<td>Active un bouton de <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> dans un bouton de <a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-nchittest"><strong>WM_NCHITTEST</strong></a></td>
<td>Retourne HTTRANSPARENT, si le contrôle bouton est une zone de groupe.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a></td>
<td>Dessine le bouton en fonction de son style et de son état actuel.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-setfocus"><strong>WM_SETFOCUS</strong></a></td>
<td>Dessine un rectangle de focus sur le bouton qui obtient le focus. Pour les cases d’option et les cases d’option automatiques, la fenêtre parente reçoit un code de notification <a href="bn-clicked.md">BN_CLICKED</a> .</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-setfont"><strong>WM_SETFONT</strong></a></td>
<td>Définit une nouvelle police et éventuellement met à jour la fenêtre.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/winmsg/wm-settext"><strong>WM_SETTEXT</strong></a></td>
<td>Définit le texte du bouton. Dans le cas d’une zone de groupe, le message est peint sur le texte préexistant avant de repeindre la zone de groupe avec le nouveau texte.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-syskeyup"><strong>WM_SYSKEYUP</strong></a></td>
<td>Libère la capture de la souris pour tous les cas, à l’exception de la touche TAB.</td>
</tr>
</tbody>
</table>



 

La procédure de fenêtre prédéfinie transmet tous les autres messages à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour le traitement par défaut.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Messages de contrôle](control-messages.md)
</dt> </dl>

 

 