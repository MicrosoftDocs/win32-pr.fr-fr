---
title: Rebar
description: Cette section contient des informations sur la programmation des éléments utilisés avec les contrôles Rebar.
ms.assetid: vs|controls|~\controls\rebar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14ac71ea71b5e0b0bd1e222d46c070a62512f0f5ff3b885fe13b19fad10f7bf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434839"
---
# <a name="rebar"></a>Rebar

Cette section contient des informations sur la programmation des éléments utilisés avec les contrôles Rebar.

### <a name="overviews"></a>Vues d'ensemble



| Rubrique                                            | Contenu                                                                               |
|--------------------------------------------------|----------------------------------------------------------------------------------------|
| [Contrôles Rebar](rebar-controls.md)             | Les *contrôles Rebar* jouent le rôle de conteneurs pour les fenêtres enfants.<br/>                       |
| [Utilisation des contrôles Rebar](using-rebar-controls.md) | Cette section contient un exemple de code illustrant comment implémenter des contrôles Rebar.<br/> |



 

### <a name="messages"></a>Messages



| Rubrique                                               | Contenu                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_BEGINDRAG RB**](rb-begindrag.md)               | Place le contrôle rebar en mode glisser-déplacer. Ce message n’entraîne pas l’envoi d’une notification [ \_ BEGINDRAG RBN](rbn-begindrag.md) . <br/>                                                 |
| [**\_DELETEBAND RB**](rb-deleteband.md)             | Supprime une bande d’un contrôle rebar. <br/>                                                                                                                                                     |
| [**\_DRAGMOVE RB**](rb-dragmove.md)                 | Met à jour la position de glissement dans le contrôle rebar après un message [**RB \_ BEGINDRAG**](rb-begindrag.md) précédent. <br/>                                                                           |
| [**\_ENDDRAG RB**](rb-enddrag.md)                   | Termine l’opération de glisser-déplacer du contrôle rebar. Ce message n’entraîne pas l’envoi d’une notification [ \_ ENDDRAG RBN](rbn-enddrag.md) . <br/>                                          |
| [**\_GETBANDBORDERS RB**](rb-getbandborders.md)     | Récupère les bordures d’une bande. Le résultat de ce message peut être utilisé pour calculer la zone utilisable dans une bande. <br/>                                                                          |
| [**\_GETBANDCOUNT RB**](rb-getbandcount.md)         | Récupère le nombre de bandes actuellement dans le contrôle rebar. <br/>                                                                                                                             |
| [**\_GETBANDINFO RB**](rb-getbandinfo.md)           | Récupère des informations sur une bande spécifiée dans un contrôle rebar. <br/>                                                                                                                         |
| [**\_GETBANDMARGINS RB**](rb-getbandmargins.md)     | Récupère les marges d’une bande.<br/>                                                                                                                                                          |
| [**\_GETBARHEIGHT RB**](rb-getbarheight.md)         | Récupère la hauteur du contrôle rebar. <br/>                                                                                                                                               |
| [**\_GETBARINFO RB**](rb-getbarinfo.md)             | Récupère des informations sur le contrôle rebar et la liste d’images qu’il utilise. <br/>                                                                                                                |
| [**\_GETBKCOLOR RB**](rb-getbkcolor.md)             | Récupère la couleur d’arrière-plan par défaut d’un contrôle rebar. <br/>                                                                                                                                    |
| [**\_GETCOLORSCHEME RB**](rb-getcolorscheme.md)     | Récupère les informations de modèle de couleur à partir du contrôle rebar. <br/>                                                                                                                           |
| [**\_GETDROPTARGET RB**](rb-getdroptarget.md)       | Récupère le pointeur d’interface [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) d’un contrôle rebar. <br/>                                                                                                        |
| [**\_GETEXTENDEDSTYLE RB**](rb-getextendedstyle.md) | Obtient le style étendu. <br/>                                                                                                                                                                 |
| [**\_GETPALETTE RB**](rb-getpalette.md)             | Récupère la palette actuelle du contrôle rebar. <br/>                                                                                                                                           |
| [**\_GETRECT RB**](rb-getrect.md)                   | Récupère le rectangle englobant pour une bande donnée dans un contrôle rebar. <br/>                                                                                                                    |
| [**RB, \_ GETROWCOUNT**](rb-getrowcount.md)           | Récupère le nombre de lignes de bandes dans un contrôle rebar. <br/>                                                                                                                                |
| [**\_GETROWHEIGHT RB**](rb-getrowheight.md)         | Récupère la hauteur d’une ligne spécifiée dans un contrôle rebar. <br/>                                                                                                                              |
| [**\_GETTEXTCOLOR RB**](rb-gettextcolor.md)         | Récupère la couleur de texte par défaut d’un contrôle rebar. <br/>                                                                                                                                          |
| [**\_GETTOOLTIPS RB**](rb-gettooltips.md)           | Récupère le handle d’un contrôle ToolTip associé au contrôle rebar. <br/>                                                                                                           |
| [**\_GETUNICODEFORMAT RB**](rb-getunicodeformat.md) | Récupère l’indicateur de format de caractère Unicode pour le contrôle. <br/>                                                                                                                             |
| [**RB \_ HITTEST**](rb-hittest.md)                   | Détermine la partie d’une bande rebar située à un point donné sur l’écran, si une bande rebar existe à ce point. <br/>                                                                        |
| [**\_IDTOINDEX RB**](rb-idtoindex.md)               | Convertit un identificateur de bande en un index de bande dans un contrôle rebar. <br/>                                                                                                                           |
| [**\_INSERTBAND RB**](rb-insertband.md)             | Insère une nouvelle bande dans un contrôle rebar. <br/>                                                                                                                                                   |
| [**\_MAXIMIZEBAND RB**](rb-maximizeband.md)         | Redimensionne une bande dans un contrôle rebar en sa taille idéale ou la plus grande taille. <br/>                                                                                                                   |
| [**\_MINIMIZEBAND RB**](rb-minimizeband.md)         | Redimensionne une bande dans un contrôle rebar à sa plus petite taille. <br/>                                                                                                                                  |
| [**\_MOVEBAND RB**](rb-moveband.md)                 | Déplace une bande d’un index vers un autre. <br/>                                                                                                                                                  |
| [**\_PUSHCHEVRON RB**](rb-pushchevron.md)           | Envoyé à un contrôle rebar pour pousser par programme un chevron.<br/>                                                                                                                               |
| [**\_SETBANDINFO RB**](rb-setbandinfo.md)           | Définit les caractéristiques d’une bande existante dans un contrôle rebar. <br/>                                                                                                                             |
| [**\_SETBANDWIDTH RB**](rb-setbandwidth.md)         | Définit la largeur d’une bande ancrée.<br/>                                                                                                                                                         |
| [**\_SETBARINFO RB**](rb-setbarinfo.md)             | Définit les caractéristiques d’un contrôle rebar. <br/>                                                                                                                                             |
| [**\_SETBKCOLOR RB**](rb-setbkcolor.md)             | Définit la couleur d’arrière-plan par défaut d’un contrôle rebar. <br/>                                                                                                                                         |
| [**\_SETCOLORSCHEME RB**](rb-setcolorscheme.md)     | Définit les informations de jeu de couleurs pour le contrôle rebar. <br/>                                                                                                                                 |
| [**\_SETEXTENDEDSTYLE RB**](rb-setextendedstyle.md) | Définit le style étendu. Ce message n’est pas implémenté.<br/>                                                                                                                                 |
| [**\_SETPALETTE RB**](rb-setpalette.md)             | Définit la palette actuelle du contrôle rebar. <br/>                                                                                                                                                |
| [**\_SETPARENT, RB**](rb-setparent.md)               | Définit la fenêtre parente d’un contrôle rebar. <br/>                                                                                                                                                    |
| [**\_SETTEXTCOLOR RB**](rb-settextcolor.md)         | Définit la couleur de texte par défaut d’un contrôle rebar. <br/>                                                                                                                                               |
| [**\_SETTOOLTIPS RB**](rb-settooltips.md)           | Associe un contrôle ToolTip au contrôle rebar. <br/>                                                                                                                                     |
| [**\_SETUNICODEFORMAT RB**](rb-setunicodeformat.md) | Définit l’indicateur de format de caractère Unicode pour le contrôle. Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle. <br/> |
| [**\_SETWINDOWTHEME RB**](rb-setwindowtheme.md)     | Définit le style visuel d’un contrôle rebar.<br/>                                                                                                                                                 |
| [**\_SHOWBAND RB**](rb-showband.md)                 | Affiche ou masque une bande donnée dans un contrôle rebar. <br/>                                                                                                                                          |
| [**\_SIZETORECT RB**](rb-sizetorect.md)             | Tente de trouver la meilleure disposition des bandes pour le rectangle donné. <br/>                                                                                                                   |



 

