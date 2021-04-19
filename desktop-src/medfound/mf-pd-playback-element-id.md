---
description: Contient l’identificateur de l’élément de sélection dans la présentation.
ms.assetid: 355818cf-1e00-46ad-9ce1-ab3a178164f9
title: Attribut MF_PD_PLAYBACK_ELEMENT_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 744a1d164c71cbd7eb8bb47ef12be68d47b8351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529445"
---
# <a name="mf_pd_playback_element_id-attribute"></a><span data-ttu-id="3d177-103">\_Attribut d' \_ ID d’élément de lecture MF PD \_ \_</span><span class="sxs-lookup"><span data-stu-id="3d177-103">MF\_PD\_PLAYBACK\_ELEMENT\_ID attribute</span></span>

<span data-ttu-id="3d177-104">Contient l’identificateur de l’élément de sélection dans la présentation.</span><span class="sxs-lookup"><span data-stu-id="3d177-104">Contains the identifier of the playlist element in the presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="3d177-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="3d177-105">Data type</span></span>

<span data-ttu-id="3d177-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3d177-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="3d177-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="3d177-107">Get/set</span></span>

<span data-ttu-id="3d177-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="3d177-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="3d177-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="3d177-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="3d177-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="3d177-110">Applies to</span></span>

[<span data-ttu-id="3d177-111">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="3d177-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="3d177-112">Notes</span><span class="sxs-lookup"><span data-stu-id="3d177-112">Remarks</span></span>

<span data-ttu-id="3d177-113">Les sources multimédias qui fournissent des sélections peuvent éventuellement définir cet attribut sur leurs descripteurs de présentation.</span><span class="sxs-lookup"><span data-stu-id="3d177-113">Media sources that deliver playlists can optionally set this attribute on their presentation descriptors.</span></span>

<span data-ttu-id="3d177-114">Lorsqu’une source de média remet une sélection, elle envoie un événement [MENewPresentation](menewpresentation.md) pour chaque élément de sélection après le premier.</span><span class="sxs-lookup"><span data-stu-id="3d177-114">When a media source delivers a playlist, it sends a [MENewPresentation](menewpresentation.md) event for each playlist element after the first.</span></span> <span data-ttu-id="3d177-115">Cet événement contient un descripteur de présentation pour le nouvel élément playlist.</span><span class="sxs-lookup"><span data-stu-id="3d177-115">This event contains a presentation descriptor for the new playlist element.</span></span> <span data-ttu-id="3d177-116">La source du média peut affecter des identificateurs aux éléments en définissant l' \_ attribut d’ID d’élément de lecture MF PD \_ \_ \_ sur chaque descripteur de présentation, y compris celui créé par [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="3d177-116">The media source can assign identifiers to the elements by setting the MF\_PD\_PLAYBACK\_ELEMENT\_ID attribute on each presentation descriptor, including the one created by [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>

<span data-ttu-id="3d177-117">Une source de média peut également envoyer l’événement [MENewPresentation](menewpresentation.md) en raison d’un changement de flux dynamique ou d’une modification du nombre de flux.</span><span class="sxs-lookup"><span data-stu-id="3d177-117">A media source might also send the [MENewPresentation](menewpresentation.md) event because of a dynamic stream switch or a change in the number of streams.</span></span> <span data-ttu-id="3d177-118">Dans ce cas, la valeur de l' \_ ID d’élément de lecture MF PD \_ \_ \_ doit rester la même dans les deux présentations, pour indiquer que les deux présentations représentent le même élément de sélection.</span><span class="sxs-lookup"><span data-stu-id="3d177-118">In that situation, the value of MF\_PD\_PLAYBACK\_ELEMENT\_ID should remain the same across both presentations, to indicate that both presentations represent the same playlist element.</span></span> <span data-ttu-id="3d177-119">Si deux présentations consécutives ont la même valeur pour cet attribut, le pipeline Microsoft Media Foundation s’attend à ce que les horodatages restent continus au sein de la transition.</span><span class="sxs-lookup"><span data-stu-id="3d177-119">If two consecutive presentations have the same value for this attribute, the Microsoft Media Foundation pipeline expects the time stamps to remain continuous across the transition.</span></span> <span data-ttu-id="3d177-120">Par conséquent, la source du média ne doit pas utiliser l’attribut de [ \_ \_ \_ \_ début réel](mf-event-source-actual-start-attribute.md) de la source de l’événement MF lorsqu’elle passe à la présentation suivante.</span><span class="sxs-lookup"><span data-stu-id="3d177-120">Therefore, the media source must not use the [MF\_EVENT\_SOURCE\_ACTUAL\_START](mf-event-source-actual-start-attribute.md) attribute when it transitions to the next presentation.</span></span>

<span data-ttu-id="3d177-121">Les sources multimédias qui implémentent [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) doivent utiliser l’attribut d' [ \_ \_ \_ ELEMENTID de séquence TOPONODE MF](mf-toponode-sequence-elementid-attribute.md) plutôt que l' \_ attribut d’ID d’élément de lecture MF PD \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3d177-121">Media sources that implement [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) should use the [MF\_TOPONODE\_SEQUENCE\_ELEMENTID](mf-toponode-sequence-elementid-attribute.md) attribute rather than the MF\_PD\_PLAYBACK\_ELEMENT\_ID attribute.</span></span>

<span data-ttu-id="3d177-122">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="3d177-122">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d177-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d177-123">Requirements</span></span>



| <span data-ttu-id="3d177-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d177-124">Requirement</span></span> | <span data-ttu-id="3d177-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d177-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3d177-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d177-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3d177-127">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3d177-127">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="3d177-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d177-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3d177-129">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3d177-129">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="3d177-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="3d177-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d177-131"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d177-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d177-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d177-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d177-133">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3d177-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3d177-134">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="3d177-134">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




