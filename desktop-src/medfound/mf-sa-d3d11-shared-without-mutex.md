---
description: Indique à l’allocateur d’échantillon vidéo de créer des textures partageables à l’aide du mécanisme hérité.
ms.assetid: A9F4D4AF-BB47-48E2-B40A-D0245FD61FAF
title: Attribut MF_SA_D3D11_SHARED_WITHOUT_MUTEX (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9139328c9d272007be6e5cd9434614cb1de8c9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518564"
---
# <a name="mf_sa_d3d11_shared_without_mutex-attribute"></a><span data-ttu-id="42abc-103">MF \_ sa \_ d3d11 \_ partagée \_ sans \_ attribut MUTEX</span><span class="sxs-lookup"><span data-stu-id="42abc-103">MF\_SA\_D3D11\_SHARED\_WITHOUT\_MUTEX attribute</span></span>

<span data-ttu-id="42abc-104">Indique à l’allocateur d’échantillon vidéo de créer des textures partageables à l’aide du mécanisme hérité.</span><span class="sxs-lookup"><span data-stu-id="42abc-104">Indicates to the video sample allocator to create textures as shareable using the legacy mechanism.</span></span>

## <a name="data-type"></a><span data-ttu-id="42abc-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="42abc-105">Data type</span></span>

<span data-ttu-id="42abc-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="42abc-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="42abc-107">Notes</span><span class="sxs-lookup"><span data-stu-id="42abc-107">Remarks</span></span>

### <a name="sample-allocator"></a><span data-ttu-id="42abc-108">Allocateur d’échantillon</span><span class="sxs-lookup"><span data-stu-id="42abc-108">Sample Allocator</span></span>

<span data-ttu-id="42abc-109">Cet attribut peut être défini sur l’allocateur d’échantillon vidéo, dans la méthode [**IMFVideoSampleAllocatorEx :: InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .</span><span class="sxs-lookup"><span data-stu-id="42abc-109">This attribute can be set on the video sample allocator, in the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="42abc-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42abc-110">Requirements</span></span>



| <span data-ttu-id="42abc-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42abc-111">Requirement</span></span> | <span data-ttu-id="42abc-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="42abc-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="42abc-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42abc-113">Minimum supported client</span></span><br/> | <span data-ttu-id="42abc-114">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="42abc-114">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="42abc-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42abc-115">Minimum supported server</span></span><br/> | <span data-ttu-id="42abc-116">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="42abc-116">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="42abc-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="42abc-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="42abc-118"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="42abc-118"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42abc-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42abc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42abc-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="42abc-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="42abc-121">**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**</span><span class="sxs-lookup"><span data-stu-id="42abc-121">**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex)
</dt> <dt>

[<span data-ttu-id="42abc-122">MF \_ sa \_ d3d11 \_ partagée</span><span class="sxs-lookup"><span data-stu-id="42abc-122">MF\_SA\_D3D11\_SHARED</span></span>](mf-sa-d3d11-shared.md)
</dt> </dl>

 

 




