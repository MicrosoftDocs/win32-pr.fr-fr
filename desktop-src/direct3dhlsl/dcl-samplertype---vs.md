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
ms.openlocfilehash: 556655d793e94b9290fcd1a4a40fdf7f797e80ae
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990825"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a>DCL \_ samplerType (SM3-vs ASM)

Déclarez un échantillon de nuanceur de sommets.

## <a name="syntax"></a>Syntaxe



|                      |
|----------------------|
| DCL \_ samplerType s\# |



 

où :

-   \_samplerType définit le type de données de l’échantillonneur. Cela détermine le nombre de coordonnées requises par chaque coordonnée de texture lors de l’échantillonnage. Les dimensions de coordonnée de texture suivantes sont définies.
    -   \_dimensionnel
    -   \_dernier
    -   \_agrégat
-   s \# identifie un échantillonneur où s est l’abréviation de l’échantillonneur, et \# est le numéro de l’échantillonneur. L' [échantillonneur (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)est un Pseudo-Registre, car vous ne pouvez pas y lire ou écrire directement.

## <a name="remarks"></a>Notes



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| \_samplerType DCL       |      |      |      |       | x    | x     |



 

Toutes les \_ instructions DCL samplerType doivent apparaître avant la première instruction exécutable.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




