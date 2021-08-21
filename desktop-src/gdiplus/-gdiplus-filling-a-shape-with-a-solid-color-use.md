---
description: Pour remplir une forme avec une couleur unie, créez un objet SolidBrush, puis transmettez l’adresse de cet objet SolidBrush en tant qu’argument à l’une des méthodes de remplissage de la classe Graphics.
ms.assetid: cedef138-5047-4a72-8b89-5a95062a351c
title: Remplissage d’une forme avec une couleur unie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ad3ecb5efb3bde32f696db8b97319d89834886eb63a70cd45289e49db03863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036717"
---
# <a name="filling-a-shape-with-a-solid-color"></a>Remplissage d’une forme avec une couleur unie

Pour remplir une forme avec une couleur unie, créez un objet [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) , puis transmettez l’adresse de cet objet **SolidBrush** en tant qu’argument à l’une des méthodes de remplissage de la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . L’exemple suivant montre comment remplir une ellipse avec la couleur rouge :


```
SolidBrush solidBrush(Color(255, 255, 0, 0));
stat = graphics.FillEllipse(&solidBrush, 0, 0, 100, 60);
```



Dans l’exemple précédent, le constructeur [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) prend une référence d’objet [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) comme seul argument. Les valeurs utilisées par le constructeur de **couleur** représentent les composants alpha, rouge, vert et bleu de la couleur. Chacune de ces valeurs doit être comprise entre 0 et 255. Le premier 255 indique que la couleur est entièrement opaque, tandis que le deuxième 255 indique que le composant rouge est en intensité complète. Les deux zéros indiquent que les composants vert et bleu ont tous les deux une intensité égale à 0.

Les quatre nombres (0, 0, 100, 60) passés à la méthode [**Graphics :: FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inint_inint_inint_inint)) spécifient l’emplacement et la taille du rectangle englobant pour l’ellipse. Le rectangle a un angle supérieur gauche de (0,0), une largeur de 100 et une hauteur de 60.

 

 
