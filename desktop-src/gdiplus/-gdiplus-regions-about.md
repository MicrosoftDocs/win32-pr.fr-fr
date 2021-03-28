---
description: Une région est une partie de la surface d’affichage.
ms.assetid: eb78d7a0-6293-487f-88c5-88ba455b965f
title: Régions (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d6a7f0a5a6d3df4b11a491111dbedf9e155c3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104562110"
---
# <a name="regions-gdi"></a>Régions (GDI+)

Une région est une partie de la surface d’affichage. Les régions peuvent être simples (un rectangle unique) ou complexes (une combinaison de polygones et de courbes fermées). L’illustration suivante montre deux régions : l’une construite à partir d’un rectangle et l’autre construite à partir d’un chemin d’accès.

![Illustration montrant une région rectangulaire transparente chevauchant une forme incurvée opaque](images/aboutgdip02-art27.png)

Les régions sont souvent utilisées pour le découpage et le test de positionnement. Le découpage implique la restriction du dessin à une certaine région de l’écran, généralement la partie de l’écran qui doit être mise à jour. Le test de positionnement implique la vérification pour déterminer si le curseur se trouve dans une certaine région de l’écran lorsqu’un bouton de la souris est enfoncé.

Vous pouvez construire une région à partir d’un rectangle ou d’un chemin d’accès. Vous pouvez également créer des régions complexes en combinant des régions existantes. La classe [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) fournit les méthodes suivantes pour combiner des régions [: Intersect](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-intersect(inconstregion)), [Union](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-union(inconstregion)), [Xor](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-xor(inconstrect_)), [Exclude](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-exclude(inconstregion))et [**Region :: complement**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-complement(inconstgraphicspath)).

L’intersection de deux régions est l’ensemble de tous les points appartenant aux deux régions. L’Union est l’ensemble de tous les points appartenant à l’une ou à l’autre, ou aux deux régions. Le complément d’une région est l’ensemble de tous les points qui ne sont pas dans la région. L’illustration suivante montre l’intersection et l’Union des deux régions de la figure précédente.

![Illustration montrant l’intersection des régions de l’illustration précédente, et leur intersection](images/aboutgdip02-art28.png)

La méthode [Xor](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-xor(inconstrect_)) , appliquée à une paire de régions, produit une région qui contient tous les points appartenant à une région ou à l’autre, mais pas les deux. La méthode [Exclude](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-exclude(inconstregion)) , appliquée à une paire de régions, produit une région qui contient tous les points de la première région qui ne sont pas dans la deuxième région. L’illustration suivante montre les régions qui résultent de l’application des méthodes XOR et Exclude aux deux régions indiquées au début de cette rubrique.

![Illustration montrant les parties dans l’une ou l’autre des régions, mais pas les deux, et la partie du rectangle qui ne chevauche pas la région incurvée](images/aboutgdip02-art29.png)

Pour remplir une région, vous avez besoin d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , d’un objet [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) et d’un objet [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) . L’objet **Graphics** fournit la méthode [**Graphics :: FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion) , et l’objet **Brush** stocke les attributs du remplissage, tels que la couleur ou le motif. L’exemple suivant remplit une région avec une couleur unie.


```
myGraphics.FillRegion(&mySolidBrush, &myRegion);
```



 

 
