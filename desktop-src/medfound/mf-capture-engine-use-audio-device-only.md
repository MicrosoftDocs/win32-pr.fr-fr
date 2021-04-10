---
description: Spécifie si le moteur de capture capture l’audio mais pas la vidéo.
ms.assetid: 0A905D55-CEE5-44FC-97A5-9474872D5724
title: Attribut MF_CAPTURE_ENGINE_USE_AUDIO_DEVICE_ONLY (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f02e0b8f1002bcfff12f8a2bea93612456b6072
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951298"
---
# <a name="mf_capture_engine_use_audio_device_only-attribute"></a><span data-ttu-id="39b81-103">\_ \_ \_ \_ \_ Attribut appareil audio \_ de l’utilisation du moteur de capture MF uniquement</span><span class="sxs-lookup"><span data-stu-id="39b81-103">MF\_CAPTURE\_ENGINE\_USE\_AUDIO\_DEVICE\_ONLY attribute</span></span>

<span data-ttu-id="39b81-104">Spécifie si le moteur de capture capture l’audio mais pas la vidéo.</span><span class="sxs-lookup"><span data-stu-id="39b81-104">Specifies whether the capture engine captures audio but not video.</span></span>

## <a name="data-type"></a><span data-ttu-id="39b81-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="39b81-105">Data type</span></span>

<span data-ttu-id="39b81-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="39b81-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="39b81-107">Notes</span><span class="sxs-lookup"><span data-stu-id="39b81-107">Remarks</span></span>

<span data-ttu-id="39b81-108">Si cet attribut a la **valeur true**, le moteur de capture ne sélectionne pas ou n’utilise pas d’appareil de capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="39b81-108">If this attribute is **TRUE**, the capture engine does not select or use a video capture device.</span></span> <span data-ttu-id="39b81-109">Affectez la **valeur true** à cet attribut si vous souhaitez capturer du son sans vidéo.</span><span class="sxs-lookup"><span data-stu-id="39b81-109">Set this attribute to **TRUE** if you want to capture audio without video.</span></span> <span data-ttu-id="39b81-110">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="39b81-110">The default value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="39b81-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39b81-111">Requirements</span></span>



| <span data-ttu-id="39b81-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39b81-112">Requirement</span></span> | <span data-ttu-id="39b81-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="39b81-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="39b81-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39b81-114">Minimum supported client</span></span><br/> | <span data-ttu-id="39b81-115">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39b81-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="39b81-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39b81-116">Minimum supported server</span></span><br/> | <span data-ttu-id="39b81-117">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39b81-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="39b81-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="39b81-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="39b81-119"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="39b81-119"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39b81-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39b81-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39b81-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="39b81-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="39b81-122">Attributs du moteur de capture</span><span class="sxs-lookup"><span data-stu-id="39b81-122">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="39b81-123">**IMFCaptureEngine :: Initialize**</span><span class="sxs-lookup"><span data-stu-id="39b81-123">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




