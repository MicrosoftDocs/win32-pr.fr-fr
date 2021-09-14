---
title: Récepteur de radiomessagerie
description: Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles de pagineur.
ms.assetid: vs|controls|~\controls\pager\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21df98100ed649e4237c51bfcabf41420c49d004
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117761"
---
# <a name="pager"></a>Récepteur de radiomessagerie

Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles de pagineur.

### <a name="overviews"></a>Vues d'ensemble



| Rubrique                                | Contenu                                                                                                                                         |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Contrôles de pagineur](pager-controls.md) | Un *contrôle de pagineur* est un conteneur de fenêtre qui est utilisé avec une fenêtre qui n’a pas assez de zone d’affichage pour afficher tout son contenu.<br/> |



 

### <a name="macros"></a>Macros



| Rubrique                                                 | Contenu                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Radiomessagerie \_ ForwardMouse**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse)     | Active ou désactive le transfert de la souris pour le contrôle de pagineur. Lorsque le transfert de souris est activé, le contrôle de pagineur transfère les messages de la souris [**WM \_**](/windows/desktop/inputdev/wm-mousemove) à la fenêtre contenue. Vous pouvez utiliser cette macro ou envoyer le [**message \_ FORWARDMOUSE PGM**](pgm-forwardmouse.md) de manière explicite. <br/>                                                                                                                     |
| [**Radiomessagerie \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor)         | Récupère la couleur d’arrière-plan actuelle pour le contrôle de pagineur. Vous pouvez utiliser cette macro ou envoyer le [**message \_ GETBKCOLOR PGM**](pgm-getbkcolor.md) de manière explicite. <br/>                                                                                                                                                                                                                                                                 |
| [**Radiomessagerie \_ GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder)           | Récupère la taille de bordure actuelle pour le contrôle de pagineur. Vous pouvez utiliser cette macro ou envoyer le [**message \_ GETBORDER PGM**](pgm-getborder.md) de manière explicite. <br/>                                                                                                                                                                                                                                                                        |
| [**Radiomessagerie \_ GetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize)   | Récupère la taille de bouton actuelle pour le contrôle de pagineur. Vous pouvez utiliser cette macro ou envoyer le [**message \_ GETBUTTONSIZE PGM**](pgm-getbuttonsize.md) de manière explicite. <br/>                                                                                                                                                                                                                                                                |
| [**Radiomessagerie \_ GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) | Récupère l’état du bouton spécifié dans un contrôle de pagineur. Vous pouvez utiliser cette macro ou envoyer le [**message \_ GETBUTTONSTATE PGM**](pgm-getbuttonstate.md) de manière explicite. <br/>                                                                                                                                                                                                                                                       |
| [**Radiomessagerie \_ GetDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget)   | Récupère le pointeur d’interface [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) d’un contrôle de pagineur. Vous pouvez utiliser cette macro ou envoyer le [**message \_ GETDROPTARGET PGM**](pgm-getdroptarget.md) de manière explicite. <br/>                                                                                                                                                                                                                                       |
| [**Radiomessagerie \_ GetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos)                 | Récupère la position de défilement actuelle du contrôle de pagineur. Vous pouvez utiliser cette macro ou envoyer le [**message \_ GETPOS PGM**](pgm-getpos.md) de manière explicite. <br/>                                                                                                                                                                                                                                                                           |
| [**Radiomessagerie \_ RecalcSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize)         | Force le contrôle de pagineur à recalculer la taille de la fenêtre contenue. L’utilisation de cette macro entraîne l’envoi d’une notification [PGN \_ CALCSIZE](pgn-calcsize.md) . Vous pouvez utiliser cette macro ou envoyer le [**message \_ RECALCSIZE PGM**](pgm-recalcsize.md) de manière explicite. <br/>                                                                                                                                                        |
| [**Radiomessagerie \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor)         | Définit la couleur d’arrière-plan actuelle pour le contrôle de pagineur. Vous pouvez utiliser cette macro ou envoyer le [**message \_ SETBKCOLOR PGM**](pgm-setbkcolor.md) de manière explicite. <br/>                                                                                                                                                                                                                                                                      |
| [**Radiomessagerie \_ setBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder)           | Définit la taille de bordure actuelle pour le contrôle de pagineur. Vous pouvez utiliser cette macro ou envoyer le [**message \_ SETBORDER PGM**](pgm-setborder.md) de manière explicite. <br/>                                                                                                                                                                                                                                                                             |
| [**Radiomessagerie \_ SetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize)   | Définit la taille actuelle du bouton pour le contrôle de pagineur. Vous pouvez utiliser cette macro ou envoyer le [**message \_ SETBUTTONSIZE PGM**](pgm-setbuttonsize.md) de manière explicite. <br/>                                                                                                                                                                                                                                                                     |
| [**Radiomessagerie \_ SetChild**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild)             | Définit la fenêtre contenue pour le contrôle de pagineur. Cette macro ne modifiera pas le parent de la fenêtre contenue ; Il assigne uniquement un handle de fenêtre au contrôle de pagineur pour le défilement. Dans la plupart des cas, la fenêtre contenue est une fenêtre enfant. Si c’est le cas, la fenêtre contenue doit être un enfant du contrôle pager. Vous pouvez utiliser cette macro ou envoyer le [**message \_ SETCHILD PGM**](pgm-setchild.md) de manière explicite. <br/> |
| [**Radiomessagerie \_ SetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos)                 | Définit la position de défilement pour le contrôle de pagineur. Vous pouvez utiliser cette macro ou envoyer le [**message \_ SetPos PGM**](pgm-setpos.md) de manière explicite. <br/>                                                                                                                                                                                                                                                                                       |
| [**Radiomessagerie \_ SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo)   | **Destiné à un usage interne ; non recommandé pour une utilisation dans les applications.**<br/> Définit les paramètres de défilement du contrôle de pagineur, y compris la valeur du délai d’attente, les lignes par délai d’attente et les pixels par ligne. Vous pouvez utiliser cette macro ou envoyer le [**message \_ SETSETSCROLLINFO PGM**](pgm-setscrollinfo.md) de manière explicite. <br/>                                                                                                  |



 

