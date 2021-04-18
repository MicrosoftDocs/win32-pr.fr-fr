---
description: Les constantes de type de média sont définies ci-dessous.
ms.assetid: 3e418c9a-a008-4b94-b5d2-7c2eccb3bf87
title: Constantes TAPIMEDIATYPE_ (Tapi3. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d71a7d7ffb411d84e99863bb89274e43200b319d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533427"
---
# <a name="tapimediatype_-constants"></a><span data-ttu-id="0278c-103">\_Constantes TAPIMEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="0278c-103">TAPIMEDIATYPE\_ Constants</span></span>

<span data-ttu-id="0278c-104">Les types de média suivants sont définis :</span><span class="sxs-lookup"><span data-stu-id="0278c-104">The following media types are defined:</span></span>



| <span data-ttu-id="0278c-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="0278c-105">Constant/value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="0278c-106">Description</span><span class="sxs-lookup"><span data-stu-id="0278c-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TAPIMEDIATYPE_AUDIO"></span><span id="tapimediatype_audio"></span><dl> <span data-ttu-id="0278c-107"><dt>**TAPIMEDIATYPE \_ AUDIO**</dt> <dt>0x8</dt></span><span class="sxs-lookup"><span data-stu-id="0278c-107"><dt>**TAPIMEDIATYPE\_AUDIO**</dt> <dt>0x8</dt></span></span> </dl>                    | <span data-ttu-id="0278c-108">Flux multimédia audio qui entre ou quitte l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0278c-108">An audio media stream that is entering or leaving the computer.</span></span> <span data-ttu-id="0278c-109">Une entrée de flux multimédia est généralement lue sur les intervenants, ou envoyée à un appareil combiné et un flux de sortie est généralement capturé via un microphone ou un appareil combiné.</span><span class="sxs-lookup"><span data-stu-id="0278c-109">An entering media stream would typically be played on speakers, or sent to a handset device and a leaving stream would typically be captured through a microphone or handset device.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="TAPIMEDIATYPE_VIDEO"></span><span id="tapimediatype_video"></span><dl> <span data-ttu-id="0278c-110"><dt>**TAPIMEDIATYPE \_ VIDÉO**</dt> <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="0278c-110"><dt>**TAPIMEDIATYPE\_VIDEO**</dt> <dt>0x8000</dt></span></span> </dl>                 | <span data-ttu-id="0278c-111">Flux de média vidéo qui entre ou quitte l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0278c-111">A video media stream that is entering or leaving the computer.</span></span> <span data-ttu-id="0278c-112">Une entrée de flux multimédia est généralement rendue dans une fenêtre vidéo et un flux multimédia de sortie est généralement capturé avec une caméra vidéo.</span><span class="sxs-lookup"><span data-stu-id="0278c-112">An entering media stream would typically be rendered in a video window and a leaving media stream would typically be captured with a video camera.</span></span><br/>                                                                                                                                                                                                                                                                         |
| <span id="TAPIMEDIATYPE_DATAMODEM"></span><span id="tapimediatype_datamodem"></span><dl> <span data-ttu-id="0278c-113"><dt>**TAPIMEDIATYPE \_ DATAMODEM**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="0278c-113"><dt>**TAPIMEDIATYPE\_DATAMODEM**</dt> <dt>0x10</dt></span></span> </dl>       | <span data-ttu-id="0278c-114">Flux de données multimédia qui est associé à un modem de données.</span><span class="sxs-lookup"><span data-stu-id="0278c-114">A data media stream that is associated with a data modem.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="TAPIMEDIATYPE_G3FAX"></span><span id="tapimediatype_g3fax"></span><dl> <span data-ttu-id="0278c-115"><dt>**TAPIMEDIATYPE \_ G3FAX**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="0278c-115"><dt>**TAPIMEDIATYPE\_G3FAX**</dt> <dt>0x20</dt></span></span> </dl>                   | <span data-ttu-id="0278c-116">Flux de données multimédia associé à une télécopie de protocole G3.</span><span class="sxs-lookup"><span data-stu-id="0278c-116">A data media stream that is associated with a G3 protocol fax.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="TAPIMEDIATYPE_MULTITRACK"></span><span id="tapimediatype_multitrack"></span><dl> <span data-ttu-id="0278c-117"><dt>**TAPIMEDIATYPE \_**</dt> <dt>0x10000</dt> multipiste</span><span class="sxs-lookup"><span data-stu-id="0278c-117"><dt>**TAPIMEDIATYPE\_MULTITRACK**</dt> <dt>0x10000</dt></span></span> </dl> | <span data-ttu-id="0278c-118">Un flux se trouve sur un terminal multipiste.</span><span class="sxs-lookup"><span data-stu-id="0278c-118">A stream is on a multitrack terminal.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="MEDIATYPE_RTP_Single_Stream"></span><span id="mediatype_rtp_single_stream"></span><span id="MEDIATYPE_RTP_SINGLE_STREAM"></span><dl> <span data-ttu-id="0278c-119"><dt>**\_ \_ Flux unique de MediaType RTP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0278c-119"><dt>**MEDIATYPE\_RTP\_Single\_Stream**</dt></span></span> </dl>     | <span data-ttu-id="0278c-120">Ce GUID est utilisé entre un terminal fourni par une application et le flux du MSP.</span><span class="sxs-lookup"><span data-stu-id="0278c-120">This GUID is used between an application supplied terminal and the MSP's stream.</span></span> <span data-ttu-id="0278c-121">Si le code pin du terminal prend en charge ce type de média, le flux échangera des données RTP brutes avec le terminal.</span><span class="sxs-lookup"><span data-stu-id="0278c-121">If the pin of the terminal supports this media type, the stream will exchange raw RTP data with the terminal.</span></span> <span data-ttu-id="0278c-122">Ce mode est pris en charge uniquement par les flux vidéo sur le MSP H323 et IPConf MSP pour Windows 2000 SP1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="0278c-122">This mode is supported only by the video streams on the H323 MSP and IPConf MSP for Windows 2000 SP1 or above.</span></span><br/> <span data-ttu-id="0278c-123">**En-tête :** Déclaré dans ipmsp. h.</span><span class="sxs-lookup"><span data-stu-id="0278c-123">**Header:** Declared in ipmsp.h.</span></span> <span data-ttu-id="0278c-124">L’en-tête ipmsp. h n’est pas disponible dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0278c-124">The header ipmsp.h is not available in in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="0278c-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0278c-125">Requirements</span></span>



| <span data-ttu-id="0278c-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0278c-126">Requirement</span></span> | <span data-ttu-id="0278c-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="0278c-127">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0278c-128">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="0278c-128">TAPI version</span></span><br/> | <span data-ttu-id="0278c-129">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="0278c-129">Requires TAPI 3.0 or later</span></span><br/>                                              |
| <span data-ttu-id="0278c-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="0278c-130">Header</span></span><br/>       | <dl> <span data-ttu-id="0278c-131"><dt>Tapi3. h</dt></span><span class="sxs-lookup"><span data-stu-id="0278c-131"><dt>Tapi3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0278c-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0278c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0278c-133">**ITQOSEvent :: obtient le \_ MediaType**</span><span class="sxs-lookup"><span data-stu-id="0278c-133">**ITQOSEvent::get\_MediaType**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itqosevent-get_mediatype)
</dt> <dt>

