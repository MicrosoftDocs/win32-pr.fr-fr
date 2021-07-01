---
title: dcl_samplerType (SM3-vs ASM)
description: Déclarez un échantillon de nuanceur de sommets.
ms.assetid: 733307ac-24ab-4db7-bf70-58a83b4c39b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2fbcb934ad591274d743f09c810de2db42278261
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129867"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a>DCL \_ samplerType (SM3-vs ASM)

Déclarez un échantillon de nuanceur de sommets.

## <a name="syntax"></a>Syntaxe

DCL \_ samplerType s\#



 

où :

-   \_samplerType définit le type de données de l’échantillonneur. Cela détermine le nombre de coordonnées requises par chaque coordonnée de texture lors de l’échantillonnage. Les dimensions de coordonnée de texture suivantes sont définies.
    -   \_dimensionnel
    -   \_dernier
    -   \_agrégat
-   s \# identifie un échantillonneur où s est l’abréviation de l’échantillonneur, et \# est le numéro de l’échantillonneur. L' [échantillonneur (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)est un Pseudo-Registre, car vous ne pouvez pas y lire ou écrire directement.

## <a name="remarks"></a>Remarques



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| \_samplerType DCL       |      |      |      |       | x    | x     |



 

Toutes les \_ instructions DCL samplerType doivent apparaître avant la première instruction exécutable.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