### <a name="messages"></a>Messages



| Rubrique                                              | Contenu                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_FORWARDMOUSE PGM**](pgm-forwardmouse.md)      | Active ou désactive le transfert de la souris pour le contrôle de pagineur. Lorsque le transfert de souris est activé, le contrôle de pagineur transfère les messages de la souris [**WM \_**](/windows/desktop/inputdev/wm-mousemove) à la fenêtre contenue. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ ForwardMouse**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) . <br/>                                                                                                                       |
| [**\_GETBKCOLOR PGM**](pgm-getbkcolor.md)          | Récupère la couleur d’arrière-plan actuelle pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) . <br/>                                                                                                                                                                                                                                                                   |
| [**\_GETBORDER PGM**](pgm-getborder.md)            | Récupère la taille de bordure actuelle pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) . <br/>                                                                                                                                                                                                                                                                          |
| [**\_GETBUTTONSIZE PGM**](pgm-getbuttonsize.md)    | Récupère la taille de bouton actuelle pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ GetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) . <br/>                                                                                                                                                                                                                                                                  |
| [**\_GETBUTTONSTATE PGM**](pgm-getbuttonstate.md)  | Récupère l’état du bouton spécifié dans un contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) . <br/>                                                                                                                                                                                                                                                         |
| [**\_GETDROPTARGET PGM**](pgm-getdroptarget.md)    | Récupère le pointeur d’interface [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) d’un contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ GetDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) . <br/>                                                                                                                                                                                                                                         |
| [**\_GETPOS PGM**](pgm-getpos.md)                  | Récupère la position de défilement actuelle du contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ GetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) . <br/>                                                                                                                                                                                                                                                                             |
| [**\_RECALCSIZE PGM**](pgm-recalcsize.md)          | Force le contrôle de pagineur à recalculer la taille de la fenêtre contenue. L’envoi de ce message entraîne l’envoi d’une notification [PGN \_ CALCSIZE](pgn-calcsize.md) . Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ RecalcSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) . <br/>                                                                                                                                                      |
| [**\_SETBKCOLOR PGM**](pgm-setbkcolor.md)          | Définit la couleur d’arrière-plan actuelle pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) . <br/>                                                                                                                                                                                                                                                                        |
| [**\_SETBORDER PGM**](pgm-setborder.md)            | Définit la taille de bordure actuelle pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ setBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) . <br/>                                                                                                                                                                                                                                                                               |
| [**\_SETBUTTONSIZE PGM**](pgm-setbuttonsize.md)    | Définit la taille actuelle du bouton pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ SetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) . <br/>                                                                                                                                                                                                                                                                       |
| [**\_SETCHILD PGM**](pgm-setchild.md)              | Définit la fenêtre contenue pour le contrôle de pagineur. Ce message ne change pas le parent de la fenêtre contenue. Il assigne uniquement un handle de fenêtre au contrôle de pagineur pour le défilement. Dans la plupart des cas, la fenêtre contenue est une fenêtre enfant. Si c’est le cas, la fenêtre contenue doit être un enfant du contrôle pager. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ SetChild**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) . <br/> |
| [**\_SetPos PGM**](pgm-setpos.md)                  | Définit la position de défilement actuelle pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ SetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) . <br/>                                                                                                                                                                                                                                                                                 |
| [**\_SETSETSCROLLINFO PGM**](pgm-setscrollinfo.md) | **Destiné à un usage interne ; non recommandé pour une utilisation dans les applications.**<br/> Définit les paramètres de défilement du contrôle de pagineur, y compris la valeur du délai d’attente, les lignes par délai d’attente et les pixels par ligne. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro de [**radiomessagerie \_ SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) . <br/>                                                                                                  |



 

