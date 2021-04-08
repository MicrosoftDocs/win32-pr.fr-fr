---
title: Scroll Bar
description: Cette section contient des informations sur les éléments de programmation utilisés avec les barres de défilement.
ms.assetid: vs|controls|~\controls\scrollbars\scrollbars.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38cf549a37fd5d4a271f6e12642a9bfd45b65d79
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730605"
---
# <a name="scroll-bar"></a>Scroll Bar

Cette section contient des informations sur les éléments de programmation utilisés avec les barres de défilement. Une fenêtre peut afficher un objet de données, tel qu’un document ou un bitmap, qui est plus grand que la zone cliente de la fenêtre. Lorsqu’il est fourni avec une *barre de défilement*, l’utilisateur peut faire défiler un objet de données dans la zone cliente pour afficher les parties de l’objet qui s’étendent au-delà des bordures de la fenêtre.

### <a name="overviews"></a>Vues d'ensemble



| Rubrique                                      | Contenu                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [À propos des barres de défilement](about-scroll-bars.md) | Une barre de défilement se compose d’un arbre ombré avec un bouton fléché à chaque extrémité et d’une *case de défilement* (parfois appelée curseur de défilement) entre les boutons fléchés.<br/>                                                                                                                                                                     |
| [Utilisation des barres de défilement](using-scroll-bars.md) | Lors de la création d’une fenêtre superposée, indépendante ou enfant, vous pouvez ajouter des barres de défilement standard à l’aide de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) et en spécifiant [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles), [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles)ou les deux styles.<br/> |



 

### <a name="functions"></a>Fonctions



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rubrique</th>
<th>Contenu</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a></td>
<td>La fonction <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a> active ou désactive une ou deux flèches de barre de défilement. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo"><strong>GetScrollBarInfo</strong></a></td>
<td>La fonction <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo"><strong>GetScrollBarInfo</strong></a> récupère des informations sur la barre de défilement spécifiée.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a></td>
<td>La fonction <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> récupère les paramètres d’une barre de défilement, y compris les positions de défilement minimale et maximale, la taille de la page et la position de la case de défilement (curseur de défilement).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a></td>
<td>La fonction <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> récupère la position actuelle de la case de défilement (Thumb) dans la barre de défilement spécifiée. La position actuelle est une valeur relative qui dépend de la plage de défilement actuelle. Par exemple, si la plage de défilement est comprise entre 0 et 100 et que la case de défilement se trouve au milieu de la barre, la position actuelle est 50.
<blockquote>
[!Note]<br />
La fonction <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> est fournie à des fins de compatibilité descendante. Les nouvelles applications doivent utiliser la fonction <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a></td>
<td>La fonction <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> récupère les positions de la zone de défilement minimale et maximale actuelle (Thumb) pour la barre de défilement spécifiée.
<blockquote>
[!Note]<br />
La fonction <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> est fournie à des fins de compatibilité uniquement. Les nouvelles applications doivent utiliser la fonction <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-scrolldc"><strong>ScrollDC</strong></a></td>
<td>La fonction <a href="/windows/desktop/api/Winuser/nf-winuser-scrolldc"><strong>ScrollDC</strong></a> fait défiler un rectangle de bits horizontalement et verticalement. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindow"><strong>ScrollWindow</strong></a></td>
<td>La fonction <a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindow"><strong>ScrollWindow</strong></a> fait défiler le contenu de la zone cliente de la fenêtre spécifiée.
<blockquote>
[!Note]<br />
La fonction <a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindow"><strong>ScrollWindow</strong></a> est fournie à des fins de compatibilité descendante. Les nouvelles applications doivent utiliser la fonction <a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindowex"><strong>ScrollWindowEx</strong></a> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindowex"><strong>ScrollWindowEx</strong></a></td>
<td>La fonction <a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindowex"><strong>ScrollWindowEx</strong></a> fait défiler le contenu de la zone cliente de la fenêtre spécifiée. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a></td>
<td>La fonction <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> définit les paramètres d’une barre de défilement, y compris les positions de défilement minimale et maximale, la taille de la page et la position de la case de défilement (curseur de défilement). La fonction redessine également la barre de défilement, si elle est demandée.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a></td>
<td>La fonction <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> définit la position de la case de défilement (Thumb) dans la barre de défilement spécifiée et, si nécessaire, redessine la barre de défilement pour refléter la nouvelle position de la case de défilement.
<blockquote>
[!Note]<br />
La fonction <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> est fournie à des fins de compatibilité descendante. Les nouvelles applications doivent utiliser la fonction <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a></td>
<td>La fonction <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> définit les positions minimale et maximale des cases de défilement pour la barre de défilement spécifiée.
<blockquote>
[!Note]<br />
La fonction <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> est fournie à des fins de compatibilité descendante. Les nouvelles applications doivent utiliser la fonction <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a></td>
<td>La fonction <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a> affiche ou masque la barre de défilement spécifiée. <br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a>Messages



