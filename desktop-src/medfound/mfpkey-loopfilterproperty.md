---
description: Spécifie si le codec doit utiliser le filtre de déblocage en boucle lors de l’encodage.
ms.assetid: 395a356a-5f58-46b4-b2ff-47f98106f487
title: MFPKEY_LOOPFILTER, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fbb723c4145f9769cc157d5db8eb7893d89b389
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531883"
---
# <a name="mfpkey_loopfilter-property"></a><span data-ttu-id="37d1f-103">MFPKEY \_ propriété LOOPFILTER</span><span class="sxs-lookup"><span data-stu-id="37d1f-103">MFPKEY\_LOOPFILTER Property</span></span>

<span data-ttu-id="37d1f-104">Spécifie si le codec doit utiliser le filtre de déblocage en boucle lors de l’encodage.</span><span class="sxs-lookup"><span data-stu-id="37d1f-104">Specifies whether the codec should use the in-loop deblocking filter during encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="37d1f-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="37d1f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="37d1f-106">\_wszWMVCLoopFilter g</span><span class="sxs-lookup"><span data-stu-id="37d1f-106">g\_wszWMVCLoopFilter</span></span>

## <a name="data-type"></a><span data-ttu-id="37d1f-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="37d1f-107">Data Type</span></span>

<span data-ttu-id="37d1f-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="37d1f-108">VT\_BOOL</span></span>

## <a name="remarks"></a><span data-ttu-id="37d1f-109">Notes</span><span class="sxs-lookup"><span data-stu-id="37d1f-109">Remarks</span></span>

<span data-ttu-id="37d1f-110">Le filtre en boucle est une méthode de déblocage appliquée lors de l’encodage et du décodage, afin de réduire les artefacts de blocage au moment de l’encodage (« dans la boucle ») afin que les futurs frames P et B-frames ne les transmettent pas en avant.</span><span class="sxs-lookup"><span data-stu-id="37d1f-110">The in-loop filter is a deblocking method that is applied during both encoding and decoding, to reduce blocking artifacts at encoding time ("in the loop") so that future P-frames and B-frames don't carry them forward.</span></span>

<span data-ttu-id="37d1f-111">L’application du filtre en boucle a pour effet que les bords des blocs de macros dans les trames vidéo de sortie sont moins perceptibles.</span><span class="sxs-lookup"><span data-stu-id="37d1f-111">The effect of applying the in-loop filter is that the edges of the macro-blocks in the output video frames are less noticeable.</span></span> <span data-ttu-id="37d1f-112">En même temps, l’image peut devenir plus douce en apparence.</span><span class="sxs-lookup"><span data-stu-id="37d1f-112">At the same time the image can become softer in appearance.</span></span>

<span data-ttu-id="37d1f-113">Bien que le filtre en boucle puisse entraîner une réduction des détails de l’image dans certains frames, la qualité vidéo globale sera avantageuse.</span><span class="sxs-lookup"><span data-stu-id="37d1f-113">Although the in-loop filter can lead to reduced image detail in some frames, the overall video quality will benefit noticeably.</span></span> <span data-ttu-id="37d1f-114">Le plus grand inconvénient de l’utilisation du filtrage en boucle est le coût supplémentaire de décodage des performances.</span><span class="sxs-lookup"><span data-stu-id="37d1f-114">The biggest disadvantage to using in-loop filtering is the additional decoding performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="37d1f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37d1f-115">Requirements</span></span>



| <span data-ttu-id="37d1f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37d1f-116">Requirement</span></span> | <span data-ttu-id="37d1f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="37d1f-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37d1f-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37d1f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="37d1f-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37d1f-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="37d1f-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37d1f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="37d1f-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37d1f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="37d1f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="37d1f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="37d1f-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="37d1f-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37d1f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37d1f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37d1f-125">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="37d1f-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




