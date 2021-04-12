---
description: Les propriétés de lumière décrivent le type et la couleur d’une source de lumière.
ms.assetid: b39f1287-c67b-4cbb-b599-4a1b2f4981ac
title: Propriétés de la lumière (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63239024109327e483ff93c2ee29fe42fc22c922
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108842"
---
# <a name="light-properties-direct3d-9"></a>Propriétés de la lumière (Direct3D 9)

Les propriétés de lumière décrivent le type et la couleur d’une source de lumière. Selon le type de lumière utilisé, une lumière peut avoir des propriétés pour l’atténuation et la plage, ou pour les effets de Spotlight. Toutefois, tous les types d’éclairage n’utilisent pas toutes les propriétés. Direct3D utilise la structure [**D3DLIGHT9**](d3dlight9.md) pour transporter des informations sur les propriétés de lumière pour tous les types de sources de lumière. Cette section contient des informations sur toutes les propriétés de Light. Les informations sont réparties dans les groupes suivants.

Les propriétés de position, de plage et d’atténuation définissent l’emplacement d’une lumière dans l’espace universel et la façon dont la lumière émet le comportement sur la distance. Comme avec toutes les propriétés de lumière que vous utilisez en C++, celles-ci sont contenues dans la structure [**D3DLIGHT9**](d3dlight9.md) d’une lumière.

-   [Atténuation de la lumière](#light-attenuation)
-   [Couleur claire](#light-color)
-   [Direction de la lumière](#light-direction)
-   [Position de la lumière](#light-position)
-   [Plage de lumière](#light-range)

## <a name="light-attenuation"></a>Atténuation de la lumière

L’atténuation contrôle la manière dont l’intensité d’une lumière diminue vers la distance maximale spécifiée par la propriété de la plage. Trois membres de la structure [**D3DLIGHT9**](d3dlight9.md) représentent l’atténuation légère : Attenuation0, Attenuation1 et Attenuation2. Ces membres contiennent des valeurs à virgule flottante allant de 0,0 à Infinity, contrôlant l’atténuation d’une lumière. Certaines applications définissent le membre Attenuation1 sur 1,0 et les autres sur 0,0, ce qui donne une intensité légère qui change en 1/D, où D est la distance entre la source de lumière et le sommet. L’intensité de la lumière maximale est à la source, ce qui diminue jusqu’à 1/(plage d’éclairage) à la plage de la lumière. En règle générale, une application définit Attenuation0 sur 0,0, Attenuation1 sur une valeur constante et Attenuation2 sur 0,0.

Vous pouvez combiner des valeurs d’atténuation pour obtenir des effets d’atténuation plus complexes. Vous pouvez également les définir sur des valeurs en dehors de la plage normale pour créer des effets d’atténuation étrangers. Toutefois, les valeurs d’atténuation négatives ne sont pas autorisées. Consultez [facteur d’atténuation et de focalisation (Direct3D 9)](attenuation-and-spotlight-factor.md).

## <a name="light-color"></a>Couleur claire

Les lumières dans Direct3D émettent trois couleurs qui sont utilisées indépendamment dans les calculs d’éclairage du système : une couleur diffuse, une couleur ambiante et une couleur spéculaire. Chaque est incorporée par le module d’éclairage Direct3D, qui interagit avec un équivalent de la matière actuelle, pour produire une couleur finale utilisée dans le rendu. La couleur diffuse interagit avec la propriété de réflexion diffuse du matériau actuel, la couleur spéculaire avec la propriété de réflectivité spéculaire du matériau, et ainsi de suite. Pour plus d’informations sur la façon dont Direct3D applique ces couleurs, consultez [mathématique d’éclairage (Direct3D 9)](mathematics-of-lighting.md).

Dans une application C++, la structure [**D3DLIGHT9**](d3dlight9.md) comprend trois membres pour ces couleurs : diffusion, ambiant et spéculaire. chacune d’elles est une structure [**D3DCOLORVALUE**](d3dcolorvalue.md) qui définit la couleur émise.

Le type de couleur qui s’applique le plus lourdement aux calculs du système est la couleur diffuse. La couleur diffuse la plus courante est le blanc (R :1.0 G :1.0 B :1.0), mais vous pouvez créer des couleurs en fonction des besoins pour atteindre les effets souhaités. Par exemple, vous pouvez utiliser un feu rouge pour un foyer, ou vous pouvez utiliser une lumière verte pour un signal de trafic défini sur « Go ».

En règle générale, vous définissez les composants de couleur claire sur des valeurs comprises entre 0,0 et 1,0, inclus, mais ce n’est pas une condition requise. Par exemple, vous pouvez définir tous les composants sur 2,0, en créant une lumière « plus claire que le blanc ». Ce type de paramètre peut être particulièrement utile lorsque vous utilisez des paramètres d’atténuation autres que constants.

Notez que, bien que Direct3D utilise des valeurs RVBA pour les lumières, le composant de couleur alpha n’est pas utilisé.

En général, les couleurs matérielles sont utilisées pour l’éclairage. Toutefois, vous pouvez spécifier que les couleurs de matériau-émissif, ambiante, diffuse et spéculaire doivent être remplacées par des couleurs de vertex diffuses ou spéculaires. Pour ce faire, appelez [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) et définissez les variables d’état de l’appareil indiquées dans le tableau suivant.



| Variable d’état de l’appareil         | Signification                                       | Type                   | Default          |
|-------------------------------|-----------------------------------------------|------------------------|------------------|
| D3DRS \_ AMBIENTMATERIALSOURCE  | Définit où se trouver la couleur du matériau ambiant.  | D3DMATERIALCOLORSOURCE | \_Matériau D3DMCS |
| D3DRS \_ DIFFUSEMATERIALSOURCE  | Définit l’emplacement de la couleur du matériau diffus.  | D3DMATERIALCOLORSOURCE | D3DMCS \_ COLOR1   |
| D3DRS \_ SPECULARMATERIALSOURCE | Définit où se trouver la couleur de matériau spéculaire. | D3DMATERIALCOLORSOURCE | D3DMCS \_ COLOR2   |
| D3DRS \_ EMISSIVEMATERIALSOURCE | Définit où se trouver la couleur du matériau émissif. | D3DMATERIALCOLORSOURCE | \_Matériau D3DMCS |
| D3DRS \_ COLORVERTEX            | Désactive ou active l’utilisation des couleurs de vertex.     | BOOL                   | TRUE             |



 

La valeur alpha/Transparency provient toujours uniquement du canal alpha de la couleur diffuse.

La valeur de brouillard provient toujours uniquement du canal alpha de la couleur spéculaire.

D3DMATERIALCOLORSOURCE peut avoir les valeurs suivantes.

-   \_Matériau D3DMCS : la couleur du matériau est utilisée en tant que source.
-   D3DMCS \_ COLOR1 : la couleur de vertex diffuse est utilisée en tant que source.
-   D3DMCS \_ COLOR2-la couleur de vertex spéculaire est utilisée en tant que source.

## <a name="light-direction"></a>Direction de la lumière

La propriété direction d’une lumière détermine la direction de la lumière émise par l’objet, dans l’espace universel. La direction est utilisée uniquement par les lumières directionnelles et les Spotlights, et est décrite par un vecteur.

Définissez la direction de la lumière dans le membre direction de la structure [**D3DLIGHT9**](d3dlight9.md) de la lumière. Le membre de direction est de type [**D3DVECTOR**](d3dvector.md). Les vecteurs de direction sont décrits comme des distances à partir d’une origine logique, quelle que soit la position de la lumière dans une scène. Par conséquent, un projecteur qui pointe directement vers une scène, le long de l’axe z positif, a un vecteur de direction de <0, 0, 1> peu importe où sa position est définie comme étant. De même, vous pouvez simuler la lumière du soleil directement sur une scène en utilisant une lumière directionnelle dont la direction est <0,-1,0>. Évidemment, vous n’êtes pas obligé de créer des lumières qui brillent le long des axes de coordonnées ; vous pouvez mélanger et faire correspondre des valeurs pour créer des lumières qui brillent à des angles plus intéressants.

> [!Note]  
> Même si vous n’avez pas besoin de normaliser le vecteur de direction d’une lumière, assurez-vous qu’il a de l’amplitude. En d’autres termes, n’utilisez pas de vecteur de direction de <0, 0, 0>.

 

## <a name="light-position"></a>Position de la lumière

La position de la lumière est décrite à l’aide d’une structure [**D3DVECTOR**](d3dvector.md) dans le membre position de la structure [**D3DLIGHT9**](d3dlight9.md) . Les coordonnées x, y et z sont supposées être dans l’espace universel. Les lumières directionnelles sont le seul type de lumière qui n’utilise pas la propriété position.

## <a name="light-range"></a>Plage de lumière

La propriété de plage d’une lumière détermine la distance, dans l’espace universel, à laquelle les maillages dans une scène ne reçoivent plus de lumière émise par cet objet. Le membre de plage contient une valeur à virgule flottante qui représente la plage maximale de la lumière, dans l’espace universel. Les lumières directionnelles n’utilisent pas la propriété Range.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lumières et matériaux](lights-and-materials.md)
</dt> </dl>

 

 
