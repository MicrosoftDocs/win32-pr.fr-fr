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
# <a name="idxgifactory3getcreationflags-method"></a><span data-ttu-id="d7d71-103">IDXGIFactory3 :: GetCreationFlags, méthode</span><span class="sxs-lookup"><span data-stu-id="d7d71-103">IDXGIFactory3::GetCreationFlags method</span></span>

<span data-ttu-id="d7d71-104">Obtient les indicateurs qui ont été utilisés lors de la création d’un objet d’infrastructure Microsoft DirectX Graphics (DXGI).</span><span class="sxs-lookup"><span data-stu-id="d7d71-104">Gets the flags that were used when a Microsoft DirectX Graphics Infrastructure (DXGI) object was created.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7d71-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7d71-105">Syntax</span></span>


```C++
UINT GetCreationFlags();
```



## <a name="parameters"></a><span data-ttu-id="d7d71-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7d71-106">Parameters</span></span>

<span data-ttu-id="d7d71-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d7d71-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d7d71-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d7d71-108">Return value</span></span>

<span data-ttu-id="d7d71-109">Indicateurs de création.</span><span class="sxs-lookup"><span data-stu-id="d7d71-109">The creation flags.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7d71-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d7d71-110">Remarks</span></span>

<span data-ttu-id="d7d71-111">La méthode **GetCreationFlags** retourne les indicateurs passés à la fonction [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) ou construits implicitement par [**CreateDXGIFactory**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory), [**CreateDXGIFactory1**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1), [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice)ou [**D3D11CreateDeviceAndSwapChain**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain).</span><span class="sxs-lookup"><span data-stu-id="d7d71-111">The **GetCreationFlags** method returns flags that were passed to the [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) function, or were implicitly constructed by [**CreateDXGIFactory**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory), [**CreateDXGIFactory1**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1), [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice), or [**D3D11CreateDeviceAndSwapChain**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>

## <a name="see-also"></a><span data-ttu-id="d7d71-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7d71-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7d71-113">**IDXGIFactory3**</span><span class="sxs-lookup"><span data-stu-id="d7d71-113">**IDXGIFactory3**</span></span>](/windows/desktop/api/DXGI1_3/nn-dxgi1_3-idxgifactory3)
</dt> </dl>

 

 
