---
title: 'ID3D12DeviceDownlevel :: QueryVideoMemoryInfo, méthode'
description: 'Copie le contenu d’une ressource Direct3D 12 Texture2D dans une fenêtre. | ID3D12DeviceDownlevel :: QueryVideoMemoryInfo, méthode'
keywords:
- Méthode QueryVideoMemoryInfo
- Méthode QueryVideoMemoryInfo, interface ID3D12DeviceDownlevel
- Interface ID3D12DeviceDownlevel, méthode QueryVideoMemoryInfo
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel.QueryVideoMemoryInfo
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 526d25e8331fc949eb470c0813a083774afddc94312ed6751aaab9672e557d3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124107"
---
# <a name="id3d12devicedownlevelqueryvideomemoryinfo-method"></a>ID3D12DeviceDownlevel :: QueryVideoMemoryInfo, méthode

fournit des statistiques de mémoire sur Windows 7. cette méthode est équivalente à [IDXGIAdapter3 :: QueryVideoMemoryInfo](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo), qui n’est pas disponible sur Windows 7.

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT QueryVideoMemoryInfo( 
    UINT NodeIndex,
    DXGI_MEMORY_SEGMENT_GROUP MemorySegmentGroup,
    DXGI_QUERY_VIDEO_MEMORY_INFO *pVideoMemoryInfo
);
```

## <a name="parameters"></a>Paramètres

`NodeIndex`

Type : **uint**

Spécifie la carte physique de l’appareil pour laquelle les informations de mémoire vidéo sont interrogées. Pour une opération à processeur unique, affectez-lui la valeur zéro. S’il existe plusieurs nœuds GPU, définissez cette valeur sur l’index du nœud (la carte physique de l’appareil) pour lequel les informations de mémoire vidéo sont interrogées. Consultez [systèmes à plusieurs adaptateurs](multi-engine.md).

`MemorySegmentGroup`

Type : **[DXGI_MEMORY_SEGMENT_GROUP](/windows/win32/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)**

Spécifie un **DXGI_MEMORY_SEGMENT_GROUP** qui identifie le groupe comme local ou non local.

`pVideoMemoryInfo`

Type : **[DXGI_QUERY_VIDEO_MEMORY_INFO](/windows/win32/api/dxgi1_4/ns-dxgi1_4-dxgi_query_video_memory_info)\***

Remplit une structure **DXGI_QUERY_VIDEO_MEMORY_INFO** avec les valeurs actuelles.

## <a name="return-value"></a>Valeur retournée

Retourne **S_OK** en cas de réussite, ou un HRESULT qui a échoué.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|--------|------------------|
| En-tête | d3d12downlevel. h et dxgi1_4. h |
| DLL    | D3D12.dll (Windows 7 uniquement) |

## <a name="see-also"></a>Voir aussi
* [ID3D12DeviceDownlevel](id3d12devicedownlevel.md)
* [Interfaces Direct3D 12 sur Windows 7](direct3d-12on7-interfaces.md)
* [informations de référence sur Direct3D 12 sur Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [Direct3D 12 sur Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