| Rubrique                                                 | Contenu                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_lignes d’activation SBM \_**](sbm-enable-arrows.md)      | Une application envoie un message de [**\_ \_ flèches d’activation SBM**](sbm-enable-arrows.md) pour activer ou désactiver une ou deux flèches d’un contrôle de barre de défilement.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**\_GETPOS SBM**](sbm-getpos.md)                     | Le message [**SBM \_ GETPOS**](sbm-getpos.md) est envoyé pour récupérer la position actuelle de la case de défilement d’un contrôle de barre de défilement. La position actuelle est une valeur relative qui dépend de la plage de défilement actuelle. Par exemple, si la plage de défilement est comprise entre 0 et 100 et que la case de défilement se trouve au milieu de la barre, la position actuelle est 50. <br/> Les applications ne doivent pas envoyer ce message directement. Au lieu de cela, ils doivent utiliser la fonction [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) . Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Les applications qui implémentent un contrôle de barre de défilement personnalisé doivent répondre à ces messages pour que la fonction **GetScrollPos** fonctionne correctement.<br/> |
| [**\_GETRANGE SBM**](sbm-getrange.md)                 | Le message [**SBM \_ GETRANGE**](sbm-getrange.md) est envoyé pour récupérer les valeurs de position minimale et maximale pour le contrôle de barre de défilement. <br/> Les applications ne doivent pas envoyer ce message directement. Au lieu de cela, ils doivent utiliser la fonction [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) . Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Les applications qui implémentent un contrôle de barre de défilement personnalisé doivent répondre à ces messages pour que la fonction **GetScrollRange** fonctionne correctement.<br/>                                                                                                                                                                                                              |
| [**\_GETSCROLLBARINFO SBM**](sbm-getscrollbarinfo.md) | Envoyé par une application pour récupérer des informations sur la barre de défilement spécifiée.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**\_GETSCROLLINFO SBM**](sbm-getscrollinfo.md)       | Le message [**SBM \_ GETSCROLLINFO**](sbm-getscrollinfo.md) est envoyé pour récupérer les paramètres d’une barre de défilement. <br/> Les applications ne doivent pas envoyer ce message directement. Au lieu de cela, ils doivent utiliser la fonction [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) . Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Les applications qui implémentent un contrôle de barre de défilement personnalisé doivent répondre à ces messages pour que la fonction **GetScrollInfo** fonctionne correctement.<br/>                                                                                                                                                                                                                                           |
| [**\_SetPos SBM**](sbm-setpos.md)                     | Le message [**SBM \_ SetPos**](sbm-setpos.md) est envoyé pour définir la position de la case de défilement (Thumb) et, le cas échéant, redessine la barre de défilement pour refléter la nouvelle position de la case de défilement. <br/> Les applications ne doivent pas envoyer ce message directement. Au lieu de cela, ils doivent utiliser la fonction [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) . Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Les applications qui implémentent un contrôle de barre de défilement personnalisé doivent répondre à ces messages pour que la fonction **SetScrollPos** fonctionne correctement.<br/>                                                                                                                                                                  |
| [**\_DÉtrange SBM**](sbm-setrange.md)                 | Le message [**SBM \_ SetRange**](sbm-setrange.md) est envoyé pour définir les valeurs de position minimale et maximale pour le contrôle de barre de défilement. <br/> Les applications ne doivent pas envoyer ce message directement. Au lieu de cela, ils doivent utiliser la fonction [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) . Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Les applications qui implémentent un contrôle de barre de défilement personnalisé doivent répondre à ces messages pour que la fonction **SetScrollRange** fonctionne correctement.<br/>                                                                                                                                                                                                                   |
| [**\_SETRANGEREDRAW SBM**](sbm-setrangeredraw.md)     | Une application envoie le message [**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md) à un contrôle de barre de défilement pour définir les valeurs de position minimale et maximale et pour redessiner le contrôle.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**\_SETSCROLLINFO SBM**](sbm-setscrollinfo.md)       | Le message [**SBM \_ SETSCROLLINFO**](sbm-setscrollinfo.md) est envoyé pour définir les paramètres d’une barre de défilement. <br/> Les applications ne doivent pas envoyer ce message directement. Au lieu de cela, ils doivent utiliser la fonction [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) . Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Les applications qui implémentent un contrôle de barre de défilement personnalisé doivent répondre à ces messages pour que la fonction **SetScrollInfo** fonctionne correctement.<br/>                                                                                                                                                                                                                                            |



 

