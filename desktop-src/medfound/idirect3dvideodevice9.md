---
description: Active le décodage accéléré par le matériel à partir d’un appareil Direct3D 9, à l’aide de DirectX Video Acceleration (DXVA) version 1,0.
ms.assetid: abe3beac-f3f8-413d-8b83-9da3340b19ac
title: Interface IDirect3DVideoDevice9 (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 89afef6f39b3aa196d8b1013e3d8873e329ce6ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114223"
---
# <a name="idirect3dvideodevice9-interface"></a><span data-ttu-id="2bb99-103">Interface IDirect3DVideoDevice9</span><span class="sxs-lookup"><span data-stu-id="2bb99-103">IDirect3DVideoDevice9 interface</span></span>

<span data-ttu-id="2bb99-104">Active le décodage accéléré par le matériel à partir d’un appareil Direct3D 9, à l’aide de DirectX Video Acceleration (DXVA) version 1,0.</span><span class="sxs-lookup"><span data-stu-id="2bb99-104">Enables hardware-accelerated decoding from a Direct3D 9 device, using DirectX Video Acceleration (DXVA) version 1.0.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="2bb99-105">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="2bb99-105">When to use</span></span>

<span data-ttu-id="2bb99-106">Cette interface n’est pas destinée à une utilisation générale des applications.</span><span class="sxs-lookup"><span data-stu-id="2bb99-106">This interface is not intended for general application use.</span></span> <span data-ttu-id="2bb99-107">Les filtres de décodeur DirectShow doivent utiliser l’interface [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) , et non **IDirect3DVideoDevice9**.</span><span class="sxs-lookup"><span data-stu-id="2bb99-107">DirectShow decoder filters should use the [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) interface, not **IDirect3DVideoDevice9**.</span></span> <span data-ttu-id="2bb99-108">Les broches d’entrée du filtre de mixage vidéo (VMR) et du filtre de mixage de superposition exposent **IAMVideoAccelerator**.</span><span class="sxs-lookup"><span data-stu-id="2bb99-108">The input pins of the Video Mixing Renderer (VMR) filter and the Overlay Mixer filter expose **IAMVideoAccelerator**.</span></span>

## <a name="members"></a><span data-ttu-id="2bb99-109">Membres</span><span class="sxs-lookup"><span data-stu-id="2bb99-109">Members</span></span>

<span data-ttu-id="2bb99-110">L’interface **IDirect3DVideoDevice9** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2bb99-110">The **IDirect3DVideoDevice9** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2bb99-111">**IDirect3DVideoDevice9** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2bb99-111">**IDirect3DVideoDevice9** also has these types of members:</span></span>

-   [<span data-ttu-id="2bb99-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2bb99-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2bb99-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2bb99-113">Methods</span></span>

<span data-ttu-id="2bb99-114">L’interface **IDirect3DVideoDevice9** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2bb99-114">The **IDirect3DVideoDevice9** interface has these methods.</span></span>



| <span data-ttu-id="2bb99-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="2bb99-115">Method</span></span>                                                                                   | <span data-ttu-id="2bb99-116">Description</span><span class="sxs-lookup"><span data-stu-id="2bb99-116">Description</span></span>                                                                                                                       |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2bb99-117">**CreateDXVADevice**</span><span class="sxs-lookup"><span data-stu-id="2bb99-117">**CreateDXVADevice**</span></span>](idirect3dvideodevice9-createdxvadevice.md)                       | <span data-ttu-id="2bb99-118">Crée un appareil de décodage DXVA.</span><span class="sxs-lookup"><span data-stu-id="2bb99-118">Creates a DXVA decoder device.</span></span><br/>                                                                                         |
| [<span data-ttu-id="2bb99-119">**CreateSurface**</span><span class="sxs-lookup"><span data-stu-id="2bb99-119">**CreateSurface**</span></span>](idirect3dvideodevice9-createsurface.md)                             | <span data-ttu-id="2bb99-120">Crée une surface compressée pour le décodage DXVA.</span><span class="sxs-lookup"><span data-stu-id="2bb99-120">Creates a compressed surface for DXVA decoding.</span></span><br/>                                                                        |
| [<span data-ttu-id="2bb99-121">**GetDXVACompressedBufferInfo**</span><span class="sxs-lookup"><span data-stu-id="2bb99-121">**GetDXVACompressedBufferInfo**</span></span>](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) | <span data-ttu-id="2bb99-122">Obtient des informations sur les mémoires tampons compressées nécessaires au décodage accéléré par le matériel.</span><span class="sxs-lookup"><span data-stu-id="2bb99-122">Gets information about the compressed buffers needed for hardware-accelerated decoding.</span></span><br/>                                |
| [<span data-ttu-id="2bb99-123">**GetDXVAGuids**</span><span class="sxs-lookup"><span data-stu-id="2bb99-123">**GetDXVAGuids**</span></span>](idirect3dvideodevice9-getdxvaguids.md)                               | <span data-ttu-id="2bb99-124">Obtient une liste des profils DXVA pris en charge par le pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="2bb99-124">Gets a list of the DXVA profiles that are supported by the display driver.</span></span><br/>                                             |
| [<span data-ttu-id="2bb99-125">**GetDXVAInternalInfo**</span><span class="sxs-lookup"><span data-stu-id="2bb99-125">**GetDXVAInternalInfo**</span></span>](idirect3dvideodevice9-getdxvainternalinfo.md)                 | <span data-ttu-id="2bb99-126">Recherche la quantité de mémoire de travail allouée par la couche d’abstraction matérielle (HAL) pour son usage privé.</span><span class="sxs-lookup"><span data-stu-id="2bb99-126">Queries for the amount of scratch memory that the hardware abstraction layer (HAL) will allocate for its private use.</span></span> <br/> |
| [<span data-ttu-id="2bb99-127">**GetUncompressedDXVAFormats**</span><span class="sxs-lookup"><span data-stu-id="2bb99-127">**GetUncompressedDXVAFormats**</span></span>](idirect3dvideodevice9-getuncompresseddxvaformats.md)   | <span data-ttu-id="2bb99-128">Obtient une liste de formats de pixel non compressés qui peuvent être rendus à l’aide d’un profil DXVA spécifié.</span><span class="sxs-lookup"><span data-stu-id="2bb99-128">Gets a list of uncompressed pixel formats that can be rendered using a specified DXVA profile.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="2bb99-129">Notes</span><span class="sxs-lookup"><span data-stu-id="2bb99-129">Remarks</span></span>

<span data-ttu-id="2bb99-130">Pour obtenir un pointeur vers cette interface, appelez **QueryInterface** sur un pointeur [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) ou [**IDirect3DDevice9Ex**](/windows/win32/api/d3d9/nn-d3d9-idirect3ddevice9ex) .</span><span class="sxs-lookup"><span data-stu-id="2bb99-130">To get a pointer to this interface, call **QueryInterface** on an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) or [**IDirect3DDevice9Ex**](/windows/win32/api/d3d9/nn-d3d9-idirect3ddevice9ex) pointer.</span></span>

