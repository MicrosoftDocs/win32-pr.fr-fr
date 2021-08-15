---
title: atomic_cmp_store (SM5-ASM)
description: Comparaison atomique et écriture en mémoire.
ms.assetid: 1B97E983-11A9-47E4-B274-E94083837C6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dbc57b14b4279b9bd4844d89492852ae915d9d900ed04421eeeccc367979a63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118795161"
---
# <a name="atomic_cmp_store-sm5---asm"></a>\_stockage CMP atomique \_ (SM5-ASM)

Comparaison atomique et écriture en mémoire.



| Atomic \_ CMP \_ Store DST, dstAddress \[ . Swizzle \] , src0 \[ . Select \_ \] , composant, src1 \[ . Select \_ Component\] |
|--------------------------------------------------------------------------------------------------------|



 



| Élément                                                                                                           | Description                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst"></span><span id="DST"></span>*destination*<br/>                                                   | \[dans \] les composants à comparer à *src0*. Cette valeur doit être un affichage d’accès non ordonné (UAV) \# . Dans le nuanceur de calcul, il peut également s’agir d’une mémoire partagée de groupe de threads (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[dans \] l’adresse mémoire.<br/>                                                                                                                                                     |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[dans \] la valeur 32 bits à comparer avec l' *heure d’été*.<br/>                                                                                                                                 |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                                | \[dans \] la valeur à écrire dans la mémoire si les valeurs comparées sont identiques. <br/>                                                                                                     |



 

## <a name="remarks"></a>Remarques

Cette instruction effectue une comparaison de valeurs 32 bits de composant unique avec l’opérande *src0* avec l' *heure d’été* à 32 bits par adresse de composant *dstAddress*.

Si les valeurs comparées sont identiques, la valeur 32 bits d’un seul composant dans *src1* est écrite dans la mémoire de destination. Dans le cas contraire, la destination n’est pas modifiée.

La totalité de l’opération de comparaison et d’écriture est effectuée de manière atomique.

Si *DST* est un u \# , il peut être déclaré comme brut, typé ou structuré. Si elle est typée, elle doit être déclarée en tant que UINT/Saint-avec le format de ressource lié R32 \_ uint/Saint-est \_ .

Si l' *heure d’été* est g \# , elle doit être déclarée comme brute ou structurée.

Le nombre de composants pris à partir de l’adresse est déterminé par la dimensionnalité de l’heure d’été u \# ou g \# .

Rien n’est retourné au nuanceur.

Si l’appel du nuanceur est inactif, par exemple si le pixel a été ignoré plus tôt dans son exécution, ou si une instruction pixel/échantillon ne modifie pas la mémoire de l' *heure d’été* (en mode silencieux).

L’adressage hors limites sur u n' \# entraîne pas l’écriture dans la mémoire, sauf si u \# est structuré et que l’offset d’octet dans le struct (composant « second » de l’adresse) est à l’origine de l’accès hors limites, alors que le contenu entier du UAV devient non défini.

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

 

 





