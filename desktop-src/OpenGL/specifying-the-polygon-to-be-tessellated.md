---
title: Spécification du polygone à répartir
description: Vous spécifiez un polygone (contenant éventuellement des trous) à utiliser
ms.assetid: 23e56d3e-c26c-4158-b0ce-cf8fcea22927
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff36b74f9484a76f938a7a24847c218f5c4e8dbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940281"
---
# <a name="specifying-the-polygon-to-be-tessellated"></a>Spécification du polygone à répartir

Vous spécifiez un polygone (éventuellement contenant des trous) à utiliser comme suit :

-   [**gluBeginPolygon**](glubeginpolygon.md)
-   [**gluTessVertex**](glutessvertex.md)
-   [**gluNextContour**](glunextcontour.md)
-   [**gluEndPolygon**](gluendpolygon.md)

Pour les polygones sans trous, le processus de spécification est exactement le même que dans OpenGL :

1.  Commencez par [**gluBeginPolygon**](glubeginpolygon.md).
2.  Appelez [**gluTessVertex**](glutessvertex.md) pour chaque vertex de la limite.
3.  Terminez le polygone avec un appel à [**gluEndPolygon**](gluendpolygon.md).

Si un polygone est constitué de plusieurs contours, y compris des trous et des trous dans des trous, vous spécifiez les contournements l’un après l’autre, avant chacun par [**gluNextContour**](glunextcontour.md). Lorsque vous appelez [**gluEndPolygon**](gluendpolygon.md), il signale la fin du contour final et démarre le pavage. Vous pouvez omettre l’appel à **gluNextContour** avant le premier contour. La fonction [**gluBeginPolygon**](glubeginpolygon.md) commence la spécification d’un polygone à fractionner et associe un objet polygonalisation, **tessobj**, à ce dernier. Les fonctions de rappel à utiliser sont celles que vous liez à l’objet de pavage avec [*gluTessCallback*](glutess.md).

La fonction [**gluTessVertex**](glutessvertex.md) spécifie un sommet dans le polygone à détourer. Appelez **gluTessVertex** pour chaque vertex du polygone. Le paramètre *tessobj* de la fonction est l’objet de pavage à utiliser, *v* contient les coordonnées des sommets à trois dimensions, et les *données* sont un pointeur arbitraire qui est envoyé au rappel associé au **\_ vertex Glu**. En règle générale, les *données* contiennent des données de vertex, des coordonnées de texture, des informations de couleur ou tout autre que l’application peut nécessiter.

La fonction [**gluNextContour**](glunextcontour.md) marque le début de l’isolignes suivant lorsque plusieurs contournements composent la limite du polygone à déborder. Le paramètre de *type* de la fonction peut être **Glu \_ extérieur**, **Glu \_ Interior**, **Glu \_ CCW**, **Glu \_ CW** ou **Glu \_ Unknown**. Ces constantes servent uniquement d’indicateurs au pavage. Si vous le faites, le pavage peut être plus rapide. Si vous les recevez mal, elles sont ignorées et le pavage fonctionne toujours.

Pour un polygone avec trous, un contour est le contour extérieur et les autres sont intérieurs. Si vous n’appelez pas **gluNextContour** immédiatement après [**gluBeginPolygon**](glubeginpolygon.md), le premier contour est supposé être de type **Glu \_ externe**.

**Glu \_** Les **\_ CCW** en PV et Glu indiquent les polygones orientés dans le sens des aiguilles d’une montre. Choisir les sens des aiguilles d’une montre et qui sont des aiguilles d’une montre arbitraire dans trois dimensions, mais dans n’importe quel plan, il existe deux orientations différentes ; Utilisez les types **\_ CCW** **Glu \_ CW** et Glu de manière cohérente. Utilisez **Glu \_ Unknown** si vous ne savez pas lequel utiliser.

La fonction [**gluEndPolygon**](gluendpolygon.md) indique la fin de la spécification Polygon. Il indique également que le pavage peut commencer à utiliser l’objet de pavage *tessobj*.

 

 




