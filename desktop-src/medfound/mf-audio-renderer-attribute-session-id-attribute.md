---
description: Spécifie la classe de stratégie audio pour le convertisseur audio.
ms.assetid: 80b028f5-7756-4bb8-b5e3-ebc8343e168c
title: Attribut MF_AUDIO_RENDERER_ATTRIBUTE_SESSION_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4952a60d4438e610677b494290e9738e469770d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866806"
---
# <a name="mf_audio_renderer_attribute_session_id-attribute"></a><span data-ttu-id="5398d-103">Attribut d’ID de session de l' \_ attribut de convertisseur audio MF \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="5398d-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_SESSION\_ID attribute</span></span>

<span data-ttu-id="5398d-104">Spécifie la classe de stratégie audio pour le convertisseur audio.</span><span class="sxs-lookup"><span data-stu-id="5398d-104">Specifies the audio policy class for the audio renderer.</span></span>

## <a name="data-type"></a><span data-ttu-id="5398d-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="5398d-105">Data type</span></span>

<span data-ttu-id="5398d-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="5398d-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="5398d-107">Notes</span><span class="sxs-lookup"><span data-stu-id="5398d-107">Remarks</span></span>

<span data-ttu-id="5398d-108">Cet attribut associe le convertisseur audio à une classe de stratégie audio.</span><span class="sxs-lookup"><span data-stu-id="5398d-108">This attribute associates the audio renderer with an audio policy class.</span></span> <span data-ttu-id="5398d-109">Chaque classe de stratégie dispose de son propre contrôle de volume et de stratégie.</span><span class="sxs-lookup"><span data-stu-id="5398d-109">Each policy class has its own volume and policy control.</span></span> <span data-ttu-id="5398d-110">Si cet attribut n’est pas défini, le nouveau SAR rejoint la session audio par défaut de l’application.</span><span class="sxs-lookup"><span data-stu-id="5398d-110">If this attribute is not set, the new SAR joins the application's default audio session.</span></span> <span data-ttu-id="5398d-111">Pour plus d’informations, consultez [**IAudioClient :: Initialize**](/windows/win32/api/audioclient/nf-audioclient-iaudioclient-initialize) dans la documentation de l’API audio principale.</span><span class="sxs-lookup"><span data-stu-id="5398d-111">For more information, see [**IAudioClient::Initialize**](/windows/win32/api/audioclient/nf-audioclient-iaudioclient-initialize) in the core audio API documentation.</span></span>

<span data-ttu-id="5398d-112">Vous pouvez utiliser cet attribut pour configurer le convertisseur audio.</span><span class="sxs-lookup"><span data-stu-id="5398d-112">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="5398d-113">L’utilisation dépend de la fonction que vous appelez pour créer le convertisseur audio :</span><span class="sxs-lookup"><span data-stu-id="5398d-113">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="5398d-114">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): définissez cet attribut à l’aide du pointeur d’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) spécifié dans le paramètre *pAudioAttributes* .</span><span class="sxs-lookup"><span data-stu-id="5398d-114">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="5398d-115">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): définissez cet attribut à l’aide du pointeur d’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) récupéré dans le paramètre *ppActivate* .</span><span class="sxs-lookup"><span data-stu-id="5398d-115">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="5398d-116">Définissez l’attribut avant d’appeler [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="5398d-116">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="5398d-117">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5398d-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5398d-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5398d-118">Requirements</span></span>



| <span data-ttu-id="5398d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5398d-119">Requirement</span></span> | <span data-ttu-id="5398d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="5398d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5398d-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5398d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5398d-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5398d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5398d-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5398d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5398d-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5398d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5398d-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="5398d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5398d-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5398d-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5398d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5398d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5398d-128">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5398d-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5398d-129">Attributs du convertisseur audio</span><span class="sxs-lookup"><span data-stu-id="5398d-129">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="5398d-130">**IMFAttributes :: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="5398d-130">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="5398d-131">**IMFAttributes :: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="5398d-131">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="5398d-132">Convertisseur audio de streaming</span><span class="sxs-lookup"><span data-stu-id="5398d-132">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
