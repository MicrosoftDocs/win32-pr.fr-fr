---
description: La propriété type de lumière définit le type de source de lumière que vous utilisez.
ms.assetid: 7718383a-6e49-4ad2-acc1-fc8fec0d4844
title: Types de lumière (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd451fcf45e67f1d789b7481fcc1884282d2018db98ab26d27481bec5277031
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674419"
---
# <a name="light-types-direct3d-9"></a>Types de lumière (Direct3D 9)

La propriété type de lumière définit le type de source de lumière que vous utilisez. Le type de lumière est défini à l’aide d’une valeur de l’énumération C++ [**D3DLIGHTTYPE**](./d3dlighttype.md) dans le membre de type de la structure [**D3DLIGHT9**](d3dlight9.md) de la lumière. Il existe trois types d’éclairages dans les lumières de point Direct3D, les lumières et les lumières directionnelles. Chaque type éclaire les objets dans une scène différemment, avec des niveaux de surcharge de calcul différents.

## <a name="point-light"></a>Lumière du point

Les lumières de point ont une couleur et une position dans une scène, mais pas de sens unique. Elles s’imbriquent uniformément dans toutes les directions, comme indiqué dans l’illustration suivante.

![illustration de la lumière du point](images/ptlight.png)

Une ampoule est un bon exemple de lumière de point. Les lumières de point sont affectées par l’atténuation et la plage, et illuminent une maille sur une base vertex-par-vertex. Pendant l’éclairage, Direct3D utilise la position de la lumière dans l’espace universel et les coordonnées du sommet qui sont allumées pour dériver un vecteur pour la direction de la lumière, et la distance que la lumière a parcourue. Les deux sont utilisés, avec la normale au vertex, pour calculer la contribution de la lumière à l’éclairage de l’aire.

## <a name="directional-light"></a>Clair directionnel

Les lumières directionnelles ont uniquement des couleurs et des directions, et non des positions. Ils émettent une lumière parallèle. Cela signifie que toute la lumière générée par les lumières directionnelles se déplace dans une scène dans la même direction. Imagine une lumière directionnelle comme source de lumière à une distance proche de l’infini, telle que le soleil. Les lumières directionnelles ne sont pas affectées par l’atténuation ou la plage. par conséquent, la direction et la couleur que vous spécifiez sont les seuls facteurs pris en compte lorsque Direct3D calcule les couleurs des sommets. En raison du petit nombre de facteurs d’éclairage, il s’agit du moins de lumières gourmandes en calculs à utiliser.

## <a name="spotlight"></a>Vedette

Les spotlights ont une couleur, une position et une direction dans lesquelles ils émettent de la lumière. La lumière émise à partir d’une Spotlight est constituée d’un cône interne vif et d’un cône externe plus grand, avec l’intensité de la lumière qui diminue entre les deux, comme indiqué dans l’illustration suivante.

![illustration d’une lumière en vedette avec cône interne et cône externe](images/spotlt.png)

Les actualités sont affectées par l’atténuation, l’atténuation et la plage. Ces facteurs, ainsi que la distance qui traverse chaque vertex, sont présents dans le calcul des effets d’éclairage pour les objets d’une scène. Le calcul de ces effets pour chaque vertex rend les actualités plus gourmandes en termes de temps pour toutes les lumières dans Direct3D.

La structure C++ [**D3DLIGHT9**](d3dlight9.md) contient trois membres qui sont utilisés uniquement par les actualités. Ces membres (atténuation, thêta et Phi) contrôlent la taille ou la taille des cônes internes et externes d’un objet Spotlight, et la façon dont la lumière les réduit.

La valeur thêta est l’angle Radian du cône interne de la lumière, et la valeur Phi est l’angle du cône externe de la lumière. La valeur de retrait contrôle la manière dont l’intensité lumineuse diminue entre le bord extérieur du cône interne et le bord intérieur du cône externe. La plupart des applications définissent la valeur 1,0 pour créer une atténuation qui se produit uniformément entre les deux cônes, mais vous pouvez définir d’autres valeurs en fonction des besoins.

L’illustration suivante montre la relation entre les valeurs de ces membres et la manière dont ils peuvent affecter les cônes internes et externes d’un projecteur de lumière.

![illustration de la relation entre les valeurs Phi et thêta et les cônes Spotlight](images/spotlt2.png)

Les lumières émettent un cône de lumière qui comporte deux parties : un cône interne vif et un cône externe. La lumière est claire dans le cône interne et n’est pas présente en dehors du cône externe, avec une intensité lumineuse qui atténue entre les deux zones. Ce type d’atténuation est communément appelé atténuation.

La quantité de lumière reçue par un vertex est basée sur l’emplacement du vertex dans les cônes internes ou externes. Direct3D calcule le produit scalaire du vecteur de direction du projecteur (L) et du vecteur de la lumière jusqu’au sommet (D). Cette valeur est égale au cosinus de l’angle entre les deux vecteurs et sert d’indicateur de la position du sommet qui peut être comparé aux angles coniques de la lumière pour déterminer où le vertex peut se trouver dans les cônes internes ou externes. L’illustration suivante fournit une représentation graphique de l’association entre ces deux vecteurs.

![illustration du vecteur de direction Spotlight et du vecteur du sommet à la lumière](images/spotalg1.png)

Le système compare cette valeur au cosinus des angles de cône interne et externe de la lumière. Dans la structure [**D3DLIGHT9**](d3dlight9.md) de la lumière, les membres thêta et Phi représentent les angles de cônes totaux pour les cônes internes et externes. Étant donné que l’atténuation se produit lorsque le vertex devient plus éloigné du centre d’éclairage (plutôt qu’à travers l’angle de cône total), le runtime divise ces angles de cône en deux avant de calculer leurs cosinus.

Si le produit scalaire des vecteurs L et D est inférieur ou égal au cosinus de l’angle du cône externe, le sommet se situe au-delà du cône externe et ne reçoit pas de lumière. Si le produit scalaire de L et D est supérieur au cosinus de l’angle du cône interne, le vertex se trouve dans le cône interne et reçoit la quantité maximale de lumière, en prenant toujours en compte l’atténuation sur la distance. Si le vertex est situé entre les deux régions, le retrait est calculé avec l’équation suivante.

![formule pour l’intensité de l’éclairage au sommet, après retrait](images/falloff.png)

Où :

-   I <sub>f</sub> est une intensité légère après retrait
-   Alpha est l’angle entre les vecteurs L et D
-   Thêta est l’angle conique interne
-   Phi est l’angle du cône externe
-   p est le retrait

Cette formule génère une valeur comprise entre 0,0 et 1,0 qui met à l’échelle l’intensité de la lumière au niveau du vertex pour prendre en compte la dépassation. L’atténuation en tant que facteur de la distance du sommet par rapport à la lumière est également appliquée. Le graphique suivant montre comment différentes valeurs de retrait peuvent affecter la courbe d’atténuation.

![graphique de l’intensité de la lumière et de la distance du vertex par rapport à la lumière](images/fallgraf.png)

L’effet de diverses valeurs d’atténuation sur l’éclairage réel est subtil, et une faible baisse des performances est provoquée par la mise en forme de la courbe décroissante avec des valeurs d’atténuation autres que 1,0. Pour ces raisons, cette valeur est généralement définie sur 1,0.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lumières et matériaux](lights-and-materials.md)
</dt> </dl>

 

 
