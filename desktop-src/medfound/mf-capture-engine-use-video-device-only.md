---
description: Spécifie si le moteur de capture capture la vidéo mais pas l’audio.
ms.assetid: B0B7A7F2-02F9-46A6-954F-D6E9C3B73A29
title: Attribut MF_CAPTURE_ENGINE_USE_VIDEO_DEVICE_ONLY (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b687bfa7ec2f30f296dd83997f3e64ac4198fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951544"
---
# <a name="mf_capture_engine_use_video_device_only-attribute"></a><span data-ttu-id="dc156-103">\_ \_ \_ \_ Attribut appareil vidéo utiliser le moteur de capture MF \_ \_ uniquement</span><span class="sxs-lookup"><span data-stu-id="dc156-103">MF\_CAPTURE\_ENGINE\_USE\_VIDEO\_DEVICE\_ONLY attribute</span></span>

<span data-ttu-id="dc156-104">Spécifie si le moteur de capture capture la vidéo mais pas l’audio.</span><span class="sxs-lookup"><span data-stu-id="dc156-104">Specifies whether the capture engine captures video but not audio.</span></span>

## <a name="data-type"></a><span data-ttu-id="dc156-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="dc156-105">Data type</span></span>

<span data-ttu-id="dc156-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="dc156-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="dc156-107">Notes</span><span class="sxs-lookup"><span data-stu-id="dc156-107">Remarks</span></span>

<span data-ttu-id="dc156-108">Si cet attribut a la **valeur true**, le moteur de capture ne sélectionne pas ou n’utilise pas de périphérique de capture audio.</span><span class="sxs-lookup"><span data-stu-id="dc156-108">If this attribute is **TRUE**, the capture engine does not select or use an audio capture device.</span></span> <span data-ttu-id="dc156-109">Affectez la **valeur true** à cet attribut si vous souhaitez capturer une vidéo sans audio.</span><span class="sxs-lookup"><span data-stu-id="dc156-109">Set this attribute to **TRUE** if you want to capture video without audio.</span></span> <span data-ttu-id="dc156-110">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="dc156-110">The default value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc156-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc156-111">Requirements</span></span>



| <span data-ttu-id="dc156-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc156-112">Requirement</span></span> | <span data-ttu-id="dc156-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc156-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc156-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc156-114">Minimum supported client</span></span><br/> | <span data-ttu-id="dc156-115">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc156-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="dc156-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc156-116">Minimum supported server</span></span><br/> | <span data-ttu-id="dc156-117">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc156-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dc156-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc156-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc156-119"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc156-119"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc156-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc156-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc156-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dc156-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="dc156-122">Attributs du moteur de capture</span><span class="sxs-lookup"><span data-stu-id="dc156-122">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="dc156-123">**IMFCaptureEngine :: Initialize**</span><span class="sxs-lookup"><span data-stu-id="dc156-123">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




