---
description: Spécifie le rôle de point de terminaison audio pour le convertisseur audio.
ms.assetid: f0456337-5351-457e-9830-920bf346bfc4
title: Attribut MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ROLE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1b6599ffc97cfa9c7fc2b6a75f4ed4ae7c2c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952342"
---
# <a name="mf_audio_renderer_attribute_endpoint_role-attribute"></a><span data-ttu-id="c97a0-103">\_Attribut de \_ rôle de \_ \_ point de terminaison d’attribut de convertisseur audio MF \_</span><span class="sxs-lookup"><span data-stu-id="c97a0-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ROLE attribute</span></span>

<span data-ttu-id="c97a0-104">Spécifie le rôle de point de terminaison audio pour le convertisseur audio.</span><span class="sxs-lookup"><span data-stu-id="c97a0-104">Specifies the audio endpoint role for the audio renderer.</span></span>

## <a name="data-type"></a><span data-ttu-id="c97a0-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="c97a0-105">Data type</span></span>

<span data-ttu-id="c97a0-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c97a0-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c97a0-107">Notes</span><span class="sxs-lookup"><span data-stu-id="c97a0-107">Remarks</span></span>

<span data-ttu-id="c97a0-108">Vous pouvez utiliser cet attribut pour configurer le convertisseur audio.</span><span class="sxs-lookup"><span data-stu-id="c97a0-108">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="c97a0-109">L’utilisation dépend de la fonction que vous appelez pour créer le convertisseur audio :</span><span class="sxs-lookup"><span data-stu-id="c97a0-109">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="c97a0-110">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): définissez cet attribut à l’aide du pointeur d’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) spécifié dans le paramètre *pAudioAttributes* .</span><span class="sxs-lookup"><span data-stu-id="c97a0-110">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="c97a0-111">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): définissez cet attribut à l’aide du pointeur d’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) récupéré dans le paramètre *ppActivate* .</span><span class="sxs-lookup"><span data-stu-id="c97a0-111">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="c97a0-112">Définissez l’attribut avant d’appeler [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="c97a0-112">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="c97a0-113">Un périphérique de point de terminaison audio est un périphérique matériel qui se trouve à une extrémité d’un chemin de données audio, tel qu’un casque ou un haut-parleur.</span><span class="sxs-lookup"><span data-stu-id="c97a0-113">An audio endpoint device is a hardware device that lies at one end of an audio data path, such as a headphone or a speaker.</span></span>

<span data-ttu-id="c97a0-114">Si cet attribut est défini, le convertisseur audio utilise le périphérique audio par défaut pour le rôle spécifié.</span><span class="sxs-lookup"><span data-stu-id="c97a0-114">If this attribute is set, the audio renderer uses the default audio device for the specified role.</span></span> <span data-ttu-id="c97a0-115">La valeur de cet attribut est un membre de l’énumération **ERole** , qui est définie dans le fichier d’en-tête MMDeviceAPI. h.</span><span class="sxs-lookup"><span data-stu-id="c97a0-115">The value of this attribute is a member of the **ERole** enumeration, which is defined in the header file mmdeviceapi.h.</span></span> <span data-ttu-id="c97a0-116">Pour plus d’informations, consultez la documentation de l’API audio principale.</span><span class="sxs-lookup"><span data-stu-id="c97a0-116">For more information, see the Core Audio API documentation.</span></span> <span data-ttu-id="c97a0-117">Si cet attribut n’est pas défini, le convertisseur audio utilise l’appareil de point de terminaison par défaut.</span><span class="sxs-lookup"><span data-stu-id="c97a0-117">If this attribute is not set, the audio renderer uses the default endpoint device.</span></span>

<span data-ttu-id="c97a0-118">Si cet attribut est défini, ne définissez pas l’attribut ID de point de terminaison de l' [**\_ \_ attribut de convertisseur \_ \_ \_ audio MF**](mf-audio-renderer-attribute-endpoint-id-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="c97a0-118">If this attribute is set, do not set the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ID**](mf-audio-renderer-attribute-endpoint-id-attribute.md) attribute.</span></span> <span data-ttu-id="c97a0-119">Si les deux attributs sont définis, un échec se produit lors de la création du convertisseur audio.</span><span class="sxs-lookup"><span data-stu-id="c97a0-119">If both attributes are set, a failure will occur when the audio renderer is created.</span></span>

<span data-ttu-id="c97a0-120">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c97a0-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c97a0-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c97a0-121">Requirements</span></span>



| <span data-ttu-id="c97a0-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c97a0-122">Requirement</span></span> | <span data-ttu-id="c97a0-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c97a0-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c97a0-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c97a0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c97a0-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c97a0-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c97a0-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c97a0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c97a0-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c97a0-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c97a0-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="c97a0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c97a0-129"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c97a0-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c97a0-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c97a0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c97a0-131">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c97a0-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c97a0-132">Attributs du convertisseur audio</span><span class="sxs-lookup"><span data-stu-id="c97a0-132">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="c97a0-133">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c97a0-133">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c97a0-134">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c97a0-134">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="c97a0-135">Convertisseur audio de streaming</span><span class="sxs-lookup"><span data-stu-id="c97a0-135">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 




