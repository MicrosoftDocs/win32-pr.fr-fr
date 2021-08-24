---
description: Les composants d’éclairage diffus et spéculaire de l’équation d’éclairage global contiennent des termes qui décrivent l’atténuation de la lumière et le cône en vedette. Ces termes sont décrits ci-dessous.
ms.assetid: 960b5fc2-3074-4e51-b3de-5ed370379b01
title: Facteur d’atténuation et de focalisation (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb80fff287749e2979a89f2e20c830fdad3961d90ec05bf90a4ee2f6a51f8bcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850613"
---
# <a name="attenuation-and-spotlight-factor-direct3d-9"></a>Facteur d’atténuation et de focalisation (Direct3D 9)

Les composants d’éclairage diffus et spéculaire de l’équation d’éclairage global contiennent des termes qui décrivent l’atténuation de la lumière et le cône en vedette. Ces termes sont décrits ci-dessous.

## <a name="attenuation"></a>Atténuation

L’atténuation d’une lumière dépend du type de lumière et de la distance entre la lumière et la position du sommet. Pour calculer l’atténuation, utilisez l’une des équations suivantes.

Atten = 1/(att0<sub>i</sub> + Att1<sub>i</sub> \* d + att2<sub>i</sub> \* d ²)

Où :



| Paramètre        | Valeur par défaut | Type  | Description                                     | Plage          |
|------------------|---------------|-------|-------------------------------------------------|----------------|
| att0<sub>i</sub> | 0.0           | FLOAT | Facteur d’atténuation constant                     | 0 à + infini |
| Att1<sub>i</sub> | 0.0           | FLOAT | Facteur d’atténuation linéaire                       | 0 à + infini |
| att2<sub>i</sub> | 0.0           | FLOAT | Facteur d’atténuation quadratique                    | 0 à + infini |
| d                | N/A           | FLOAT | Distance de la position du sommet à la position de la lumière | N/A            |



 

-   Atten = 1, si la lumière est une lumière directionnelle.
-   Atten = 0, si la distance entre la lumière et le vertex est supérieure à la plage de la lumière.

Les valeurs att0, Att1, att2 sont spécifiées par les membres Attenuation0, Attenuation1 et Attenuation2 de [**D3DLIGHT9**](d3dlight9.md).

La distance entre la lumière et la position du vertex est toujours positive.

d = \| L<sub>Rép</sub>\|

Où :



| Paramètre       | Valeur par défaut | Type      | Description                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| <sub>Rép</sub> . | N/A           | D3DVECTOR | Vecteur de direction de la position du vertex à la position de la lumière |



 

Si d est supérieur à la plage de la lumière, autrement dit, le membre de plage d’une structure [**D3DLIGHT9**](d3dlight9.md) , Direct3D n’effectue aucun calcul d’atténuation supplémentaire et n’applique aucun effet de la lumière au vertex.

Les constantes d’atténuation jouent le rôle de coefficient dans la formule. vous pouvez produire diverses courbes d’atténuation en effectuant des ajustements simples. Vous pouvez affecter à Attenuation1 la valeur 1,0 pour créer une lumière qui n’est pas atténuée, mais qui est toujours limitée par plage, ou vous pouvez faire des essais avec différentes valeurs pour obtenir divers effets d’atténuation.

L’atténuation à la plage maximale de la lumière n’est pas 0,0. Pour empêcher l’apparition soudaine de voyants lorsqu’ils sont à l’intervalle de luminosité, une application peut augmenter la plage lumineuse. Ou bien, l’application peut configurer des constantes d’atténuation afin que le facteur d’atténuation soit proche de 0,0 à la plage lumineuse. La valeur d’atténuation est multipliée par les composants rouge, vert et bleu de la couleur de la lumière pour mettre à l’échelle l’intensité de la lumière en tant que facteur de la lumière de distance se déplace vers un sommet.

## <a name="spotlight-factor"></a>Facteur Gong

L’équation suivante spécifie le facteur Spotlight.

![équation du facteur Spotlight](images/dx8light9.png)



| Paramètre         | Valeur par défaut | Type  | Description                              | Plage                    |
|-------------------|---------------|-------|------------------------------------------|--------------------------|
| Rhô<sub>i</sub>   | N/A           | FLOAT | cosinus (angle) pour la lumière            | N/A                      |
| Phi<sub>i</sub>   | 0.0           | FLOAT | Penumbra angle de lumière en radians | \[thêta<sub>i</sub>, pi) |
| thêta<sub>i</sub> | 0.0           | FLOAT | Umbra angle de lumière en radians    | \[0, pi)                 |
| atténuation           | 0.0           | FLOAT | Facteur d’atténuation                           | (-infini, + infini)   |



 

Où :

Rhô = normal (L<sub>DCS</sub>)<sup>.</sup> normal (L<sub>Rép</sub>)

et



| Paramètre       | Valeur par défaut | Type      | Description                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| L<sub>DC</sub> | N/A           | D3DVECTOR | Négatif de la direction de la lumière dans l’espace de l’appareil photo         |
| <sub>Rép</sub> . | N/A           | D3DVECTOR | Vecteur de direction de la position du vertex à la position de la lumière |



 

Après le calcul de l’atténuation légère, Direct3D considère également les effets de Spotlight, le cas échéant, l’angle que la lumière reflète d’une surface et la réflectivité de la matière actuelle pour calculer les composants diffus et spéculaire pour ce vertex. Pour plus d’informations, consultez [Spotlight](light-types.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mathématiques d’éclairage](mathematics-of-lighting.md)
</dt> </dl>

 

 



