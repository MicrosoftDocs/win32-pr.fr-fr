---
title: SV_InnerCoverage
description: SV \_ InputCoverage représente des informations de pixellisation conservatrice sous-estimées (par exemple, si un pixel est garanti comme étant entièrement couvert).
ms.assetid: 5BB3C3FB-E5ED-4395-B389-300DE67C984B
keywords:
- SV_InnerCoverage HLSL
topic_type:
- apiref
api_name:
- SV_InnerCoverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2f1393a6a11a95c8c08746f57083fe193791a60
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990997"
---
# <a name="sv_innercoverage"></a>SV \_ InnerCoverage

SV \_ InputCoverage représente des informations de pixellisation conservatrice sous-estimées (par exemple, si un pixel est garanti comme étant entièrement couvert).

## <a name="type"></a>Type



|      |
|------|
| Type |
| uint |



 

## <a name="remarks"></a>Notes

Cette valeur générée par le système est requise pour la prise en charge de niveau 3 et n’est disponible que dans ce niveau. Cette entrée s’exclut mutuellement avec la \_ couverture SV-les deux ne peuvent pas être utilisés.

Pour accéder à SV \_ InnerCoverage, il doit être déclaré en tant que composant unique parmi l’un des registres d’entrée de nuanceur de pixels. Le mode d’interpolation sur la déclaration doit être constant (l’interpolation ne s’applique pas).

La pixellisation conservatrice est disponible à la fois dans D3D 11.3 et D3D12. Consultez :

-   [Pixellisation de D3D 11,3 en toute prudence](/windows/desktop/direct3d11/conservative-rasterization)
-   [Pixellisation D3D12](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[Valeurs système du modèle de nuanceur 5,1](shader-model-5-1-system-values.md)
</dt> </dl>

 

 