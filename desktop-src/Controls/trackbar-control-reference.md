---
title: TrackBar
description: Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles TrackBar.
ms.assetid: vs|controls|~\controls\trackbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe8e58cd8db9c2811f31cac92ee3d1d31c2c02d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512438"
---
# <a name="trackbar"></a>TrackBar

Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles TrackBar.

### <a name="overviews"></a>Vues d'ensemble



| Rubrique                                                  | Contenu                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [À propos des contrôles TrackBar](trackbar-controls.md)       | Un TrackBar est une fenêtre qui contient un curseur (parfois appelé curseur de défilement) dans un canal et des graduations facultatives. Lorsque l’utilisateur déplace le curseur, à l’aide de la souris ou des touches de direction, le TrackBar envoie des messages de notification pour indiquer la modification.<br/> |
| [Utilisation des contrôles TrackBar](using-trackbar-controls.md) | Cette section fournit des détails d’implémentation et des exemples pour les contrôles TrackBar.<br/>                                                                                                                                                                               |



 

### <a name="messages"></a>Messages



| Rubrique                                                 | Contenu                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TBM \_ CLEARSEL**](tbm-clearsel.md)                 | Efface la plage de sélection actuelle dans un TrackBar. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ CLEARTICS**](tbm-cleartics.md)               | Supprime les graduations actuelles d’un TrackBar. Ce message ne supprime pas les première et dernière graduations, qui sont créées automatiquement par le TrackBar. <br/>                                                                                                                                           |
| [**TBM \_ GETBUDDY**](tbm-getbuddy.md)                 | Récupère le handle d’une fenêtre associée du contrôle TrackBar à un emplacement donné. L’emplacement spécifié est relatif à l’orientation du contrôle (horizontale ou verticale). <br/>                                                                                                                                 |
| [**TBM \_ GETCHANNELRECT**](tbm-getchannelrect.md)     | Récupère la taille et la position du rectangle englobant pour le canal d’un TrackBar. (Le canal est la zone sur laquelle le curseur se déplace. Elle contient la surbrillance lorsqu’une plage est sélectionnée.) <br/>                                                                                                         |
| [**TBM \_ GETLINESIZE**](tbm-getlinesize.md)           | Récupère le nombre de positions logiques placées dans le curseur de la barre de défilement en réponse à l’entrée au clavier à partir des touches de direction, telles que les touches ou. Les positions logiques sont les incréments de l’entier dans la plage de la plage de la barre de défilement minimale à la position maximale du curseur. <br/>                                         |
| [**TBM \_ GETNUMTICS**](tbm-getnumtics.md)             | Récupère le nombre de graduations dans un TrackBar. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ GETPAGESIZE**](tbm-getpagesize.md)           | Récupère le nombre de positions logiques du curseur de la barre de défilement en réponse à l’entrée au clavier, comme les touches ou, ou l’entrée de la souris, comme les clics dans le canal de la barre de défilement. Les positions logiques sont les incréments de l’entier dans la plage de la plage de la barre de défilement minimale à la position maximale du curseur. <br/>   |
| [**TBM \_ GETPOS**](tbm-getpos.md)                     | Récupère la position logique actuelle du curseur dans un TrackBar. Les positions logiques sont les valeurs entières de la plage de la plage de la barre de défilement minimale à la position maximale du curseur. <br/>                                                                                                                       |
| [**TBM \_ GETPTICS**](tbm-getptics.md)                 | Récupère l’adresse d’un tableau qui contient les positions des graduations d’un TrackBar. <br/>                                                                                                                                                                                                        |
| [**TBM \_ GETRANGEMAX**](tbm-getrangemax.md)           | Récupère la position maximale du curseur dans un TrackBar. <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ GETRANGEMIN**](tbm-getrangemin.md)           | Récupère la position minimale du curseur dans un TrackBar. <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ GETSELEND**](tbm-getselend.md)               | Récupère la position de fin de la plage de sélection actuelle dans un TrackBar. <br/>                                                                                                                                                                                                                            |
| [**TBM \_ GETSELSTART**](tbm-getselstart.md)           | Récupère la position de départ de la plage de sélection actuelle dans un TrackBar. <br/>                                                                                                                                                                                                                          |
| [**TBM \_ GETTHUMBLENGTH**](tbm-getthumblength.md)     | Récupère la longueur du curseur dans un TrackBar. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ GETTHUMBRECT**](tbm-getthumbrect.md)         | Récupère la taille et la position du rectangle englobant pour le curseur dans un TrackBar. <br/>                                                                                                                                                                                                                |
| [**TBM \_ GETTIC**](tbm-gettic.md)                     | Récupère la position logique d’une graduation dans un TrackBar. La position logique peut être l’une des valeurs entières dans la plage de la plage de la barre de défilement minimale à la position de curseur maximale. <br/>                                                                                                                     |
| [**TBM \_ GETTICPOS**](tbm-getticpos.md)               | Récupère la position physique actuelle d’une graduation dans un TrackBar.<br/>                                                                                                                                                                                                                                   |
| [**TBM \_ GETTOOLTIPS**](tbm-gettooltips.md)           | Récupère le handle du contrôle ToolTip assigné au TrackBar, le cas échéant. <br/>                                                                                                                                                                                                                          |
| [**TBM \_ GETUNICODEFORMAT**](tbm-getunicodeformat.md) | Récupère l’indicateur de format de caractère Unicode pour le contrôle. <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ SETBUDDY**](tbm-setbuddy.md)                 | Assigne une fenêtre comme fenêtre associée pour un contrôle TrackBar. Les fenêtres de l’ami TrackBar s’affichent automatiquement à un emplacement relatif à l’orientation du contrôle (horizontale ou verticale). <br/>                                                                                                          |
| [**TBM \_ SETLINESIZE**](tbm-setlinesize.md)           | Définit le nombre de positions logiques du curseur de la barre de défilement en réponse à une entrée au clavier à partir des touches de direction, telles que les touches ou. Les positions logiques sont les incréments de l’entier dans la plage de la plage de la barre de défilement minimale à la position maximale du curseur. <br/>                                              |
| [**TBM \_ SETPAGESIZE**](tbm-setpagesize.md)           | Définit le nombre de positions logiques du curseur de la barre de défilement en réponse à l’entrée au clavier, comme les touches ou, ou l’entrée de la souris, comme les clics dans le canal de la barre de défilement. Les positions logiques sont les incréments de l’entier dans la plage de la plage de la barre de défilement minimale à la position maximale du curseur. <br/>        |
| [**TBM \_ SetPos**](tbm-setpos.md)                     | Définit la position logique actuelle du curseur dans un TrackBar. <br/>                                                                                                                                                                                                                                         |
| [**TBM \_ SETPOSNOTIFY**](tbm-setposnotify.md)         | Définit la position logique actuelle du curseur dans un TrackBar. <br/>                                                                                                                                                                                                                                         |
| [**TBM \_ SEtrange**](tbm-setrange.md)                 | Définit la plage de positions logiques minimale et maximale pour le curseur dans un TrackBar. <br/>                                                                                                                                                                                                                  |
| [**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)           | Définit la position logique maximale du curseur dans un TrackBar. <br/>                                                                                                                                                                                                                                        |
| [**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)           | Définit la position logique minimale du curseur dans un TrackBar. <br/>                                                                                                                                                                                                                                        |
| [**TBM \_ SETSEL**](tbm-setsel.md)                     | Définit les positions de début et de fin de la plage de sélection disponible dans un TrackBar. <br/>                                                                                                                                                                                                                |
| [**TBM \_ SETSELEND**](tbm-setselend.md)               | Définit la position logique de fin de la plage de sélection actuelle dans un TrackBar. Ce message est ignoré si le TrackBar n’a pas le style [**tbs \_ ENABLESELRANGE**](trackbar-control-styles.md) . <br/>                                                                              |
| [**TBM \_ SETSELSTART**](tbm-setselstart.md)           | Définit la position logique de départ de la plage de sélection actuelle dans un TrackBar. Ce message est ignoré si le TrackBar n’a pas le style [**tbs \_ ENABLESELRANGE**](trackbar-control-styles.md) . <br/>                                                                            |
| [**TBM \_ SETTHUMBLENGTH**](tbm-setthumblength.md)     | Définit la longueur du curseur dans un TrackBar. Ce message est ignoré si le TrackBar n’a pas le style [**tbs \_ multiple**](trackbar-control-styles.md) . <br/>                                                                                                                      |
| [**TBM \_ SETTIC**](tbm-settic.md)                     | Définit une graduation dans un TrackBar à la position logique spécifiée. <br/>                                                                                                                                                                                                                                      |
| [**TBM \_ SETTICFREQ**](tbm-setticfreq.md)             | Définit la fréquence d’intervalle des graduations d’un TrackBar. Par exemple, si la fréquence est définie sur deux, une graduation est affichée pour chaque autre incrément dans la plage du TrackBar. Le paramètre par défaut de la fréquence est un ; autrement dit, chaque incrément de la plage est associé à une graduation. <br/> |
| [**TBM \_ SETTIPSIDE**](tbm-settipside.md)             | Positionne un contrôle ToolTip utilisé par un contrôle TrackBar. Les contrôles TrackBar qui utilisent le style des [**\_ info-bulles tbs**](trackbar-control-styles.md) affichent des info-bulles. <br/>                                                                                                                           |
| [**TBM \_ SETTOOLTIPS**](tbm-settooltips.md)           | Assigne un contrôle ToolTip à un contrôle TrackBar. <br/>                                                                                                                                                                                                                                                       |
| [**TBM \_ SETUNICODEFORMAT**](tbm-setunicodeformat.md) | Définit l’indicateur de format de caractère Unicode pour le contrôle. Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle. <br/>                                                                                                               |



 

### <a name="notifications"></a>Notifications



| Rubrique                                                              | Contenu                                                                                                                                                                                      |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_CUSTOMDRAW nm (TrackBar)](nm-customdraw-trackbar.md)            | Envoyé par un contrôle TrackBar pour notifier à ses fenêtres parentes les opérations de dessin. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>        |
| [\_RELEASEDCAPTURE nm (TrackBar)](nm-releasedcapture-trackbar-.md) | Avertit la fenêtre parente d’un contrôle TrackBar que le contrôle libère la capture de la souris. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/> |
| [TRBN \_ THUMBPOSCHANGING](trbn-thumbposchanging.md)                | Indique que la position du curseur sur un TrackBar est modifiée. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                               |



 

### <a name="constants"></a>Constantes



| Rubrique                                                  | Contenu                                                                                    |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Valeurs de dessin personnalisées](custom-draw-values.md)           | Cette section répertorie les valeurs utilisées pour identifier les parties d’un contrôle TrackBar. <br/>      |
| [Styles de contrôle TrackBar](trackbar-control-styles.md) | Cette section contient des informations sur les styles utilisés avec les contrôles TrackBar. <br/> |



 

 

 