### <a name="notifications"></a>Notifications



| Rubrique                                                        | Contenu                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_RELEASEDCAPTURE nm (récepteur de radiomessagerie)](nm-releasedcapture-pager-.md) | Notifie la fenêtre parente d’un contrôle de pagineur que le contrôle a relâché la capture de la souris. NM \_ RELEASEDCAPTURE est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                                |
| [PGN \_ CALCSIZE](pgn-calcsize.md)                            | Notification envoyée par un contrôle pager pour obtenir les dimensions déroulantes de la fenêtre contenue. Ces dimensions sont utilisées par le contrôle de pagineur pour déterminer la taille de défilement de la fenêtre contenue. Cette notification est envoyée sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/> |
| [PGN \_ HOTITEMCHANGE](pgn-hotitemchange.md)                  | Envoyé par un contrôle pager lorsque l’élément réactif (en surbrillance) change. <br/>                                                                                                                                                                                                                               |
| [PGN \_ défilement](pgn-scroll.md)                                | Notification envoyée par un contrôle pager avant le défilement de la fenêtre contenue. Cette notification est envoyée sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                                         |



 

### <a name="structures"></a>Structures



| Rubrique                                | Contenu                                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) | Contient et reçoit des informations que le contrôle de pagineur utilise pour calculer la zone défilante de la fenêtre contenue. Elle est utilisée avec la [notification \_ CALCSIZE PGN](pgn-calcsize.md) . <br/> |
| [**NMPGHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem)   | Contient des informations utilisées avec la notification [ \_ HOTITEMCHANGE PGN](pgn-hotitemchange.md) . <br/>                                                                                                |
| [**NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll)     | Contient et reçoit des informations que le contrôle de pagineur utilise lorsque vous faites défiler la fenêtre contenue. Elle est utilisée avec la notification de [ \_ défilement PGN](pgn-scroll.md) . <br/>                          |



 

### <a name="constants"></a>Constantes



| Rubrique                                            | Contenu                                                                            |
|--------------------------------------------------|-------------------------------------------------------------------------------------|
| [Styles de contrôle de pagineur](pager-control-styles.md) | Cette section répertorie les styles de fenêtre utilisés lors de la création de contrôles de pagineur. <br/> |



 

 

