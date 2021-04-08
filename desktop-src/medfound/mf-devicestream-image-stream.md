---
description: Spécifie si un flux sur une source de capture vidéo est un flux d’image continue.
ms.assetid: 52251A45-3603-41C7-A869-7F6319BD337F
title: Attribut MF_DEVICESTREAM_IMAGE_STREAM (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 382ce587574d6ec46509a460dfb964e23dd416d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752445"
---
# <a name="mf_devicestream_image_stream-attribute"></a><span data-ttu-id="e8084-103">\_Attribut de \_ flux d’image MF DEVICESTREAM \_</span><span class="sxs-lookup"><span data-stu-id="e8084-103">MF\_DEVICESTREAM\_IMAGE\_STREAM attribute</span></span>

<span data-ttu-id="e8084-104">Spécifie si un flux sur une source de capture vidéo est un flux d’image continue.</span><span class="sxs-lookup"><span data-stu-id="e8084-104">Specifies whether a stream on a video capture source is a still-image stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="e8084-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="e8084-105">Data type</span></span>

<span data-ttu-id="e8084-106">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e8084-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e8084-107">Notes</span><span class="sxs-lookup"><span data-stu-id="e8084-107">Remarks</span></span>

<span data-ttu-id="e8084-108">Certaines caméras vidéo exposent un flux d’image continue qui produit des images haute résolution.</span><span class="sxs-lookup"><span data-stu-id="e8084-108">Some video cameras expose a still-image stream that produces high-resolution images.</span></span> <span data-ttu-id="e8084-109">Le flux d’image peut produire des images non compressées ou des images JPEG.</span><span class="sxs-lookup"><span data-stu-id="e8084-109">The image stream might produce uncompressed images or JPEG images.</span></span> <span data-ttu-id="e8084-110">Si la caméra a un flux d’image, la source du média pour l’appareil de capture affecte la **valeur true** à cet attribut sur le flux de l’image.</span><span class="sxs-lookup"><span data-stu-id="e8084-110">If the camera has an image stream, the media source for the capture device sets this attribute to **TRUE** on the image stream.</span></span>

<span data-ttu-id="e8084-111">Pour accéder à cet attribut, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="e8084-111">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="e8084-112">Interrogez la source du média pour l’interface [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .</span><span class="sxs-lookup"><span data-stu-id="e8084-112">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="e8084-113">Appelez [**IMFMediaSourceEx :: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) pour obtenir un pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pour le flux.</span><span class="sxs-lookup"><span data-stu-id="e8084-113">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="e8084-114">Appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) pour accéder à l’attribut.</span><span class="sxs-lookup"><span data-stu-id="e8084-114">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8084-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8084-115">Requirements</span></span>



| <span data-ttu-id="e8084-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8084-116">Requirement</span></span> | <span data-ttu-id="e8084-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8084-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e8084-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8084-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e8084-119">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e8084-119">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e8084-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8084-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e8084-121">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e8084-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e8084-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="e8084-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8084-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8084-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8084-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8084-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8084-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e8084-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




