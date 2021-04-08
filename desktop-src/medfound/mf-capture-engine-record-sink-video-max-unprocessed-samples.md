---
description: Définit le nombre maximal d’échantillons non traités qui peuvent être mis en mémoire tampon pour traitement dans le chemin d’accès vidéo du récepteur d’enregistrements.
ms.assetid: B3B5C547-1F06-45B1-BFCB-513AD7B6A9B6
title: Attribut MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_UNPROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5f5e297ddb5f06e71fe05a95df73aa205a7889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863594"
---
# <a name="mf_capture_engine_record_sink_video_max_unprocessed_samples-attribute"></a><span data-ttu-id="79603-103">Vidéo du récepteur d’enregistrements du moteur de capture MF- \_ \_ \_ \_ \_ \_ nombre maximal d' \_ échantillons non traités \_</span><span class="sxs-lookup"><span data-stu-id="79603-103">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_VIDEO\_MAX\_UNPROCESSED\_SAMPLES attribute</span></span>

<span data-ttu-id="79603-104">Définit le nombre maximal d’échantillons non traités qui peuvent être mis en mémoire tampon pour traitement dans le chemin d’accès vidéo du récepteur d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="79603-104">Sets the maximum number of unprocessed samples that can be buffered for processing in the record sink video path.</span></span>

## <a name="data-type"></a><span data-ttu-id="79603-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="79603-105">Data type</span></span>

<span data-ttu-id="79603-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="79603-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="79603-107">Notes</span><span class="sxs-lookup"><span data-stu-id="79603-107">Remarks</span></span>

<span data-ttu-id="79603-108">Pour configurer cet attribut sur le moteur de capture, ajoutez-le au paramètre *pAttributes* lorsque vous appelez [**IMFCaptureEngine :: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span><span class="sxs-lookup"><span data-stu-id="79603-108">To configure this attribute on the capture engine, add it to the *pAttributes* parameter when you call [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span></span>

<span data-ttu-id="79603-109">La valeur maximale de cet attribut est 17.</span><span class="sxs-lookup"><span data-stu-id="79603-109">The maximum value for this attribute is 17.</span></span>

<span data-ttu-id="79603-110">Une fois que l’enregistrement a mis en mémoire tampon le nombre maximal d’échantillons non traités, spécifié par le récepteur d’enregistrement du moteur de capture MF, nombre maximal d’échantillons non \_ \_ \_ \_ \_ \_ \_ traités \_ , il supprime la fréquence d’images en supprimant des échantillons.</span><span class="sxs-lookup"><span data-stu-id="79603-110">Once the record has buffered the maximum number of unprocessed samples, specified by MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_VIDEO\_MAX\_UNPROCESSED\_SAMPLES, it drops the frame rate by dropping samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="79603-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79603-111">Requirements</span></span>



| <span data-ttu-id="79603-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79603-112">Requirement</span></span> | <span data-ttu-id="79603-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="79603-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="79603-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79603-114">Minimum supported client</span></span><br/> | <span data-ttu-id="79603-115">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79603-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="79603-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79603-116">Minimum supported server</span></span><br/> | <span data-ttu-id="79603-117">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79603-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="79603-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="79603-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="79603-119"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="79603-119"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79603-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79603-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79603-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="79603-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="79603-122">Attributs du moteur de capture</span><span class="sxs-lookup"><span data-stu-id="79603-122">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="79603-123">**IMFCaptureEngine :: Initialize**</span><span class="sxs-lookup"><span data-stu-id="79603-123">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




