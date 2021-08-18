---
title: defb-vs
description: Définit une valeur constante booléenne, qui doit être chargée chaque fois qu’un nuanceur est défini sur un appareil.
ms.assetid: 1db41115-14aa-462e-a7ee-c0a53fee97d8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e5ace74e275ae63a62306d47d50924e9c4e9a9771027e75659ef72345f69906d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792670"
---
# <a name="defb---vs"></a>defb-vs

Définit une valeur constante booléenne, qui doit être chargée chaque fois qu’un nuanceur est défini sur un appareil.

## <a name="syntax"></a>Syntaxe



| defb dest, booleanValue |
|-------------------------|



 

where

-   l’heure d’été est le registre de destination.
-   booleanValue est une valeur booléenne, true ou false.

## <a name="remarks"></a>Remarques



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| defb                   |      | x    | x    | x     | x    | x     |



 

L’instruction defb-vs définit une constante de nuanceur booléenne dont la valeur est chargée chaque fois qu’un nuanceur est défini sur un appareil. Celles-ci sont appelées constantes immédiates. Les constantes immédiates sont prioritaires sur les constantes définies par la méthode d’API SetVertexShaderConstantB.

Il existe deux façons de définir une constante booléenne dans un nuanceur.

1.  Utilisez defb-vs pour définir la constante directement à l’intérieur d’un nuanceur.
2.  Utilisez les méthodes de l’API pour définir une constante.
    -   Utilisez [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb) pour définir une constante booléenne.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[def-vs](def---vs.md)
</dt> <dt>

[signatures-vs](defi---vs.md)
</dt> </dl>

 

 