### <a name="notifications"></a>Notifications



| Rubrique                                                 | Contenu                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CTLCOLORSCROLLBAR WM**](wm-ctlcolorscrollbar.md) | Le message [**WM \_ CTLCOLORSCROLLBAR**](wm-ctlcolorscrollbar.md) est envoyé à la fenêtre parente d’un contrôle de barre de défilement lorsque le contrôle va être dessiné. En répondant à ce message, la fenêtre parente peut utiliser le handle de contexte d’affichage pour définir la couleur d’arrière-plan du contrôle de barre de défilement. <br/> Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . <br/> |
| [**\_HSCROLL WM**](wm-hscroll.md)                     | Le message [**WM \_ HSCROLL**](wm-hscroll.md) est envoyé à une fenêtre lorsqu’un événement de défilement se produit dans la barre de défilement horizontale standard de la fenêtre. Ce message est également envoyé au propriétaire d’un contrôle de barre de défilement horizontale lorsqu’un événement de défilement se produit dans le contrôle. <br/> Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . <br/>                                        |
| [**\_VSCROLL WM**](wm-vscroll.md)                     | Le message [**WM \_ VSCROLL**](wm-vscroll.md) est envoyé à une fenêtre lorsqu’un événement de défilement se produit dans la barre de défilement verticale standard de la fenêtre. Ce message est également envoyé au propriétaire d’un contrôle de barre de défilement vertical lorsqu’un événement de défilement se produit dans le contrôle. <br/> Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . <br/>                                            |



 

### <a name="structures"></a>Structures



| Rubrique                                  | Contenu                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) | La structure [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) contient des informations sur la barre de défilement.<br/>                                                                                                                                                                                                                                                           |
| [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)       | La structure [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) contient les paramètres de barre de défilement à définir par la fonction [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) (ou le message [**SBM \_ SetScrollInfo**](sbm-setscrollinfo.md) ) ou récupérés par la fonction [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) (ou le message [**SBM \_ GetScrollInfo**](sbm-getscrollinfo.md) ). <br/> |



 

### <a name="constants"></a>Constantes



| Rubrique                                                      | Contenu                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Styles de contrôle de barre de défilement](scroll-bar-control-styles.md) | Pour créer un contrôle de barre de défilement à l’aide de la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , spécifiez la classe ScrollBar, les constantes de style de fenêtre appropriées et une combinaison des styles de contrôle de barre de défilement suivants. Certains styles créent un contrôle de barre de défilement qui utilise une largeur ou une hauteur par défaut. Toutefois, vous devez toujours spécifier les coordonnées x et y et les autres dimensions de la barre de défilement lorsque vous appelez **CreateWindow** ou **CreateWindowEx**. <br/> |



 

 

