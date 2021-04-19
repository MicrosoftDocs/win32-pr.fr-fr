---
description: Obtient un pointeur d’interface de périphérique Direct3D 10,1 à partir d’un pointeur d’interface Direct3D 10,0.
ms.assetid: cf31a67f-0493-4e79-8e73-0297ab93bbae
title: D3DX10GetFeatureLevel1, fonction (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetFeatureLevel1
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 817eb4dd68ce797da76c0609e2ead01a21b5b270
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522337"
---
# <a name="d3dx10getfeaturelevel1-function"></a><span data-ttu-id="6a42c-103">D3DX10GetFeatureLevel1 fonction)</span><span class="sxs-lookup"><span data-stu-id="6a42c-103">D3DX10GetFeatureLevel1 function</span></span>

<span data-ttu-id="6a42c-104">Obtient un pointeur d’interface de périphérique Direct3D 10,1 à partir d’un pointeur d’interface Direct3D 10,0.</span><span class="sxs-lookup"><span data-stu-id="6a42c-104">Get a Direct3D 10.1 device interface pointer from a Direct3D 10.0 interface pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a42c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a42c-105">Syntax</span></span>


```C++
HRESULT D3DX10GetFeatureLevel1(
  _In_  ID3D10Device  *pDevice,
  _Out_ ID3D10Device1 **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="6a42c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a42c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a42c-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a42c-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a42c-108">Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="6a42c-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="6a42c-109">Pointeur vers l’appareil Direct3D 10,0 (Voir l’interface [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) ).</span><span class="sxs-lookup"><span data-stu-id="6a42c-109">Pointer to the Direct3D 10.0 device (see the [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface).</span></span>

</dd> <dt>

<span data-ttu-id="6a42c-110">*ppDevice* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6a42c-110">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a42c-111">Type : **[ **ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)\*\***</span><span class="sxs-lookup"><span data-stu-id="6a42c-111">Type: **[**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)\*\***</span></span>

<span data-ttu-id="6a42c-112">Pointeur vers l’appareil Direct3D 10,1 (Voir l’interface [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) ).</span><span class="sxs-lookup"><span data-stu-id="6a42c-112">Pointer to the Direct3D 10.1 device (see the [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) interface).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a42c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6a42c-113">Return value</span></span>

<span data-ttu-id="6a42c-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6a42c-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6a42c-115">Cette fonction retourne l’un des [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="6a42c-115">This function returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span> <span data-ttu-id="6a42c-116">Si une interface de périphérique Direct3D 10,1 peut être acquise, cette fonction réussit et passe un pointeur vers l’interface 10,1 à l’aide du paramètre *ppDevice* .</span><span class="sxs-lookup"><span data-stu-id="6a42c-116">If a Direct3D 10.1 device interface can be acquired, this function succeeds and passes a pointer to the 10.1 interface using the *ppDevice* parameter.</span></span> <span data-ttu-id="6a42c-117">Si une interface de périphérique Direct3D 10,1 ne peut pas être acquise, cette fonction retourne E \_ Fail et ne retourne rien pour le paramètre *ppDevice* .</span><span class="sxs-lookup"><span data-stu-id="6a42c-117">If a Direct3D 10.1 device interface cannot be acquired, this function returns E\_FAIL, and will not return anything for the *ppDevice* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a42c-118">Notes</span><span class="sxs-lookup"><span data-stu-id="6a42c-118">Remarks</span></span>

<span data-ttu-id="6a42c-119">Pour que cette fonction aboutisse, vous devez avoir acquis le pointeur [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) fourni à l’aide d’un appel à la fonction [**D3DX10CreateDevice**](d3dx10createdevice.md) , à la fonction [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md) , à la fonction [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) ou à la fonction [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) .</span><span class="sxs-lookup"><span data-stu-id="6a42c-119">For this function to succeed, you must have acquired the supplied [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) pointer using a call to the [**D3DX10CreateDevice**](d3dx10createdevice.md) function, the [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md) function, the [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) function, or the [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) function.</span></span>

<span data-ttu-id="6a42c-120">Vous pouvez uniquement créer un périphérique Direct3D 10,1 sur des ordinateurs exécutant Windows Vista Service Pack 1 ou une version ultérieure et sur lequel le matériel compatible Direct3D 10,1 est installé.</span><span class="sxs-lookup"><span data-stu-id="6a42c-120">You can only create a Direct3D 10.1 device on computers running Windows Vista Service Pack 1 or later, and with Direct3D 10.1-compatible hardware installed.</span></span> <span data-ttu-id="6a42c-121">Cette fonction renvoie E \_ Fail sur tout ordinateur qui ne répond pas à ces exigences.</span><span class="sxs-lookup"><span data-stu-id="6a42c-121">This function will return E\_FAIL on any computer not meeting these requirements.</span></span> <span data-ttu-id="6a42c-122">Toutefois, vous pouvez appeler cette fonction sur n’importe quelle version de Windows sur laquelle la DLL D3DX10 est installée.</span><span class="sxs-lookup"><span data-stu-id="6a42c-122">However, you can call this function on any version of Windows that has the D3DX10 DLL installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a42c-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a42c-123">Requirements</span></span>



| <span data-ttu-id="6a42c-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a42c-124">Requirement</span></span> | <span data-ttu-id="6a42c-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a42c-125">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a42c-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="6a42c-126">Header</span></span><br/> | <dl> <span data-ttu-id="6a42c-127"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a42c-127"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a42c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a42c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a42c-129">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="6a42c-129">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




