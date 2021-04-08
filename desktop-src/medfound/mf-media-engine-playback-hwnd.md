---
description: Définit un handle vers une fenêtre de lecture vidéo pour le moteur multimédia.
ms.assetid: 63889D81-12C5-47C1-B52A-6358E68830C3
title: Attribut MF_MEDIA_ENGINE_PLAYBACK_HWND (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6a9d38d40b04b32244f48289d3334199a7e035
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953374"
---
# <a name="mf_media_engine_playback_hwnd-attribute"></a><span data-ttu-id="7d3ba-103">\_ \_ \_ Attribut HWND de lecture du moteur multimédia MF \_</span><span class="sxs-lookup"><span data-stu-id="7d3ba-103">MF\_MEDIA\_ENGINE\_PLAYBACK\_HWND attribute</span></span>

<span data-ttu-id="7d3ba-104">Définit un handle vers une fenêtre de lecture vidéo pour le moteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="7d3ba-104">Sets a handle to a video playback window for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="7d3ba-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="7d3ba-105">Data type</span></span>

<span data-ttu-id="7d3ba-106">**HWND** stocké comme **UINT64**</span><span class="sxs-lookup"><span data-stu-id="7d3ba-106">**HWND** stored as **UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="7d3ba-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="7d3ba-107">Get/set</span></span>

<span data-ttu-id="7d3ba-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="7d3ba-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="7d3ba-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="7d3ba-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="remarks"></a><span data-ttu-id="7d3ba-110">Notes</span><span class="sxs-lookup"><span data-stu-id="7d3ba-110">Remarks</span></span>

<span data-ttu-id="7d3ba-111">Cet attribut est utilisé avec la méthode [**IMFMediaEngineClassFactory :: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) pour initialiser le moteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="7d3ba-111">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d3ba-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d3ba-112">Requirements</span></span>



| <span data-ttu-id="7d3ba-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d3ba-113">Requirement</span></span> | <span data-ttu-id="7d3ba-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d3ba-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d3ba-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d3ba-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7d3ba-116">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7d3ba-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="7d3ba-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d3ba-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7d3ba-118">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="7d3ba-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="7d3ba-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="7d3ba-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d3ba-120"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d3ba-120"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d3ba-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d3ba-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d3ba-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7d3ba-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




