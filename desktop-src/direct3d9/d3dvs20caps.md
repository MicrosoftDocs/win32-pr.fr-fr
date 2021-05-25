---
description: Constantes de sommets de nuanceur de sommets. Ces constantes sont utilisées par le membre VS20Caps de D3DCAPS9.
ms.assetid: c1321957-4ba5-45d0-984a-4f4267221c59
title: D3DVS20CAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bd0905a0996e2dc9df77adb0896c9397a93450
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342944"
---
# <a name="d3dvs20caps"></a>D3DVS20CAPS

Constantes de sommets de nuanceur de sommets. Ces constantes sont utilisées par le membre VS20Caps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).



| \#définition                              | Valeur          | Description                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_PRÉDICAT D3DVS20CAPS              | (1 << 0) | Le prédicat d’instruction est pris en charge. Voir [ \_ COMP setp-vs](../direct3dhlsl/setp-comp---vs.md).                                                                                                                                                                                                                   |
| D3DVS20 \_ Max \_ DYNAMICFLOWCONTROLDEPTH | 24             | Le niveau maximal d’imbrication des instructions de contrôle de workflow dynamique ([interruption-vs](../direct3dhlsl/break---vs.md), [rupture \_ COMP-vs](../direct3dhlsl/break-comp---vs.md), [breakp-vs](../direct3dhlsl/breakp---vs.md), si [COMP- \_ vs](../direct3dhlsl/if-comp---vs.md), si COMP-vs, \_ [si prédit-vs](../direct3dhlsl/if-pred---vs.md)). |
| D3DVS20 \_ Min \_ DYNAMICFLOWCONTROLDEPTH | 0              | Le niveau minimal d’imbrication des instructions de contrôle de workflow dynamique ([break-vs](../direct3dhlsl/break---vs.md), [pause \_ COMP-vs](../direct3dhlsl/break-comp---vs.md), [breakp-vs](../direct3dhlsl/breakp---vs.md), [si \_ COMP-vs](../direct3dhlsl/if-comp---vs.md), si COMP-vs, \_ [si préditd-vs](../direct3dhlsl/if-pred---vs.md)). |
| D3DVS20 \_ Max \_ NUMTEMPS                | 32             | Nombre maximal de registres temporaires pris en charge.                                                                                                                                                                                                                                                        |
| D3DVS20 \_ Min \_ NUMTEMPS                | 12             | Nombre minimal de registres temporaires pris en charge.                                                                                                                                                                                                                                                        |
| D3DVS20 \_ Max \_ STATICFLOWCONTROLDEPTH  | 4              | Profondeur maximale d’imbrication des instructions [Loop-vs](../direct3dhlsl/loop---vs.md) / [REP-vs](../direct3dhlsl/rep---vs.md) et [Call-vs](../direct3dhlsl/call---vs.md) / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md) .                                                                                           |
| D3DVS20 \_ Min \_ STATICFLOWCONTROLDEPTH  | 1              | Profondeur minimale de l’imbrication des instructions [Loop-vs](../direct3dhlsl/loop---vs.md) / [REP-vs](../direct3dhlsl/rep---vs.md) et [Call-vs](../direct3dhlsl/call---vs.md) / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md) .                                                                                           |



 

## <a name="constant-information"></a>Informations constantes



| Condition requise                         | Valeur           |
|--------------------------|------------|
| En-tête                   | d3d9caps. h |
| Système d’exploitation minimal | Windows 98 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**D3DVSHADERCAPS2 \_ 0**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dvshadercaps2_0)
</dt> </dl>

 

 
