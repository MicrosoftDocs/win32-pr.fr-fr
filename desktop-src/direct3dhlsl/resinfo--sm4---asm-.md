---
title: ResInfo (SM4-ASM)
description: Interrogez les dimensions d’une ressource d’entrée donnée.
ms.assetid: 5D549AC6-E0CB-4395-953C-5E5ECEEE234D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a252195a4b59ed791f6ac625fe1d95bbd9925f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292667"
---
# <a name="resinfo-sm4---asm"></a>ResInfo (SM4-ASM)

Interrogez les dimensions d’une ressource d’entrée donnée.



| ResInfo \[ \_ uint \|\_rcpFloat \] dest \[ . Mask \] , srcMipLevel. Select, \_ srcResource \[ . Swizzle\] |
|-----------------------------------------------------------------------------------------------------|



 



| Élément                                                                                                               | Description                                                                               |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[dans \] l’adresse du résultat de l’opération.<br/>                             |
| <span id="srcMipLevel"></span><span id="srcmiplevel"></span><span id="SRCMIPLEVEL"></span>*srcMipLevel*<br/> | \[au \] niveau MIP.<br/>                                                          |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[dans \] une \# \# texture d’entrée t ou u pour laquelle les dimensions sont interrogées. <br/> |



 

## <a name="remarks"></a>Notes

*srcMipLevel* est lu en tant que valeur scalaire d’entier non signé, ce qui signifie qu’un sélecteur de composant unique est requis pour le registre source, s’il ne s’agit pas d’une valeur immédiate scalaire.

*dest* reçoit \[ la largeur, la hauteur, la profondeur ou la taille du tableau, total-MIP-Count \] , sélectionné par le masque d’écriture.

Les valeurs de largeur, de hauteur et de profondeur retournées sont pour le niveau MIP sélectionné par le paramètre *srcMipLevel* et sont en nombre de texels, indépendamment de la taille des données Texel. Pour les exemples de ressources (texture2D \[ array \] MS \# ), la largeur et la hauteur sont également retournées dans des texels, et non des exemples.

Le nombre total de MIP renvoyés dans *dest. w* n’est pas affecté par le paramètre *srcMipLevel* .

Pour UAVs (u \# ), le nombre de niveaux MIP est toujours 1.

Tous les aspects de cette instruction sont basés sur les caractéristiques de la vue de ressource liée au t \# /u \# , et non sur la ressource de base sous-jacente.

Les valeurs retournées sont toutes à virgule flottante, sauf si le \_ modificateur uint est utilisé, auquel cas les valeurs retournées sont tous des entiers. Si le \_ modificateur rcpFloat est utilisé, toutes les valeurs retournées sont à virgule flottante, et la largeur, la hauteur et la profondeur sont retournées en tant que réciproques (1,0 f/Width, 1,0 f/Height, 1,0 f/depth), y compris le fichier INF si la largeur/hauteur/profondeur est 0 du comportement *srcMipLevel* hors limites. Le \_ modificateur rcpFloat s’applique uniquement aux valeurs retournées de largeur, de hauteur et de profondeur. il ne s’applique pas aux valeurs qui ont la valeur 0 et n’est donc pas retourné, et il ne s’applique pas non plus aux retours de taille de tableau.

Swizzle sur *srcResource* permet aux valeurs retournées d’être swizzled arbitrairement avant d’être écrites dans la destination.

Si *srcResource* est un Texture1D, la largeur est retournée dans *dest. x*, tandis que *dest. YZ* a la valeur 0.

Si *srcResource* est un Texture1DArray, la largeur est retournée dans *dest. x*, la taille du tableau est retournée dans *dest. y*, tandis que *dest. z* a la valeur 0.

Si *srcResource* est un Texture2D, la largeur et la hauteur sont retournées dans *dest. XY*, tandis que *dest. z* a la valeur 0.

Si *srcResource* est un Texture2DArray, la largeur et la hauteur sont retournées dans *dest. XY*, et la taille du tableau est retournée dans *dest. z*.

Si *srcResource* est un Texture3D, la largeur, la hauteur et la profondeur sont retournées dans *dest.xyz*.

Si *srcResource* est un TextureCube, la largeur et la hauteur des dimensions de la face individuelle du cube sont retournées dans *dest. XY*, tandis que *dest. z* a la valeur 0.

Si *srcResource* est un TextureCubeArray, la largeur et la hauteur des dimensions de la face individuelle du cube sont retournées dans *dest. XY*. *dest. z* est défini sur une valeur non définie.

Si la bride MIP par ressource a été spécifiée sur *srcResource*, ResInfo retourne toujours le nombre total de des mipmaps dans la vue pour le nombre MIP, quelle que soit la bride. Toutefois, si les dimensions d’un miplevel donné sont demandées par ResInfo et que le miplevel a été désactivé (par exemple, une bride de 2,2 signifie que les mips 0 et 1 ont été désactivés), les dimensions retournées ne sont pas définies. Certaines implémentations retournent le comportement hors limites spécifié pour ResInfo lorsque le miplevel est hors limites. D’autres implémentations retournent les dimensions du MIP comme s’il n’avait pas été ancré.

### <a name="restrictions"></a>Restrictions

-   *srcResource* doit être un \# Registre t ou u \# qui n’est pas une mémoire tampon, mais qui est une texture \* .
-   L’adressage relatif de *srcResource* n’est pas autorisé.
-   *srcMipLevel* doit utiliser un sélecteur de composant unique s’il n’est pas un scalaire immédiat.
-   Une extraction à partir de t \# ou u \# qui n’a rien lié à elle retourne 0 pour la largeur, la hauteur, la profondeur ou le arraySize et le nombre total-MIP-Count. Le \_ modificateur rcpFloat est toujours respecté dans ce cas, renvoyant donc INF aux valeurs retournées applicables.
-   Si *srcMipLevel* est en dehors de la plage du nombre de miplevels a disponibles dans la ressource, le comportement de la valeur Return size (*dest.xyz*) est identique à celui d’une \# ressource t ou u indépendante \# . Le nombre total de MIP est toujours retourné dans *dest. w* pour ce cas.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | Oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | Oui       |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | Oui       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 4 du nuanceur (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





