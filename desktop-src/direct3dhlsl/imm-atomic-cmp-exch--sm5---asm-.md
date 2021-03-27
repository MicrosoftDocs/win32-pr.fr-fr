---
title: imm_atomic_cmp_exch (SM5-ASM)
description: Comparer et échanger immédiatement avec la mémoire.
ms.assetid: 317A69E1-0E0A-45C8-8E0A-B88659ADBECC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63e1be030d7cce0d6f0a581788db39a599272b2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841685"
---
# <a name="imm_atomic_cmp_exch-sm5---asm"></a>IMM \_ Atomic \_ CMP \_ Exch (SM5-ASM)

Comparer et échanger immédiatement avec la mémoire.



| IMM \_ Atomic \_ CMP \_ Exch dst0 \[ . \_ \_ masque de composant unique \] , dst1, dstAddress \[ . Swizzle \] , src0 \[ . Select \_ \] , src1 \[ . Select \_ Component\] |
|-----------------------------------------------------------------------------------------------------------------------------------------------|



 



| Élément                                                                                                           | Description                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[out \] contient *dst1* avant l’écriture.<br/>                                                                              |
| <span id="dst1"></span><span id="DST1"></span>*dst1*<br/>                                                | \[dans \] un affichage d’accès non ordonné (UAV) (u \# ). Dans le nuanceur de calcul, il peut également s’agir d’une mémoire partagée de groupe de threads (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[dans \] la mémoire de destination.<br/>                                                                                         |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[dans \] la valeur à comparer à *dst1*.<br/>                                                                                 |
| <span id="scr1"></span><span id="SCR1"></span>*scr1*<br/>                                                | \[dans \] la valeur écrite dans la mémoire de destination si les valeurs comparées sont identiques.<br/>                               |



 

Cette instruction effectue une comparaison de valeurs 32 bits de composant unique avec l’opérande *src0* avec *dst1* à 32 bits par adresse de composant *dstAddress*.

Si *dst1* est un u \# , il a peut-être été déclaré comme brut, typé ou structuré. Si elle est typée, elle doit être déclarée en tant que UINT/Saint-avec le format de ressource lié R32 \_ uint/Saint-est \_ .

Si *dst1* est g \# , il doit être déclaré comme RAW ou Structured.

Si les valeurs comparées sont identiques, la valeur 32 bits d’un seul composant dans *src1* est écrite dans la mémoire de destination. Dans le cas contraire, la mémoire de destination n’est pas modifiée.

La valeur 32 bits d’origine dans la mémoire de destination est toujours écrite dans *dst0*.

La totalité de l’opération est effectuée atomiquement.

Si l’appel du nuanceur est inactif, par exemple si le pixel a été ignoré plus tôt dans son exécution, ou s’il n’existe qu’un appel d’assistance à un réel pixel/échantillon pour les dérivés, cette instruction ne modifie pas le tout la mémoire *dst1* , et la valeur retournée n’est pas définie.

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

 

 





