---
description: Indique à l’allocateur d’échantillon vidéo de créer des textures pouvant être partagées à l’aide de clé-mutex.
ms.assetid: 798CA474-3B1A-4795-81B7-563749197104
title: Attribut MF_SA_D3D11_SHARED (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff6ecb23a99a732e183bc16942e33bbb4f8e3a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203107"
---
# <a name="mf_sa_d3d11_shared-attribute"></a><span data-ttu-id="7fd8c-103">\_ \_ Attribut partagé d3d11 MF sa \_</span><span class="sxs-lookup"><span data-stu-id="7fd8c-103">MF\_SA\_D3D11\_SHARED attribute</span></span>

<span data-ttu-id="7fd8c-104">Indique à l’allocateur d’échantillon vidéo de créer des textures pouvant être partagées à l’aide de clé-mutex.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-104">Indicates to the video sample allocator to create textures as shareable using keyed-mutex.</span></span>

## <a name="data-type"></a><span data-ttu-id="7fd8c-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="7fd8c-105">Data type</span></span>

<span data-ttu-id="7fd8c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7fd8c-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="7fd8c-107">Notes</span><span class="sxs-lookup"><span data-stu-id="7fd8c-107">Remarks</span></span>

### <a name="sample-allocator"></a><span data-ttu-id="7fd8c-108">Allocateur d’échantillon</span><span class="sxs-lookup"><span data-stu-id="7fd8c-108">Sample Allocator</span></span>

<span data-ttu-id="7fd8c-109">Cet attribut peut être défini sur l’allocateur d’échantillon vidéo, dans la méthode [**IMFVideoSampleAllocatorEx :: InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .</span><span class="sxs-lookup"><span data-stu-id="7fd8c-109">This attribute can be set on the video sample allocator, in the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fd8c-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7fd8c-110">Requirements</span></span>



| <span data-ttu-id="7fd8c-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7fd8c-111">Requirement</span></span> | <span data-ttu-id="7fd8c-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="7fd8c-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fd8c-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fd8c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="7fd8c-114">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7fd8c-114">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="7fd8c-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fd8c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="7fd8c-116">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="7fd8c-116">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="7fd8c-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="7fd8c-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fd8c-118"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fd8c-118"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fd8c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fd8c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fd8c-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7fd8c-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7fd8c-121">**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**</span><span class="sxs-lookup"><span data-stu-id="7fd8c-121">**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex)
</dt> <dt>

[<span data-ttu-id="7fd8c-122">MF \_ sa \_ d3d11 \_ partagée \_ sans \_ MUTEX</span><span class="sxs-lookup"><span data-stu-id="7fd8c-122">MF\_SA\_D3D11\_SHARED\_WITHOUT\_MUTEX</span></span>](mf-sa-d3d11-shared-without-mutex.md)
</dt> </dl>

 

 




