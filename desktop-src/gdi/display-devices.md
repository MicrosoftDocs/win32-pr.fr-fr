---
description: Avant de peindre, le système doit préparer le périphérique d’affichage pour les opérations de dessin.
ms.assetid: a3802aa7-deec-4151-b1b1-4cd38f769864
title: Périphériques d’affichage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd71b943d294bf89e932f965b023ecbce7f4e594044fe96b70bb84d41a27f777
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038117"
---
# <a name="display-devices"></a>Périphériques d’affichage

Avant de peindre, le système doit préparer le périphérique d’affichage pour les opérations de dessin. Un contexte de périphérique d’affichage définit un ensemble d’objets graphiques et leurs attributs associés, ainsi que les modes graphiques qui affectent la sortie. Le système prépare chaque contexte de périphérique d’affichage pour la sortie dans une fenêtre, en définissant les objets de dessin, les couleurs et les modes de la fenêtre au lieu du périphérique d’affichage. Lorsque l’application fournit le contexte de périphérique d’affichage par le biais d’appels aux fonctions GDI, GDI utilise les informations dans le contexte pour générer la sortie dans la fenêtre spécifiée sans aucune intrusion sur les autres fenêtres ou autres parties de l’écran.

Le système fournit cinq types de contextes de périphérique d’affichage.



| Type                                           | Signification                                                                                                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [classiques](common-display-device-contexts.md)   | Autorise le dessin dans la zone cliente d’une fenêtre spécifiée.                                                                                                        |
| [class](class-display-device-contexts.md)     | Autorise le dessin dans la zone cliente d’une fenêtre spécifiée.                                                                                                        |
| [parent](parent-display-device-contexts.md)   | Autorise le dessin n’importe où dans la fenêtre. Bien que le contexte de périphérique parent autorise également le dessin dans la fenêtre parente, il n’est pas destiné à être utilisé de cette façon. |
| [priv](private-display-device-contexts.md) | Autorise le dessin dans la zone cliente d’une fenêtre spécifiée.                                                                                                        |
| [fenetre](window-display-device-contexts.md)   | Autorise le dessin n’importe où dans la fenêtre.                                                                                                                          |



 

Le système fournit un contexte de périphérique commun, de classe, parent ou privé à une fenêtre en fonction du type de contexte de périphérique d’affichage spécifié dans le style de classe de cette fenêtre. Le système fournit un contexte de périphérique Windows uniquement lorsque l’application en demande explicitement une, par exemple, en appelant la fonction [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) ou [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) . Dans tous les cas, une application peut utiliser la fonction [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc) pour déterminer la fenêtre qu’un DC d’affichage représente actuellement.

Cette section fournit des informations sur les rubriques suivantes.

-   [Afficher le cache du contexte de périphérique](display-device-context-cache.md)
-   [Afficher les paramètres par défaut du contexte de périphérique](display-device-context-defaults.md)
-   [Contextes de périphérique d’affichage courants](common-display-device-contexts.md)
-   [Contextes de périphérique d’affichage privé](private-display-device-contexts.md)
-   [Contextes de périphérique d’affichage parent](parent-display-device-contexts.md)
-   [Affichage de la classe contextes de périphérique](class-display-device-contexts.md)
-   [Fenêtre Affichage des contextes de périphérique](window-display-device-contexts.md)
-   [Contextes de périphérique d’affichage parent](parent-display-device-contexts.md)

 

 



