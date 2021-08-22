---
title: imm_atomic_consume (SM5-ASM)
description: Décrémenter atomiquement le compteur 32 bits masqué stocké avec un nombre ou ajouter la vue d’accès non ordonné (UAV), en retournant la nouvelle valeur.
ms.assetid: 1115C318-2F86-4161-AC5C-2A61A262DC28
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0244b885d9d2c46b734994d5e101f79147839d0cf76e2bab5669e52700cf59e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119313"
---
# <a name="imm_atomic_consume-sm5---asm"></a>IMM \_ Atomic \_ consume (SM5-ASM)

Décrémenter atomiquement le compteur 32 bits masqué stocké avec un nombre ou ajouter la vue d’accès non ordonné (UAV), en retournant la nouvelle valeur.



| IMM \_ Atomic \_ consomme dst0 \[ . \_ \_ masque de composant unique \] , dstUAV |
|---------------------------------------------------------------|



 



| Élément                                                                                           | Description                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                | \[dans \] contient la valeur de compteur d’origine retournée.<br/>           |
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[dans \] une mémoire tampon structurée UAV avec l’indicateur Count ou Append. <br/> |



 

## <a name="remarks"></a>Remarques

Consultez [IMM \_ Atomic \_ Alloc](imm-atomic-alloc--sm5---asm-.md) pour une discussion sur la validité de la valeur du nombre retourné selon que le UAV est Count ou Append. Il en va de même pour la **\_ \_ consommation atomique IMM**.

**IMM \_ Atomic \_ consume** effectue une décrémentation atomique de la valeur de compteur, en retournant la nouvelle valeur à *dst0*.

Il n’y a pas de fixation du nombre. il est donc encapsulé sur un dépassement de capacité négatif.

Le même nuanceur ne peut pas tenter à la fois l' **\_ \_ allocation atomique de IMM** et le **IMM \_ Atomic \_ consommer** sur le même UAV. En outre, le GPU ne peut pas autoriser plusieurs appels de nuanceur à mélanger **\_ Atomic Atomic \_ Alloc** et **IMM \_ Atomic \_ consommer** sur le même UAV.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette instruction est prise en charge dans les modèles de nuanceur suivants :



| Modèle de nuanceur                                              | Pris en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | non        |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | non        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 5 du nuanceur (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





