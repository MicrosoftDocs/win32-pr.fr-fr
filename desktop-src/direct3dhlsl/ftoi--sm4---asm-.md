---
title: 'ftoi (sm4 - asm) '
description: Conversion d’un entier à virgule flottante en valeur signée.
ms.assetid: 580AB4A6-0C1C-409B-B2B9-BA1D37772F46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02ce1b506d112a59d3087f59d219557575b8def
ms.sourcegitcommit: 8c658e9872a2173e3dcec94195f9067fbcd85d3d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2020
ms.locfileid: "104316668"
---
# <a name="ftoi-sm4---asm"></a>ftoi (sm4 - asm) 

Conversion d’un entier à virgule flottante en valeur signée.

| ftoi dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\] |
|-|

| Élément | Description |
|-|-|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse du résultat de l’opération.<br/> *dest*  =  . [rond \_ z](round-z--sm4---asm-.md)(*src0*)<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] le composant à convertir.<br/> |

## <a name="remarks"></a>Notes

La conversion est effectuée par composant. L’arrondi est toujours effectué vers zéro, suivant la Convention C pour les conversions de float en int. Les applications qui requièrent une sémantique d’arrondi différente peuvent appeler les instructions **Round** avant d’effectuer un cast en Integer.

Les entrées sont ancrées dans la plage \[ 2147483648.999 f... 2147483647.999 f \] avant la conversion, et les valeurs NaN d’entrée produisent un résultat zéro.

Les modificateurs de valeur absolue et de négation facultatifs sont appliqués aux valeurs sources avant la conversion.

Cette instruction s’applique aux étapes suivantes du nuanceur :

| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|-|-|-|
| x | x | x |

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.

| Modèle de nuanceur | Prise en charge |
|-|-|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md) | Oui |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md) | Oui |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md) | Oui |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non |

## <a name="related-topics"></a>Rubriques connexes

[Assembly modèle 4 du nuanceur (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