### <a name="notifications"></a>Notifications



| Rubrique                                                        | Contenu                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CUSTOMDRAW (Rebar)](nm-customdraw-rebar.md)            | Envoyé par le contrôle rebar pour signaler à sa fenêtre parente les opérations de dessin. Cette notification est envoyée sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                                               |
| [NM \_ NCHITTEST (Rebar)](nm-nchittest-rebar.md)              | Envoyé par un contrôle rebar lorsque le contrôle reçoit un message [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) . Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                 |
| [NM \_ RELEASEDCAPTURE (Rebar)](nm-releasedcapture-rebar-.md) | Notifie la fenêtre parente d’un contrôle rebar que le contrôle libère la capture de la souris. Cette notification est envoyée sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                        |
| [\_arrêt RBN](rbn-autobreak.md)                          | Avertit le parent [d’un Rebar](rebar-controls.md) qu’un saut apparaîtra dans la barre. Le parent détermine s’il faut effectuer l’arrêt. <br/>                                                                                                                            |
| [\_REdimensionnement automatique RBN](rbn-autosize.md)                            | Envoyé par un contrôle rebar créé avec le style [**RBS \_ AutoSize**](rebar-control-styles.md) quand le rebar se redimensionne automatiquement. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                  |
| [RBN \_ BEGINDRAG](rbn-begindrag.md)                          | Envoyé par un contrôle rebar lorsque l’utilisateur commence à faire glisser une bande. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                           |
| [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md)                  | Envoyé par un contrôle rebar lorsqu’un chevron fait l’objet d’un push. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                                                                        |
| [RBN \_ CHILDSIZE](rbn-childsize.md)                          | Envoyé par un contrôle rebar lorsque la fenêtre enfant d’une bande est redimensionnée. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                          |
| [RBN \_ DELETEDBAND](rbn-deletedband.md)                      | Envoyé par un contrôle rebar après la suppression d’une bande. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                                  |
| [RBN \_ DELETINGBAND](rbn-deletingband.md)                    | Envoyé par un contrôle rebar lorsqu’une bande va être supprimée. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                             |
| [RBN \_ ENDDRAG](rbn-enddrag.md)                              | Envoyé par un contrôle rebar lorsque l’utilisateur arrête de faire glisser une bande. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                            |
| [RBN \_ GETOBJECT](rbn-getobject.md)                          | Envoyé par un contrôle rebar créé avec le style [**RBS \_ REGISTERDROP**](rebar-control-styles.md) lorsqu’un objet est glissé sur une bande dans le contrôle. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/> |
| [RBN \_ HEIGHTCHANGE](rbn-heightchange.md)                    | Envoyé par un contrôle rebar lorsque sa hauteur a changé. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                                    |
| [RBN \_ LAYOUTCHANGED](rbn-layoutchanged.md)                  | Envoyé par un contrôle rebar lorsque l’utilisateur modifie la disposition des bandes du contrôle. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                        |
| [RBN \_ MinMax](rbn-minmax.md)                                | Envoyé par un contrôle rebar avant d’agrandir ou de réduire une bande. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                       |
| [RBN \_ SPLITTERDRAG](rbn-splitterdrag.md)                    | Envoyé par un contrôle rebar lorsque l’utilisateur fait glisser un séparateur. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                                 |



 

