---
description: Une application doit utiliser une structure RECT pour définir un rectangle.
ms.assetid: 93c63dcb-6c8e-4c8b-aa19-6f8952d75e2e
title: Coordonnées des rectangles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bf39ba5676b56fc3b9a32fbdd002944955d9e977e93eb4a7943c8a07be75946
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092789"
---
# <a name="rectangle-coordinates"></a>Coordonnées des rectangles

Une application doit utiliser une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) pour définir un rectangle. La structure spécifie les coordonnées de deux points : les angles supérieur gauche et inférieur droit du rectangle. Les côtés du rectangle s’étendent à partir de ces deux points et sont parallèles aux axes x et y.

Les valeurs de coordonnée d’un rectangle sont exprimées en tant qu’entiers signés. La valeur de coordonnée du côté droit d’un rectangle doit être supérieure à celle du côté gauche. De même, la valeur de coordonnée du bas doit être supérieure à celle du haut.

Étant donné que les applications peuvent utiliser des rectangles à de nombreuses fins différentes, les fonctions rectangle n’utilisent pas d’unité de mesure explicite. Au lieu de cela, toutes les coordonnées et les dimensions des rectangles sont indiquées dans des valeurs logiques signées. Le mode de mappage et la fonction dans laquelle le rectangle est utilisé déterminent les unités de mesure. Pour plus d’informations sur les coordonnées et les modes de mappage, consultez [espaces de coordonnées et transformations](coordinate-spaces-and-transformations.md).

 

 
