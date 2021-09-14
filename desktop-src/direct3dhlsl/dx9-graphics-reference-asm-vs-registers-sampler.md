---
title: Échantillonneur (Direct3D 9 ASM-vs)
description: Un échantillonneur est un Pseudo-registre d’entrée pour un nuanceur de sommets, qui est utilisé pour identifier la phase d’échantillonnage. Il existe quatre échantillonneurs de nuanceur de sommets S0 à S3. Quatre surfaces de texture peuvent être lues dans une seule passe de nuanceur.
ms.assetid: a4588ced-24e2-4d4e-93e4-35a985bafaa4
keywords:
- Échantillonneur, type (Direct3D 9 ASM-vs)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 685f261da9d56dc29c0632d01cabbf29cd13a00f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922420"
---
# <a name="sampler-direct3d-9-asm-vs"></a>Échantillonneur (Direct3D 9 ASM-vs)

Un échantillonneur est un Pseudo-registre d’entrée pour un nuanceur de sommets, qui est utilisé pour identifier la phase d’échantillonnage. Il existe quatre échantillonneurs de nuanceur vertex : S0 à S3. Quatre surfaces de texture peuvent être lues dans une seule passe de nuanceur.

L’échantillonneur (Direct3D 9 ASM-vs) est un Pseudo-Registre, car vous ne pouvez pas y lire ou écrire directement.

Une unité d’échantillonnage correspond à la phase d’échantillonnage de texture, en encapsulant l’état spécifique à l’échantillonnage fourni par [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate). Chaque échantillonneur identifie de façon unique une surface de texture unique, qui est définie sur l’échantillonneur correspondant à l’aide de [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture). Toutefois, la même surface de texture peut être définie sur plusieurs échantillonneurs.

Au moment du tracé, une texture ne peut pas être définie simultanément comme une cible de rendu et une texture à une étape.

Étant donné qu’il y a quatre échantillonneurs, jusqu’à quatre surfaces de texture peuvent être lues à partir d’une seule passe de nuanceur. Un échantillonneur peut apparaître comme le seul argument dans l’instruction de chargement de texture : [texldl-vs](texldl---vs.md).

Dans vs \_ 3 \_ 0, si un échantillonneur est utilisé, il doit être déclaré au début du programme du nuanceur à l’aide de l’instruction [DCL \_ samplerType (SM3-vs ASM)](dcl-samplertype---vs.md) .



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ logiciels | 2 \_ x | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|-------|------|------|-------|
| Échantillonneur                |      |      |       |      | x    | x     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Registres de nuanceur vertex](dx9-graphics-reference-asm-vs-registers.md)
</dt> <dt>

[Textures de vertex dans vs \_ 3 \_ 0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0)
</dt> </dl>

 

 