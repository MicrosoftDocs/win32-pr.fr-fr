---
title: Échantillonneur (Direct3D 9 ASM-PS)
description: Un échantillonneur est un Pseudo-registre d’entrée pour un nuanceur de pixels, qui est utilisé pour identifier la phase d’échantillonnage.
ms.assetid: 37cc28ae-fbd0-4f81-9e8e-f9609980d84e
keywords:
- Échantillonneur, type (Direct3D 9 ASM-PS)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: abf8887f229669273b26c9afeb036821842bf19311a752654ba1b5909d943090
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982839"
---
# <a name="sampler-direct3d-9-asm-ps"></a>Échantillonneur (Direct3D 9 ASM-PS)

Un échantillonneur est un Pseudo-registre d’entrée pour un nuanceur de pixels, qui est utilisé pour identifier la phase d’échantillonnage. Il y a 16 registres de l’étape d’échantillonnage du nuanceur de pixels : S0 à S15. Par conséquent, jusqu’à 16 surfaces de texture peuvent être lues dans une seule passe de nuanceur. Les instructions qui utilisent un registre d’échantillonnage sont texld et texldp.

L’échantillonneur doit être déclaré avant d’être utilisé avec l’instruction [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) .



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ logiciels | 2 \_ x | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Échantillonneur               |      |      |      |      | x    | x     | x    | x    | x     |



 

Les échantillonneurs sont des Pseudo-registres, car vous ne pouvez pas les lire ou les écrire directement.

Une unité d’échantillonnage correspond à la phase d’échantillonnage de texture, en encapsulant l’état spécifique à l’échantillonnage fourni par [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate). Chaque échantillonneur identifie de façon unique une surface de texture unique, qui est définie sur l’échantillonneur correspondant à l’aide de [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture). Toutefois, la même surface de texture peut être définie sur plusieurs échantillonneurs.

Au moment du tracé, une texture ne peut pas être définie simultanément comme une cible de rendu et une texture à une étape.

Un échantillonneur peut apparaître comme le seul argument dans l’instruction de chargement de texture : [texldl-PS](texldl---ps.md).

Dans PS \_ 3 \_ 0, si un échantillonneur est utilisé, il doit être déclaré au début du programme du nuanceur à l’aide de l’instruction [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) .

L’échantillonnage d’une texture avec une dimension supérieure à celle présente dans les coordonnées de texture n’est pas conforme. L’échantillonnage d’une texture avec une dimension inférieure à celle qui est présente dans les coordonnées de texture ignore les coordonnées de texture supplémentaires.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscrit](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 