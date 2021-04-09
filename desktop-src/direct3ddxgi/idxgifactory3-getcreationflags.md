---
description: Obtient les indicateurs qui ont été utilisés lors de la création d’un objet d’infrastructure Microsoft DirectX Graphics (DXGI).
ms.assetid: 1B4A5DC9-6853-4047-B64D-BD251352AC89
title: 'IDXGIFactory3 :: GetCreationFlags, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDXGIFactory3.GetCreationFlags
api_type:
- COM
api_location:
- dxgi1_3.h
ms.openlocfilehash: 56d1f35ea5a4ce26a0d9ccb5ee0d79035f74a0ad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108383"
---
# <a name="idxgifactory3getcreationflags-method"></a>IDXGIFactory3 :: GetCreationFlags, méthode

Obtient les indicateurs qui ont été utilisés lors de la création d’un objet d’infrastructure Microsoft DirectX Graphics (DXGI).

## <a name="syntax"></a>Syntaxe


```C++
UINT GetCreationFlags();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Indicateurs de création.

## <a name="remarks"></a>Notes

La méthode **GetCreationFlags** retourne les indicateurs passés à la fonction [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) ou construits implicitement par [**CreateDXGIFactory**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory), [**CreateDXGIFactory1**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1), [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice)ou [**D3D11CreateDeviceAndSwapChain**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDXGIFactory3**](/windows/desktop/api/DXGI1_3/nn-dxgi1_3-idxgifactory3)
</dt> </dl>

 

 
