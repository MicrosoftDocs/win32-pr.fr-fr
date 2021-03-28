---
title: imm_atomic_umin (SM5-ASM)
description: Min non signé atomique immédiat en mémoire. Retourne la valeur en mémoire avant l’opération max.
ms.assetid: B4556DA0-EE34-4420-A3AE-B340B4B1EB83
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8c65b2b5a58859e0729f567d9575f889b589821
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030560"
---
# <a name="imm_atomic_umin-sm5---asm"></a>IMM \_ Atomic \_ Umin (SM5-ASM)

Min non signé atomique immédiat en mémoire. Retourne la valeur en mémoire avant l’opération max.



| IMM \_ Atomic \_ Umin dst0 \[ . \_ \_ masque de composant unique \] , dst1, dstAddress \[ . Swizzle \] , src0 \[ . Sélectionner un \_ composant\] |
|--------------------------------------------------------------------------------------------------------------|



 



| Élément                                                                                                           | Description                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[dans \] contient la valeur de *dst1* avant cette instruction.<br/>                                                         |
| <span id="dst1"></span><span id="DST1"></span>*dst1*<br/>                                                | \[dans \] un affichage d’accès non ordonné (UAV) (u \# ). Dans le nuanceur de calcul, il peut également s’agir d’une mémoire partagée de groupe de threads (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[dans \] l’adresse mémoire.<br/>                                                                                             |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[dans \] la valeur à comparer à *Dst1* sur *dstAddress*.<br/>                                                                 |



 

## <a name="remarks"></a>Notes

Cette instruction exécute un seul composant 32 bits non signé de l’opérande *src0* avec *dst1* à 32 bits par adresse de composant *dstAddress*.

Si *dst1* est un u \# , il a peut-être été déclaré comme brut, typé ou structuré. Si elle est typée, elle doit être déclarée en tant que UINT/Saint-avec le format de ressource lié R32 \_ uint/Saint-est \_ .

Si *dst1* est g \# , il doit être déclaré comme RAW ou Structured.

La valeur de la mémoire *dst1* avant min est retournée à *dst0*.

Le nombre de composants pris à partir de l’adresse est déterminé par la dimensionnalité de *dst1*.

La totalité de l’opération est effectuée atomiquement.

Si l’appel du nuanceur est inactif, par exemple si le pixel qui a été ignoré précédemment dans son exécution, ou un appel pixel/échantillon n’existe que pour servir d’assistance à un réel pixel/échantillon pour les dérivés, cette instruction ne modifie pas du tout la mémoire *dst1* , et la valeur retournée n’est pas définie.

L’adressage hors limites sur u n' \# entraîne pas l’écriture dans la mémoire, sauf si u \# est structuré et que l’offset d’octet dans le struct (composant « second » de l’adresse) est à l’origine de l’accès hors limites, alors que le contenu entier du UAV devient non défini.

L’adressage hors limites sur u \# ou g \# entraîne le retour d’un résultat non défini au nuanceur dans *dst0*.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette instruction est prise en charge dans les modèles de nuanceur suivants :



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | Oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | non        |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | non        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 5 du nuanceur (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





