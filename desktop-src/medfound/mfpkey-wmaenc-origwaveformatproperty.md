---
description: Spécifie la structure WAVEFORMATEX décrivant le contenu audio d’entrée.
ms.assetid: d424f243-5ad6-46f2-b99b-9bb780715e8a
title: MFPKEY_WMAENC_ORIGWAVEFORMAT, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3475e5578124b8f0a762beddf713f701a5695110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202259"
---
# <a name="mfpkey_wmaenc_origwaveformat-property"></a><span data-ttu-id="b3e9c-103">MFPKEY \_ WMAENC \_ ORIGWAVEFORMAT, propriété</span><span class="sxs-lookup"><span data-stu-id="b3e9c-103">MFPKEY\_WMAENC\_ORIGWAVEFORMAT Property</span></span>

<span data-ttu-id="b3e9c-104">Spécifie la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) décrivant le contenu audio d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b3e9c-104">Specifies the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure describing the input audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b3e9c-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="b3e9c-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b3e9c-106">\_wszWMACOriginalWaveFormat g</span><span class="sxs-lookup"><span data-stu-id="b3e9c-106">g\_wszWMACOriginalWaveFormat</span></span>

## <a name="data-type"></a><span data-ttu-id="b3e9c-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="b3e9c-107">Data Type</span></span>

<span data-ttu-id="b3e9c-108">\_Tableau VT \| \_ UI1 ([**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) en tant que tableau d’octets)</span><span class="sxs-lookup"><span data-stu-id="b3e9c-108">VT\_ARRAY \| VT\_UI1 ([**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) as an array of bytes)</span></span>

## <a name="remarks"></a><span data-ttu-id="b3e9c-109">Notes</span><span class="sxs-lookup"><span data-stu-id="b3e9c-109">Remarks</span></span>

<span data-ttu-id="b3e9c-110">Lors du transcodage de contenu Windows Media Audio à une vitesse de transmission inférieure, vous pouvez transmettre la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) du contenu au codec pour permettre au codec d’optimiser ses algorithmes.</span><span class="sxs-lookup"><span data-stu-id="b3e9c-110">When transcoding Windows Media Audio-based content to a lower bit rate, you can pass the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure of the content to the codec to enable the codec to optimize its algorithms.</span></span> <span data-ttu-id="b3e9c-111">Cette fonctionnalité, appelée « recompression intelligente », fournit de meilleurs résultats que la décompression du contenu, puis l’alimentation des exemples PCM reconstruits par le biais du codec.</span><span class="sxs-lookup"><span data-stu-id="b3e9c-111">This feature, called smart recompression, provides better results than decompressing the content and then feeding the reconstructed PCM samples back through the codec.</span></span>

<span data-ttu-id="b3e9c-112">Lors du passage de la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) , incluez les octets supplémentaires à la fin de la structure spécifiée par **WAVEFORMATEX. cbSize**.</span><span class="sxs-lookup"><span data-stu-id="b3e9c-112">When passing the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure, include any extra bytes at the end of the structure specified by **WAVEFORMATEX.cbSize**.</span></span>

<span data-ttu-id="b3e9c-113">L’encodeur audio accepte uniquement les entrées et sorties pour lesquelles le nombre de canaux, le nombre de bits par échantillon et le taux d’échantillonnage sont identiques.</span><span class="sxs-lookup"><span data-stu-id="b3e9c-113">The audio encoder accepts only inputs and outputs for which the number of channels, bits per sample, and sample rate are identical.</span></span> <span data-ttu-id="b3e9c-114">Vous pouvez transcoder du contenu uniquement à une vitesse de transmission inférieure dans ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="b3e9c-114">You can transcode content only to a lower bit rate within those parameters.</span></span> <span data-ttu-id="b3e9c-115">Dans tous les cas, vous devez décoder le contenu et transmettre les exemples non compressés comme entrée à l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="b3e9c-115">In any case, you must decode the content and pass the uncompressed samples as input to the encoder.</span></span> <span data-ttu-id="b3e9c-116">La définition de cette propriété donne à l’encodeur des informations sur le traitement qui a déjà été effectué sur le contenu.</span><span class="sxs-lookup"><span data-stu-id="b3e9c-116">Setting this property gives the encoder some information about the processing that has already been performed on the content.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3e9c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3e9c-117">Requirements</span></span>



| <span data-ttu-id="b3e9c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3e9c-118">Requirement</span></span> | <span data-ttu-id="b3e9c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3e9c-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3e9c-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3e9c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b3e9c-121">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3e9c-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b3e9c-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3e9c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b3e9c-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3e9c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b3e9c-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3e9c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3e9c-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3e9c-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3e9c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3e9c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3e9c-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b3e9c-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
