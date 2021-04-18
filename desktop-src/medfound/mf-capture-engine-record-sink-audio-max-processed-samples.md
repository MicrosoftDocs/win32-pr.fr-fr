---
description: Définit le nombre maximal d’exemples traités qui peuvent être mis en mémoire tampon dans le chemin d’accès audio du récepteur d’enregistrements.
ms.assetid: 216886DB-B206-4944-925A-C2106331F1CB
title: Attribut MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_PROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d1ce4d649c75106545eb2ff39d4f3ea742e6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526907"
---
# <a name="mf_capture_engine_record_sink_audio_max_processed_samples-attribute"></a><span data-ttu-id="22e5d-103">\_Attribut des \_ \_ exemples de \_ \_ données audio \_ Max \_ processed du \_ récepteur d’enregistrements du moteur de capture MF</span><span class="sxs-lookup"><span data-stu-id="22e5d-103">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_AUDIO\_MAX\_PROCESSED\_SAMPLES attribute</span></span>

<span data-ttu-id="22e5d-104">Définit le nombre maximal d’exemples traités qui peuvent être mis en mémoire tampon dans le chemin d’accès audio du récepteur d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="22e5d-104">Sets the maximum number of processed samples that can be buffered in the record sink audio path.</span></span>

## <a name="data-type"></a><span data-ttu-id="22e5d-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="22e5d-105">Data type</span></span>

<span data-ttu-id="22e5d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="22e5d-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="22e5d-107">Notes</span><span class="sxs-lookup"><span data-stu-id="22e5d-107">Remarks</span></span>

<span data-ttu-id="22e5d-108">Pour configurer cet attribut sur le moteur de capture, ajoutez-le au paramètre *pAttributes* lorsque vous appelez [**IMFCaptureEngine :: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span><span class="sxs-lookup"><span data-stu-id="22e5d-108">To configure this attribute on the capture engine, add it to the *pAttributes* parameter when you call [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span></span>

<span data-ttu-id="22e5d-109">La valeur maximale de cet attribut est 100.</span><span class="sxs-lookup"><span data-stu-id="22e5d-109">The maximum value for this attribute is 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="22e5d-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22e5d-110">Requirements</span></span>



| <span data-ttu-id="22e5d-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22e5d-111">Requirement</span></span> | <span data-ttu-id="22e5d-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="22e5d-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="22e5d-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22e5d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="22e5d-114">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22e5d-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="22e5d-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22e5d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="22e5d-116">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22e5d-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="22e5d-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="22e5d-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="22e5d-118"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="22e5d-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22e5d-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22e5d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22e5d-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="22e5d-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="22e5d-121">Attributs du moteur de capture</span><span class="sxs-lookup"><span data-stu-id="22e5d-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="22e5d-122">**IMFCaptureEngine :: Initialize**</span><span class="sxs-lookup"><span data-stu-id="22e5d-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




