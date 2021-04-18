---
description: Spécifie le degré auquel le codec doit réduire la plage de couleurs effectives de la vidéo.
ms.assetid: 7227957b-59c9-4dd9-ad2b-a383e888cd46
title: MFPKEY_RANGEREDUX, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ec326e5d21a72792aab38f08d8c8c9207ab867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519642"
---
# <a name="mfpkey_rangeredux-property"></a><span data-ttu-id="5872c-103">MFPKEY \_ propriété RANGEREDUX</span><span class="sxs-lookup"><span data-stu-id="5872c-103">MFPKEY\_RANGEREDUX Property</span></span>

<span data-ttu-id="5872c-104">Spécifie le degré auquel le codec doit réduire la plage de couleurs effectives de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="5872c-104">Specifies the degree to which the codec should reduce the effective color range of the video.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="5872c-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="5872c-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="5872c-106">\_wszWMVCRangeRedux g</span><span class="sxs-lookup"><span data-stu-id="5872c-106">g\_wszWMVCRangeRedux</span></span>

## <a name="data-type"></a><span data-ttu-id="5872c-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="5872c-107">Data Type</span></span>

<span data-ttu-id="5872c-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="5872c-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="5872c-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="5872c-109">Default Value</span></span>

<span data-ttu-id="5872c-110">0</span><span class="sxs-lookup"><span data-stu-id="5872c-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="5872c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="5872c-111">Remarks</span></span>

<span data-ttu-id="5872c-112">La réduction de plage spécifie le degré auquel le codec doit réduire la luminance et la plage de chrominance de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="5872c-112">Range reduction specifies the degree to which the codec should reduce luma and chroma range of the video.</span></span> <span data-ttu-id="5872c-113">La réduction de la plage réduit la taille des images vidéo encodées, mais réduit également le détail des couleurs de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="5872c-113">Reducing range reduces the size of encoded video frames but also reduces the color detail of the video.</span></span>

<span data-ttu-id="5872c-114">La réduction de plage se compose d’une réduction lors du décodage et de l’extension.</span><span class="sxs-lookup"><span data-stu-id="5872c-114">Range reduction consists of reduction during encoding and expansion during decoding.</span></span> <span data-ttu-id="5872c-115">Il est possible de faire en sorte que les facteurs d’expansion ne soient pas les mêmes que les facteurs de réduction, mais cela n’est pas recommandé dans la plupart des scénarios où le remappage de plage est utile.</span><span class="sxs-lookup"><span data-stu-id="5872c-115">It is possible to make the expansion factors different than the reduction factors, but this is not recommended in most scenarios where range remapping is useful.</span></span>

<span data-ttu-id="5872c-116">La réduction de la plage et l’expansion sont effectuées séparément sur les canaux de luminance et de chrominance.</span><span class="sxs-lookup"><span data-stu-id="5872c-116">Range reduction and expansion is performed separately on luma and chroma channels.</span></span> <span data-ttu-id="5872c-117">La réduction de la plage peut être un moyen efficace de réduire la complexité de la vidéo à faible vitesse de transmission sans sacrifier les détails de l’image.</span><span class="sxs-lookup"><span data-stu-id="5872c-117">Reducing range can be an efficient way to reduce the complexity of low bit-rate video without sacrificing image detail.</span></span> <span data-ttu-id="5872c-118">En définissant les quatre valeurs sur 8, vous réduisez la quantité d’informations de luminance et de chrominance de moitié, en laissant plus de bits à rediriger pour conserver les détails de l’image.</span><span class="sxs-lookup"><span data-stu-id="5872c-118">Setting all four values to 8 reduces the amount of luma and chroma information by half, leaving more bits to be directed to preserving image detail.</span></span>

