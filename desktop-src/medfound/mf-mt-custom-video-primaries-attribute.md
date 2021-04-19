---
description: Spécifie des couleurs primaires personnalisées pour un type de média vidéo.
ms.assetid: dc5df755-53cf-4910-af42-309f1f46b1ed
title: Attribut MF_MT_CUSTOM_VIDEO_PRIMARIES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3286d63e39638f74cacafa1b4376b28c7703f7c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106537075"
---
# <a name="mf_mt_custom_video_primaries-attribute"></a><span data-ttu-id="92191-103">\_Attribut de \_ prédictionnaires vidéo personnalisé MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="92191-103">MF\_MT\_CUSTOM\_VIDEO\_PRIMARIES attribute</span></span>

<span data-ttu-id="92191-104">Spécifie des couleurs primaires personnalisées pour un type de média vidéo.</span><span class="sxs-lookup"><span data-stu-id="92191-104">Specifies custom color primaries for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="92191-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="92191-105">Data type</span></span>

<span data-ttu-id="92191-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="92191-106">**UINT32**</span></span>

<span data-ttu-id="92191-107">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="92191-107">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="92191-108">Notes</span><span class="sxs-lookup"><span data-stu-id="92191-108">Remarks</span></span>

<span data-ttu-id="92191-109">Les données d’attribut sont une structure de préversion [**\_ \_ vidéo \_ personnalisée MT**](/windows/desktop/api/mfapi/ns-mfapi-mt_custom_video_primaries) .</span><span class="sxs-lookup"><span data-stu-id="92191-109">The attribute data is an [**MT\_CUSTOM\_VIDEO\_PRIMARIES**](/windows/desktop/api/mfapi/ns-mfapi-mt_custom_video_primaries) structure.</span></span>

<span data-ttu-id="92191-110">Cet attribut spécifie le volume de couleurs réel du contenu ou un affichage.</span><span class="sxs-lookup"><span data-stu-id="92191-110">This attribute specifies the actual color volume of content or a display.</span></span> <span data-ttu-id="92191-111">Les informations de mastérisation du volume de couleurs CEA-861,3/SMPTE ST. 2086 sont stockées dans cet attribut par décodeurs.</span><span class="sxs-lookup"><span data-stu-id="92191-111">CEA-861.3 / SMPTE ST.2086 color volume mastering information is stored in this attribute by decoders.</span></span> <span data-ttu-id="92191-112">Notez que cet attribut ne remplace pas l’attribut de préversions [**\_ \_ vidéo \_ de MF MT**](mf-mt-video-primaries-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="92191-112">Note that this attribute does not replace the [**MF\_MT\_VIDEO\_PRIMARIES**](mf-mt-video-primaries-attribute.md)attribute.</span></span> <span data-ttu-id="92191-113">Cet attribut décrit une indication sur le volume de couleurs du contenu, tandis que les **\_ vidéos MF MT \_ vidéo \_ primaires** décrivent les couleurs primaires dans lesquelles le contenu est effectivement codé (par exemple, la signification de 1,0 dans les canaux R/g/B d’une représentation à virgule flottante).</span><span class="sxs-lookup"><span data-stu-id="92191-113">This attribute describes a hint about the color volume of the content, whereas **MF\_MT\_VIDEO\_PRIMARIES** describes the color primaries in which the content is actually coded (e.g: the meaning of 1.0 in the R/G/B channels of a floating point representation).</span></span>

<span data-ttu-id="92191-114">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="92191-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="92191-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92191-115">Requirements</span></span>



| <span data-ttu-id="92191-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92191-116">Requirement</span></span> | <span data-ttu-id="92191-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="92191-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="92191-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92191-118">Minimum supported client</span></span><br/> | <span data-ttu-id="92191-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92191-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="92191-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92191-120">Minimum supported server</span></span><br/> | <span data-ttu-id="92191-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92191-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="92191-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="92191-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="92191-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="92191-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92191-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92191-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92191-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="92191-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="92191-126">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="92191-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="92191-127">**IMFAttributes :: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="92191-127">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="92191-128">**IMFAttributes :: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="92191-128">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="92191-129">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="92191-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

 




