---
title: Interface ID3D12DeviceDownlevel
description: fournit une requête de statistiques de mémoire spécifique à la Windows 7.
keywords:
- Interface ID3D12DeviceDownlevel
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 8cd9b39e865377734fca3d0791b89219d611f57f456a85a8f9b12e345aba9e99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124077"
---
# <a name="id3d12devicedownlevel-interface"></a>Interface ID3D12DeviceDownlevel

cette interface est accessible via **QueryInterface** sur un [appareil direct3d 12](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) lors de l’utilisation de [direct3d 12 sur Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/). il fournit une requête de statistiques de mémoire spécifique à la Windows 7.

### <a name="methods"></a>Méthodes

L’interface **ID3D12DeviceDownlevel** possède ces méthodes.

| Méthode | Description |
|:-------|:------------|
| [**QueryVideoMemoryInfo**](id3d12devicedownlevel-queryvideomemoryinfo.md) | fournit des statistiques de mémoire sur Windows 7. |

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|--------|------------------|
| En-tête | d3d12downlevel. h |
| DLL    | D3D12.dll (Windows 7 uniquement) |

## <a name="see-also"></a>Voir aussi
* [Interfaces Direct3D 12 sur Windows 7](direct3d-12on7-interfaces.md)
* [informations de référence sur Direct3D 12 sur Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [Direct3D 12 sur Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
