---
title: Modèle de nuanceur HLSL 6,4
description: Décrit les Machine Learning intrinsèques ajoutés au modèle de nuanceur HLSL 6,4.
ms.topic: article
ms.date: 02/21/2019
ms.openlocfilehash: 5e161d77439eef63547d92fcc4f47e3185ac798141d20017d7e7102ee86a38cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511833"
---
# <a name="hlsl-shader-model-64"></a>Modèle de nuanceur HLSL 6,4

Décrit les Machine Learning intrinsèques ajoutés au modèle de nuanceur HLSL 6,4.

## <a name="shader-model-64"></a>Modèle de nuanceur 6,4
Ces fonctions intrinsèques sont une fonctionnalité requise/prise en charge du modèle de nuanceur 6,4. Par conséquent, aucune vérification de bit de capacité distincte n’est requise, au-delà de la garantie de l’utilisation du modèle de nuanceur 6,4. le client minimal pris en charge pour ces routines est Windows 10, version 1903.

## <a name="shading-language-intrinsics"></a>Intrinsèques du langage d’ombrage

### <a name="unsigned-integer-dot-product-of-4-elements-and-accumulate"></a>Entier non signé Dot-Product de 4 éléments et cumuler
```syntax
uint32 dot4add_u8packed(uint32 a, uint32 b, uint32 acc); // ubyte4 a, b;
```
 
Un point-produit d’entier non signé à 4 dimensions avec Add. Multiplie chaque paire correspondante d’octets de type entier 8 bits non signés dans les deux valeurs DWORD d’entrée et additionne les résultats dans l’accumulation d’entiers non signés 32 bits. Cette instruction fonctionne dans une seule voie SIMD de 32 bits. Les entrées sont également supposées être des quantités de 32 bits.
 
### <a name="signed-integer-dot-product-of-4-elements-and-accumulate"></a>Dot-Product entier signé de 4 éléments et cumul
```syntax
int32 dot4add_i8packed(uint32 a, uint32 b, int32 acc); // signed byte4 a, b;
```

Un produit-point entier signé à 4 dimensions avec Add. Multiplie chaque paire correspondante d’octets de type entier 8 bits signés dans les deux valeurs DWORD d’entrée et additionne les résultats dans l’accumulation d’entiers signés 32 bits. Cette instruction fonctionne dans une seule voie SIMD de 32 bits. Les entrées sont également supposées être des quantités de 32 bits.
 
### <a name="single-precision-floating-point-2-element-dot-product-and-accumulate"></a>Dot-Product à virgule flottante simple précision 2 éléments et cumuler
```syntax
float dot2add( half2 a, half2 b, float acc );
```

Un point à virgule flottante à deux dimensions-produit de vecteurs Half2 avec Add. Multiplie les éléments des deux vecteurs d’entrée float demi-précision et additionne les résultats dans l’accumulateur float 32 bits. Ces instructions fonctionnent au sein d’une seule voie SIMD 32 bits. Les entrées sont des quantités de 16 bits compressées dans la même voie.

Cette fonctionnalité est couverte par le bit de fonctionnalité de faible précision (indiquant que la prise en charge native est présente).

### <a name="sv_shadingrate"></a>SV_ShadingRate
```syntax
uint shadingRate : SV_ShadingRate
```

Entier non signé représentant le nombre de pixels cibles écrits par chaque appel du nuanceur de pixels. Les valeurs valides appartiennent à un ensemble de valeurs d’énumération [D3D12_SHADING_RATE](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate).

Cette valeur système est disponible sur les plateformes qui sont [D3D12_VARIABLE_SHADING_RATE_TIER_2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) ou version ultérieure. Il peut être écrit à partir de au plus une des étapes du nuanceur de vertex ou Geometry. Il peut être lu à partir de l’étape nuanceur de pixels. Pour plus d’informations, consultez l' [ombrage à taux variable](../direct3d12/vrs.md).