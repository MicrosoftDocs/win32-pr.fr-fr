---
description: Spécifie l’identificateur pour l’appareil de point de terminaison audio.
ms.assetid: f145fb80-c136-421c-9a65-e69c52109348
title: Attribut MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e042f59baf4812c177358acca6badb2422914afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318814"
---
# <a name="mf_audio_renderer_attribute_endpoint_id-attribute"></a><span data-ttu-id="ddb0f-103">\_Attribut d' \_ ID de \_ \_ point de terminaison d’attribut de convertisseur audio MF \_</span><span class="sxs-lookup"><span data-stu-id="ddb0f-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ID attribute</span></span>

<span data-ttu-id="ddb0f-104">Spécifie l’identificateur pour l’appareil de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="ddb0f-104">Specifies the identifier for the audio endpoint device.</span></span>

## <a name="data-type"></a><span data-ttu-id="ddb0f-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="ddb0f-105">Data type</span></span>

<span data-ttu-id="ddb0f-106">Chaîne de caractères larges</span><span class="sxs-lookup"><span data-stu-id="ddb0f-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="ddb0f-107">Notes</span><span class="sxs-lookup"><span data-stu-id="ddb0f-107">Remarks</span></span>

<span data-ttu-id="ddb0f-108">Vous pouvez utiliser cet attribut pour configurer le convertisseur audio.</span><span class="sxs-lookup"><span data-stu-id="ddb0f-108">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="ddb0f-109">L’utilisation dépend de la fonction que vous appelez pour créer le convertisseur audio :</span><span class="sxs-lookup"><span data-stu-id="ddb0f-109">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="ddb0f-110">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): définissez cet attribut à l’aide du pointeur d’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) spécifié dans le paramètre *pAudioAttributes* .</span><span class="sxs-lookup"><span data-stu-id="ddb0f-110">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="ddb0f-111">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): définissez cet attribut à l’aide du pointeur d’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) récupéré dans le paramètre *ppActivate* .</span><span class="sxs-lookup"><span data-stu-id="ddb0f-111">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="ddb0f-112">Définissez l’attribut avant d’appeler [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="ddb0f-112">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="ddb0f-113">Un périphérique de point de terminaison audio est un périphérique matériel qui se trouve à une extrémité d’un chemin de données audio, tel qu’un casque ou un haut-parleur.</span><span class="sxs-lookup"><span data-stu-id="ddb0f-113">An audio endpoint device is a hardware device that lies at one end of an audio data path, such as a headphone or a speaker.</span></span> <span data-ttu-id="ddb0f-114">Pour obtenir l’identificateur de point de terminaison audio, utilisez les API audio principales suivantes :</span><span class="sxs-lookup"><span data-stu-id="ddb0f-114">To obtain the audio endpoint identifier, use the following core audio APIs:</span></span>

-   <span data-ttu-id="ddb0f-115">Utilisez l’interface [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) pour énumérer les appareils sur le système.</span><span class="sxs-lookup"><span data-stu-id="ddb0f-115">Use the [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface to enumerate the devices on the system.</span></span>
-   <span data-ttu-id="ddb0f-116">Appelez [**IMMDevice :: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) pour obtenir l’identificateur de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ddb0f-116">Call [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) to get the identifier for the device.</span></span>

<span data-ttu-id="ddb0f-117">Pour plus d’informations, consultez la documentation de l’API [audio principale](../coreaudio/core-audio-apis-in-windows-vista.md) .</span><span class="sxs-lookup"><span data-stu-id="ddb0f-117">For more information, see the [Core Audio](../coreaudio/core-audio-apis-in-windows-vista.md) API documentation.</span></span> <span data-ttu-id="ddb0f-118">Si cet attribut n’est pas défini, le convertisseur audio utilise l’appareil de point de terminaison par défaut.</span><span class="sxs-lookup"><span data-stu-id="ddb0f-118">If this attribute is not set, the audio renderer uses the default endpoint device.</span></span>

<span data-ttu-id="ddb0f-119">Si cet attribut est défini, ne définissez pas l’attribut de [**\_ rôle de point de \_ terminaison d’attribut de convertisseur \_ \_ \_ audio MF**](mf-audio-renderer-attribute-endpoint-role-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="ddb0f-119">If this attribute is set, do not set the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ROLE**](mf-audio-renderer-attribute-endpoint-role-attribute.md) attribute.</span></span> <span data-ttu-id="ddb0f-120">Si les deux attributs sont définis, un échec se produit lors de la création du convertisseur audio.</span><span class="sxs-lookup"><span data-stu-id="ddb0f-120">If both attributes are set, a failure will occur when the audio renderer is created.</span></span>

<span data-ttu-id="ddb0f-121">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ddb0f-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddb0f-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ddb0f-122">Requirements</span></span>



| <span data-ttu-id="ddb0f-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ddb0f-123">Requirement</span></span> | <span data-ttu-id="ddb0f-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ddb0f-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ddb0f-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddb0f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ddb0f-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ddb0f-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ddb0f-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddb0f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ddb0f-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ddb0f-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ddb0f-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="ddb0f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddb0f-130"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddb0f-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddb0f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddb0f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddb0f-132">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ddb0f-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ddb0f-133">Attributs du convertisseur audio</span><span class="sxs-lookup"><span data-stu-id="ddb0f-133">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="ddb0f-134">**IMFAttributes :: GetString**</span><span class="sxs-lookup"><span data-stu-id="ddb0f-134">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="ddb0f-135">**IMFAttributes :: SetString**</span><span class="sxs-lookup"><span data-stu-id="ddb0f-135">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="ddb0f-136">Convertisseur audio de streaming</span><span class="sxs-lookup"><span data-stu-id="ddb0f-136">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
