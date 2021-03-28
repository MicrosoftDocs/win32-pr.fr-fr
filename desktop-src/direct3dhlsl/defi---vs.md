---
title: signatures-vs
description: Définit une valeur de constante entière, qui doit être chargée chaque fois qu’un nuanceur est défini sur un appareil.
ms.assetid: d6067a7d-58fb-4553-a42f-192c29bf78b7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 897a544cc9974b8ffa727f2d39219cfeab82d52a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508061"
---
# <a name="defi---vs"></a>signatures-vs

Définit une valeur de constante entière, qui doit être chargée chaque fois qu’un nuanceur est défini sur un appareil.

## <a name="syntax"></a>Syntaxe



| detest DST, integerValue0, integerValue1, integerValue2, integerValue3 |
|----------------------------------------------------------------------|



 

-   l’heure d’été est le registre de destination.
-   integerValue \# est une valeur entière constante.

## <a name="remarks"></a>Notes



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| signatures                   |      | x    | x    | x     | x    | x     |



 

L’instruction de définition définit une constante de nuanceur entière dont la valeur est chargée chaque fois qu’un nuanceur est défini sur un appareil. Celles-ci sont appelées constantes immédiates. Les constantes immédiates sont prioritaires sur les constantes définies par la méthode d’API SetVertexShaderConstantI.

Il existe deux façons de définir une constante entière dans un nuanceur.

1.  Utilisez la définition de type pour définir le vecteur de constante entier directement à l’intérieur d’un nuanceur.
2.  Utilisez les méthodes de l’API pour définir une constante.
    -   Utilisez [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti) pour définir une constante entière.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[def-vs](def---vs.md)
</dt> <dt>

[defb-vs](defb---vs.md)
</dt> </dl>

 

 