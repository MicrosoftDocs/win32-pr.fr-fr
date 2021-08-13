---
title: DCL-(SM2, SM3-PS ASM)
description: Déclarez un registre d’entrée de nuanceur de pixels.
ms.assetid: d6fcd94e-80d7-4e8a-8b4f-ff86c980cc38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dab377a36cb1323daf450b9566e419b60edc1fb80dde54591a932b2e0f28223a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793465"
---
# <a name="dcl---sm2-sm3---ps-asm"></a>DCL-(SM2, SM3-PS ASM)

Déclarez un registre d’entrée de nuanceur de pixels.

## <a name="syntax"></a>Syntaxe

DCL \[ \_ pp \] dest \[ . Mask\]



 

Où :

-   \[\_pp \] est une précision partielle facultative. Consultez [précision partielle](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md).
-   dest est un registre de destination. Il doit s’agir d’un [Registre de couleur d’entrée](dx9-graphics-reference-asm-ps-registers-input-color.md) (VN) ou d’un [Registre de coordonnées de texture](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN).
-   \[. Mask \] est un masque d’écriture facultatif qui contrôle les composants du registre de destination dans lesquels il est possible d’écrire. Voir [masque d’écriture de registre de destination](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).

## <a name="remarks"></a>Remarques



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| DCL                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Toutes les instructions DCL doivent apparaître avant la première instruction exécutable.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




