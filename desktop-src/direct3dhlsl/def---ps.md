---
title: def-PS
description: Définit des constantes à virgule flottante de nuanceur de pixels.
ms.assetid: 679b3074-73f3-48de-8c7a-f43bff76b25a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce5f842f44e915d3f3240618261b501f2240c3636227f930538e1bbcbe0d9367
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726559"
---
# <a name="def---ps"></a>def-PS

Définit des constantes à virgule flottante de nuanceur de pixels.

## <a name="syntax"></a>Syntaxe



| def DST, fVvalue1, fValue2, fValue3, fValue4 |
|----------------------------------------------|



 

Où :

-   l’heure d’été est le registre de destination.
-   fValue1 à fValue4 sont des valeurs à virgule flottante.

## <a name="remarks"></a>Remarques



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| def                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Il existe deux façons de définir une constante à virgule flottante dans un nuanceur de pixels.

1.  Utilisez DEF pour définir la constante directement à l’intérieur d’un nuanceur.
2.  Utilisez l’API pour définir une constante avec [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).

def définit une constante de nuanceur dont la valeur est chargée à chaque fois qu’un nuanceur est défini sur un appareil. Celles-ci sont appelées constantes immédiates. Les constantes immédiates sont prioritaires sur les constantes définies par la méthode API.

-   Doit apparaître avant la première instruction arithmétique ou d’adressage dans le nuanceur.
-   Peut être mélangé avec les instructions [DCL-(SM2, SM3-PS ASM)](dcl---ps.md) (qui sont l’autre type d’instruction qui réside au début d’un nuanceur).
-   le registre de l’heure d’été doit être un [Registre constant](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).
-   Le masque d’écriture doit être complet (par défaut).
-   Si un [Registre de constante](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) est défini plusieurs fois dans un nuanceur, le dernier est conservé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 