---
description: Créez le meilleur appareil Direct3D et une chaîne de permutation.
ms.assetid: c320a6c4-fa68-47fc-b2cb-0dc53c2767e7
title: D3DX10CreateDeviceAndSwapChain, fonction (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDeviceAndSwapChain
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: fe71aeae91f8c43966e0fda2d2f430c7908f2855
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323197"
---
# <a name="d3dx10createdeviceandswapchain-function"></a><span data-ttu-id="6ac33-103">D3DX10CreateDeviceAndSwapChain fonction)</span><span class="sxs-lookup"><span data-stu-id="6ac33-103">D3DX10CreateDeviceAndSwapChain function</span></span>

<span data-ttu-id="6ac33-104">Créez le meilleur appareil Direct3D et une chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="6ac33-104">Create the best Direct3D device and a swap chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ac33-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ac33-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateDeviceAndSwapChain(
  _In_  IDXGIAdapter         *pAdapter,
  _In_  D3D10_DRIVER_TYPE    DriverType,
  _In_  HMODULE              Software,
  _In_  UINT                 Flags,
  _In_  DXGI_SWAP_CHAIN_DESC *pSwapChainDesc,
  _Out_ IDXGISwapChain       **ppSwapChain,
  _Out_ ID3D10Device         **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="6ac33-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ac33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ac33-107">*pAdapter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6ac33-107">*pAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ac33-108">Type : **[ **IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span><span class="sxs-lookup"><span data-stu-id="6ac33-108">Type: **[**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span></span>

<span data-ttu-id="6ac33-109">Pointeur vers un [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter).</span><span class="sxs-lookup"><span data-stu-id="6ac33-109">Pointer to a [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter).</span></span>

</dd> <dt>

<span data-ttu-id="6ac33-110">*DriverType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6ac33-110">*DriverType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ac33-111">Type : **[ **\_ \_ type de pilote D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span><span class="sxs-lookup"><span data-stu-id="6ac33-111">Type: **[**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span></span>

<span data-ttu-id="6ac33-112">Type de pilote de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6ac33-112">The type of driver for the device.</span></span> <span data-ttu-id="6ac33-113">Consultez [**\_ \_ type de pilote D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).</span><span class="sxs-lookup"><span data-stu-id="6ac33-113">See [**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).</span></span>

</dd> <dt>

<span data-ttu-id="6ac33-114">*Logiciel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6ac33-114">*Software* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ac33-115">Type : **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6ac33-115">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6ac33-116">Handle vers la DLL qui implémente un rastériseur logiciel.</span><span class="sxs-lookup"><span data-stu-id="6ac33-116">A handle to the DLL that implements a software rasterizer.</span></span> <span data-ttu-id="6ac33-117">Doit avoir la **valeur null** si DriverType est non-logiciel.</span><span class="sxs-lookup"><span data-stu-id="6ac33-117">Must be **NULL** if DriverType is non-software.</span></span> <span data-ttu-id="6ac33-118">Le HMODULE d’une DLL peut être obtenu avec [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [LoadLibraryEx](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)ou [GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="6ac33-118">The HMODULE of a DLL can be obtained with [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [LoadLibraryEx](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa), or [GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="6ac33-119">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="6ac33-119">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ac33-120">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6ac33-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6ac33-121">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="6ac33-121">Optional.</span></span> <span data-ttu-id="6ac33-122">Indicateurs de création de l’appareil (voir [**D3D10 \_ créer un \_ \_ indicateur d’appareil**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)) qui active les couches d' [API](d3d10-graphics-programming-guide-api-features-layers.md).</span><span class="sxs-lookup"><span data-stu-id="6ac33-122">Device creation flags (see [**D3D10\_CREATE\_DEVICE\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)) that enable [API layers](d3d10-graphics-programming-guide-api-features-layers.md).</span></span> <span data-ttu-id="6ac33-123">Ces indicateurs peuvent être des opérateurs de bits or ensemble.</span><span class="sxs-lookup"><span data-stu-id="6ac33-123">These flags can be bitwise OR'd together.</span></span>

</dd> <dt>

<span data-ttu-id="6ac33-124">*pSwapChainDesc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6ac33-124">*pSwapChainDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ac33-125">Type : description de la **[ **\_ \_ chaîne \_ de permutation dxgi**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)\***</span><span class="sxs-lookup"><span data-stu-id="6ac33-125">Type: **[**DXGI\_SWAP\_CHAIN\_DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)\***</span></span>

<span data-ttu-id="6ac33-126">Description de la chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="6ac33-126">Description of the swap chain.</span></span> <span data-ttu-id="6ac33-127">Consultez [**Description de la \_ \_ chaîne \_ de permutation dxgi**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc).</span><span class="sxs-lookup"><span data-stu-id="6ac33-127">See [**DXGI\_SWAP\_CHAIN\_DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc).</span></span>

</dd> <dt>

<span data-ttu-id="6ac33-128">*ppSwapChain* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6ac33-128">*ppSwapChain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ac33-129">Type : **[ **IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)\*\***</span><span class="sxs-lookup"><span data-stu-id="6ac33-129">Type: **[**IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)\*\***</span></span>

<span data-ttu-id="6ac33-130">Adresse d’un pointeur vers un [**IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain).</span><span class="sxs-lookup"><span data-stu-id="6ac33-130">Address of a pointer to an [**IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain).</span></span>

</dd> <dt>

<span data-ttu-id="6ac33-131">*ppDevice* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6ac33-131">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ac33-132">Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="6ac33-132">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="6ac33-133">Adresse d’un pointeur vers une [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) qui recevra l’appareil nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="6ac33-133">Address of a pointer to an [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) that will receive the newly created device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ac33-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6ac33-134">Return value</span></span>

<span data-ttu-id="6ac33-135">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6ac33-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6ac33-136">Cette méthode retourne l’un des [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="6ac33-136">This method returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6ac33-137">Notes</span><span class="sxs-lookup"><span data-stu-id="6ac33-137">Remarks</span></span>

<span data-ttu-id="6ac33-138">Pour créer le meilleur appareil, cette méthode implémente plusieurs options de création d’appareil.</span><span class="sxs-lookup"><span data-stu-id="6ac33-138">To create the best device, this method implements more than one device creation option.</span></span> <span data-ttu-id="6ac33-139">Tout d’abord, la méthode tente de créer un appareil 10,1 (et une chaîne de permutation).</span><span class="sxs-lookup"><span data-stu-id="6ac33-139">First, the method attempts to create a 10.1 device (and swap chain).</span></span> <span data-ttu-id="6ac33-140">En cas d’échec, la méthode tente de créer un appareil 10,0.</span><span class="sxs-lookup"><span data-stu-id="6ac33-140">If that fails, the method attempts to create a 10.0 device.</span></span> <span data-ttu-id="6ac33-141">En cas d’échec, la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="6ac33-141">If that fails, the method will fail.</span></span> <span data-ttu-id="6ac33-142">Si votre application doit créer uniquement un appareil 10,1 ou un appareil 10,0 uniquement, utilisez plutôt ces API :</span><span class="sxs-lookup"><span data-stu-id="6ac33-142">If your application needs to create only a 10.1 device, or a 10.0 device only, use these APIs instead:</span></span>

-   <span data-ttu-id="6ac33-143">Utilisez [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdeviceandswapchain) pour créer un appareil Direct3D 10,0 (uniquement) et une chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="6ac33-143">Use [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdeviceandswapchain) to create a Direct3D 10.0 (only) device and swap chain.</span></span>
-   <span data-ttu-id="6ac33-144">Utilisez [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) pour créer un appareil Direct3D 10,1 (uniquement) et une chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="6ac33-144">Use [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) to create a Direct3D 10.1 (only) device and swap chain.</span></span>

<span data-ttu-id="6ac33-145">Cette méthode nécessite Windows Vista Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6ac33-145">This method requires Windows Vista Service Pack 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ac33-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ac33-146">Requirements</span></span>



| <span data-ttu-id="6ac33-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ac33-147">Requirement</span></span> | <span data-ttu-id="6ac33-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ac33-148">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ac33-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="6ac33-149">Header</span></span><br/> | <dl> <span data-ttu-id="6ac33-150"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ac33-150"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ac33-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ac33-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ac33-152">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="6ac33-152">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
