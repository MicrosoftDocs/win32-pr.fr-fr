---
title: ld_structured (SM5-ASM)
description: Lecture à accès aléatoire des composants 32 bits 1-4 à partir d’une mémoire tampon structurée.
ms.assetid: ED572B76-FF6C-405E-9110-4B12AD5E5AE6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfb3c19b56271a02c20ff85dd71352b545843f62b3d01292e87c2edbd6384d83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562309"
---
# <a name="ld_structured-sm5---asm"></a>LD \_ structuré (SM5-ASM)

Lecture à accès aléatoire des composants 32 bits 1-4 à partir d’une mémoire tampon structurée.



| : LD \_ dst0 \[ . Mask \] , srcAddress \[ . Select, \_ composant, \] srcByteOffset \[ . Select \_ Component \] , src0 \[ . Swizzle\] |
|-------------------------------------------------------------------------------------------------------------------------|



 



| Élément                                                                                                                       | Description                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[dans \] l’adresse des résultats de l’opération.<br/>                                                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>             | \[dans \] spécifie l’index de la structure à lire.<br/>                                                                                            |
| <span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*<br/> | \[dans \] spécifie l’offset d’octet dans la structure à partir duquel commencer la lecture. <br/>                                                                       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | Mémoire tampon à partir de laquelle effectuer la lecture. Ce paramètre doit être un SRV (t \# ), UAV (u \# ). Dans le nuanceur de calcul, il peut également s’agir d’une mémoire partagée de groupe de threads (g \# ). <br/> |



 

## <a name="remarks"></a>Remarques

Les données lues à partir de la structure sont équivalentes au pseudocode suivant : où nous avons le décalage, l’adresse, le pointeur vers le contenu de la mémoire tampon, la Stride de la source et les données stockées de façon linéaire.

``` syntax
                    BYTE *BufferContents;         // from SRV or UAV
                    UINT BufferStride;            // from base resource
                    UINT srcAddress, srcByteOffset;   // from source registers
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + BufferStride * srcByteOffset
                                + srcOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

Ce pseudocode montre comment fonctionne l’opération, mais les données réelles n’ont pas besoin d’être stockées de façon linéaire. Si les données ne sont pas stockées de façon linéaire, l’opération réelle de l’instruction doit correspondre au comportement de l’opération ci-dessus.

L’adressage hors limites sur u \# /t \# d’un composant 32 bits donné retourne 0 pour ce composant, sauf si *srcByteOffset*, plus Swizzle est ce qui entraîne l’accès à Unlimited à vous \# /t \# , la valeur retournée pour tous les composants n’est pas définie.

En dehors des limites, l’adressage sur g \# (les limites de ce g particulier \# , par opposition à toute la mémoire partagée) pour un composant 32 bits donné retourne un résultat non défini.

*srcByteOffset* est un argument distinct de *srcAddress* , car il s’agit généralement d’un littéral. Cette séparation des paramètres n’a pas été effectuée pour les atomices sur la mémoire structurée.

CS \_ 4 \_ 0 et CS \_ 4 \_ 1 prennent en charge cette instruction pour UAV, SRV et TGSM.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour UAVs pour le runtime Direct3D 11,1, disponible à partir de Windows 8.



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



 

CS \_ 4 \_ 0 et CS \_ 4 \_ 1 prennent en charge cette instruction pour UAV, SRV et TGSM.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 5 du nuanceur (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





