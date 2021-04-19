---
description: Indique le nombre de mémoires tampons non compressées que le récepteur multimédia EVR (Enhanced Video Renderer) requiert pour l’entrelacement.
ms.assetid: b62bff64-153f-4028-a546-250419dc4152
title: Attribut MF_SA_REQUIRED_SAMPLE_COUNT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe7d47370cd4877a0f9722d443bc6bb3f7bdeb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528191"
---
# <a name="mf_sa_required_sample_count-attribute"></a><span data-ttu-id="1ce9e-103">\_Attribut de \_ \_ nombre d’exemples requis MF sa \_</span><span class="sxs-lookup"><span data-stu-id="1ce9e-103">MF\_SA\_REQUIRED\_SAMPLE\_COUNT attribute</span></span>

<span data-ttu-id="1ce9e-104">Indique le nombre de mémoires tampons non compressées que le récepteur multimédia EVR (Enhanced Video Renderer) requiert pour l’entrelacement.</span><span class="sxs-lookup"><span data-stu-id="1ce9e-104">Indicates the number of uncompressed buffers that the enhanced video renderer (EVR) media sink requires for deinterlacing.</span></span>

## <a name="data-type"></a><span data-ttu-id="1ce9e-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="1ce9e-105">Data type</span></span>

<span data-ttu-id="1ce9e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1ce9e-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="1ce9e-107">Notes</span><span class="sxs-lookup"><span data-stu-id="1ce9e-107">Remarks</span></span>

<span data-ttu-id="1ce9e-108">Il s’agit d’un attribut de niveau flux.</span><span class="sxs-lookup"><span data-stu-id="1ce9e-108">This is a stream-level attribute.</span></span> <span data-ttu-id="1ce9e-109">Pour récupérer l’attribut à partir du EVR, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="1ce9e-109">To get the attribute from the EVR, do the following:</span></span>

1.  <span data-ttu-id="1ce9e-110">Appelez [**IMFMediaSink :: GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) pour accéder au récepteur de flux.</span><span class="sxs-lookup"><span data-stu-id="1ce9e-110">Call [**IMFMediaSink::GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) to get the stream sink.</span></span>
2.  <span data-ttu-id="1ce9e-111">Interrogez le récepteur de flux pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="1ce9e-111">Query the stream sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>
3.  <span data-ttu-id="1ce9e-112">Appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="1ce9e-112">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="1ce9e-113">En interne, le mélangeur fournit cet attribut au EVR.</span><span class="sxs-lookup"><span data-stu-id="1ce9e-113">Internally, the mixer provides this attribute to the EVR.</span></span> <span data-ttu-id="1ce9e-114">Pour récupérer l’attribut à partir du mélangeur, appelez [**IMFTransform :: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes).</span><span class="sxs-lookup"><span data-stu-id="1ce9e-114">To get the attribute from the mixer, call [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes).</span></span>

<span data-ttu-id="1ce9e-115">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="1ce9e-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ce9e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ce9e-116">Requirements</span></span>



| <span data-ttu-id="1ce9e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ce9e-117">Requirement</span></span> | <span data-ttu-id="1ce9e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ce9e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ce9e-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ce9e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1ce9e-120">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="1ce9e-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                    |
| <span data-ttu-id="1ce9e-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ce9e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1ce9e-122">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="1ce9e-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="1ce9e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="1ce9e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ce9e-124"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ce9e-124"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ce9e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ce9e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ce9e-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1ce9e-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1ce9e-127">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="1ce9e-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="1ce9e-128">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="1ce9e-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="1ce9e-129">Attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1ce9e-129">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




