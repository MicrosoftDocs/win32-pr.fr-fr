---
title: ID3D12CommandQueueDownlevel ::P méthode reenvoyé
description: Copie le contenu d’une ressource Direct3D 12 Texture2D dans une fenêtre. | ID3D12CommandQueueDownlevel ::P méthode reenvoyé
keywords:
- Present (méthode)
- Méthode présente, interface ID3D12CommandQueueDownlevel
- Interface ID3D12CommandQueueDownlevel, méthode présente
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel.Present
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: a6c74685911e52a671eaeb02645754a45b8d647e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522972"
---
# <a name="id3d12commandqueuedownlevelpresent-method"></a>ID3D12CommandQueueDownlevel ::P méthode reenvoyé

Copie le contenu d’une ressource Direct3D 12 Texture2D dans une fenêtre.

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT Present
    ID3D12GraphicsCommandList *pOpenCommandList,
    ID3D12Resource *pSourceTex2D,
    HWND hWindow,
    D3D12_DOWNLEVEL_PRESENT_FLAGS Flags
);
```

## <a name="parameters"></a>Paramètres

`pOpenCommandList`

Type : **[ID3D12GraphicsCommandList](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***

Une liste de commandes ouverte, dans laquelle Direct3D 12 met en file d’attente une commande présente, puis ferme et envoie pour vous.

`pSourceTex2D`

Type : **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***

Ressource contenant le contenu que vous souhaitez afficher, avec la [**\_ dimension D3D12 \_ ressource \_ TEXTURE2D**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)dimension et un format qui est l’un des éléments suivants.

* DXGI_FORMAT_R16G16B16A16_FLOAT
* DXGI_FORMAT_R10G10B10A2_UNORM
* DXGI_FORMAT_R8G8B8A8_UNORM
* DXGI_FORMAT_R8G8B8A8_UNORM_SRGB
* DXGI_FORMAT_B8G8R8X8_UNORM
* DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM
* DXGI_FORMAT_B8G8R8A8_UNORM
* DXGI_FORMAT_B8G8R8A8_UNORM_SRGB

`hWindow`

Type : **[HWND](/windows/desktop/WinProg/windows-data-types)**

Handle de la fenêtre dans laquelle le contenu doit être affiché.

`Flags`

Type : **[ \_ indicateurs de \_ présence \_ de niveau inférieur D3D12](d3d12_downlevel_present_flags.md)**

Indicateurs permettant de modifier l’opération **présente** .

## <a name="return-value"></a>Valeur retournée

Retourne **S_OK** en cas de réussite, ou un HRESULT qui a échoué.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|--------|------------------|
| En-tête | d3d12downlevel. h |
| DLL    | D3D12.dll (Windows 7 uniquement) |

## <a name="see-also"></a>Voir aussi
* [ID3D12CommandQueueDownlevel](id3d12commandqueuedownlevel.md)
* [Interfaces Direct3D 12 sur Windows 7](direct3d-12on7-interfaces.md)
* [Informations de référence sur Direct3D 12 sur Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [Direct3D 12 sur Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
