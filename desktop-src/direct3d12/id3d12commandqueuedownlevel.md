---
title: Interface ID3D12CommandQueueDownlevel
description: fournit un mécanisme présent spécifique à la Windows 7.
keywords:
- Interface ID3D12CommandQueueDownlevel
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 61b41171d484797ff522cd32171e6ca168d586845c748de5a90e8c349bafdc1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069649"
---
# <a name="id3d12commandqueuedownlevel-interface"></a>Interface ID3D12CommandQueueDownlevel

cette interface est accessible via **QueryInterface** à partir d’une [file d’attente de commandes direct3d 12](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) lors de l’utilisation [de direct3d 12 sur Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/). il fournit un mécanisme présent spécifique à la Windows 7.

### <a name="methods"></a>Méthodes

L’interface **ID3D12CommandQueueDownlevel** possède ces méthodes.

| Méthode | Description |
|:-------|:------------|
| [**Présent**](id3d12commandqueuedownlevel-present.md) | Copie le contenu d’une ressource D3D12 Texture2D dans une fenêtre. |

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|--------|------------------|
| En-tête | d3d12downlevel. h |
| DLL    | D3D12.dll (Windows 7 uniquement) |

## <a name="see-also"></a>Voir aussi
* [Interfaces Direct3D 12 sur Windows 7](direct3d-12on7-interfaces.md)
* [informations de référence sur Direct3D 12 sur Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [Direct3D 12 sur Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