[<span data-ttu-id="0278c-134">**ITAMMediaFormat :: obtient \_ MediaFormat**</span><span class="sxs-lookup"><span data-stu-id="0278c-134">**ITAMMediaFormat::get\_MediaFormat**</span></span>](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-get_mediaformat)
</dt> <dt>

[<span data-ttu-id="0278c-135">**ITAMMediaFormat ::p ut \_ MediaFormat**</span><span class="sxs-lookup"><span data-stu-id="0278c-135">**ITAMMediaFormat::put\_MediaFormat**</span></span>](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-put_mediaformat)
</dt> <dt>

[<span data-ttu-id="0278c-136">**ITCallInfo :: obtient \_ CallInfoLong**</span><span class="sxs-lookup"><span data-stu-id="0278c-136">**ITCallInfo::get\_CallInfoLong**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)
</dt> <dt>

[<span data-ttu-id="0278c-137">**ITMediaSupport :: obtient \_ MediaTypes**</span><span class="sxs-lookup"><span data-stu-id="0278c-137">**ITMediaSupport::get\_MediaTypes**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itmediasupport-get_mediatypes)
</dt> <dt>

[<span data-ttu-id="0278c-138">**ITTerminalSupport::CreateTerminal**</span><span class="sxs-lookup"><span data-stu-id="0278c-138">**ITTerminalSupport::CreateTerminal**</span></span>](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> </dl>

 

