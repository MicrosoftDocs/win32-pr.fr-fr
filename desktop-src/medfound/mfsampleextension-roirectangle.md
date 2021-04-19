---
description: Spécifie les limites de la zone d’intérêt qui indique la région du cadre qui requiert une qualité différente.
ms.assetid: F06CACF0-AE75-4707-8CD0-7BA7D51BB80A
title: Attribut MFSampleExtension_ROIRectangle (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71d84d2054caa96feaf7bfb4ccc7a91ecf4ac9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543487"
---
# <a name="mfsampleextension_roirectangle-attribute"></a><span data-ttu-id="866e7-103">\_Attribut MFSampleExtension ROIRectangle</span><span class="sxs-lookup"><span data-stu-id="866e7-103">MFSampleExtension\_ROIRectangle attribute</span></span>

<span data-ttu-id="866e7-104">Spécifie les limites de la zone d’intérêt qui indique la région du cadre qui requiert une qualité différente.</span><span class="sxs-lookup"><span data-stu-id="866e7-104">Specifies the bounds of the region of interest which indicates the region of the frame that requires different quality.</span></span>

## <a name="data-type"></a><span data-ttu-id="866e7-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="866e7-105">Data type</span></span>

<span data-ttu-id="866e7-106">**[**Roi \_ ZONE**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)** stockée en tant qu' **objet BLOB**</span><span class="sxs-lookup"><span data-stu-id="866e7-106">**[**ROI\_AREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)** stored as **BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="866e7-107">Notes</span><span class="sxs-lookup"><span data-stu-id="866e7-107">Remarks</span></span>

<span data-ttu-id="866e7-108">Après avoir correctement défini [CODECAPI \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) sur une valeur différente de zéro sur une table MFT d’encodeur, l’application peut définir cet attribut sur les exemples d’entrée et s’attendre à ce qu’elle soit respectée.</span><span class="sxs-lookup"><span data-stu-id="866e7-108">After successfully setting [CODECAPI\_AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) to a non-zero value on an encoder MFT, the application can set this attribute on input samples and expect it to be honored.</span></span>

<span data-ttu-id="866e7-109">Si [CODECAPI \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) n’est pas défini sur une valeur différente de zéro, l' \_ attribut MFSampleExtension ROIRectangle est ignoré sur les exemples d’entrée.</span><span class="sxs-lookup"><span data-stu-id="866e7-109">If [CODECAPI\_AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) is not set to a non-zero value, the MFSampleExtension\_ROIRectangle attribute is ignored on input samples.</span></span>

<span data-ttu-id="866e7-110">MFSampleExtension \_ ROIRectangle est défini sur un exemple d’entrée et est appliqué uniquement à l’exemple d’entrée actuel.</span><span class="sxs-lookup"><span data-stu-id="866e7-110">MFSampleExtension\_ROIRectangle is set on an input sample and is only applied to the current input sample.</span></span>

<span data-ttu-id="866e7-111">Le champ **QPDelta** de la structure de la [**\_ zone roi**](/windows/desktop/api/mfapi/ns-mfapi-roi_area) spécifie le delta du paramètre de quantification pour la région spécifiée à partir du reste du cadre.</span><span class="sxs-lookup"><span data-stu-id="866e7-111">The **QPDelta** field on the [**ROI\_AREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area) structure specifies the quantization parameter delta for the specified region from the rest of the frame.</span></span> <span data-ttu-id="866e7-112">Si **QPDelta** est positif, cela indique que l’application souhaite que le rectangle ait une qualité inférieure à celle du reste du cadre.</span><span class="sxs-lookup"><span data-stu-id="866e7-112">If **QPDelta** is positive, this indicates the application wants the rectangle to have lower quality than the rest of the frame.</span></span>

<span data-ttu-id="866e7-113">**Encodeurs H. 264/AVC :** **QPDelta** doit être compris entre \[ -25, + 25 \] .</span><span class="sxs-lookup"><span data-stu-id="866e7-113">**H.264/AVC encoders:** **QPDelta** shall be between \[-25, +25\].</span></span> <span data-ttu-id="866e7-114">L’encodeur doit s’assurer que le QP final est dans une plage valide pour la norme vidéo.</span><span class="sxs-lookup"><span data-stu-id="866e7-114">The encoder shall ensure that the final QP is in a valid range for the video standard.</span></span>

<span data-ttu-id="866e7-115">La région spécifiée n’a pas besoin d’être alignée en Mo.</span><span class="sxs-lookup"><span data-stu-id="866e7-115">The specified region is not required to be MB aligned.</span></span> <span data-ttu-id="866e7-116">Les encodeurs ont la possibilité de choisir la limite réelle.</span><span class="sxs-lookup"><span data-stu-id="866e7-116">Encoders have flexibility to decide the actual boundary.</span></span> <span data-ttu-id="866e7-117">Il est recommandé de couvrir la totalité de la région spécifiée.</span><span class="sxs-lookup"><span data-stu-id="866e7-117">It is recommended to cover the entire specified region.</span></span>

## <a name="requirements"></a><span data-ttu-id="866e7-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="866e7-118">Requirements</span></span>



| <span data-ttu-id="866e7-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="866e7-119">Requirement</span></span> | <span data-ttu-id="866e7-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="866e7-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="866e7-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="866e7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="866e7-122">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="866e7-122">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="866e7-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="866e7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="866e7-124">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="866e7-124">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="866e7-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="866e7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="866e7-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="866e7-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="866e7-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="866e7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="866e7-128">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="866e7-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




