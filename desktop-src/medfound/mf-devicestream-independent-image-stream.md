---
description: Spécifie si le flux d’image sur une source de capture vidéo est indépendant du flux vidéo.
ms.assetid: DC4ED612-593B-40BF-BB42-946149042D1F
title: Attribut MF_DEVICESTREAM_INDEPENDENT_IMAGE_STREAM (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 174e62a1bdd178ad2d8dce7fab5bf9ce3104d834
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533621"
---
# <a name="mf_devicestream_independent_image_stream-attribute"></a><span data-ttu-id="e3ea5-103">\_Attribut de \_ \_ flux d’image indépendant DEVICESTREAM MF \_</span><span class="sxs-lookup"><span data-stu-id="e3ea5-103">MF\_DEVICESTREAM\_INDEPENDENT\_IMAGE\_STREAM attribute</span></span>

<span data-ttu-id="e3ea5-104">Spécifie si le flux d’image sur une source de capture vidéo est indépendant du flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="e3ea5-104">Specifies whether the image stream on a video capture source is independent of the video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="e3ea5-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="e3ea5-105">Data type</span></span>

<span data-ttu-id="e3ea5-106">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e3ea5-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e3ea5-107">Notes</span><span class="sxs-lookup"><span data-stu-id="e3ea5-107">Remarks</span></span>

<span data-ttu-id="e3ea5-108">Certaines caméras vidéo USB exposent un flux qui produit des images fixes.</span><span class="sxs-lookup"><span data-stu-id="e3ea5-108">Some USB video cameras expose a stream that produces still images.</span></span> <span data-ttu-id="e3ea5-109">Dans certains appareils photo, le flux d’image retourne simplement le frame suivant à partir du flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="e3ea5-109">In some cameras, the image stream simply returns the next frame from the video stream.</span></span> <span data-ttu-id="e3ea5-110">Dans d’autres caméras, le flux d’image fonctionne indépendamment du flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="e3ea5-110">In other cameras, the image stream functions independently of the video stream.</span></span> <span data-ttu-id="e3ea5-111">Si l’appareil photo possède un flux d’image indépendant, la source du média pour l’appareil de capture affecte la **valeur true** à cet attribut sur le flux de l’image.</span><span class="sxs-lookup"><span data-stu-id="e3ea5-111">If the camera has an independent image stream, the media source for the capture device sets this attribute to **TRUE** on the image stream.</span></span>

<span data-ttu-id="e3ea5-112">Pour accéder à cet attribut, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="e3ea5-112">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="e3ea5-113">Interrogez la source du média pour l’interface [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .</span><span class="sxs-lookup"><span data-stu-id="e3ea5-113">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="e3ea5-114">Appelez [**IMFMediaSourceEx :: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) pour obtenir un pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pour le flux.</span><span class="sxs-lookup"><span data-stu-id="e3ea5-114">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="e3ea5-115">Appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) pour accéder à l’attribut.</span><span class="sxs-lookup"><span data-stu-id="e3ea5-115">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute.</span></span>

<span data-ttu-id="e3ea5-116">Cet attribut s’applique uniquement lorsque l’attribut de [ \_ \_ \_ flux d’image DEVICESTREAM MF](mf-devicestream-image-stream.md) a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="e3ea5-116">This attribute applies only when the [MF\_DEVICESTREAM\_IMAGE\_STREAM](mf-devicestream-image-stream.md) attribute is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3ea5-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3ea5-117">Requirements</span></span>



| <span data-ttu-id="e3ea5-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3ea5-118">Requirement</span></span> | <span data-ttu-id="e3ea5-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3ea5-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e3ea5-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3ea5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e3ea5-121">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3ea5-121">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e3ea5-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3ea5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e3ea5-123">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3ea5-123">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e3ea5-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="e3ea5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3ea5-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3ea5-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3ea5-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3ea5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3ea5-127">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e3ea5-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




