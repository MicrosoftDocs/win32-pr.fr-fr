---
description: Définit le nombre maximal d’échantillons non traités qui peuvent être mis en mémoire tampon pour traitement dans le chemin d’accès audio du récepteur d’enregistrements.
ms.assetid: C959ED58-77EB-47EC-8D5D-BBFA9342295D
title: Attribut MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_UNPROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 442e9b5eca3354e87b8e36b55a3c6cb92ec6f131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318809"
---
# <a name="mf_capture_engine_record_sink_audio_max_unprocessed_samples-attribute"></a><span data-ttu-id="efb35-103">Attribut d’échantillonnage du moteur de capture MF- \_ \_ \_ \_ \_ \_ nombre maximal d' \_ échantillons non traités \_</span><span class="sxs-lookup"><span data-stu-id="efb35-103">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_AUDIO\_MAX\_UNPROCESSED\_SAMPLES attribute</span></span>

<span data-ttu-id="efb35-104">Définit le nombre maximal d’échantillons non traités qui peuvent être mis en mémoire tampon pour traitement dans le chemin d’accès audio du récepteur d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="efb35-104">Sets the maximum number of unprocessed samples that can be buffered for processing in the record sink audio path.</span></span>

## <a name="data-type"></a><span data-ttu-id="efb35-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="efb35-105">Data type</span></span>

<span data-ttu-id="efb35-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="efb35-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="efb35-107">Notes</span><span class="sxs-lookup"><span data-stu-id="efb35-107">Remarks</span></span>

<span data-ttu-id="efb35-108">Pour configurer cet attribut sur le moteur de capture, ajoutez-le au paramètre *pAttributes* lorsque vous appelez [**IMFCaptureEngine :: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span><span class="sxs-lookup"><span data-stu-id="efb35-108">To configure this attribute on the capture engine, add it to the *pAttributes* parameter when you call [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span></span>

<span data-ttu-id="efb35-109">La valeur maximale de cet attribut est 100.</span><span class="sxs-lookup"><span data-stu-id="efb35-109">The maximum value for this attribute is 100.</span></span>

<span data-ttu-id="efb35-110">Une fois que l’enregistrement a mis en mémoire tampon le nombre maximal d’échantillons non traités, spécifié par les échantillons du moteur de capture MF nombre maximal d’échantillons non \_ \_ \_ \_ \_ \_ \_ traités \_ , il supprime la fréquence d’images en supprimant des échantillons.</span><span class="sxs-lookup"><span data-stu-id="efb35-110">Once the record has buffered the maximum number of unprocessed samples, specified by MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_AUDIO\_MAX\_UNPROCESSED\_SAMPLES, it drops the frame rate by dropping samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="efb35-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="efb35-111">Requirements</span></span>



| <span data-ttu-id="efb35-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="efb35-112">Requirement</span></span> | <span data-ttu-id="efb35-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="efb35-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="efb35-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="efb35-114">Minimum supported client</span></span><br/> | <span data-ttu-id="efb35-115">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="efb35-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="efb35-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="efb35-116">Minimum supported server</span></span><br/> | <span data-ttu-id="efb35-117">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="efb35-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="efb35-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="efb35-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="efb35-119"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="efb35-119"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efb35-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efb35-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efb35-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="efb35-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="efb35-122">Attributs du moteur de capture</span><span class="sxs-lookup"><span data-stu-id="efb35-122">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="efb35-123">**IMFCaptureEngine :: Initialize**</span><span class="sxs-lookup"><span data-stu-id="efb35-123">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




