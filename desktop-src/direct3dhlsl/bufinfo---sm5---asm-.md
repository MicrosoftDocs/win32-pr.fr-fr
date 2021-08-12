---
title: bufinfo (SM5-ASM)
description: Interroge le nombre d’éléments sur une mémoire tampon (mais pas sur la mémoire tampon constante).
ms.assetid: 3A5C28F3-FE59-4C67-92AC-66B10E1D9692
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a107896973e7457b4bf596843ec77934d95675d50a146190a7f9f40e1c2ce3c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118287582"
---
# <a name="bufinfo-sm5---asm"></a>bufinfo (SM5-ASM)

Interroge le nombre d’éléments sur une mémoire tampon (mais pas sur la mémoire tampon constante).



| bufinfo dest \[ . Mask \] , srcResource |
|------------------------------------|



 



| Élément                                                                                                               | Description                                                                           |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[dans \] l’adresse des résultats.<br/>                                         |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[dans \] une mémoire tampon, autre qu’une mémoire tampon constante, dans un SRV (t \# ) ou un UAV (u \# ).<br/> |



 

## <a name="remarks"></a>Notes

Tous les composants de *dest* reçoivent le nombre entier d’éléments dans l’affichage des ressources de nuanceur de tampon s. Le nombre d’éléments dépend des paramètres de vue tels que le format de la mémoire.

Pour une mémoire tampon typée SRV ou UAV, la valeur de retour est le nombre d’éléments dans la vue (où un élément est une unité du format typé).

Pour une mémoire tampon brute SRV ou UAV, la valeur de retour est le nombre d’octets dans la vue.

Pour une mémoire tampon structurée SRV ou UAV, la valeur de retour est le nombre de structures dans la vue.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domain | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette instruction est prise en charge dans les modèles de nuanceur suivants :



| Modèle de nuanceur                                              | Pris en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | Non        |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | Non        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 5 du nuanceur (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





