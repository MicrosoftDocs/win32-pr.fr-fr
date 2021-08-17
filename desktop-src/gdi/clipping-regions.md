---
description: Une zone de découpage est l’un des objets graphiques qu’une application peut sélectionner dans un contexte de périphérique (DC).
ms.assetid: d9238ee5-3305-4e85-aef3-2c5c8b74aacd
title: Régions de découpage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0647d44d82e289b702e9111b62c5a138c8a0fa059428a6173af36f4eeca657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105914"
---
# <a name="clipping-regions"></a>Régions de découpage

Une zone de découpage est l’un des objets graphiques qu’une application peut sélectionner dans un contexte de périphérique (DC). Il est généralement rectangulaire. Certains contextes de périphérique fournissent une région de découpage prédéfinie ou par défaut, contrairement à d’autres. Par exemple, si vous obtenez un handle de contexte de périphérique à partir de la fonction [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) , le DC contient une zone de découpage rectangulaire prédéfinie qui correspond au rectangle non valide qui nécessite un redessin. Toutefois, lorsque vous obtenez un handle de contexte de périphérique en appelant la fonction [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) avec un paramètre _HWND_ **null**, ou en appelant la fonction [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) , le contrôleur de l’appareil ne contient pas de zone de découpage par défaut. Pour plus d’informations sur les contextes de périphérique retournés par la fonction **BeginPaint** , consultez [peinture et dessin](painting-and-drawing.md) . Pour plus d’informations sur les contextes de périphérique retournés par les fonctions **CreateDC** et **GetDC** , consultez [contextes de périphérique](device-contexts.md).

Les applications peuvent effectuer diverses opérations sur les régions de découpage. Certaines de ces opérations nécessitent un handle qui identifie la région, et d’autres non. Par exemple, une application peut effectuer les opérations suivantes directement sur la zone de découpage d’un contexte de périphérique.

-   Déterminez si la sortie des graphiques s’affiche dans les bordures de la région en transmettant les coordonnées de la ligne, de l’arc, de la bitmap, du texte ou de la forme remplie correspondante à la fonction [**PtVisible**](/windows/desktop/api/Wingdi/nf-wingdi-ptvisible) .
-   Déterminez si une partie de la zone cliente croise une région en appelant la fonction [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) .
-   Déplacez la région existante selon un décalage spécifié en appelant la fonction [**OffsetClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetcliprgn) .
-   Excluez une partie rectangulaire de la zone cliente de la zone de découpage en cours en appelant la fonction [**ExcludeClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-excludecliprect) .
-   Combinez une partie rectangulaire de la zone cliente avec la région de découpage en cours en appelant la fonction [**IntersectClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-intersectcliprect) .

Après avoir obtenu un handle identifiant la zone de découpage, une application peut effectuer n’importe quelle opération commune aux régions, par exemple :

-   Combinaison d’une copie de la zone de découpage en cours avec une deuxième région en appelant la fonction [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) .
-   Comparez une copie de la zone de découpage en cours à une deuxième région en appelant la fonction [**EqualRgn**](/windows/desktop/api/Wingdi/nf-wingdi-equalrgn) .
-   Déterminez si un point se trouve à l’intérieur d’une copie de la zone de découpage en cours en appelant la fonction [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) .

 

 



