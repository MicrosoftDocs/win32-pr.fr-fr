---
description: Stocke l’heure (en unités de 100 nanosecondes) à laquelle la présentation doit commencer, par rapport au début de la source du média.
ms.assetid: 7a3dddad-067b-46af-9ed9-4ccc65f9d772
title: Attribut MF_PD_PLAYBACK_BOUNDARY_TIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22abadb4e0148a2079a9a7387e43599f4f79b8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042748"
---
# <a name="mf_pd_playback_boundary_time-attribute"></a><span data-ttu-id="aecc7-103">\_ \_ \_ Attribut heure limite de lecture MF PD \_</span><span class="sxs-lookup"><span data-stu-id="aecc7-103">MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute</span></span>

<span data-ttu-id="aecc7-104">Stocke l’heure (en unités de 100 nanosecondes) à laquelle la présentation doit commencer, par rapport au début de la source du média.</span><span class="sxs-lookup"><span data-stu-id="aecc7-104">Stores the time (in 100-nanoseconds units) at which the presentation must begin, relative to the start of the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="aecc7-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="aecc7-105">Data type</span></span>

<span data-ttu-id="aecc7-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="aecc7-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="aecc7-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="aecc7-107">Get/set</span></span>

<span data-ttu-id="aecc7-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="aecc7-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="aecc7-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="aecc7-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="aecc7-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="aecc7-110">Applies to</span></span>

