---
description: Pour un format vidéo 3D, spécifie la vue de gauche.
ms.assetid: 4F33BF2D-EB32-46B6-B071-F9130D404201
title: Attribut MF_MT_VIDEO_3D_FIRST_IS_LEFT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027d91509d772a9200cdfc0ac64cce15514aa5a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393788"
---
# <a name="mf_mt_video_3d_first_is_left-attribute"></a><span data-ttu-id="4da3f-103">La \_ \_ vidéo 3D MF MT \_ \_ First est l' \_ \_ attribut Left</span><span class="sxs-lookup"><span data-stu-id="4da3f-103">MF\_MT\_VIDEO\_3D\_FIRST\_IS\_LEFT attribute</span></span>

<span data-ttu-id="4da3f-104">Pour un format vidéo 3D, spécifie la vue de gauche.</span><span class="sxs-lookup"><span data-stu-id="4da3f-104">For a 3D video format, specifies which view is the left view.</span></span>

## <a name="data-type"></a><span data-ttu-id="4da3f-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="4da3f-105">Data type</span></span>

<span data-ttu-id="4da3f-106">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4da3f-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="4da3f-107">Notes</span><span class="sxs-lookup"><span data-stu-id="4da3f-107">Remarks</span></span>

<span data-ttu-id="4da3f-108">Pour la vidéo 3D, chaque exemple de vidéo contient deux vues, qui sont désignées en *premier* et en *deuxième vue*.</span><span class="sxs-lookup"><span data-stu-id="4da3f-108">For 3D video, each video sample contains two views, which are designated *first view* and *second view*.</span></span> <span data-ttu-id="4da3f-109">La disposition exacte des vues en mémoire est indiquée par l’attribut [de \_ \_ format vidéo \_ 3D \_ MF MT](mf-mt-video-3d-format.md) .</span><span class="sxs-lookup"><span data-stu-id="4da3f-109">The exact layout of the views in memory is indicated by the [MF\_MT\_VIDEO\_3D\_FORMAT](mf-mt-video-3d-format.md) attribute.</span></span>



| <span data-ttu-id="4da3f-110">Format</span><span class="sxs-lookup"><span data-stu-id="4da3f-110">Format</span></span>               | <span data-ttu-id="4da3f-111">Premier affichage</span><span class="sxs-lookup"><span data-stu-id="4da3f-111">First View</span></span>              | <span data-ttu-id="4da3f-112">Deuxième vue</span><span class="sxs-lookup"><span data-stu-id="4da3f-112">Second View</span></span>               |
|----------------------|-------------------------|---------------------------|
| <span data-ttu-id="4da3f-113">Compressé côte à côte</span><span class="sxs-lookup"><span data-stu-id="4da3f-113">Packed side-by-side</span></span>  | <span data-ttu-id="4da3f-114">Moitié gauche de la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="4da3f-114">Left half of the buffer</span></span> | <span data-ttu-id="4da3f-115">Moitié droite de la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="4da3f-115">Right half of the buffer</span></span>  |
| <span data-ttu-id="4da3f-116">Condensé de haut en bas</span><span class="sxs-lookup"><span data-stu-id="4da3f-116">Packed top-to-bottom</span></span> | <span data-ttu-id="4da3f-117">Moitié supérieure de la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="4da3f-117">Top half of the buffer</span></span>  | <span data-ttu-id="4da3f-118">Moitié inférieure de la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="4da3f-118">Bottom half of the buffer</span></span> |
| <span data-ttu-id="4da3f-119">Multivue</span><span class="sxs-lookup"><span data-stu-id="4da3f-119">Multiview</span></span>            | <span data-ttu-id="4da3f-120">Index de mémoire tampon 0</span><span class="sxs-lookup"><span data-stu-id="4da3f-120">Buffer index 0</span></span>          | <span data-ttu-id="4da3f-121">Index de mémoire tampon 1</span><span class="sxs-lookup"><span data-stu-id="4da3f-121">Buffer index 1</span></span>            |
| <span data-ttu-id="4da3f-122">Vue de base</span><span class="sxs-lookup"><span data-stu-id="4da3f-122">Base view</span></span>            | <span data-ttu-id="4da3f-123">Frame entier</span><span class="sxs-lookup"><span data-stu-id="4da3f-123">Entire frame</span></span>            | <span data-ttu-id="4da3f-124">Non présent</span><span class="sxs-lookup"><span data-stu-id="4da3f-124">Not present</span></span>               |



 

<span data-ttu-id="4da3f-125">Par défaut, la première vue est la vue de gauche, tandis que la deuxième vue est la vue de droite.</span><span class="sxs-lookup"><span data-stu-id="4da3f-125">By default, the first view is the left view, and the second view is the right view.</span></span> <span data-ttu-id="4da3f-126">Si les affichages de gauche et de droite sont permutés, affectez \_ à l’attribut MF MT \_ Video \_ 3D First la \_ \_ \_ **valeur false** dans le type de média.</span><span class="sxs-lookup"><span data-stu-id="4da3f-126">If the left and right views are swapped, set the MF\_MT\_VIDEO\_3D\_FIRST\_IS\_LEFT attribute to **FALSE** in the media type.</span></span>

> [!Note]  
> <span data-ttu-id="4da3f-127">Dans le format de *vue de base* (**MFVideo3DSampleFormat \_ BaseView**), seule la vue de base est conservée. cet attribut ne s’applique donc pas.</span><span class="sxs-lookup"><span data-stu-id="4da3f-127">In *base view* format (**MFVideo3DSampleFormat\_BaseView**), only the base view is retained, so this attribute does not apply.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4da3f-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4da3f-128">Requirements</span></span>



| <span data-ttu-id="4da3f-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4da3f-129">Requirement</span></span> | <span data-ttu-id="4da3f-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="4da3f-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4da3f-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4da3f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4da3f-132">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4da3f-132">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="4da3f-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4da3f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4da3f-134">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="4da3f-134">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="4da3f-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="4da3f-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="4da3f-136"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4da3f-136"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4da3f-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4da3f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4da3f-138">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4da3f-138">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




