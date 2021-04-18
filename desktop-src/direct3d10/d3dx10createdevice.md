---
description: Créez le meilleur appareil Direct3D 10 qui représente la carte graphique. Si un appareil compatible Direct3D 10,1 peut être créé, il sera possible d’acquérir un pointeur d’interface ID3D10Device1 à partir du pointeur d’interface d’appareil retourné.
ms.assetid: 1af8f4e5-a59e-403a-95d2-069b91bad93e
title: D3DX10CreateDevice, fonction (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDevice
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 38236a48cdd5197f7f19ef9be3f6fc0f1faca72c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520342"
---
# <a name="d3dx10createdevice-function"></a><span data-ttu-id="5d275-104">D3DX10CreateDevice fonction)</span><span class="sxs-lookup"><span data-stu-id="5d275-104">D3DX10CreateDevice function</span></span>

<span data-ttu-id="5d275-105">Créez le meilleur appareil Direct3D 10 qui représente la carte graphique.</span><span class="sxs-lookup"><span data-stu-id="5d275-105">Create the best Direct3D 10 device that represents the display adapter.</span></span> <span data-ttu-id="5d275-106">Si un appareil compatible Direct3D 10,1 peut être créé, il sera possible d’acquérir un pointeur d' [**interface ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) à partir du pointeur d’interface d’appareil retourné.</span><span class="sxs-lookup"><span data-stu-id="5d275-106">If a Direct3D 10.1-compatible device can be created, it will be possible to acquire an [**ID3D10Device1 Interface**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) pointer from the returned device interface pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d275-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d275-107">Syntax</span></span>


```C++
HRESULT D3DX10CreateDevice(
  _In_  IDXGIAdapter      *pAdapter,
  _In_  D3D10_DRIVER_TYPE DriverType,
  _In_  HMODULE           Software,
  _In_  UINT              Flags,
  _Out_ ID3D10Device      **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="5d275-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d275-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d275-109">*pAdapter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5d275-109">*pAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d275-110">Type : **[ **IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span><span class="sxs-lookup"><span data-stu-id="5d275-110">Type: **[**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span></span>

<span data-ttu-id="5d275-111">Pointeur vers l’adaptateur d’affichage (Voir l’interface [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter) ) lors de la création d’un périphérique matériel ; Sinon, affectez la **valeur null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="5d275-111">Pointer to the display adapter (see the [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter) interface) when creating a hardware device; otherwise set this parameter to **NULL**.</span></span> <span data-ttu-id="5d275-112">Si la **valeur null** est spécifiée lors de la création d’un périphérique matériel, Direct3D utilise la première carte énumérée par l’interface [**IDXGIFactory**](/windows/win32/api/dxgi/nn-dxgi-idxgifactory) .</span><span class="sxs-lookup"><span data-stu-id="5d275-112">If **NULL** is specified when creating a hardware device, Direct3D will use the first adapter enumerated by the [**IDXGIFactory**](/windows/win32/api/dxgi/nn-dxgi-idxgifactory) interface.</span></span>

</dd> <dt>

<span data-ttu-id="5d275-113">*DriverType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5d275-113">*DriverType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d275-114">Type : **[ **\_ \_ type de pilote D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span><span class="sxs-lookup"><span data-stu-id="5d275-114">Type: **[**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span></span>

<span data-ttu-id="5d275-115">Le type de pilote de périphérique (consultez l’énumération de [**\_ \_ type de pilote D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type) ).</span><span class="sxs-lookup"><span data-stu-id="5d275-115">The device-driver type (see the [**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type) enumeration).</span></span> <span data-ttu-id="5d275-116">Le type de pilote détermine le type d’appareil que vous allez créer.</span><span class="sxs-lookup"><span data-stu-id="5d275-116">The driver type determines the type of device you will create.</span></span>

</dd> <dt>

<span data-ttu-id="5d275-117">*Logiciel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5d275-117">*Software* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d275-118">Type : **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d275-118">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5d275-119">Handle d’un module chargé qui implémente un pilote logiciel (tel que D3D10Ref.dll).</span><span class="sxs-lookup"><span data-stu-id="5d275-119">A handle to a loaded module that implements a software driver (such as D3D10Ref.dll).</span></span> <span data-ttu-id="5d275-120">Pour obtenir un handle, appelez la fonction [GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) .</span><span class="sxs-lookup"><span data-stu-id="5d275-120">To get a handle, call the [GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) function.</span></span>

</dd> <dt>

<span data-ttu-id="5d275-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="5d275-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d275-122">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d275-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5d275-123">Indicateurs de création de l’appareil (consultez [**D3D10 \_ Create \_ Device \_ Flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) Enumeration) qui active les [couches API](d3d10-graphics-programming-guide-api-features-layers.md).</span><span class="sxs-lookup"><span data-stu-id="5d275-123">Device creation flags (see the [**D3D10\_CREATE\_DEVICE\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) enumeration) that enable [API layers](d3d10-graphics-programming-guide-api-features-layers.md).</span></span> <span data-ttu-id="5d275-124">Ces indicateurs peuvent être des opérateurs de bits or ensemble.</span><span class="sxs-lookup"><span data-stu-id="5d275-124">These flags can be bitwise OR'd together.</span></span>

</dd> <dt>

<span data-ttu-id="5d275-125">*ppDevice* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5d275-125">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d275-126">Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="5d275-126">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="5d275-127">Adresse d’un pointeur vers l’appareil créé (consultez l’interface [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) ).</span><span class="sxs-lookup"><span data-stu-id="5d275-127">Address of a pointer to the device created (see the [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d275-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d275-128">Return value</span></span>

<span data-ttu-id="5d275-129">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5d275-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5d275-130">Cette fonction retourne l’un des [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="5d275-130">This function returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5d275-131">Notes</span><span class="sxs-lookup"><span data-stu-id="5d275-131">Remarks</span></span>

<span data-ttu-id="5d275-132">Cette fonction tente de créer le meilleur appareil pour le matériel.</span><span class="sxs-lookup"><span data-stu-id="5d275-132">This function attempts to create the best device for the hardware.</span></span> <span data-ttu-id="5d275-133">Tout d’abord, la fonction tente de créer un appareil 10,1.</span><span class="sxs-lookup"><span data-stu-id="5d275-133">First, the function attempts to create a 10.1 device.</span></span> <span data-ttu-id="5d275-134">Si un appareil 10,1 ne peut pas être créé, la fonction tente de créer un appareil 10,0.</span><span class="sxs-lookup"><span data-stu-id="5d275-134">If a 10.1 device cannot be created, the function attempts to create a 10.0 device.</span></span> <span data-ttu-id="5d275-135">Si aucun appareil n’est correctement créé, la fonction retourne E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="5d275-135">If neither device is successfully created, the function returns E\_FAIL.</span></span>

<span data-ttu-id="5d275-136">Si votre application doit créer uniquement un appareil 10,1 ou un appareil 10,0 uniquement, utilisez les fonctions suivantes à la place :</span><span class="sxs-lookup"><span data-stu-id="5d275-136">If your application needs to create only a 10.1 device, or a 10.0 device only, use the following functions instead:</span></span>

-   <span data-ttu-id="5d275-137">Utilisez la fonction [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) pour créer un appareil Direct3D 10,0 uniquement.</span><span class="sxs-lookup"><span data-stu-id="5d275-137">Use the [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) function to create a Direct3D 10.0 device only.</span></span>
-   <span data-ttu-id="5d275-138">Utilisez la fonction [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) pour créer un appareil Direct3D 10,1 uniquement.</span><span class="sxs-lookup"><span data-stu-id="5d275-138">Use the [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) function to create a Direct3D 10.1 device only.</span></span>
-   <span data-ttu-id="5d275-139">Utilisez la fonction [**D3DX10GetFeatureLevel1**](d3dx10getfeaturelevel1.md) pour récupérer un pointeur d’interface [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) à partir d’un pointeur d’interface [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) .</span><span class="sxs-lookup"><span data-stu-id="5d275-139">Use the [**D3DX10GetFeatureLevel1**](d3dx10getfeaturelevel1.md) function to get an [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) interface pointer from an [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface pointer.</span></span>

<span data-ttu-id="5d275-140">Un périphérique Direct3D 10,1 peut uniquement être créé sur des ordinateurs exécutant Windows Vista Service Pack 1 ou version ultérieure, et avec un matériel compatible Direct3D 10,1 installé.</span><span class="sxs-lookup"><span data-stu-id="5d275-140">A Direct3D 10.1 device can only be created on computers running Windows Vista Service Pack 1 or later, and with Direct3D 10.1-compatible hardware installed.</span></span> <span data-ttu-id="5d275-141">Toutefois, il est légal d’appeler cette fonction sur des ordinateurs exécutant n’importe quelle version de Windows sur laquelle la DLL D3DX10 est installée.</span><span class="sxs-lookup"><span data-stu-id="5d275-141">However, it is legal to call this function on computers running any version of Windows that has the D3DX10 DLL installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d275-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d275-142">Requirements</span></span>



| <span data-ttu-id="5d275-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d275-143">Requirement</span></span> | <span data-ttu-id="5d275-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d275-144">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d275-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d275-145">Header</span></span><br/> | <dl> <span data-ttu-id="5d275-146"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d275-146"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d275-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d275-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d275-148">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="5d275-148">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
