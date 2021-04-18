---
description: Valeur qui définit les unités pour une valeur de profondeur dans une image vidéo.
ms.assetid: 0D7238F3-C224-48BD-8654-B3182DFB244C
title: Attribut MF_MT_DEPTH_VALUE_UNIT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f6086a34f62c26b3fe1fa611318792c9056a50c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519597"
---
# <a name="mf_mt_depth_value_unit-attribute"></a><span data-ttu-id="a2a61-103">\_Attribut d' \_ \_ unité de valeur de profondeur MT MF \_</span><span class="sxs-lookup"><span data-stu-id="a2a61-103">MF\_MT\_DEPTH\_VALUE\_UNIT attribute</span></span>

<span data-ttu-id="a2a61-104">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="a2a61-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a2a61-105">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="a2a61-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a2a61-106">Valeur qui définit les unités pour une valeur de profondeur dans une image vidéo.</span><span class="sxs-lookup"><span data-stu-id="a2a61-106">A value that defines the units for a depth value in a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="a2a61-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="a2a61-107">Data type</span></span>

<span data-ttu-id="a2a61-108">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="a2a61-108">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="a2a61-109">Notes</span><span class="sxs-lookup"><span data-stu-id="a2a61-109">Remarks</span></span>

<span data-ttu-id="a2a61-110">La valeur d’unité est une valeur UINT64 en nanomètres, dans la plage de 1e à 9 mètres.</span><span class="sxs-lookup"><span data-stu-id="a2a61-110">The unit value is a UINT64 value in nanometers, in the range 1e - 9 meters.</span></span> <span data-ttu-id="a2a61-111">Si cette valeur n’est pas présente, la valeur par défaut de l’unité est 1e-3, ce qui indique que chaque niveau de pixel est mesuré en 1 millimètre dans l’espace physique.</span><span class="sxs-lookup"><span data-stu-id="a2a61-111">If this value is not present, the default value of the unit is 1e-3, which indicates each pixel level is measured in 1 millimeter in physical space.</span></span>

<span data-ttu-id="a2a61-112">Les caméras de profondeur ne peuvent pas détecter la profondeur de tous les pixels.</span><span class="sxs-lookup"><span data-stu-id="a2a61-112">Depth cameras cannot sense the depth of all pixels.</span></span> <span data-ttu-id="a2a61-113">Lorsque la confiance d’un pixel est faible, en raison d’un matériau, d’une occlusion ou d’une plage de valeurs, etc., la valeur de profondeur sur ce pixel peut être non valide.</span><span class="sxs-lookup"><span data-stu-id="a2a61-113">When the confidence of a pixel is low, because of material, occlusion, or out of range etc, the depth value on that pixel can be invalid.</span></span>

<span data-ttu-id="a2a61-114">Lorsqu’une valeur de pixel de profondeur est 0, le pixel n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a2a61-114">When a depth pixel value is 0, the pixel is invalid.</span></span>

<span data-ttu-id="a2a61-115">Certaines caméras de profondeur attachent des métadonnées de masque de bits pour chaque pixel, en plus de la valeur de profondeur pour représenter la raison pour laquelle la profondeur de pixel n’est pas valide, en raison d’un matériau, d’une occlusion ou d’une plage de valeurs, etc. Nous vous recommandons d’éviter d’attacher ces métadonnées en tant que bits en valeur de profondeur, car cela entraîne généralement des difficultés lors de l’utilisation de ces valeurs dans le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="a2a61-115">Some depth cameras attach bitmask metadata for each pixel in addition to the depth value to represent the reason why the depth of pixel is invalid, due to material, occlusion or out of range etc. We recommend that you avoid attaching such metadata as bits in depth value, because it will typically lead to difficulty when using such values in pixel shader.</span></span> <span data-ttu-id="a2a61-116">Qu'.</span><span class="sxs-lookup"><span data-stu-id="a2a61-116">Instead.</span></span> <span data-ttu-id="a2a61-117">Nous vous recommandons d’utiliser une mémoire tampon d’image 8 bits distincte avec la même résolution et de l’attacher en tant qu’attribut du [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span><span class="sxs-lookup"><span data-stu-id="a2a61-117">we recommend that you use a separate 8bit image buffer with same resolution and attach it as attribute of the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span></span> <span data-ttu-id="a2a61-118">Ces métadonnées varient pour chaque fournisseur d’appareils photo et ne sont pas standardisées par la plateforme.</span><span class="sxs-lookup"><span data-stu-id="a2a61-118">Such metadata varies for each camera vendor and is not standardized by the platform.</span></span> <span data-ttu-id="a2a61-119">Nous vous recommandons d’utiliser 16 bits complets pour la valeur de profondeur pour un traitement plus facile en aval et en utilisant une valeur fixe telle que 0 pour l’invalidation.</span><span class="sxs-lookup"><span data-stu-id="a2a61-119">We recommend using full 16 bits for the depth value for easier processing downstream and using a fixed value such as 0 for invalidation.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2a61-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2a61-120">Requirements</span></span>



| <span data-ttu-id="a2a61-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2a61-121">Requirement</span></span> | <span data-ttu-id="a2a61-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2a61-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a2a61-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2a61-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a2a61-124">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2a61-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a2a61-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2a61-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a2a61-126">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2a61-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="a2a61-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="a2a61-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2a61-128"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2a61-128"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




