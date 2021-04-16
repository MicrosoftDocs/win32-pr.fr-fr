---
description: Valeur qui définit le système de mesure pour une valeur de profondeur dans une image vidéo.
ms.assetid: 7BFA846B-E614-4117-A196-298E065CB7F8
title: Attribut MF_MT_DEPTH_MEASUREMENT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8be6c06ea09f4017ae65935081eaa81d1ad00cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104563618"
---
# <a name="mf_mt_depth_measurement-attribute"></a><span data-ttu-id="5801d-103">\_Attribut de \_ mesure de profondeur du Mt MF \_</span><span class="sxs-lookup"><span data-stu-id="5801d-103">MF\_MT\_DEPTH\_MEASUREMENT attribute</span></span>

<span data-ttu-id="5801d-104">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="5801d-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5801d-105">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="5801d-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5801d-106">Valeur qui définit le système de mesure pour une valeur de profondeur dans une image vidéo.</span><span class="sxs-lookup"><span data-stu-id="5801d-106">A value that defines the measurement system for a depth value in a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="5801d-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="5801d-107">Data type</span></span>

<span data-ttu-id="5801d-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5801d-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="5801d-109">Notes</span><span class="sxs-lookup"><span data-stu-id="5801d-109">Remarks</span></span>

<span data-ttu-id="5801d-110">Cette valeur est un membre de l’énumération [**\_ MFDepthMeasurement**](/windows/win32/api/mfapi/ne-mfapi-mfdepthmeasurement)</span><span class="sxs-lookup"><span data-stu-id="5801d-110">This value is a member of the [**\_MFDepthMeasurement**](/windows/win32/api/mfapi/ne-mfapi-mfdepthmeasurement) enumeration</span></span>

<span data-ttu-id="5801d-111">Si cet attribut n’est pas présent, il est supposé être **DistanceToFocalPlane**.</span><span class="sxs-lookup"><span data-stu-id="5801d-111">If this attribute is not present it is assumed to be **DistanceToFocalPlane**.</span></span> <span data-ttu-id="5801d-112">La distance au plan focal est généralement plus facile à consommer dans un système de coordonnées 3D euclidienne.</span><span class="sxs-lookup"><span data-stu-id="5801d-112">The distance to focal plane is typically easier to consume in a 3D Euclidian coordinate system.</span></span>

![illustration de distancetofocalplane](images/distance-to-focal-plane.png)

<span data-ttu-id="5801d-114">La distance au format Centre focal est généralement des données brutes provenant d’un capteur, telles que le temps des caméras de vol.</span><span class="sxs-lookup"><span data-stu-id="5801d-114">The distance to focal center format is typically raw data from sensor such as time of flight cameras.</span></span>

![illustration de distancetoopticalcenter](images/distance-to-optical-center.png)

<span data-ttu-id="5801d-116">Les caméras de profondeur ne peuvent pas détecter la profondeur de tous les pixels.</span><span class="sxs-lookup"><span data-stu-id="5801d-116">Depth cameras cannot sense the depth of all pixels.</span></span> <span data-ttu-id="5801d-117">Lorsque la confiance d’un pixel est faible, en raison d’un matériau, d’une occlusion ou d’une plage de valeurs, etc., la valeur de profondeur sur ce pixel peut être non valide.</span><span class="sxs-lookup"><span data-stu-id="5801d-117">When the confidence of a pixel is low, because of material, occlusion, or out of range etc, the depth value on that pixel can be invalid.</span></span>

<span data-ttu-id="5801d-118">Lorsqu’une valeur de pixel de profondeur est 0, le pixel n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5801d-118">When a depth pixel value is 0, the pixel is invalid.</span></span>

<span data-ttu-id="5801d-119">Certaines caméras de profondeur attachent des métadonnées de masque de bits pour chaque pixel, en plus de la valeur de profondeur pour représenter la raison pour laquelle la profondeur de pixel n’est pas valide, en raison d’un matériau, d’une occlusion ou d’une plage de valeurs, etc. Nous vous recommandons d’éviter d’attacher ces métadonnées en tant que bits en valeur de profondeur, car cela entraîne généralement des difficultés lors de l’utilisation de ces valeurs dans le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="5801d-119">Some depth cameras attach bitmask metadata for each pixel in addition to the depth value to represent the reason why the depth of pixel is invalid, due to material, occlusion or out of range etc. We recommend that you avoid attaching such metadata as bits in depth value, because it will typically lead to difficulty when using such values in pixel shader.</span></span> <span data-ttu-id="5801d-120">Qu'.</span><span class="sxs-lookup"><span data-stu-id="5801d-120">Instead.</span></span> <span data-ttu-id="5801d-121">Nous vous recommandons d’utiliser une mémoire tampon d’image 8 bits distincte avec la même résolution et de l’attacher en tant qu’attribut du [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span><span class="sxs-lookup"><span data-stu-id="5801d-121">we recommend that you use a separate 8bit image buffer with same resolution and attach it as attribute of the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span></span> <span data-ttu-id="5801d-122">Ces métadonnées varient pour chaque fournisseur d’appareils photo et ne sont pas standardisées par la plateforme.</span><span class="sxs-lookup"><span data-stu-id="5801d-122">Such metadata varies for each camera vendor and is not standardized by the platform.</span></span> <span data-ttu-id="5801d-123">Nous vous recommandons d’utiliser 16 bits complets pour la valeur de profondeur pour un traitement plus facile en aval et en utilisant une valeur fixe telle que 0 pour l’invalidation.</span><span class="sxs-lookup"><span data-stu-id="5801d-123">We recommend using full 16 bits for the depth value for easier processing downstream and using a fixed value such as 0 for invalidation.</span></span>

## <a name="requirements"></a><span data-ttu-id="5801d-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5801d-124">Requirements</span></span>



| <span data-ttu-id="5801d-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5801d-125">Requirement</span></span> | <span data-ttu-id="5801d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="5801d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5801d-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5801d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5801d-128">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5801d-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5801d-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5801d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5801d-130">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5801d-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="5801d-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="5801d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5801d-132"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5801d-132"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




