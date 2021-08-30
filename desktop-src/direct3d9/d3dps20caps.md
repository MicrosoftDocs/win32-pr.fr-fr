---
description: Indicateurs de capacité de nuanceur de pixels.
ms.assetid: 41a8939f-eba5-47ca-8628-94b606b6f43d
title: D3DD3DPSHADERCAPS2_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b7b3b23c75971b0940f61b7d8f8d4ae2f496389b7ed0895f56349407f687af2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894509"
---
# <a name="d3dd3dpshadercaps2_0"></a>D3DD3DPSHADERCAPS2 \_ 0

Indicateurs de capacité de nuanceur de pixels.



| \#définition                                     | Valeur          | Description                                                                                                                                                                                                       |
|----------------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE      | (1 << 0) | Swizzling arbitraire est pris en charge.                                                                                                                                                                                 |
| D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS  | (1 << 1) | Les instructions de dégradé sont prises en charge.                                                                                                                                                                              |
| \_PRÉDICAT D3DD3DPSHADERCAPS2 0 \_           | (1 << 2) | Le prédicat d’instruction est pris en charge. Consultez [setp \_ COMP-PS](../direct3dhlsl/setp-comp---ps.md).                                                                                                                         |
| D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT  | (1 << 3) | Il n’existe aucune limite quant au nombre de lectures dépendantes par instruction.                                                                                                                                               |
| D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT | (1 << 4) | Il n’existe aucune limite quant au nombre d’instructions de Tex.                                                                                                                                                              |
| D3DPS20 \_ Max \_ DYNAMICFLOWCONTROLDEPTH        | 24             | Niveau maximal d’imbrication des instructions de contrôle de workflow dynamique (break, breakc, IFC).                                                                                                                           |
| D3DPS20 \_ Min \_ DYNAMICFLOWCONTROLDEPTH        | 0              | Niveau minimal d’imbrication des instructions de contrôle de workflow dynamique (break, breakc, IFC).                                                                                                                           |
| D3DPS20 \_ Max \_ NUMTEMPS                       | 32             | Le pilote prendra en charge au maximum ce nombre temporaire de registres.                                                                                                                                                     |
| D3DPS20 \_ Min \_ NUMTEMPS                       | 12             | Le pilote prendra en charge au moins ce nombre temporaire de registres.                                                                                                                                                    |
| D3DPS20 \_ Max \_ STATICFLOWCONTROLDEPTH         | 4              | Profondeur maximale d’imbrication des instructions [Loop-vs](../direct3dhlsl/loop---vs.md) / [REP-vs](../direct3dhlsl/rep---vs.md) et [Call-vs](../direct3dhlsl/call---vs.md) / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md) . |
| D3DPS20 \_ Min \_ STATICFLOWCONTROLDEPTH         | 1              | Profondeur minimale de l’imbrication des instructions [Loop-vs](../direct3dhlsl/loop---vs.md) / [REP-vs](../direct3dhlsl/rep---vs.md) et [Call-vs](../direct3dhlsl/call---vs.md) / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md) . |
| D3DPS20 \_ Max \_ NUMINSTRUCTIONSLOTS            | 512            | Le pilote prendra en charge le plus grand nombre d’instructions.                                                                                                                                                           |
| D3DPS20 \_ Min \_ NUMINSTRUCTIONSLOTS            | 96             | Le pilote prendra en charge au moins ce nombre d’instructions.                                                                                                                                                          |



 

Ces constantes sont utilisées par le \_ membre D3DPSHADERCAPS2 0 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="constant-information"></a>Informations constantes



|  Condition requise                        | Valeur           |
|--------------------------|------------|
| En-tête                   | d3d9caps. h |
| Système d’exploitation minimal | Windows 98 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**D3DPSHADERCAPS2 \_ 0**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dpshadercaps2_0)
</dt> </dl>

 

 
