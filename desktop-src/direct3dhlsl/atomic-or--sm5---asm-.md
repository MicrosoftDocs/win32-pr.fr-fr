---
title: atomic_or (SM5-ASM)
description: Au niveau du bit atomique ou en mémoire.
ms.assetid: 5AFB96AA-267B-454E-9526-BA61A876ED42
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9b86bbdb7d282c14b0e2d30f8e1f996b9c0f4d2f1a09de7b03e549327e309e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794867"
---
# <a name="atomic_or-sm5---asm"></a>Atomic \_ ou (SM5-ASM)

Au niveau du bit atomique ou en mémoire.



| Atomic \_ ou DST, dstAddress \[ . Swizzle \] , src0 \[ . Select \_ Component\] |
|--------------------------------------------------------------------|



 



| Élément                                                                                                           | Description                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst"></span><span id="DST"></span>*destination*<br/>                                                   | \[dans \] les composants de ou avec *src0*. Cette valeur doit être un affichage d’accès non ordonné (UAV) \# . Dans le nuanceur de calcul, il peut également s’agir d’une mémoire partagée de groupe de threads (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[dans \] l’adresse mémoire.<br/>                                                                                                                                                |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[dans \] les composants de ou avec l' *heure d’été*.<br/>                                                                                                                                   |



 

## <a name="remarks"></a>Remarques

Cette instruction effectue un seul composant au niveau du bit 32 bits ou d’un opérande *src0* en *heure d’été* à 32 bits par adresse de composant *dstAddress*, exécuté atomiquement.

Le nombre de composants pris à partir de l’adresse est déterminé par la dimensionnalité de l' *heure d’été* u \# ou g \# .

Si *DST* est un u \# , il peut être déclaré comme brut, typé ou structuré. Si elle est typée, elle doit être déclarée en tant que UINT/Saint-avec le format de ressource lié R32 \_ uint/Saint-est \_ .

Si l' *heure d’été* est g \# , elle doit être déclarée comme brute ou structurée.

Rien n’est retourné au nuanceur.

Si l’appel du nuanceur est inactif, par exemple si le pixel a été ignoré plus tôt dans son exécution, ou si un appel pixel/échantillon n’existe que pour servir d’assistance à un réel pixel/échantillon pour les dérivés, cette instruction ne modifie pas la mémoire de l' *heure d’été* (en mode silencieux).

L’adressage hors limites sur u n' \# entraîne pas l’écriture dans la mémoire, sauf si u \# est structuré et que l’offset d’octet dans le struct (composant « second » de l’adresse) est à l’origine de l’accès hors limites, le contenu entier du UAV devient non défini.

En dehors des limites d’adressage sur g \# (les limites de ce g particulier \# , par opposition à toute la mémoire partagée), la totalité du contenu de la mémoire partagée devient non définie.

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

 

 





