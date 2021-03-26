---
description: Le système de coordonnées d’une fenêtre est basé sur le système de coordonnées du périphérique d’affichage.
ms.assetid: 8590fc59-d7ad-4149-9a77-242037a11188
title: Système de coordonnées de fenêtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c69c5faa7359700af8a3bb04413fa9b25648b0cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755829"
---
# <a name="window-coordinate-system"></a>Système de coordonnées de fenêtre

Le système de coordonnées d’une fenêtre est basé sur le système de coordonnées du périphérique d’affichage. L’unité de mesure de base est l’unité de l’appareil (en général, le pixel). Les points sur l’écran sont décrits par des paires de coordonnées x et y. Les coordonnées x augmentent à droite ; les coordonnées y augmentent de haut en bas. L’origine (0,0) du système dépend du type de coordonnées utilisé.

Le système et les applications spécifient la position d’une fenêtre sur l’écran en *coordonnées d’écran*. Pour les coordonnées d’écran, l’origine est l’angle supérieur gauche de l’écran. La position complète d’une fenêtre est souvent décrite par une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) contenant les coordonnées d’écran de deux points qui définissent les angles supérieur gauche et inférieur droit de la fenêtre.

Le système et les applications spécifient la position des points dans une fenêtre à l’aide de *coordonnées clientes*. Dans ce cas, l’origine est l’angle supérieur gauche de la fenêtre ou de la zone cliente. Les coordonnées clientes garantissent qu’une application peut utiliser des valeurs de coordonnées cohérentes lors du dessin dans la fenêtre, quelle que soit la position de la fenêtre à l’écran.

Les dimensions de la zone cliente sont également décrites par une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui contient les coordonnées clientes pour la zone. Dans tous les cas, la coordonnée supérieure gauche du rectangle est incluse dans la zone de la fenêtre ou du client, tandis que la coordonnée inférieure droite est exclue. Les opérations graphiques dans une fenêtre ou une zone cliente sont exclues des bords droit et inférieur du rectangle englobant.

Parfois, les applications peuvent être amenées à mapper les coordonnées d’une fenêtre à celles d’une autre fenêtre. Une application peut mapper les coordonnées à l’aide de la fonction [**MapWindowPoints**](/windows/desktop/api/Winuser/nf-winuser-mapwindowpoints) . Si l’une des fenêtres est la fenêtre du bureau, la fonction convertit effectivement les coordonnées d’écran en coordonnées clientes et vice versa ; la fenêtre du Bureau est toujours spécifiée en coordonnées d’écran.

 

 
