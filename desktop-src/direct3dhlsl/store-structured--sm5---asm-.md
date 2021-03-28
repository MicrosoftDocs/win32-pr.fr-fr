---
title: store_structured (SM5-ASM)
description: Écriture à accès aléatoire des composants 1-4 32 bits dans une vue de l’accès non ordonné de la mémoire tampon structurée (UAV).
ms.assetid: 8080B2CA-5BDA-4F01-8B2B-B85BDD58C5AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5890d30fac57923365f0bdea89fcce55f7922c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030574"
---
# <a name="store_structured-sm5---asm"></a>stockage \_ structuré (SM5-ASM)

Écriture à accès aléatoire des composants 1-4 32 bits dans une vue de l’accès non ordonné de la mémoire tampon structurée (UAV).



| stocker le \_ \[ masque dst0. Write structuré \_ \] , dstAddress \[ . Select \_ Component \] , dstByteOffset \[ . Select \_ Component \] , src0 \[ . Swizzle\] |
|---------------------------------------------------------------------------------------------------------------------------------|



 



| Élément                                                                                                                       | Description                                                    |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[dans \] l’adresse des résultats de l’opération.<br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/>             | \[dans \] l’adresse à laquelle écrire.<br/>               |
| <span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*<br/> | \[dans \] l’index de la structure à écrire.<br/>         |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | \[dans \] les composants à écrire.<br/>                     |



 

## <a name="remarks"></a>Notes

Cette instruction exécute \* les composants 32 bits 1-4 du composant écrits à partir de *src0* vers *dst0* à l’adresse dans *dstAddress* et *dstByteOffset*. Aucune conversion de format.

*dst0* doit être un UAV (u \# ). Dans le nuanceur de calcul, il peut également s’agir d’une mémoire partagée de groupe de threads (g \# ).

*dstAddress* spécifie l’index de la structure à écrire.

L’emplacement des données écrites est équivalent au pseudo-code suivant, qui montre l’offset, l’adresse, le pointeur vers le contenu de la mémoire tampon, la Stride de la source et les données stockées de façon linéaire.

``` syntax
                    BYTE *BufferContents;             // from dst0
                    UINT BufferStride;                // from dst0
                    UINT dstAddress, dstByteOffset;   // source registers
                    BYTE *WriteLocation;              // value to calculate

                    // calculate writing location
                     WriteLocation = BufferContents 
                                + BufferStride * dstAddress 
                                + dstByteOffset;

                    // calculate the number of components to write
                    switch (dstWriteMask)
                    {
                        x:    WriteComponents = 1; break;
                        xy:   WriteComponents = 2; break;
                        xyz:  WriteComponents = 3; break;
                        xyzw: WriteComponents = 4; break;
                        default:  // only these masks are valid                              
                    }

                    // copy the data from the source register with
                    //    the swizzle applied
                    memcpy(WriteLocation, swizzle(src0, src0.swizzle), 
                             WriteComponents * sizeof(INT32));
```

Ce pseudocode montre comment fonctionne l’opération, mais les données réelles n’ont pas besoin d’être stockées de façon linéaire. Si les données ne sont pas stockées de façon linéaire, l’opération réelle de l’instruction doit correspondre au comportement de l’opération ci-dessus.

*dst0* peut uniquement avoir un masque d’écriture qui est l’un des suivants :. x,. XY,. xyz,. XYZW. Le masque d’écriture détermine le nombre de composants 32 bits à écrire sans intervalles.

L’adressage hors limites sur u- \# attrait par *dstAddress* signifie que rien n’est écrit dans la mémoire hors limites.

Si le *dstByteOffset*, y compris *dstWriteMask*, est à l’origine de l’accès hors limites \# , le contenu entier du UAV devient non défini.

En dehors des limites d’adressage sur g \# (les limites de ce g particulier \# , par opposition à toute la mémoire partagée) pour un composant 32 bits donné, la totalité du contenu de la mémoire partagée devient non définie.

*dstByteOffset* est un argument distinct de *dstAddress* , car il s’agit généralement d’un littéral. Cette séparation des paramètres n’a pas été effectuée pour les atomices sur la mémoire structurée.

CS \_ 4 \_ 0 et CS \_ 4 \_ 1 prennent en charge cette instruction pour UAV et TGSM.

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

 

 





