---
description: Options pour énumérer les modes d’affichage.
ms.assetid: 7e0f5629-f8e2-478b-b8eb-00780a3dcf1f
title: DXGI_ENUM_MODES (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056ad959f0b86fb6f357d690f2daab908275e038
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232685"
---
# <a name="dxgi_enum_modes"></a>\_modes d’énumération dxgi \_

Options pour énumérer les modes d’affichage.



| Constante/valeur                                                                                                                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_ENUM_MODES_INTERLACED"></span><span id="dxgi_enum_modes_interlaced"></span><dl> <dt>**Dxgi \_ MODES ENUM 1UL \_ \_ entrelacés**</dt> <dt></dt> </dl>                 | Inclut les modes entrelacés.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="DXGI_ENUM_MODES_SCALING"></span><span id="dxgi_enum_modes_scaling"></span><dl> <dt>**Dxgi \_ MODES ENUM pour la \_ \_ mise à l’échelle**</dt> de <dt>2UL</dt> </dl>                          | Inclut les modes de mise à l’échelle étirée.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="DXGI_ENUM_MODES_STEREO"></span><span id="dxgi_enum_modes_stereo"></span><dl> <dt>**Dxgi \_ MODES d’ÉNUMÉRation \_ \_ stéréo**</dt> <dt>4UL</dt> </dl>                             | Inclut les modes stéréo.<br/> **Direct3D 11 :** Cette valeur d’énumération est prise en charge à partir de Windows 8.<br/>                                                                                                                                                                                                                       |
| <span id="DXGI_ENUM_MODES_DISABLED_STEREO"></span><span id="dxgi_enum_modes_disabled_stereo"></span><dl> <dt>**Dxgi \_ \_Modes enum \_ désactivés \_ stéréo**</dt> <dt>8UL</dt> </dl> | Inclut les modes stéréo qui sont masqués, car l’utilisateur a désactivé la stéréo. Les applications du panneau de configuration peuvent utiliser cette option pour afficher les fonctionnalités stéréo qui ont été désactivées dans le cadre d’une interface utilisateur qui active et désactive la fonction stéréo.<br/> **Direct3D 11 :** Cette valeur d’énumération est prise en charge à partir de Windows 8.<br/> |



## <a name="remarks"></a>Notes

Ces options d’indicateur sont utilisées dans [**IDXGIOutput :: GetDisplayModeList**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getdisplaymodelist) pour énumérer les modes d’affichage.

Ces options d’indicateur sont également utilisées dans [**IDXGIOutput1 :: GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) pour énumérer les modes d’affichage.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DXGI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




