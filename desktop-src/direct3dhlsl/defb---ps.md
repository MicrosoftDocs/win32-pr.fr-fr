---
title: defb-PS
description: Définit une valeur constante booléenne, qui doit être chargée à chaque fois qu’un nuanceur est défini sur un appareil.
ms.assetid: bb0b87cb-08a4-4790-88da-e398cea62911
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9437c7d6347da4bafae566386e09e4bc782bd16
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524721"
---
# <a name="defb---ps"></a>defb-PS

Définit une valeur constante booléenne, qui doit être chargée à chaque fois qu’un nuanceur est défini sur un appareil.

## <a name="syntax"></a>Syntaxe



| defb dest, booleanValue |
|-------------------------|



 

where

-   l’heure d’été est le registre de destination.
-   booleanValue est une valeur booléenne unique, true ou false.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| defb                  |      |      |      |      |      | x    | x     | x    | x     |



 

L’instruction defb définit une constante de nuanceur booléenne dont la valeur est chargée chaque fois qu’un nuanceur est défini sur un appareil. Celles-ci sont appelées constantes immédiates. Les constantes immédiates sont prioritaires sur les constantes définies par la méthode d’API SetPixelShaderConstantB.

Il existe deux façons de définir un BooleanConstant dans un nuanceur.

1.  Utilisez defb pour définir la constante directement à l’intérieur d’un nuanceur.
2.  Utilisez les méthodes de l’API pour définir une constante.
    -   Utilisez [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) pour définir une constante booléenne.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[def-PS](def---ps.md)
</dt> <dt>

[DEFAUT-PS](defi---ps.md)
</dt> </dl>

 

 