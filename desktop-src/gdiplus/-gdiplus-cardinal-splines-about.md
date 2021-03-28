---
description: Une spline cardinale est une séquence de courbes individuelles jointes pour former une plus grande courbe.
ms.assetid: 4fc62f00-7006-4ade-bfcc-091a3a97d889
title: Splines cardinales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d85c0163e405a6f9346f521b4057eb936108cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202447"
---
# <a name="cardinal-splines"></a>Splines cardinales

Une spline cardinale est une séquence de courbes individuelles jointes pour former une plus grande courbe. La spline est spécifiée par un tableau de points et un paramètre de tension. Une spline cardinale passe en douceur à chaque point du tableau ; Il n’y a pas d’angles aigus et aucune modification brusque de l’étanchéité de la courbe. L’illustration suivante montre un ensemble de points et une spline cardinale qui traverse chaque point du jeu.

![Illustration montrant une spline cardinale qui passe par six points définis](images/aboutgdip02-art09.gif)

Une spline physique est un morceau mince de bois ou autre matériau flexible. Avant l’avènement des splines mathématiques, les concepteurs utilisaient des splines physiques pour dessiner des courbes. Un concepteur place la spline sur une feuille de papier et l’ancre à un ensemble donné de points. Le concepteur peut ensuite créer une courbe en dessinant le long de la spline avec un crayon. Un ensemble de points donné peut produire diverses courbes, en fonction des propriétés de la spline physique. Par exemple, une spline avec une résistance élevée à la flexion produirait une courbe différente de celle d’une spline extrêmement flexible.

Les formules pour les splines mathématiques sont basées sur les propriétés des tiges flexibles, donc les courbes produites par les splines mathématiques sont similaires aux courbes qui ont été produites par les splines physiques. Tout comme les splines physiques de la traction différente produisent des courbes différentes à travers un ensemble de points donné, les splines mathématiques avec des valeurs différentes pour le paramètre de tension produisent des courbes différentes à travers un ensemble de points donné. L’illustration suivante montre quatre splines cardinales passant par le même ensemble de points. La tension est indiquée pour chaque spline. Notez qu’une tension de 0 correspond à une tension physique infinie, forçant la courbe à prendre la manière la plus rapide (lignes droites) entre les points. Une tension de 1 correspond à aucune tension physique, ce qui permet à la spline de prendre le chemin du moins de pli total. Avec les valeurs de tension supérieures à 1, la courbe se comporte comme un ressort compressé, push pour prendre un chemin d’accès plus long.

![Illustration montrant quatre splines cardinales par le biais des trois mêmes points](images/aboutgdip02-art10.gif)

Notez que les quatre splines de la figure précédente partagent la même ligne tangente au point de départ. La tangente est la ligne dessinée à partir du point de départ jusqu’au point suivant le long de la courbe. De même, la tangente partagée au point de fin est la ligne dessinée à partir du point de fin jusqu’au point précédent sur la courbe.

Pour dessiner une spline cardinale, vous avez besoin d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , d’un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) et d’un tableau d’objets [**point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) . L’objet **Graphics** fournit la méthode [DrawCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpointf_inint_inreal)) , qui dessine la spline, et l’objet **Pen** stocke les attributs de la spline, tels que la largeur et la couleur de ligne. Le tableau d’objets **point** stocke les points que la courbe passera. L’exemple suivant dessine une spline cardinale qui traverse les points de *myPointArray*. Le troisième paramètre est la tension.


```
myGraphics.DrawCurve(&myPen, myPointArray, 3, 1.5f);
```



 

 



