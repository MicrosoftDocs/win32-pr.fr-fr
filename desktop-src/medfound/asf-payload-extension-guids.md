---
description: Les GUID suivants définissent les extensions de charge utile pour les flux ASF (Advanced Systems Format).
ms.assetid: db973b41-1e5c-4bc8-921d-5e9312eb21cb
title: GUID d’extension de charge utile ASF (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7dbd27212c8f4812360ba22f89a717659307f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524663"
---
# <a name="asf-payload-extension-guids"></a><span data-ttu-id="348ce-103">GUID d’extension de charge utile ASF</span><span class="sxs-lookup"><span data-stu-id="348ce-103">ASF Payload Extension GUIDs</span></span>

<span data-ttu-id="348ce-104">Les GUID suivants définissent les extensions de charge utile pour les flux ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="348ce-104">The following GUIDs define payload extensions for Advanced Systems Format (ASF) streams.</span></span>



| <span data-ttu-id="348ce-105">Constante</span><span class="sxs-lookup"><span data-stu-id="348ce-105">Constant</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="348ce-106">Description</span><span class="sxs-lookup"><span data-stu-id="348ce-106">Description</span></span>                                                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFSampleExtension_SampleDuration"></span><span id="mfasfsampleextension_sampleduration"></span><span id="MFASFSAMPLEEXTENSION_SAMPLEDURATION"></span><dl> <span data-ttu-id="348ce-107"><dt>**MFASFSampleExtension \_ SampleDuration**</dt></span><span class="sxs-lookup"><span data-stu-id="348ce-107"><dt>**MFASFSampleExtension\_SampleDuration**</dt></span></span> </dl>         | <span data-ttu-id="348ce-108">Les données indiquent la durée, en millisecondes, de l’échantillon contenu dans l’objet buffer.</span><span class="sxs-lookup"><span data-stu-id="348ce-108">The data indicates the duration, in milliseconds, of the sample contained in the buffer object.</span></span><br/>                                                                       |
| <span id="MFASFSampleExtension_OutputCleanPoint"></span><span id="mfasfsampleextension_outputcleanpoint"></span><span id="MFASFSAMPLEEXTENSION_OUTPUTCLEANPOINT"></span><dl> <span data-ttu-id="348ce-109"><dt>**MFASFSampleExtension \_ OutputCleanPoint**</dt></span><span class="sxs-lookup"><span data-stu-id="348ce-109"><dt>**MFASFSampleExtension\_OutputCleanPoint**</dt></span></span> </dl> | <span data-ttu-id="348ce-110">Les données indiquent si l’échantillon est une image clé.</span><span class="sxs-lookup"><span data-stu-id="348ce-110">The data indicates whether the sample is a key frame.</span></span> <span data-ttu-id="348ce-111">La valeur zéro indique que l’exemple n’est pas une image clé.</span><span class="sxs-lookup"><span data-stu-id="348ce-111">A value of zero indicates that the sample is not a key frame.</span></span> <span data-ttu-id="348ce-112">Une valeur différente de zéro indique qu’il s’agit d’une image clé.</span><span class="sxs-lookup"><span data-stu-id="348ce-112">A nonzero value indicates that it is a key frame.</span></span><br/> |
| <span id="MFASFSampleExtension_SMPTE"></span><span id="mfasfsampleextension_smpte"></span><span id="MFASFSAMPLEEXTENSION_SMPTE"></span><dl> <span data-ttu-id="348ce-113"><dt>**\_SMPTE MFASFSampleExtension**</dt></span><span class="sxs-lookup"><span data-stu-id="348ce-113"><dt>**MFASFSampleExtension\_SMPTE**</dt></span></span> </dl>                                             | <span data-ttu-id="348ce-114">Les données sont un code temporel SMPTE.</span><span class="sxs-lookup"><span data-stu-id="348ce-114">The data is a SMPTE time code.</span></span><br/>                                                                                                                                        |
| <span id="MFASFSampleExtension_FileName"></span><span id="mfasfsampleextension_filename"></span><span id="MFASFSAMPLEEXTENSION_FILENAME"></span><dl> <span data-ttu-id="348ce-115"><dt>**\_Nom de fichier MFASFSampleExtension**</dt></span><span class="sxs-lookup"><span data-stu-id="348ce-115"><dt>**MFASFSampleExtension\_FileName**</dt></span></span> </dl>                                 | <span data-ttu-id="348ce-116">Les données de l’exemple d’extension spécifient le nom du fichier à partir duquel le contenu de l’échantillon a été pris.</span><span class="sxs-lookup"><span data-stu-id="348ce-116">The data in the sample extension specifies the name of the file from which the content in the sample was taken.</span></span><br/>                                                       |
| <span id="MFASFSampleExtension_ContentType"></span><span id="mfasfsampleextension_contenttype"></span><span id="MFASFSAMPLEEXTENSION_CONTENTTYPE"></span><dl> <span data-ttu-id="348ce-117"><dt>**\_ContentType MFASFSampleExtension**</dt></span><span class="sxs-lookup"><span data-stu-id="348ce-117"><dt>**MFASFSampleExtension\_ContentType**</dt></span></span> </dl>                     | <span data-ttu-id="348ce-118">Les données identifient le type de contenu que l’exemple contient.</span><span class="sxs-lookup"><span data-stu-id="348ce-118">The data identifies the type of content that the sample contains.</span></span><br/>                                                                                                     |
| <span id="MFASFSampleExtension_PixelAspectRatio"></span><span id="mfasfsampleextension_pixelaspectratio"></span><span id="MFASFSAMPLEEXTENSION_PIXELASPECTRATIO"></span><dl> <span data-ttu-id="348ce-119"><dt>**MFASFSampleExtension \_ PixelAspectRatio**</dt></span><span class="sxs-lookup"><span data-stu-id="348ce-119"><dt>**MFASFSampleExtension\_PixelAspectRatio**</dt></span></span> </dl> | <span data-ttu-id="348ce-120">Les données indiquent les proportions de pixels du contenu de l’échantillon.</span><span class="sxs-lookup"><span data-stu-id="348ce-120">The data indicates the pixel aspect ratio of the content in the sample.</span></span><br/>                                                                                               |



## <a name="requirements"></a><span data-ttu-id="348ce-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="348ce-121">Requirements</span></span>



| <span data-ttu-id="348ce-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="348ce-122">Requirement</span></span> | <span data-ttu-id="348ce-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="348ce-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="348ce-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="348ce-124">Minimum supported client</span></span><br/> | <span data-ttu-id="348ce-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="348ce-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="348ce-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="348ce-126">Minimum supported server</span></span><br/> | <span data-ttu-id="348ce-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="348ce-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="348ce-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="348ce-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="348ce-129"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="348ce-129"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="348ce-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="348ce-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="348ce-131">**IMFASFStreamConfig::AddPayloadExtension**</span><span class="sxs-lookup"><span data-stu-id="348ce-131">**IMFASFStreamConfig::AddPayloadExtension**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension)
</dt> <dt>

[<span data-ttu-id="348ce-132">**IMFASFStreamConfig::GetPayloadExtension**</span><span class="sxs-lookup"><span data-stu-id="348ce-132">**IMFASFStreamConfig::GetPayloadExtension**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension)
</dt> <dt>

[<span data-ttu-id="348ce-133">Constantes Media Foundation</span><span class="sxs-lookup"><span data-stu-id="348ce-133">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