<span data-ttu-id="2bb99-131">Cette interface prend en charge DXVA 1,0 uniquement.</span><span class="sxs-lookup"><span data-stu-id="2bb99-131">This interface supports DXVA 1.0 only.</span></span> <span data-ttu-id="2bb99-132">Elle ne prend pas en charge la 2,0 DXVA.</span><span class="sxs-lookup"><span data-stu-id="2bb99-132">It does not support DXVA 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bb99-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2bb99-133">Requirements</span></span>



| <span data-ttu-id="2bb99-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2bb99-134">Requirement</span></span> | <span data-ttu-id="2bb99-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="2bb99-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2bb99-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2bb99-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2bb99-137">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2bb99-137">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2bb99-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2bb99-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2bb99-139">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2bb99-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2bb99-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="2bb99-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bb99-141"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bb99-141"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bb99-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2bb99-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bb99-143">Interfaces vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="2bb99-143">Direct3D Video Interfaces</span></span>](direct3d-video-interfaces.md)
</dt> <dt>

[<span data-ttu-id="2bb99-144">Accélération vidéo DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="2bb99-144">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="2bb99-145">Spécification 1,0 DXVA</span><span class="sxs-lookup"><span data-stu-id="2bb99-145">DXVA 1.0 specification</span></span>](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
