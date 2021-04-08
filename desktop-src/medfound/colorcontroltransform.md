---
description: Ajuste les caractéristiques de couleur d’un flux vidéo.
ms.assetid: 738c1f0c-8417-4b12-a7f1-9bbf3c7e9dd3
title: Transformation de contrôle de couleur DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b94c8314bfd2be85a3bbc392bfa0e83767ff0b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749348"
---
# <a name="color-control-transform-dsp"></a><span data-ttu-id="e7a66-103">Transformation de contrôle de couleur DSP</span><span class="sxs-lookup"><span data-stu-id="e7a66-103">Color Control Transform DSP</span></span>

<span data-ttu-id="e7a66-104">Ajuste les caractéristiques de couleur d’un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="e7a66-104">Adjusts the color characteristics of a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="e7a66-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="e7a66-105">CLSID</span></span>

<span data-ttu-id="e7a66-106">CLSID \_ CColorControlDmo</span><span class="sxs-lookup"><span data-stu-id="e7a66-106">CLSID\_CColorControlDmo</span></span>

## <a name="interfaces"></a><span data-ttu-id="e7a66-107">Interfaces</span><span class="sxs-lookup"><span data-stu-id="e7a66-107">Interfaces</span></span>

-   <span data-ttu-id="e7a66-108">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="e7a66-108">**IMediaObject**</span></span>
-   <span data-ttu-id="e7a66-109">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="e7a66-109">**IMFTransform**</span></span>
-   <span data-ttu-id="e7a66-110">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="e7a66-110">**IPropertyStore**</span></span>

## <a name="formats"></a><span data-ttu-id="e7a66-111">Formats</span><span class="sxs-lookup"><span data-stu-id="e7a66-111">Formats</span></span>

-   <span data-ttu-id="e7a66-112">RVB 24</span><span class="sxs-lookup"><span data-stu-id="e7a66-112">RGB 24</span></span>
-   <span data-ttu-id="e7a66-113">RGB 32</span><span class="sxs-lookup"><span data-stu-id="e7a66-113">RGB 32</span></span>
-   <span data-ttu-id="e7a66-114">RGB 555</span><span class="sxs-lookup"><span data-stu-id="e7a66-114">RGB 555</span></span>
-   <span data-ttu-id="e7a66-115">RGB 565</span><span class="sxs-lookup"><span data-stu-id="e7a66-115">RGB 565</span></span>
-   <span data-ttu-id="e7a66-116">AYUV</span><span class="sxs-lookup"><span data-stu-id="e7a66-116">AYUV</span></span>
-   <span data-ttu-id="e7a66-117">UYVY</span><span class="sxs-lookup"><span data-stu-id="e7a66-117">UYVY</span></span>
-   <span data-ttu-id="e7a66-118">YUY2</span><span class="sxs-lookup"><span data-stu-id="e7a66-118">YUY2</span></span>
-   <span data-ttu-id="e7a66-119">YV12</span><span class="sxs-lookup"><span data-stu-id="e7a66-119">YV12</span></span>

## <a name="properties"></a><span data-ttu-id="e7a66-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e7a66-120">Properties</span></span>

-   [<span data-ttu-id="e7a66-121">\_luminosité des couleurs MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="e7a66-121">MFPKEY\_COLOR\_BRIGHTNESS</span></span>](mfpkey-color-brightness.md)
-   [<span data-ttu-id="e7a66-122">\_contraste des couleurs MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="e7a66-122">MFPKEY\_COLOR\_CONTRAST</span></span>](mfpkey-color-contrast.md)
-   [<span data-ttu-id="e7a66-123">\_teinte de couleur MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="e7a66-123">MFPKEY\_COLOR\_HUE</span></span>](mfpkey-color-hue.md)
-   [<span data-ttu-id="e7a66-124">SATURATION de la \_ couleur MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="e7a66-124">MFPKEY\_COLOR\_SATURATION</span></span>](mfpkey-color-saturation.md)

## <a name="remarks"></a><span data-ttu-id="e7a66-125">Notes</span><span class="sxs-lookup"><span data-stu-id="e7a66-125">Remarks</span></span>

<span data-ttu-id="e7a66-126">Ce DSP modifie le contenu du flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="e7a66-126">This DSP modifies the contents of the video stream.</span></span> <span data-ttu-id="e7a66-127">Pour la lecture, vous pourrez peut-être obtenir des effets similaires plus efficacement à l’aide de l’interface **IMFVideoProcessor** , qui contrôle le traitement vidéo dans la carte graphique.</span><span class="sxs-lookup"><span data-stu-id="e7a66-127">For playback, you might be able to achieve similar effects more efficiently by using the **IMFVideoProcessor** interface, which controls video processing in the graphics card.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7a66-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7a66-128">Requirements</span></span>



| <span data-ttu-id="e7a66-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7a66-129">Requirement</span></span> | <span data-ttu-id="e7a66-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7a66-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7a66-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7a66-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e7a66-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7a66-132">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e7a66-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7a66-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e7a66-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7a66-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e7a66-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7a66-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7a66-136"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7a66-136"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="e7a66-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e7a66-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7a66-138"><dt>Mfvdsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7a66-138"><dt>Mfvdsp.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e7a66-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7a66-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7a66-140">Processeurs de signaux numériques</span><span class="sxs-lookup"><span data-stu-id="e7a66-140">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




