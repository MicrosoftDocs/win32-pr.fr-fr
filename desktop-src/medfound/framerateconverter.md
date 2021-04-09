---
description: Modifie la fréquence d’images d’un flux vidéo.
ms.assetid: a66b9c52-a015-41d2-b27a-3ce6a4d95be9
title: Convertisseur de fréquence d’images DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6197c29e9e753db6f327aa8b2797ba04131448d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749229"
---
# <a name="frame-rate-converter-dsp"></a><span data-ttu-id="cf467-103">Convertisseur de fréquence d’images DSP</span><span class="sxs-lookup"><span data-stu-id="cf467-103">Frame Rate Converter DSP</span></span>

<span data-ttu-id="cf467-104">Modifie la fréquence d’images d’un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="cf467-104">Changes the frame rate of a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="cf467-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="cf467-105">CLSID</span></span>

<span data-ttu-id="cf467-106">CLSID \_ CFrameRateConvertDmo</span><span class="sxs-lookup"><span data-stu-id="cf467-106">CLSID\_CFrameRateConvertDmo</span></span>

## <a name="interfaces"></a><span data-ttu-id="cf467-107">Interfaces</span><span class="sxs-lookup"><span data-stu-id="cf467-107">Interfaces</span></span>

-   <span data-ttu-id="cf467-108">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="cf467-108">**IMediaObject**</span></span>
-   <span data-ttu-id="cf467-109">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="cf467-109">**IMFTransform**</span></span>
-   <span data-ttu-id="cf467-110">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="cf467-110">**IPropertyStore**</span></span>

## <a name="formats"></a><span data-ttu-id="cf467-111">Formats</span><span class="sxs-lookup"><span data-stu-id="cf467-111">Formats</span></span>

-   <span data-ttu-id="cf467-112">ARGB 32</span><span class="sxs-lookup"><span data-stu-id="cf467-112">ARGB 32</span></span>
-   <span data-ttu-id="cf467-113">RVB 24</span><span class="sxs-lookup"><span data-stu-id="cf467-113">RGB 24</span></span>
-   <span data-ttu-id="cf467-114">RGB 32</span><span class="sxs-lookup"><span data-stu-id="cf467-114">RGB 32</span></span>
-   <span data-ttu-id="cf467-115">RGB 555</span><span class="sxs-lookup"><span data-stu-id="cf467-115">RGB 555</span></span>
-   <span data-ttu-id="cf467-116">RGB 565</span><span class="sxs-lookup"><span data-stu-id="cf467-116">RGB 565</span></span>
-   <span data-ttu-id="cf467-117">AYUV</span><span class="sxs-lookup"><span data-stu-id="cf467-117">AYUV</span></span>
-   <span data-ttu-id="cf467-118">IYUV</span><span class="sxs-lookup"><span data-stu-id="cf467-118">IYUV</span></span>
-   <span data-ttu-id="cf467-119">UYVY</span><span class="sxs-lookup"><span data-stu-id="cf467-119">UYVY</span></span>
-   <span data-ttu-id="cf467-120">Y211</span><span class="sxs-lookup"><span data-stu-id="cf467-120">Y211</span></span>
-   <span data-ttu-id="cf467-121">Y411</span><span class="sxs-lookup"><span data-stu-id="cf467-121">Y411</span></span>
-   <span data-ttu-id="cf467-122">Y41P</span><span class="sxs-lookup"><span data-stu-id="cf467-122">Y41P</span></span>
-   <span data-ttu-id="cf467-123">YUY2</span><span class="sxs-lookup"><span data-stu-id="cf467-123">YUY2</span></span>
-   <span data-ttu-id="cf467-124">YUYV</span><span class="sxs-lookup"><span data-stu-id="cf467-124">YUYV</span></span>
-   <span data-ttu-id="cf467-125">YV12</span><span class="sxs-lookup"><span data-stu-id="cf467-125">YV12</span></span>
-   <span data-ttu-id="cf467-126">YVYU</span><span class="sxs-lookup"><span data-stu-id="cf467-126">YVYU</span></span>

## <a name="properties"></a><span data-ttu-id="cf467-127">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cf467-127">Properties</span></span>

-   [<span data-ttu-id="cf467-128">MFPKEY \_ conv \_ INPUTFRAMERATE</span><span class="sxs-lookup"><span data-stu-id="cf467-128">MFPKEY\_CONV\_INPUTFRAMERATE</span></span>](mfpkey-conv-inputframerate.md)
-   [<span data-ttu-id="cf467-129">MFPKEY \_ conv \_ OUTPUTFRAMERATE</span><span class="sxs-lookup"><span data-stu-id="cf467-129">MFPKEY\_CONV\_OUTPUTFRAMERATE</span></span>](mfpkey-conv-outputframerate.md)

## <a name="remarks"></a><span data-ttu-id="cf467-130">Notes</span><span class="sxs-lookup"><span data-stu-id="cf467-130">Remarks</span></span>

<span data-ttu-id="cf467-131">Ce DSP modifie la fréquence d’images en répétant ou en supprimant des frames.</span><span class="sxs-lookup"><span data-stu-id="cf467-131">This DSP changes the frame rate by repeating or dropping frames.</span></span>

<span data-ttu-id="cf467-132">Par défaut, le DSP obtient les fréquences d’images des types de médias.</span><span class="sxs-lookup"><span data-stu-id="cf467-132">By default, the DSP gets the frame rates from the media types.</span></span> <span data-ttu-id="cf467-133">Si vous le souhaitez, vous pouvez spécifier les fréquences d’images en définissant les \_ Propriétés MFPKEY CONV \_ INPUTFRAMERATE et MFPKEY \_ conv \_ OUTPUTFRAMERATE.</span><span class="sxs-lookup"><span data-stu-id="cf467-133">Optionally, you can specify the frame rates by setting the MFPKEY\_CONV\_INPUTFRAMERATE and MFPKEY\_CONV\_OUTPUTFRAMERATE properties.</span></span> <span data-ttu-id="cf467-134">Ces valeurs remplacent la fréquence d’images donnée dans le type de média.</span><span class="sxs-lookup"><span data-stu-id="cf467-134">These values override the frame rate given in the media type.</span></span> <span data-ttu-id="cf467-135">Toutefois, si vous utilisez ce DSP dans le pipeline Media Foundation, vous ne devez pas définir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="cf467-135">However, if you are using this DSP within the Media Foundation pipeline, you should not set these properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf467-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf467-136">Requirements</span></span>



| <span data-ttu-id="cf467-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf467-137">Requirement</span></span> | <span data-ttu-id="cf467-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf467-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf467-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf467-139">Minimum supported client</span></span><br/> | <span data-ttu-id="cf467-140">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf467-140">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cf467-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf467-141">Minimum supported server</span></span><br/> | <span data-ttu-id="cf467-142">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf467-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cf467-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="cf467-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf467-144"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf467-144"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="cf467-145">DLL</span><span class="sxs-lookup"><span data-stu-id="cf467-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf467-146"><dt>Mfvdsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf467-146"><dt>Mfvdsp.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cf467-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf467-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf467-148">Processeurs de signaux numériques</span><span class="sxs-lookup"><span data-stu-id="cf467-148">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