<span data-ttu-id="5872c-119">Le codec peut choisir d’utiliser automatiquement la réduction de plage lors de l’encodage de vidéos à des débits binaires très faibles.</span><span class="sxs-lookup"><span data-stu-id="5872c-119">The codec can choose to automatically use range reduction when encoding video at very low bit-rates.</span></span> <span data-ttu-id="5872c-120">Si vous affectez la valeur 0 à ces quatre valeurs, vous désactivez complètement la réduction de plage, même dans les scénarios de faible débit.</span><span class="sxs-lookup"><span data-stu-id="5872c-120">Setting all four values to 0 completely disables range reduction even in low bit-rate scenarios.</span></span>

<span data-ttu-id="5872c-121">La réduction de la plage de couleurs réduit la taille encodée des images vidéo, mais peut introduire un flou dans les frames décodés.</span><span class="sxs-lookup"><span data-stu-id="5872c-121">Reducing the color range reduces the encoded size of video frames but can introduce blurriness in the decoded frames.</span></span>

<span data-ttu-id="5872c-122">Si cette propriété n’est pas définie, le codec détermine s’il faut utiliser la réduction de plage au moment de l’encodage.</span><span class="sxs-lookup"><span data-stu-id="5872c-122">If this property is not set, the codec determines whether to use range reduction at encoding time.</span></span> <span data-ttu-id="5872c-123">En règle générale, cette option est sélectionnée par le codec uniquement aux taux de bits faibles.</span><span class="sxs-lookup"><span data-stu-id="5872c-123">Typically this option is selected by the codec only at low bit rates.</span></span>

<span data-ttu-id="5872c-124">La valeur de cette propriété est une combinaison de quatre composants, séparés par des zéros, mis en forme en tant que 0x0M0m0N0n, où :</span><span class="sxs-lookup"><span data-stu-id="5872c-124">The value of this property is a combination of four components, separated by zeros, formatted as 0x0M0m0N0n, where:</span></span>

-   <span data-ttu-id="5872c-125">M est le facteur de réduction de plage d’encodage pour le composant Y.</span><span class="sxs-lookup"><span data-stu-id="5872c-125">M is the encoding range reduction factor for the Y component.</span></span>
-   <span data-ttu-id="5872c-126">m est le facteur d’extension de la plage de décodage pour le composant Y (généralement le même que M).</span><span class="sxs-lookup"><span data-stu-id="5872c-126">m is the decoding range expansion factor for the Y component (usually the same as M).</span></span>
-   <span data-ttu-id="5872c-127">N est le facteur de réduction de la plage d’encodage pour le composant UV.</span><span class="sxs-lookup"><span data-stu-id="5872c-127">N is the encoding range reduction factor for the UV component.</span></span>
-   <span data-ttu-id="5872c-128">n est le facteur d’extension de la plage de décodage pour le composant UV (généralement identique à N).</span><span class="sxs-lookup"><span data-stu-id="5872c-128">n is the decoding range expansion factor for the UV component (usually the same as N).</span></span>

<span data-ttu-id="5872c-129">Chaque facteur est un chiffre compris entre 0 et 8, où 0 n’est pas une réduction ou une expansion et 8 est la réduction ou l’expansion maximale.</span><span class="sxs-lookup"><span data-stu-id="5872c-129">Each factor is a digit from 0 to 8, where 0 is no reduction or expansion and 8 is the maximum reduction or expansion.</span></span>

<span data-ttu-id="5872c-130">Si vous définissez la valeur sur 0x00000000, la réduction de plage est complètement désactivée.</span><span class="sxs-lookup"><span data-stu-id="5872c-130">If you set the value to 0x00000000, range reduction is completely disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="5872c-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5872c-131">Requirements</span></span>



| <span data-ttu-id="5872c-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5872c-132">Requirement</span></span> | <span data-ttu-id="5872c-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="5872c-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5872c-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5872c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5872c-135">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5872c-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5872c-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5872c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5872c-137">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5872c-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5872c-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="5872c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5872c-139"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5872c-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5872c-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5872c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5872c-141">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5872c-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