[<span data-ttu-id="aecc7-111">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="aecc7-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="aecc7-112">Notes</span><span class="sxs-lookup"><span data-stu-id="aecc7-112">Remarks</span></span>

<span data-ttu-id="aecc7-113">L' \_ \_ attribut heure limite de lecture MF PD \_ \_ est facultatif pour les sources multimédias dans une sélection.</span><span class="sxs-lookup"><span data-stu-id="aecc7-113">The MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute is optional for media sources in a playlist.</span></span> <span data-ttu-id="aecc7-114">Cette valeur indique l’heure de début réelle de la présentation.</span><span class="sxs-lookup"><span data-stu-id="aecc7-114">This value indicates the actual start time of the presentation.</span></span> <span data-ttu-id="aecc7-115">Prenons l’exemple d’une sélection qui comprend les sources multimédias *element1*, *élément2* et *Element3* dans une séquence.</span><span class="sxs-lookup"><span data-stu-id="aecc7-115">Consider a playlist that includes media sources *Element1*, *Element2*, and *Element3* in a sequence.</span></span> <span data-ttu-id="aecc7-116">15 secondes après le début de la diffusion de *element1* , une modification dynamique du flux se produit.</span><span class="sxs-lookup"><span data-stu-id="aecc7-116">15 seconds after *Element1* starts playing, a dynamic stream change occurs.</span></span> <span data-ttu-id="aecc7-117">Le nouveau flux doit commencer à lire 15 secondes dans la présentation.</span><span class="sxs-lookup"><span data-stu-id="aecc7-117">The new stream must start playing 15 seconds into the presentation.</span></span> <span data-ttu-id="aecc7-118">Toutefois, l’image clé la plus proche de l’heure de présentation de 15 secondes est de 12 secondes pour le nouveau flux.</span><span class="sxs-lookup"><span data-stu-id="aecc7-118">However, the keyframe nearest the presentation time of 15 seconds is at 12 seconds for the new stream.</span></span> <span data-ttu-id="aecc7-119">Pour démarrer la nouvelle présentation à 15 secondes, une marque est nécessaire pour que les échantillons décodés soient déposés de 12 secondes à 15 secondes.</span><span class="sxs-lookup"><span data-stu-id="aecc7-119">To start the new presentation at 15 seconds, a markin is required so that the decoded samples are dropped from 12 seconds to 15 seconds.</span></span>

<span data-ttu-id="aecc7-120">Avant la transition, l’événement [MENewPresentation](menewpresentation.md) est déclenché par la source du média.</span><span class="sxs-lookup"><span data-stu-id="aecc7-120">Before the transition, the [MENewPresentation](menewpresentation.md) event is raised by the media source.</span></span> <span data-ttu-id="aecc7-121">Cela retourne le descripteur de présentation qui contient l’attribut d' [ID d’élément de \_ \_ lecture \_ \_ MF PD](mf-pd-playback-element-id.md) pour *element1*.</span><span class="sxs-lookup"><span data-stu-id="aecc7-121">This returns the presentation descriptor that contains the [MF\_PD\_PLAYBACK\_ELEMENT\_ID](mf-pd-playback-element-id.md) attribute for *Element1*.</span></span> <span data-ttu-id="aecc7-122">En outre, il contient l' \_ attribut de \_ temps limite de lecture MF PD \_ \_ défini à 15 secondes pour indiquer l’heure à laquelle la transition s’est produite.</span><span class="sxs-lookup"><span data-stu-id="aecc7-122">Additionally, it contains the MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute that is set to 15 seconds to indicate the time when the transition occurred.</span></span> <span data-ttu-id="aecc7-123">La source du média effectue la marque à 15 secondes après le décodage, ce qui empêche l’affichage des images de 12 secondes à 15 secondes.</span><span class="sxs-lookup"><span data-stu-id="aecc7-123">The media source performs the markin at 15 seconds after decoding, which prevents the frames from 12 seconds to 15 seconds from being displayed.</span></span>

<span data-ttu-id="aecc7-124">Cette valeur affecte uniquement l’heure de la marque et n’affecte pas la manière dont la session multimédia ajuste les horodatages.</span><span class="sxs-lookup"><span data-stu-id="aecc7-124">This value affects only markin time and does not affect how the Media Session adjusts time stamps.</span></span> <span data-ttu-id="aecc7-125">Cet attribut est ignoré, sauf si la source du média indique par le biais de l’attribut d' [ \_ ID d’élément de \_ lecture \_ \_ MF PD](mf-pd-playback-element-id.md) que cette présentation est le même élément de lecture que le précédent.</span><span class="sxs-lookup"><span data-stu-id="aecc7-125">This attribute is ignored unless the media source indicates through the [MF\_PD\_PLAYBACK\_ELEMENT\_ID](mf-pd-playback-element-id.md) attribute that this presentation is the same playback element as the previous one.</span></span>

<span data-ttu-id="aecc7-126">L' \_ attribut de \_ durée limite de lecture MF PD \_ \_ est semblable à l’attribut [MF \_ TOPONODE \_ MEDIASTART](mf-toponode-mediastart-attribute.md) défini sur le nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="aecc7-126">The MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute is similar to the [MF\_TOPONODE\_MEDIASTART](mf-toponode-mediastart-attribute.md) attribute that is set on the topology node.</span></span> <span data-ttu-id="aecc7-127">Pour les applications qui s’exécutent sur Windows Vista, les sources multimédias qui implémentent [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) doivent utiliser **MF \_ TOPONODE \_ MEDIASTART** au lieu du \_ \_ temps limite de lecture MF PD \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="aecc7-127">For applications running on Windows Vista, media sources that implement [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) should use **MF\_TOPONODE\_MEDIASTART** instead of MF\_PD\_PLAYBACK\_BOUNDARY\_TIME.</span></span>

<span data-ttu-id="aecc7-128">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="aecc7-128">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="aecc7-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aecc7-129">Requirements</span></span>



| <span data-ttu-id="aecc7-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aecc7-130">Requirement</span></span> | <span data-ttu-id="aecc7-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="aecc7-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aecc7-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aecc7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="aecc7-133">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="aecc7-133">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="aecc7-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aecc7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="aecc7-135">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="aecc7-135">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="aecc7-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="aecc7-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="aecc7-137"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aecc7-137"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aecc7-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aecc7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aecc7-139">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aecc7-139">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="aecc7-140">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="aecc7-140">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




