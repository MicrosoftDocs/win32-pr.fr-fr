---
title: Énumération D3D12_DOWNLEVEL_PRESENT_FLAGS
description: Indicateurs passés à la méthode ID3D12CommandQueueDownlevel ::P retournée.
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
topic_type:
- APIRef
api_name:
- D3D12_DOWNLEVEL_PRESENT_FLAGS
api_type:
- HeaderDef
ms.openlocfilehash: 1ce1536945748bae09fc7a0981c14c076fc6394e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521737"
---
# <a name="d3d12_downlevel_present_flags-enumeration"></a>Énumération d’indicateurs D3D12 de \_ bas niveau \_ présente \_

Indicateurs passés à la fonction [**ID3D12CommandQueueDownlevel ::P renvoyée**](id3d12commandqueuedownlevel-present.md) pour modifier le comportement.

## <a name="syntax"></a>Syntaxe

```cpp
enum D3D12_DOWNLEVEL_PRESENT_FLAGS
{
    D3D12_DOWNLEVEL_PRESENT_FLAG_NONE = 0,
    D3D12_DOWNLEVEL_PRESENT_FLAG_WAIT_FOR_VBLANK = 1
};
```

## <a name="constants"></a>Constantes

**Indicateur de D3D12 de \_ niveau inférieur \_ absent \_ \_**

Aucune option sélectionnée.

**\_ \_ Indicateur de présence de niveau inférieur D3D12 \_ \_ wait \_ pour \_ vblank**

L’opération **actuelle** n’est pas effectuée tant qu’un Vsync n’a pas eu lieu depuis la dernière **Présentation** de Ed.

## <a name="requirements"></a>Spécifications

| Condition requise | Valeur |
|--------|------------------|
| En-tête | d3d12downlevel. h |
| DLL    | D3D12.dll (Windows 7 uniquement) |

## <a name="see-also"></a>Voir aussi
* [ID3D12CommandQueueDownlevel](id3d12commandqueuedownlevel.md)
* [Énumérations Direct3D 12 sur Windows 7](direct3d-12on7-enumerations.md)
* [informations de référence sur Direct3D 12 sur Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [Direct3D 12 sur Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
