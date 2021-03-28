---
title: store_raw (SM5-ASM)
description: Écriture à accès aléatoire des composants 32 bits 1-4 dans la mémoire de type.
ms.assetid: D166116A-CF4E-4020-9F6A-F9CEEFCDAB21
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44b4d22a576853fb8b7d2c43fcb6a2d7fc9a448
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381217"
---
# <a name="store_raw-sm5---asm"></a>stocker \_ brut (SM5-ASM)

Écriture à accès aléatoire des composants 32 bits 1-4 dans la mémoire de type.



| stocker le \_ \[ masque dst0. Write brut \_ \] , dstByteOffset \[ . Select \_ Component \] , src0 \[ . Swizzle\] |
|----------------------------------------------------------------------------------------|



 



| Élément                                                                                                                       | Description                                |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[dans \] l’adresse mémoire.<br/>      |
| <span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*<br/> | \[dans \] le décalage.<br/>              |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | \[dans \] les composants à écrire.<br/> |



 

## <a name="remarks"></a>Notes

Cette instruction exécute 1-4 \* composants 32 bits écrits à partir de *src0* vers *dst0* à l’offset dans *dstByteOffset*. Il n’y a aucune conversion de format.

*dst0* doit être un UAV (u \# ) ou, dans le nuanceur de calcul, il peut également s’agir d’une mémoire partagée de groupe de threads (g \# ).

*dstByteOffset* spécifie la valeur de base de 32 bits en mémoire pour une fenêtre de 4 valeurs de 32 bits séquentielles dans lesquelles les données peuvent être écrites, en fonction du Swizzle et du masque sur les autres paramètres.

L’emplacement des données écrites est équivalent au pseudo-code suivant, qui affiche l’adresse, le pointeur vers le contenu de la mémoire tampon et les données stockées de façon linéaire.

``` syntax
                    BYTE *BufferContents;          // from src0
                    UINT dstByteOffset;            // source register
                    BYTE *WriteLocation;           // value to calculate

                    // calculate writing location
                    WriteLocation = BufferContents 
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
                             WriteComponents * sizeof(UINT32));
```

Ce pseudocode montre comment fonctionne l’opération, mais les données réelles n’ont pas besoin d’être stockées de façon linéaire. *dst0* peut uniquement avoir un masque d’écriture qui est l’un des suivants :. x,. XY,. xyz,. XYZW. Le masque d’écriture détermine le nombre de composants 32 bits à écrire sans écarts.

L’adressage hors limites sur u \# signifie que rien n’est écrit dans la mémoire en dehors des limites ; toute partie qui se trouve dans des limites est écrite correctement.

En dehors des limites d’adressage sur g \# (les limites de ce g particulier \# , par opposition à toute la mémoire partagée) pour un composant 32 bits donné, la totalité du contenu de la mémoire partagée devient non définie.

CS \_ 4 \_ 0 et CS \_ 4 \_ 1 prennent en charge cette instruction pour UAV.

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

 

 





