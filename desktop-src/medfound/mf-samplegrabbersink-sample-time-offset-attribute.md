---
description: Décalage entre l’horodatage de chaque échantillon reçu par l’accroche échantillon et l’heure à laquelle l’exemple d’accrochage présente l’exemple.
ms.assetid: 8d06b415-aafc-4276-9a88-4b7262df62f1
title: Attribut MF_SAMPLEGRABBERSINK_SAMPLE_TIME_OFFSET (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d99f65c5023bbe8705e21269dfb07d6f24db4190
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518563"
---
# <a name="mf_samplegrabbersink_sample_time_offset-attribute"></a><span data-ttu-id="b6916-103">Attribut de décalage de l’heure d’exemple MF \_ SAMPLEGRABBERSINK \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="b6916-103">MF\_SAMPLEGRABBERSINK\_SAMPLE\_TIME\_OFFSET attribute</span></span>

<span data-ttu-id="b6916-104">Décalage entre l’horodatage de chaque échantillon reçu par l’accroche échantillon et l’heure à laquelle l’exemple d’accrochage présente l’exemple.</span><span class="sxs-lookup"><span data-stu-id="b6916-104">Offset between the time stamp on each sample received by the sample grabber, and the time when the sample grabber presents the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="b6916-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="b6916-105">Data type</span></span>

<span data-ttu-id="b6916-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="b6916-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="b6916-107">Notes</span><span class="sxs-lookup"><span data-stu-id="b6916-107">Remarks</span></span>

<span data-ttu-id="b6916-108">Vous pouvez définir cet attribut sur l’objet [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) qui est retourné par la fonction [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) .</span><span class="sxs-lookup"><span data-stu-id="b6916-108">You can set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object that is returned by the [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) function.</span></span> <span data-ttu-id="b6916-109">Cet attribut permet à la fonction de rappel de l’exemple de la fonction de rappel de recevoir des exemples antérieurs à l’heure de la présentation.</span><span class="sxs-lookup"><span data-stu-id="b6916-109">This attribute enables the sample grabber's callback function to receive samples earlier than the presentation time.</span></span>

<span data-ttu-id="b6916-110">Lorsque l’exemple d’accrochage reçoit un nouvel échantillon, il présente l’exemple à l’heure *t* − *offset*, où *t* est l’horodatage de l’échantillon et *offset* est la valeur de cet attribut.</span><span class="sxs-lookup"><span data-stu-id="b6916-110">When the sample grabber receives a new sample, it presents the sample at time *t* − *offset*, where *t* is the time stamp on the sample and *offset* is the value of this attribute.</span></span> <span data-ttu-id="b6916-111">Si cet attribut n’est pas défini, la valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="b6916-111">If this attribute is not set, the default value is zero.</span></span>

<span data-ttu-id="b6916-112">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b6916-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6916-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6916-113">Requirements</span></span>



| <span data-ttu-id="b6916-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6916-114">Requirement</span></span> | <span data-ttu-id="b6916-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6916-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b6916-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6916-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b6916-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6916-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b6916-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6916-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b6916-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6916-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b6916-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6916-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6916-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6916-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6916-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6916-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6916-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b6916-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b6916-124">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="b6916-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="b6916-125">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="b6916-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="b6916-126">**IMFSampleGrabberSinkCallback**</span><span class="sxs-lookup"><span data-stu-id="b6916-126">**IMFSampleGrabberSinkCallback**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback)
</dt> <dt>

[<span data-ttu-id="b6916-127">Attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b6916-127">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




