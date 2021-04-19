---
title: Interface ID3D12CommandQueueDownlevel
description: Fournit un mécanisme présent spécifique à Windows 7.
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
ms.openlocfilehash: 6f2aee6fd1b0f58469162c640d92aeb187bd9641
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531520"
---
# <a name="id3d12commandqueuedownlevel-interface"></a>Interface ID3D12CommandQueueDownlevel

Cette interface est accessible via **QueryInterface** à partir d’une [file d’attente de commandes Direct3D 12](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) lors de l’utilisation [de Direct3D 12 sur Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/). Il fournit un mécanisme présent spécifique à Windows 7.

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
* [Informations de référence sur Direct3D 12 sur Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [Direct3D 12 sur Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
