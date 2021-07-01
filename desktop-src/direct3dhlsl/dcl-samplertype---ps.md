---
title: dcl_samplerType (SM2, SM3-PS ASM)
description: Déclarez un échantillon de nuanceur de pixels.
ms.assetid: c90ff5b6-f89a-4993-8a5d-dbbc4a7896b0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7a6da220e50b43ce990c090c61d1caf84afec653
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129666"
---
# <a name="dcl_samplertype-sm2-sm3---ps-asm"></a>DCL \_ samplerType (SM2, SM3-PS ASM)

Déclarez un échantillon de nuanceur de pixels.

## <a name="syntax"></a>Syntaxe

DCL \_ samplerType s\#



 

où :

-   \_samplerType définit le type de données de l’échantillonneur. Cela détermine le nombre de coordonnées requises par chaque coordonnée de texture lors de l’échantillonnage. Les dimensions de coordonnée de texture suivantes sont définies.
    -   \_dimensionnel
    -   \_dernier
    -   \_agrégat
-   s \# identifie un échantillonneur où s est l’abréviation de l’échantillonneur, et \# est le numéro de l’échantillonneur. Les échantillonneurs sont des Pseudo-registres, car vous ne pouvez pas les lire ou les écrire directement.

## <a name="remarks"></a>Remarques



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| \_samplerType DCL      |      |      |      |      | x    | x    | x     | x    | x     |



 

Toutes les \_ instructions DCL samplerType doivent apparaître avant la première instruction exécutable.

## <a name="example"></a>Exemple


```
dcl_cube t0.rgb;  // Define a 3D texture map.

add r0, r0, t0;   // Perturb texture coordinates. 
texld r0, s0, r0; // Load r0 with a color sampled from stage0
                  //   at perturbed texture coordinates r0.
                  // This is a dependent texture read.
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




