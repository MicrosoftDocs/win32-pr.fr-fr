---
title: DEFAUT-PS
description: Définit une valeur de constante entière, qui doit être chargée à chaque fois qu’un nuanceur est défini sur un appareil.
ms.assetid: c51982a1-45b4-48db-a49a-93165d61efd3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3552d5cfe322dd384e1c6bd219e35af19b469a56
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411247"
---
# <a name="defi---ps"></a>DEFAUT-PS

Définit une valeur de constante entière, qui doit être chargée à chaque fois qu’un nuanceur est défini sur un appareil.

## <a name="syntax"></a>Syntax



| detest DST, integerValue |
|------------------------|



 

-   l’heure d’été est le registre de destination.
-   integerValue est une valeur entière constante.

## <a name="remarks"></a>Remarques



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| signatures                  |      |      |      |      |      | x    | x     | x    | x     |



 

L’instruction de définition définit une constante de nuanceur dont la valeur est chargée chaque fois qu’un nuanceur est défini sur un appareil. Celles-ci sont appelées constantes immédiates. Les constantes immédiates sont prioritaires sur les constantes définies par la méthode d’API SetPixelShaderConstantB.

Il existe deux façons de définir une constante dans un nuanceur.

1.  Utilisez la définition de définition pour définir la constante directement à l’intérieur d’un nuanceur.
2.  Utilisez les méthodes de l’API pour définir une constante.
    -   Utilisez [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) pour définir une constante booléenne.
    -   Utilisez [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) pour définir une constante à virgule flottante.
    -   Utilisez [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti) pour définir une constante entière.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 