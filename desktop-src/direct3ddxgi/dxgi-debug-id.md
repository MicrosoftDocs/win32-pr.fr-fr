---
description: Valeurs d’identificateur global unique (GUID) qui identifient les producteurs de messages de débogage.
ms.assetid: 85946D30-5E49-4E4B-AC25-394ABFF0DB11
title: DXGI_DEBUG_ID (DXGIDebug. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc750d94fbdc51ba3399a6e3d4ff45b0adeb68b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513298"
---
# <a name="dxgi_debug_id"></a><span data-ttu-id="851c5-103">\_ID de débogage dxgi \_</span><span class="sxs-lookup"><span data-stu-id="851c5-103">DXGI\_DEBUG\_ID</span></span>

<span data-ttu-id="851c5-104">Valeurs d’identificateur global unique (GUID) qui identifient les producteurs de messages de débogage.</span><span class="sxs-lookup"><span data-stu-id="851c5-104">Globally unique identifier (GUID) values that identify producers of debug messages.</span></span>



| <span data-ttu-id="851c5-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="851c5-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                         | <span data-ttu-id="851c5-106">Description</span><span class="sxs-lookup"><span data-stu-id="851c5-106">Description</span></span>                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_DEBUG_ALL"></span><span id="dxgi_debug_all"></span><dl> <span data-ttu-id="851c5-107"><dt>**Dxgi \_ Déboguer \_ tous les**</dt> <dt>0xe48ae283, 0xda80, 0x490b, 0x87, 0xe6, 0x43, 0xE9, 0xA9, 0xcf, 0xDA, 0x8</dt></span><span class="sxs-lookup"><span data-stu-id="851c5-107"><dt>**DXGI\_DEBUG\_ALL**</dt> <dt>0xe48ae283, 0xda80, 0x490b, 0x87, 0xe6, 0x43, 0xe9, 0xa9, 0xcf, 0xda, 0x8</dt></span></span> </dl>       | <span data-ttu-id="851c5-108">Tous les objets Direct3D et DXGI et les applications privées.</span><span class="sxs-lookup"><span data-stu-id="851c5-108">All Direct3D and DXGI objects and private apps.</span></span><br/>                                                                                     |
| <span id="DXGI_DEBUG_DX"></span><span id="dxgi_debug_dx"></span><dl> <span data-ttu-id="851c5-109"><dt>**Dxgi \_ DEBUG \_ DX**</dt> <dt>0x35cdd7fc, 0x13B2, 0x421d, 0xa5, 0xd7, 0x7E, 0x44, 0x51, 0x28, 0x7d, 0x64</dt></span><span class="sxs-lookup"><span data-stu-id="851c5-109"><dt>**DXGI\_DEBUG\_DX**</dt> <dt>0x35cdd7fc, 0x13b2, 0x421d, 0xa5, 0xd7, 0x7e, 0x44, 0x51, 0x28, 0x7d, 0x64</dt></span></span> </dl>         | <span data-ttu-id="851c5-110">Les objets Direct3D et DXGI.</span><span class="sxs-lookup"><span data-stu-id="851c5-110">Direct3D and DXGI objects.</span></span><br/>                                                                                                          |
| <span id="DXGI_DEBUG_DXGI"></span><span id="dxgi_debug_dxgi"></span><dl> <span data-ttu-id="851c5-111"><dt>**Dxgi \_ DEBUG \_ dxgi**</dt> <dt>0x25cddaa4, 0xb1c6, 0x47e1, 0xac, 0x3E, 0x98, 0x87, 0x5B, 0x5A, 0x2E, 0x2A</dt></span><span class="sxs-lookup"><span data-stu-id="851c5-111"><dt>**DXGI\_DEBUG\_DXGI**</dt> <dt>0x25cddaa4, 0xb1c6, 0x47e1, 0xac, 0x3e, 0x98, 0x87, 0x5b, 0x5a, 0x2e, 0x2a</dt></span></span> </dl>   | <span data-ttu-id="851c5-112">DXGI.</span><span class="sxs-lookup"><span data-stu-id="851c5-112">DXGI.</span></span><br/>                                                                                                                               |
| <span id="DXGI_DEBUG_APP"></span><span id="dxgi_debug_app"></span><dl> <span data-ttu-id="851c5-113"><dt>**Dxgi \_ Déboguer l' \_ application**</dt> <dt>0x6cd6e01, 0x4219, 0x4ebd, 0x87, 0x9, 0x27, 0xED, 0x23, 0x36, 0xc, 0x62</dt></span><span class="sxs-lookup"><span data-stu-id="851c5-113"><dt>**DXGI\_DEBUG\_APP**</dt> <dt>0x6cd6e01, 0x4219, 0x4ebd, 0x87, 0x9, 0x27, 0xed, 0x23, 0x36, 0xc, 0x62</dt></span></span> </dl>         | <span data-ttu-id="851c5-114">Applications privées.</span><span class="sxs-lookup"><span data-stu-id="851c5-114">Private apps.</span></span> <span data-ttu-id="851c5-115">Tous les messages que vous ajoutez avec [**IDXGIInfoQueue :: AddApplicationMessage**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-idxgiinfoqueue-addapplicationmessage).</span><span class="sxs-lookup"><span data-stu-id="851c5-115">Any messages that you add with [**IDXGIInfoQueue::AddApplicationMessage**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-idxgiinfoqueue-addapplicationmessage).</span></span><br/> |
| <span id="DXGI_DEBUG_D3D11"></span><span id="dxgi_debug_d3d11"></span><dl> <span data-ttu-id="851c5-116"><dt>**Dxgi \_ DEBUG \_ d3d11**</dt> <dt>0x4b99317b, 0xac39, 0x4aa6, 0xBB, 0xb, 0xba, 0xa0, 0x47, 0x84, 0x79, 0x8F</dt></span><span class="sxs-lookup"><span data-stu-id="851c5-116"><dt>**DXGI\_DEBUG\_D3D11**</dt> <dt>0x4b99317b, 0xac39, 0x4aa6, 0xbb, 0xb, 0xba, 0xa0, 0x47, 0x84, 0x79, 0x8f</dt></span></span> </dl> | <span data-ttu-id="851c5-117">Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="851c5-117">Direct3D 11.</span></span> <span data-ttu-id="851c5-118">Défini dans D3D11SDKLayers. h.</span><span class="sxs-lookup"><span data-stu-id="851c5-118">Defined in D3D11SDKLayers.h.</span></span><br/>                                                                                           |



## <a name="remarks"></a><span data-ttu-id="851c5-119">Notes</span><span class="sxs-lookup"><span data-stu-id="851c5-119">Remarks</span></span>

<span data-ttu-id="851c5-120">Utilisez ces valeurs avec l’interface [**IDXGIInfoQueue**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgiinfoqueue) .</span><span class="sxs-lookup"><span data-stu-id="851c5-120">Use these values with the [**IDXGIInfoQueue**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgiinfoqueue) interface.</span></span>

``` syntax
typedef GUID DXGI_DEBUG_ID;

DEFINE_GUID(DXGI_DEBUG_ALL, 0xe48ae283, 0xda80, 0x490b, 0x87, 0xe6, 0x43, 0xe9, 0xa9, 0xcf, 0xda, 0x8);
DEFINE_GUID(DXGI_DEBUG_DX, 0x35cdd7fc, 0x13b2, 0x421d, 0xa5, 0xd7, 0x7e, 0x44, 0x51, 0x28, 0x7d, 0x64);
DEFINE_GUID(DXGI_DEBUG_DXGI, 0x25cddaa4, 0xb1c6, 0x47e1, 0xac, 0x3e, 0x98, 0x87, 0x5b, 0x5a, 0x2e, 0x2a);
DEFINE_GUID(DXGI_DEBUG_APP, 0x6cd6e01, 0x4219, 0x4ebd, 0x87, 0x9, 0x27, 0xed, 0x23, 0x36, 0xc, 0x62);

DEFINE_GUID(DXGI_DEBUG_D3D11, 0x4b99317b, 0xac39, 0x4aa6, 0xbb, 0xb, 0xba, 0xa0, 0x47, 0x84, 0x79, 0x8f);
```

<span data-ttu-id="851c5-121">Pour utiliser l’une de ces valeurs GUID, incluez DXGIDebug. h dans votre code et liez-le à dxguid. lib.</span><span class="sxs-lookup"><span data-stu-id="851c5-121">To use any of these GUID values, include DXGIDebug.h in your code and link to dxguid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="851c5-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="851c5-122">Requirements</span></span>



| <span data-ttu-id="851c5-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="851c5-123">Requirement</span></span> | <span data-ttu-id="851c5-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="851c5-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="851c5-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="851c5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="851c5-126">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="851c5-126">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                      |
| <span data-ttu-id="851c5-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="851c5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="851c5-128">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="851c5-128">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                            |
| <span data-ttu-id="851c5-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="851c5-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="851c5-130"><dt>DXGIDebug. h</dt></span><span class="sxs-lookup"><span data-stu-id="851c5-130"><dt>DXGIDebug.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="851c5-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="851c5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="851c5-132">Constantes DXGI</span><span class="sxs-lookup"><span data-stu-id="851c5-132">DXGI Constants</span></span>](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




