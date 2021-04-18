---
description: Spécifie la catégorie de flux audio pour le convertisseur audio de streaming (SAR).
ms.assetid: 88E79DE6-2062-4471-A939-D1D4DD2EC42D
title: Attribut MF_AUDIO_RENDERER_ATTRIBUTE_STREAM_CATEGORY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd96c219e43f85c516a5f862e2a978724328a69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106522678"
---
# <a name="mf_audio_renderer_attribute_stream_category-attribute"></a><span data-ttu-id="1b615-103">\_Attribut de \_ catégorie de \_ flux d’attribut de convertisseur audio \_ MF \_</span><span class="sxs-lookup"><span data-stu-id="1b615-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_STREAM\_CATEGORY attribute</span></span>

<span data-ttu-id="1b615-104">Spécifie la catégorie de flux audio pour le [convertisseur audio de streaming](streaming-audio-renderer.md) (SAR).</span><span class="sxs-lookup"><span data-stu-id="1b615-104">Specifies the audio stream category for the [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR).</span></span>

## <a name="data-type"></a><span data-ttu-id="1b615-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="1b615-105">Data type</span></span>

<span data-ttu-id="1b615-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1b615-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="1b615-107">Notes</span><span class="sxs-lookup"><span data-stu-id="1b615-107">Remarks</span></span>

<span data-ttu-id="1b615-108">Vous pouvez utiliser cet attribut pour configurer le convertisseur audio.</span><span class="sxs-lookup"><span data-stu-id="1b615-108">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="1b615-109">L’utilisation dépend de la fonction que vous appelez pour créer le convertisseur audio.</span><span class="sxs-lookup"><span data-stu-id="1b615-109">The usage depends on which function you call to create the audio renderer.</span></span>



| <span data-ttu-id="1b615-110">Fonction</span><span class="sxs-lookup"><span data-stu-id="1b615-110">Function</span></span>                                                               | <span data-ttu-id="1b615-111">Définition de l’attribut</span><span class="sxs-lookup"><span data-stu-id="1b615-111">How to Set the attribute</span></span>                                                                                                                                                                       |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b615-112">**MFCreateAudioRenderer**</span><span class="sxs-lookup"><span data-stu-id="1b615-112">**MFCreateAudioRenderer**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)                 | <span data-ttu-id="1b615-113">Utilisez le pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) spécifié dans le paramètre *pAudioAttributes* .</span><span class="sxs-lookup"><span data-stu-id="1b615-113">Use the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer specified in the *pAudioAttributes* parameter.</span></span>                                                                                          |
| [<span data-ttu-id="1b615-114">**MFCreateAudioRendererActivate**</span><span class="sxs-lookup"><span data-stu-id="1b615-114">**MFCreateAudioRendererActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) | <span data-ttu-id="1b615-115">Utilisez le pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retourné dans le paramètre *ppActivate* .</span><span class="sxs-lookup"><span data-stu-id="1b615-115">Use the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer returned in the *ppActivate* parameter.</span></span> <span data-ttu-id="1b615-116">Définissez l’attribut avant d’appeler [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="1b615-116">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span> |



 

<span data-ttu-id="1b615-117">La valeur de l’attribut est un membre de l’énumération de [**\_ \_ catégorie de flux audio**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) .</span><span class="sxs-lookup"><span data-stu-id="1b615-117">The value of the attribute is a member of the [**AUDIO\_STREAM\_CATEGORY**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) enumeration.</span></span> <span data-ttu-id="1b615-118">Le service audio utilise la catégorie Stream pour déterminer les stratégies audio lorsque plusieurs applications lisent l’audio en même temps.</span><span class="sxs-lookup"><span data-stu-id="1b615-118">The audio service uses the stream category to determine audio policies when multiple applications play audio at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b615-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b615-119">Requirements</span></span>



| <span data-ttu-id="1b615-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b615-120">Requirement</span></span> | <span data-ttu-id="1b615-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b615-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1b615-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b615-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1b615-123">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b615-123">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1b615-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b615-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1b615-125">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b615-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1b615-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b615-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b615-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b615-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b615-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b615-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b615-129">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1b615-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
