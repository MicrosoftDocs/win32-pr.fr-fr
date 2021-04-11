---
description: Spécifie si le codec doit utiliser l’optimisation de perception conservatrice lors de l’encodage.
ms.assetid: f44fd932-d8f8-46c7-b17c-27e6141408ab
title: MFPKEY_PERCEPTUALOPTLEVEL, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d86857ca9d7e4205afc0baf9c212e92606511ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202342"
---
# <a name="mfpkey_perceptualoptlevel-property"></a><span data-ttu-id="b66f0-103">MFPKEY \_ propriété PERCEPTUALOPTLEVEL</span><span class="sxs-lookup"><span data-stu-id="b66f0-103">MFPKEY\_PERCEPTUALOPTLEVEL Property</span></span>

<span data-ttu-id="b66f0-104">Spécifie si le codec doit utiliser l’optimisation de perception conservatrice lors de l’encodage.</span><span class="sxs-lookup"><span data-stu-id="b66f0-104">Specifies whether the codec should use conservative perceptual optimization when encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b66f0-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="b66f0-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b66f0-106">\_wszWMVCPerceptualOptLevel g</span><span class="sxs-lookup"><span data-stu-id="b66f0-106">g\_wszWMVCPerceptualOptLevel</span></span>

## <a name="data-type"></a><span data-ttu-id="b66f0-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="b66f0-107">Data Type</span></span>

<span data-ttu-id="b66f0-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="b66f0-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="b66f0-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="b66f0-109">Default Value</span></span>

<span data-ttu-id="b66f0-110">0</span><span class="sxs-lookup"><span data-stu-id="b66f0-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="b66f0-111">Notes</span><span class="sxs-lookup"><span data-stu-id="b66f0-111">Remarks</span></span>

<span data-ttu-id="b66f0-112">L’optimisation de perception conservatrice est un processus par lequel le codec tente d’identifier les régions « importantes » et « sans importance » dans la trame vidéo.</span><span class="sxs-lookup"><span data-stu-id="b66f0-112">Conservative perceptual optimization is a process by which the codec attempts to identify "important" and "unimportant" regions in the video frame.</span></span> <span data-ttu-id="b66f0-113">Après avoir identifié ces régions du cadre, le codec offre une priorité plus élevée à la qualité des régions importantes, au détriment de la qualité des régions inimportants.</span><span class="sxs-lookup"><span data-stu-id="b66f0-113">After identifying these regions of the frame, the codec will give a higher priority to the quality of important regions, at the expense of the quality of unimportant regions.</span></span>

<span data-ttu-id="b66f0-114">L’optimisation de la perception insiste sur le fait que l’image semble correcte à l’oeil humain au lieu d’insister sur une précision mathématique stricte.</span><span class="sxs-lookup"><span data-stu-id="b66f0-114">Perceptual optimization emphasizes making the image appear correct to the human eye instead of insisting on strict mathematical accuracy.</span></span>

<span data-ttu-id="b66f0-115">Les résultats de l’optimisation varient considérablement en fonction du type de vidéo encodé.</span><span class="sxs-lookup"><span data-stu-id="b66f0-115">The results of the optimization will vary considerably depending on the type of video being encoded.</span></span> <span data-ttu-id="b66f0-116">Cette fonctionnalité peut être parfaitement adaptée aux encodages à faible débit et à faible résolution (par exemple, la diffusion Web), mais elle doit probablement être évitée pour la qualité vidéo d’archivage.</span><span class="sxs-lookup"><span data-stu-id="b66f0-116">This feature could be well suited for low bit-rate and low resolution encoding (for example, web streaming), but should probably be avoided when aiming for archival video quality.</span></span>

## <a name="requirements"></a><span data-ttu-id="b66f0-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b66f0-117">Requirements</span></span>



| <span data-ttu-id="b66f0-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b66f0-118">Requirement</span></span> | <span data-ttu-id="b66f0-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b66f0-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b66f0-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b66f0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b66f0-121">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b66f0-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b66f0-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b66f0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b66f0-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b66f0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b66f0-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="b66f0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b66f0-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b66f0-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b66f0-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b66f0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b66f0-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b66f0-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




