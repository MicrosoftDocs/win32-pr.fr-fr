---
title: Barre d’état
description: Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles de barre d’État.
ms.assetid: 77923055-9d00-4528-bda7-b602a26b577f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8e1b4119754d524bccfbe4153e12783d9bd38d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116969"
---
# <a name="status-bar"></a>Barre d’état

Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles de barre d’État.

### <a name="overviews"></a>Vues d'ensemble



| Rubrique                          | Contenu                                                                                                                                                   |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Barres d’État](status-bars.md) | Une *barre d’État* est une fenêtre horizontale au bas d’une fenêtre parente dans laquelle une application peut afficher différents types d’informations d’État.<br/> |



 

### <a name="functions"></a>Fonctions




| Rubrique | Contenu | 
|-------|----------|
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa"><strong>CreateStatusWindow</strong></a> | Crée une fenêtre d’État, qui est généralement utilisée pour afficher l’état d’une application. La fenêtre apparaît généralement au bas de la fenêtre parente et contient le texte spécifié.<blockquote>[!Note]<br />Cette fonction est obsolète. Utilisez <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa"><strong>CreateWindow</strong></a> à la place.</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a> | La fonction <a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a> dessine le texte spécifié dans le style d’une fenêtre d’État avec des bordures.<br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-menuhelp"><strong>MenuHelp</strong></a> | Traite les messages <a href="/windows/desktop/menurc/wm-menuselect"><strong>WM_MENUSELECT</strong></a> et <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> et affiche le texte d’aide à propos du menu en cours dans la fenêtre d’état spécifiée.<br /> | 




 

### <a name="messages"></a>Messages



| Rubrique                                               | Contenu                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_GETBORDERS SB**](sb-getborders.md)             | Récupère les largeurs actuelles des bordures horizontale et verticale d’une fenêtre d’État. <br/>                                                                                                  |
| [**\_GETICON SB**](sb-geticon.md)                   | Récupère l’icône pour un composant dans une barre d’État. <br/>                                                                                                                                           |
| [**\_GETPARTS SB**](sb-getparts.md)                 | Récupère le nombre de parties dans une fenêtre d’État. Le message récupère également la coordonnée du bord droit du nombre spécifié de parties. <br/>                                         |
| [**\_GETRECT SB**](sb-getrect.md)                   | Récupère le rectangle englobant d’un composant dans une fenêtre d’État. <br/>                                                                                                                           |
| [**SB \_ GETTEXT**](sb-gettext.md)                   | Le message [**SB \_ GETTEXT**](sb-gettext.md) récupère le texte à partir de la partie spécifiée d’une fenêtre d’État. <br/>                                                                             |
| [**\_GETTEXTLENGTH SB**](sb-gettextlength.md)       | Le message [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) récupère la longueur, en caractères, du texte à partir de la partie spécifiée d’une fenêtre d’État. <br/>                                   |
| [**\_GETTIPTEXT SB**](sb-gettiptext.md)             | Récupère le texte d’info-bulle pour un composant dans une barre d’État. La barre d’État doit être créée avec le style [**\_ info-bulles SBT**](status-bar-styles.md) pour activer les info-bulles. <br/>         |
| [**\_GETUNICODEFORMAT SB**](sb-getunicodeformat.md) | Récupère l’indicateur de format de caractère Unicode pour le contrôle. <br/>                                                                                                                             |
| [**\_ISSIMPLE SB**](sb-issimple.md)                 | Vérifie un contrôle de barre d’État pour déterminer s’il est en mode simple. <br/>                                                                                                                        |
| [**\_SETBKCOLOR SB**](sb-setbkcolor.md)             | Définit la couleur d’arrière-plan dans une barre d’État. <br/>                                                                                                                                               |
| [**\_SETICON SB**](sb-seticon.md)                   | Définit l’icône d’un composant dans une barre d’État. <br/>                                                                                                                                                |
| [**\_SETMINHEIGHT SB**](sb-setminheight.md)         | Définit la hauteur minimale de la zone de dessin d’une fenêtre d’État. <br/>                                                                                                                               |
| [**\_SETPARTS SB**](sb-setparts.md)                 | Définit le nombre de parties dans une fenêtre d’État et la coordonnée du bord droit de chaque partie. <br/>                                                                                           |
| [**unisettext SB \_**](sb-settext.md)                   | Le \_ message SB SETTEXT définit le texte dans la partie spécifiée d’une fenêtre d’État.<br/>                                                                                                           |
| [**\_SETTIPTEXT SB**](sb-settiptext.md)             | Définit le texte d’info-bulle pour un composant dans une barre d’État. La barre d’État doit avoir été créée avec le style [**\_ info-bulles SBT**](status-bar-styles.md) pour activer les info-bulles.<br/>        |
| [**\_SETUNICODEFORMAT SB**](sb-setunicodeformat.md) | Définit l’indicateur de format de caractère Unicode pour le contrôle. Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle. <br/> |
| [**\_simple SB**](sb-simple.md)                     | Spécifie si une fenêtre d’état affiche du texte simple ou affiche toutes les parties de fenêtre définies par un message [**SB \_ SETPARTS**](sb-setparts.md) précédent. <br/>                                       |



 

### <a name="notifications"></a>Notifications



| Rubrique                                                 | Contenu                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM- \_ cliquer (barre d’État)](nm-click-status-bar.md)     | Notifie la fenêtre parente d’un contrôle de barre d’État que l’utilisateur a cliqué avec le bouton gauche de la souris dans le contrôle. [Nm \_ Cliquez (barre d’État)](nm-click-status-bar.md) est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>              |
| [\_DBLCLK nm (barre d’État)](nm-dblclk-status-bar.md)   | Notifie la fenêtre parente d’un contrôle de barre d’État que l’utilisateur a double-cliqué dans le contrôle avec le bouton gauche de la souris. Cette notification est envoyée sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                       |
| [\_RCLICK nm (barre d’État)](nm-rclick-status-bar.md)   | Notifie la fenêtre parente d’un contrôle de barre d’État sur lequel l’utilisateur a cliqué avec le bouton droit de la souris dans le contrôle. Cette notification est envoyée sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                             |
| [\_RDBLCLK nm (barre d’État)](nm-rdblclk-status-bar.md) | Avertit les fenêtres parentes d’un contrôle de barre d’État que l’utilisateur a double-cliqué sur le bouton droit de la souris dans le contrôle. [Nm \_ RDBLCLK (barre d’État)](nm-rdblclk-status-bar.md) est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/> |
| [SBN \_ SIMPLEMODECHANGE](sbn-simplemodechange.md)     | Envoyé par un contrôle de barre d’État lorsque le mode simple change en raison d’un message [**SB \_ simple**](sb-simple.md) . Cette notification est envoyée sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                        |



 

### <a name="constants"></a>Constantes



| Rubrique                                      | Contenu                                                                                                              |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Styles de barre d’État](status-bar-styles.md) | Cette section répertorie les styles, en plus des styles de fenêtre standard, pris en charge par les contrôles de *barre d’État* . <br/> |



 

 

