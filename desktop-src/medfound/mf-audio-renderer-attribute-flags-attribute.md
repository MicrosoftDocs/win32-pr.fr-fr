---
description: Contient des indicateurs pour configurer le convertisseur audio.
ms.assetid: 07433904-1bf6-4e8d-9571-8d663bf4fd13
title: Attribut MF_AUDIO_RENDERER_ATTRIBUTE_FLAGS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c17d4b5a51384ebcd180643e0a07601d25e5fb5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517605"
---
# <a name="mf_audio_renderer_attribute_flags-attribute"></a><span data-ttu-id="0a8d3-103">\_ \_ \_ Attribut indicateurs d’attribut de convertisseur audio MF \_</span><span class="sxs-lookup"><span data-stu-id="0a8d3-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS attribute</span></span>

<span data-ttu-id="0a8d3-104">Contient des indicateurs pour configurer le convertisseur audio.</span><span class="sxs-lookup"><span data-stu-id="0a8d3-104">Contains flags to configure the audio renderer.</span></span>

## <a name="data-type"></a><span data-ttu-id="0a8d3-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="0a8d3-105">Data type</span></span>

<span data-ttu-id="0a8d3-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0a8d3-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="0a8d3-107">Notes</span><span class="sxs-lookup"><span data-stu-id="0a8d3-107">Remarks</span></span>

<span data-ttu-id="0a8d3-108">La valeur de cet attribut est **une opération or au niveau du bit** des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="0a8d3-108">The value of this attribute is a bitwise **OR** of the following flags.</span></span>



| <span data-ttu-id="0a8d3-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a8d3-109">Value</span></span>                                                   | <span data-ttu-id="0a8d3-110">Description</span><span class="sxs-lookup"><span data-stu-id="0a8d3-110">Description</span></span>                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a8d3-111">**\_indicateurs d' \_ attribut de convertisseur audio MF \_ \_ \_ CROSSPROCESS**</span><span class="sxs-lookup"><span data-stu-id="0a8d3-111">**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS\_CROSSPROCESS**</span></span> | <span data-ttu-id="0a8d3-112">Le convertisseur audio utilise une session audio inter-processus.</span><span class="sxs-lookup"><span data-stu-id="0a8d3-112">The audio renderer is uses a cross-process audio session.</span></span> <span data-ttu-id="0a8d3-113">Cet indicateur active les convertisseurs audio dans plusieurs processus pour partager la même session audio, ainsi que les contrôles de volume et de stratégie associés.</span><span class="sxs-lookup"><span data-stu-id="0a8d3-113">This flag enables audio renderers in multiple processes to share the same audio session, along with the associated volume and policy controls.</span></span><br/> <span data-ttu-id="0a8d3-114">Si cet indicateur n’est pas défini, la session audio ne peut pas être partagée par les convertisseurs audio dans d’autres processus.</span><span class="sxs-lookup"><span data-stu-id="0a8d3-114">If this flag is not set, the audio session cannot be shared by audio renderers in other processes.</span></span><br/> |
| <span data-ttu-id="0a8d3-115">**\_indicateurs d’attribut de convertisseur audio MF non \_ \_ \_ \_ persistance**</span><span class="sxs-lookup"><span data-stu-id="0a8d3-115">**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS\_NOPERSIST**</span></span>    | <span data-ttu-id="0a8d3-116">L’API de session audio Windows (WASAPI) ne rend pas persistantes les propriétés de cette session audio, telles que le volume de session.</span><span class="sxs-lookup"><span data-stu-id="0a8d3-116">The Windows audio session API (WASAPI) will not persist the properties for this audio session, such as the session volume.</span></span><br/> <span data-ttu-id="0a8d3-117">Si cet indicateur n’est pas défini, WASAPI conserve les propriétés de session audio.</span><span class="sxs-lookup"><span data-stu-id="0a8d3-117">If this flag is not set, WASAPI will persist the audio session properties.</span></span><br/>                                                                                                       |



 

<span data-ttu-id="0a8d3-118">Vous pouvez utiliser cet attribut pour configurer le convertisseur audio.</span><span class="sxs-lookup"><span data-stu-id="0a8d3-118">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="0a8d3-119">L’utilisation dépend de la fonction que vous appelez pour créer le convertisseur audio :</span><span class="sxs-lookup"><span data-stu-id="0a8d3-119">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="0a8d3-120">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): définissez cet attribut à l’aide du pointeur d’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) spécifié dans le paramètre *pAudioAttributes* .</span><span class="sxs-lookup"><span data-stu-id="0a8d3-120">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="0a8d3-121">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): définissez cet attribut à l’aide du pointeur d’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) récupéré dans le paramètre *ppActivate* .</span><span class="sxs-lookup"><span data-stu-id="0a8d3-121">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="0a8d3-122">Définissez l’attribut avant d’appeler [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="0a8d3-122">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="0a8d3-123">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0a8d3-123">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a8d3-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a8d3-124">Requirements</span></span>



| <span data-ttu-id="0a8d3-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a8d3-125">Requirement</span></span> | <span data-ttu-id="0a8d3-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a8d3-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0a8d3-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a8d3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0a8d3-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0a8d3-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0a8d3-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a8d3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0a8d3-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0a8d3-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0a8d3-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a8d3-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a8d3-132"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a8d3-132"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a8d3-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a8d3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a8d3-134">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0a8d3-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0a8d3-135">Attributs du convertisseur audio</span><span class="sxs-lookup"><span data-stu-id="0a8d3-135">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="0a8d3-136">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0a8d3-136">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="0a8d3-137">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0a8d3-137">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="0a8d3-138">Convertisseur audio de streaming</span><span class="sxs-lookup"><span data-stu-id="0a8d3-138">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 




