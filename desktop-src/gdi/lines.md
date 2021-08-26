---
description: 'Une ligne est un ensemble de pixels en surbrillance sur un affichage raster (ou un ensemble de points sur une page imprimée) identifié par deux points : un point de départ et un point de fin.'
ms.assetid: 538aa3c3-e13a-40dc-b977-3e353a7e9893
title: Lignes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b81976984cecc3d4d3b27fb3e474e896c6e81f03e6f601db36418b9e3cf197c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062099"
---
# <a name="lines"></a>Lignes

Une ligne est un ensemble de pixels en surbrillance sur un affichage raster (ou un ensemble de points sur une page imprimée) identifié par deux points : un point de départ et un point de fin. Le pixel situé au point de départ est toujours inclus dans la ligne, et le pixel situé au point de fin est toujours exclu. (Ce type de ligne est parfois appelé inclusive-exclusive.)

Lorsqu’une application appelle l’une des fonctions de dessin de ligne, GDI (Graphics Device Interface) ou, dans certains cas, un pilote de périphérique, détermine les pixels qui doivent être mis en surbrillance. GDI est une bibliothèque de liens dynamiques (DLL) qui traite les appels de fonction graphique d’une application et transmet ces appels à un pilote de périphérique. Un pilote de périphérique est une DLL qui reçoit l’entrée de GDI, convertit l’entrée en commandes de périphérique et transmet ces commandes à l’appareil approprié. GDI utilise un analyseur différentiel numérique (DDA) pour déterminer l’ensemble des pixels qui définissent une ligne. Un DDA détermine le jeu de pixels en examinant chaque point sur la ligne et en identifiant les pixels sur la surface d’affichage (ou les points d’une page imprimée) qui correspondent aux points. L’illustration suivante montre une ligne, son point de départ, son point de fin et les pixels mis en surbrillance à l’aide d’un DDA simple.

![Illustration montrant une grille de pixels, les points de début et de fin, une ligne et une trame de fond sur les pixels qui se trouvent le long de la ligne](images/cslcv-01.png)

Le DDA le plus simple et le plus courant est Bresenham, ou incrémentiel, DDA. Une version modifiée de cet algorithme dessine des lignes dans Windows. Le DDA incrémentiel est noté pour sa simplicité, mais il est également indiqué comme étant inexact. Étant donné qu’elle s’arrondit à la valeur entière la plus proche, elle ne peut parfois pas représenter la ligne d’origine demandée par l’application. Le DDA utilisé par GDI n’est pas arrondi à l’entier le plus proche. Par conséquent, ce nouveau DDA produit une sortie qui est parfois nettement plus proche de l’apparence de la ligne d’origine demandée par l’application.

> [!Note]  
> Si une application requiert une sortie de ligne qui ne peut pas être obtenue avec le nouveau DDA, elle peut dessiner ses propres lignes en appelant la fonction [**LineDDA**](/windows/desktop/api/Wingdi/nf-wingdi-linedda) et en fournissant un DDA privé ([**LineDDAProc**](/windows/desktop/api/Wingdi/nc-wingdi-lineddaproc)). Toutefois, la fonction **LineDDA** dessine des lignes beaucoup plus lentes que les fonctions de dessin de lignes. N’utilisez pas cette fonction dans une application si la vitesse est une préoccupation principale.

 

Une application peut utiliser le nouveau DDA pour dessiner des lignes uniques et plusieurs segments de ligne connectés. Une application peut dessiner une seule ligne en appelant la fonction [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) . Cette fonction dessine une ligne à partir de la position actuelle jusqu’à un point de terminaison spécifié, sans l’inclure. Une application peut dessiner une série de segments de ligne connectés en appelant la fonction [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) , en fournissant un tableau de points qui spécifient le point de fin de chaque segment de ligne. Une application peut dessiner plusieurs séries disjointes de segments de ligne connectés en appelant la fonction [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline) , en fournissant les points de terminaison requis.

L’illustration suivante montre la sortie de ligne créée en appelant les fonctions [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto), [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)et [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline) .

![Illustration montrant une ligne droite, une zone en forme de « l » et deux formes qui apparaissent en trois dimensions](images/cslcv-02.png)

 

 