### <a name="structures"></a>Structures



| Rubrique                                        | Contenu                                                                                                                                      |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize)         | Contient des informations utilisées pour gérer les codes de notification de [ \_ redimensionnement automatique RBN](rbn-autosize.md) . <br/>                                   |
| [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar)                   | Contient des informations utilisées pour gérer différents codes de notification Rebar. <br/>                                                           |
| [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) | Contient des informations utilisées avec la notification d' [ \_ autobreak RBN](rbn-autobreak.md) .<br/>                                               |
| [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron)     | Contient des informations utilisées pour gérer le code de notification [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) . <br/>                          |
| [**NMREBARCHILDSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) | Contient des informations utilisées pour gérer le code de notification [RBN \_ CHILDSIZE](rbn-childsize.md) . <br/>                                  |
| [**NMREBARSPLITTER**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter)   | Contient les informations utilisées pour gérer un code de notification [RBN \_ SPLITTERDRAG](rbn-splitterdrag.md) .<br/>                                |
| [**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo)       | Contient des informations spécifiques à une opération de test de positionnement. Cette structure est utilisée avec le message [**RB \_ HITTEST**](rb-hittest.md) . <br/> |
| [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)       | Contient des informations qui définissent une bande dans un contrôle rebar. <br/>                                                                      |
| [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo)               | Contient des informations qui décrivent les caractéristiques du contrôle rebar. <br/>                                                                |



 

### <a name="constants"></a>Constantes



| Rubrique                                            | Contenu                                                                                              |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Styles de contrôle rebar](rebar-control-styles.md) | Les contrôles Rebar prennent en charge un grand nombre de styles de contrôle en plus des styles de fenêtre standard. <br/> |



 

 

