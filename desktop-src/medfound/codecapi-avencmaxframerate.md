---
description: Définit la vitesse d’entrée maximale en temps réel des trames vidéo en cours d’alimentation sur l’encodeur.
ms.assetid: ACBE8799-A81C-44C3-B985-88ADFB1E51B4
title: CODECAPI_AVEncMaxFrameRate, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c04d1fd1297f299db133cd98bd493c968fcc29c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513339"
---
# <a name="codecapi_avencmaxframerate-property"></a><span data-ttu-id="764a9-103">CODECAPI \_ propriété AVEncMaxFrameRate</span><span class="sxs-lookup"><span data-stu-id="764a9-103">CODECAPI\_AVEncMaxFrameRate property</span></span>

<span data-ttu-id="764a9-104">Définit la vitesse d’entrée maximale en temps réel des trames vidéo en cours d’alimentation sur l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="764a9-104">Sets the maximum real-time input rate of video frames being fed to the encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="764a9-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="764a9-105">Data type</span></span>

<span data-ttu-id="764a9-106">**ULONGULONG** (VT \_ UI8)</span><span class="sxs-lookup"><span data-stu-id="764a9-106">**ULONGULONG** (VT\_UI8)</span></span>

## <a name="property-guid"></a><span data-ttu-id="764a9-107">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="764a9-107">Property GUID</span></span>

<span data-ttu-id="764a9-108">**CODECAPI \_ AVEncMaxFrameRate**</span><span class="sxs-lookup"><span data-stu-id="764a9-108">**CODECAPI\_AVEncMaxFrameRate**</span></span>

## <a name="remarks"></a><span data-ttu-id="764a9-109">Notes</span><span class="sxs-lookup"><span data-stu-id="764a9-109">Remarks</span></span>

<span data-ttu-id="764a9-110">Cette propriété permet à l’appelant de spécifier la vitesse d’entrée maximale en temps réel des trames vidéo en cours d’alimentation sur l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="764a9-110">This property allows the caller to specify the maximum real-time input rate of video frames being fed to the encoder.</span></span> <span data-ttu-id="764a9-111">Cela donne à l’encodeur une indication de la fréquence nécessaire au traitement des trames entrantes.</span><span class="sxs-lookup"><span data-stu-id="764a9-111">This gives the encoder an indication of the rate that it will need to process the incoming frames.</span></span> <span data-ttu-id="764a9-112">Cela est utile pour les encodeurs qui se définissent eux-mêmes dans une configuration d’état d’alimentation particulière en fonction de la résolution et de la fréquence d’images de la vidéo source.</span><span class="sxs-lookup"><span data-stu-id="764a9-112">This is useful for encoders that set themselves into a particular power state configuration based on the resolution and frame-rate of the source video.</span></span>

<span data-ttu-id="764a9-113">La fréquence d’images est exprimée sous la forme d’un rapport.</span><span class="sxs-lookup"><span data-stu-id="764a9-113">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="764a9-114">Les 32 bits supérieurs de la valeur de l’attribut contiennent le numérateur et les 32 inférieurs contiennent le dénominateur.</span><span class="sxs-lookup"><span data-stu-id="764a9-114">The upper 32 bits of the attribute value contain the numerator and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="764a9-115">Par exemple, si la fréquence d’images est de 30 images par seconde (FPS), le ratio est de 30/1.</span><span class="sxs-lookup"><span data-stu-id="764a9-115">For example, if the frame rate is 30 frames per second (fps), the ratio is 30/1.</span></span> <span data-ttu-id="764a9-116">Si la fréquence d’images est de 29,97 fps, le ratio est de 30000/1001.</span><span class="sxs-lookup"><span data-stu-id="764a9-116">If the frame rate is 29.97 fps, the ratio is 30,000/1001.</span></span>

## <a name="requirements"></a><span data-ttu-id="764a9-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="764a9-117">Requirements</span></span>



| <span data-ttu-id="764a9-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="764a9-118">Requirement</span></span> | <span data-ttu-id="764a9-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="764a9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="764a9-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="764a9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="764a9-121">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="764a9-121">Windows 10 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="764a9-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="764a9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="764a9-123">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="764a9-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="764a9-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="764a9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="764a9-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="764a9-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="764a9-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="764a9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="764a9-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="764a9-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="764a9-128">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="764a9-128">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

