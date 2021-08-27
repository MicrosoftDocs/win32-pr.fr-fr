---
title: texldp-PS
description: Instruction de chargement de texture projetée. Cette instruction divise la coordonnée de texture d’entrée par le quatrième élément (. a ou. w) juste avant l’échantillonnage.
ms.assetid: 82e62ba3-a9f5-4afb-8dca-4c54a00843eb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d5c362e81af22b46cd443ade7cd4b466112ba9a4d98bd5852ee3d92a285936aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117849"
---
# <a name="texldp---ps"></a>texldp-PS

Instruction de chargement de texture projetée. Cette instruction divise la coordonnée de texture d’entrée par le quatrième élément (. a ou. w) juste avant l’échantillonnage.

## <a name="syntax"></a>Syntaxe



| texldp DST, src0, src1 |
|------------------------|



 

where

-   l’heure d’été est le registre de destination.
-   src0 est un registre source qui fournit les coordonnées de texture pour l’échantillon de texture. Consultez [Registre de coordonnées de texture](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).
-   src1 identifie l' [échantillonneur (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , où \# spécifie le numéro d’échantillonnage de texture à échantillonner. L’échantillonneur lui est associé une texture et un état d’échantillonneur défini par [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).

Pour obtenir le jeu de restrictions lors de l’utilisation de texldp, consultez [texld](texld---ps-2-0.md).

## <a name="remarks"></a>Remarques

texldp effectue la projection sur les coordonnées lues à partir de src0 avant d’effectuer l’exemple. Chaque coordonnée de texture est divisée par src0. w, puis la texture est échantillonnée. Quand texldp se termine, le contenu de src0 n’est pas affecté (sauf si l’heure d’été est le même registre). Une alternative à l’utilisation de texldp consiste à effectuer manuellement la Division de projection dans le nuanceur. Toutefois, l’exécution de la division dans le code du nuanceur est généralement plus lente que lorsqu’elle est exécutée par l’instruction texldp. par conséquent, évitez de tels calculs supplémentaires lorsque cela est possible.

Le nombre de coordonnées nécessaires à l’exécution de l’exemple de texture par src0 dépend de la manière dont src1 a été déclaré, plus le composant. w. Les types d’échantillonneur sont déclarés avec le [ \_ samplerType DCL (SM2, SM3-PS ASM)](dcl-samplertype---ps.md). Si src1 est déclaré comme un échantillonneur 2D, src0 doit contenir des coordonnées. XYW ; Si src1 est déclaré comme un échantillonneur de cube ou un échantillonneur de volume, src0 doit contenir des coordonnées. XYZW. L’échantillonnage d’une texture 2D avec des coordonnées. XYZW est autorisé (la coordonnée z est ignorée).

Si la texture source contient moins de quatre composants, les valeurs par défaut sont placées dans les composants manquants. Les valeurs par défaut dépendent du format de texture, comme indiqué dans le tableau suivant.



| Format de texture                                                                                          | Valeurs par défaut pour les composants manquants |
|---------------------------------------------------------------------------------------------------------|---------------------------------------|
| D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT \_ L8, D3DFMT \_ L16, D3DFMT \_ R3G3B2, D3DFMT \_ CxV8U8, D3DFMT \_ L6V5U5 | A = 1,0                               |
| D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT \_ G16R16, D3DFMT \_ G16R16F, D3DFMT \_ G32R32F                          | B = A = 1,0                           |
| D3DFMT \_ a8                                                                                              | R = G = B = 0,0                       |
| D3DFMT \_ R16F, D3DFMT \_ R32F                                                                              | G = B = A = 1,0                       |
| Tous les formats de profondeur/gabarit                                                                               | R = B = 0,0, A = 1,0                  |



 

Cette instruction est prise en charge dans les versions suivantes :



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldp                |      |      |      |      | x    | x    | x     | x    | x     |



 

### <a name="ps_2_0-and-ps_2_x"></a>PS \_ 2 \_ 0 et PS \_ 2 \_ x

l’heure d’été doit être un [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) et seul le masque XYZW (masque par défaut) est autorisé.

src0 doit être un [Registre de coordonnées de texture](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ) ou un [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), sans modificateur ni Swizzle.

src1 doit être un [échantillonneur (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) , sans \# modificateur ni Swizzle.

Si le \_ \_ bit d’extrémité D3DD3DPSHADERCAPS2 0 NODEPENDENTREADLIMIT n’est pas défini (dans D3DPSHADERCAPS2 \_ 0), une instruction de texture donnée ([texld](texld---ps-1-4.md), texldp, [texldb-PS](texldb---ps.md), [texldd](texldd---ps.md) ) peut dépendre, au plus, du troisième ordre. Une instruction de texture dépendante de premier ordre est une instruction de texture dans laquelle :

-   src0 est un [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# )
-   l’heure d’été a été écrite précédemment, en cours de réécriture.

Une instruction de texture dépendante d’une seconde commande est définie comme une instruction de texture qui lit ou écrit dans un [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) dont le contenu, avant d’exécuter l’instruction de texture, dépend (peut-être indirectement) du résultat d’une instruction de texture dépendante de premier ordre. Une instruction de texture dépendante (n)<sup>th</sup>dérive d’une instruction de texture (n-1)<sup>th</sup>-Order.

### <a name="ps_3_0"></a>PS \_ 3 \_ 0

Pour PS \_ 3 \_ 0, src1 doit être un [échantillonneur (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) , sans \# modificateur. Swizzle est autorisé sur src1 et, lorsqu’il est appliqué, les résultats de la recherche de texture sont antérieurs à swizzled avant d’être écrits dans l’heure d’été.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 