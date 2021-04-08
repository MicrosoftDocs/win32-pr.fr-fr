---
description: Spécifie le nombre de mémoires tampons créées par l’allocateur d’échantillon vidéo pour chaque échantillon vidéo.
ms.assetid: A782BF8A-822A-407D-A30A-F2045BBB0BC0
title: Attribut MF_SA_BUFFERS_PER_SAMPLE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d658ae72c53d986b364b2b6a3f405ae0052ea3fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753173"
---
# <a name="mf_sa_buffers_per_sample-attribute"></a><span data-ttu-id="67c57-103">\_Tampons sa de l' \_ exemple MF \_ par \_ attribut</span><span class="sxs-lookup"><span data-stu-id="67c57-103">MF\_SA\_BUFFERS\_PER\_SAMPLE attribute</span></span>

<span data-ttu-id="67c57-104">Spécifie le nombre de mémoires tampons créées par l’allocateur d’échantillon vidéo pour chaque échantillon vidéo.</span><span class="sxs-lookup"><span data-stu-id="67c57-104">Specifies how many buffers the video-sample allocator creates for each video sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="67c57-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="67c57-105">Data type</span></span>

<span data-ttu-id="67c57-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="67c57-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="67c57-107">Notes</span><span class="sxs-lookup"><span data-stu-id="67c57-107">Remarks</span></span>

<span data-ttu-id="67c57-108">Si vous utilisez l’interface [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) pour allouer des exemples vidéo, vous pouvez utiliser cet attribut pour créer des exemples vidéo qui contiennent plusieurs mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="67c57-108">If you use the [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) interface to allocate video samples, you can use this attribute to create video samples that contain multiple buffers.</span></span> <span data-ttu-id="67c57-109">Par exemple, si la valeur de l’attribut est 2, l’allocateur crée deux mémoires tampons vidéo pour chaque échantillon vidéo.</span><span class="sxs-lookup"><span data-stu-id="67c57-109">For example, if the attribute value is 2, the allocator creates two video buffers for each video sample.</span></span> <span data-ttu-id="67c57-110">Définissez l’attribut dans le paramètre *pAttributes* de la méthode [**IMFVideoSampleAllocatorEx :: InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .</span><span class="sxs-lookup"><span data-stu-id="67c57-110">Set the attribute in the *pAttributes* parameter of the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

<span data-ttu-id="67c57-111">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="67c57-111">The default value is 1.</span></span> <span data-ttu-id="67c57-112">Si l’attribut n’est pas défini, l’allocateur crée des exemples vidéo qui contiennent une seule mémoire tampon par échantillon.</span><span class="sxs-lookup"><span data-stu-id="67c57-112">If the attribute is not set, the allocator creates video samples that contain a single buffer per sample.</span></span>

<span data-ttu-id="67c57-113">Cet attribut est principalement destiné aux transformations Media Foundation (MFTs) qui prennent en charge la sortie stéréo 3D, dans la situation suivante :</span><span class="sxs-lookup"><span data-stu-id="67c57-113">This attribute is primarily intended for Media Foundation transforms (MFTs) that support stereo 3D output, in the following situation:</span></span>

-   <span data-ttu-id="67c57-114">La table MFT prend en charge Microsoft DirectX Graphics infrastructure (DXGI).</span><span class="sxs-lookup"><span data-stu-id="67c57-114">The MFT supports Microsoft DirectX Graphics Infrastructure (DXGI).</span></span>
-   <span data-ttu-id="67c57-115">La table MFT alloue ses propres exemples de sortie.</span><span class="sxs-lookup"><span data-stu-id="67c57-115">The MFT allocates its own output samples.</span></span>
-   <span data-ttu-id="67c57-116">La table MFT utilise l’interface [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) pour allouer les exemples de sortie.</span><span class="sxs-lookup"><span data-stu-id="67c57-116">The MFT uses the [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) interface to allocate the output samples.</span></span>
-   <span data-ttu-id="67c57-117">Le format vidéo 3D utilise une mémoire tampon distincte pour chaque vue.</span><span class="sxs-lookup"><span data-stu-id="67c57-117">The 3D video format uses a separate buffer for each view.</span></span>

<span data-ttu-id="67c57-118">Si tous ces critères sont vrais, la table MFT doit définir la valeur de l’attribut sur 2 (une mémoire tampon par vue).</span><span class="sxs-lookup"><span data-stu-id="67c57-118">If all of these criteria are true, the MFT should set the attribute value to 2 (one buffer per view).</span></span>

## <a name="requirements"></a><span data-ttu-id="67c57-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67c57-119">Requirements</span></span>



| <span data-ttu-id="67c57-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67c57-120">Requirement</span></span> | <span data-ttu-id="67c57-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="67c57-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="67c57-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67c57-122">Minimum supported client</span></span><br/> | <span data-ttu-id="67c57-123">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="67c57-123">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="67c57-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67c57-124">Minimum supported server</span></span><br/> | <span data-ttu-id="67c57-125">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="67c57-125">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="67c57-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="67c57-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="67c57-127"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="67c57-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67c57-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67c57-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67c57-129">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="67c57-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




