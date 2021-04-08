---
description: Définit le nombre maximal d’exemples traités qui peuvent être mis en mémoire tampon dans le chemin d’accès vidéo du récepteur d’enregistrements.
ms.assetid: 5AFA197E-5A7F-402E-A62B-4F624A5DD917
title: Attribut MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_PROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70c3840f449cebb6579b2c1df5f330379ba30655
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752453"
---
# <a name="mf_capture_engine_record_sink_video_max_processed_samples-attribute"></a><span data-ttu-id="cba5c-103">Attribut du récepteur d’enregistrements du moteur de capture MF- \_ \_ \_ \_ \_ \_ nombre maximal d' \_ \_ échantillons traités</span><span class="sxs-lookup"><span data-stu-id="cba5c-103">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_VIDEO\_MAX\_PROCESSED\_SAMPLES attribute</span></span>

<span data-ttu-id="cba5c-104">Définit le nombre maximal d’exemples traités qui peuvent être mis en mémoire tampon dans le chemin d’accès vidéo du récepteur d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="cba5c-104">Sets the maximum number of processed samples that can be buffered in the record sink video path.</span></span>

## <a name="data-type"></a><span data-ttu-id="cba5c-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="cba5c-105">Data type</span></span>

<span data-ttu-id="cba5c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="cba5c-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="cba5c-107">Notes</span><span class="sxs-lookup"><span data-stu-id="cba5c-107">Remarks</span></span>

<span data-ttu-id="cba5c-108">Pour configurer cet attribut sur le moteur de capture, ajoutez-le au paramètre *pAttributes* lorsque vous appelez [**IMFCaptureEngine :: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span><span class="sxs-lookup"><span data-stu-id="cba5c-108">To configure this attribute on the capture engine, add it to the *pAttributes* parameter when you call [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span></span>

<span data-ttu-id="cba5c-109">La valeur maximale de cet attribut est 17.</span><span class="sxs-lookup"><span data-stu-id="cba5c-109">The maximum value for this attribute is 17.</span></span>

## <a name="requirements"></a><span data-ttu-id="cba5c-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cba5c-110">Requirements</span></span>



| <span data-ttu-id="cba5c-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cba5c-111">Requirement</span></span> | <span data-ttu-id="cba5c-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="cba5c-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cba5c-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cba5c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="cba5c-114">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cba5c-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="cba5c-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cba5c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="cba5c-116">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cba5c-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cba5c-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="cba5c-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="cba5c-118"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="cba5c-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cba5c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cba5c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cba5c-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cba5c-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cba5c-121">Attributs du moteur de capture</span><span class="sxs-lookup"><span data-stu-id="cba5c-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="cba5c-122">**IMFCaptureEngine :: Initialize**</span><span class="sxs-lookup"><span data-stu-id="cba5c-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




