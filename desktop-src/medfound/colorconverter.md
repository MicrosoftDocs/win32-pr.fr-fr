---
description: Convertit un flux vidéo entre des formats de couleur.
ms.assetid: 1c15dc2b-0e69-4d16-af02-8056a1eb2c5c
title: Convertisseur de couleurs DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a8418d6eeeffcf83a38452b19f18a6baa60bcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484105"
---
# <a name="color-converter-dsp"></a><span data-ttu-id="181cf-103">Convertisseur de couleurs DSP</span><span class="sxs-lookup"><span data-stu-id="181cf-103">Color Converter DSP</span></span>

<span data-ttu-id="181cf-104">Convertit un flux vidéo entre des formats de couleur.</span><span class="sxs-lookup"><span data-stu-id="181cf-104">Converts a video stream between color formats.</span></span>

## <a name="clsid"></a><span data-ttu-id="181cf-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="181cf-105">CLSID</span></span>

<span data-ttu-id="181cf-106">CLSID \_ CColorConvertDMO</span><span class="sxs-lookup"><span data-stu-id="181cf-106">CLSID\_CColorConvertDMO</span></span>

## <a name="interfaces"></a><span data-ttu-id="181cf-107">Interfaces</span><span class="sxs-lookup"><span data-stu-id="181cf-107">Interfaces</span></span>

-   [<span data-ttu-id="181cf-108">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="181cf-108">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [<span data-ttu-id="181cf-109">**IMFRealTimeClient**</span><span class="sxs-lookup"><span data-stu-id="181cf-109">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="181cf-110">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="181cf-110">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="181cf-111">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="181cf-111">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [<span data-ttu-id="181cf-112">IWMColorConvProps</span><span class="sxs-lookup"><span data-stu-id="181cf-112">IWMColorConvProps</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcolorconvprops)

## <a name="input-formats"></a><span data-ttu-id="181cf-113">Formats d’entrée</span><span class="sxs-lookup"><span data-stu-id="181cf-113">Input Formats</span></span>

-   <span data-ttu-id="181cf-114">RVB 24</span><span class="sxs-lookup"><span data-stu-id="181cf-114">RGB 24</span></span>
-   <span data-ttu-id="181cf-115">RGB 32</span><span class="sxs-lookup"><span data-stu-id="181cf-115">RGB 32</span></span>
-   <span data-ttu-id="181cf-116">RGB 555</span><span class="sxs-lookup"><span data-stu-id="181cf-116">RGB 555</span></span>
-   <span data-ttu-id="181cf-117">RGB 565</span><span class="sxs-lookup"><span data-stu-id="181cf-117">RGB 565</span></span>
-   <span data-ttu-id="181cf-118">RVB 8</span><span class="sxs-lookup"><span data-stu-id="181cf-118">RGB 8</span></span>
-   <span data-ttu-id="181cf-119">AYUV</span><span class="sxs-lookup"><span data-stu-id="181cf-119">AYUV</span></span>
-   <span data-ttu-id="181cf-120">I420</span><span class="sxs-lookup"><span data-stu-id="181cf-120">I420</span></span>
-   <span data-ttu-id="181cf-121">IYUV</span><span class="sxs-lookup"><span data-stu-id="181cf-121">IYUV</span></span>
-   <span data-ttu-id="181cf-122">NV11</span><span class="sxs-lookup"><span data-stu-id="181cf-122">NV11</span></span>
-   <span data-ttu-id="181cf-123">NV12</span><span class="sxs-lookup"><span data-stu-id="181cf-123">NV12</span></span>
-   <span data-ttu-id="181cf-124">UYVY</span><span class="sxs-lookup"><span data-stu-id="181cf-124">UYVY</span></span>
-   <span data-ttu-id="181cf-125">V216</span><span class="sxs-lookup"><span data-stu-id="181cf-125">V216</span></span>
-   <span data-ttu-id="181cf-126">V410</span><span class="sxs-lookup"><span data-stu-id="181cf-126">V410</span></span>
-   <span data-ttu-id="181cf-127">Y41P</span><span class="sxs-lookup"><span data-stu-id="181cf-127">Y41P</span></span>
-   <span data-ttu-id="181cf-128">Y41T</span><span class="sxs-lookup"><span data-stu-id="181cf-128">Y41T</span></span>
-   <span data-ttu-id="181cf-129">Y42T</span><span class="sxs-lookup"><span data-stu-id="181cf-129">Y42T</span></span>
-   <span data-ttu-id="181cf-130">YUY2</span><span class="sxs-lookup"><span data-stu-id="181cf-130">YUY2</span></span>
-   <span data-ttu-id="181cf-131">YV12</span><span class="sxs-lookup"><span data-stu-id="181cf-131">YV12</span></span>
-   <span data-ttu-id="181cf-132">YVU9</span><span class="sxs-lookup"><span data-stu-id="181cf-132">YVU9</span></span>
-   <span data-ttu-id="181cf-133">YVYU</span><span class="sxs-lookup"><span data-stu-id="181cf-133">YVYU</span></span>

## <a name="output-formats"></a><span data-ttu-id="181cf-134">Formats de sortie</span><span class="sxs-lookup"><span data-stu-id="181cf-134">Output Formats</span></span>

-   <span data-ttu-id="181cf-135">RVB 24</span><span class="sxs-lookup"><span data-stu-id="181cf-135">RGB 24</span></span>
-   <span data-ttu-id="181cf-136">RGB 32</span><span class="sxs-lookup"><span data-stu-id="181cf-136">RGB 32</span></span>
-   <span data-ttu-id="181cf-137">RGB 555</span><span class="sxs-lookup"><span data-stu-id="181cf-137">RGB 555</span></span>
-   <span data-ttu-id="181cf-138">RGB 565</span><span class="sxs-lookup"><span data-stu-id="181cf-138">RGB 565</span></span>
-   <span data-ttu-id="181cf-139">RVB 8</span><span class="sxs-lookup"><span data-stu-id="181cf-139">RGB 8</span></span>
-   <span data-ttu-id="181cf-140">AYUV</span><span class="sxs-lookup"><span data-stu-id="181cf-140">AYUV</span></span>
-   <span data-ttu-id="181cf-141">I420</span><span class="sxs-lookup"><span data-stu-id="181cf-141">I420</span></span>
-   <span data-ttu-id="181cf-142">IYUV</span><span class="sxs-lookup"><span data-stu-id="181cf-142">IYUV</span></span>
-   <span data-ttu-id="181cf-143">NV11</span><span class="sxs-lookup"><span data-stu-id="181cf-143">NV11</span></span>
-   <span data-ttu-id="181cf-144">NV12</span><span class="sxs-lookup"><span data-stu-id="181cf-144">NV12</span></span>
-   <span data-ttu-id="181cf-145">UYVY</span><span class="sxs-lookup"><span data-stu-id="181cf-145">UYVY</span></span>
-   <span data-ttu-id="181cf-146">V216</span><span class="sxs-lookup"><span data-stu-id="181cf-146">V216</span></span>
-   <span data-ttu-id="181cf-147">V410</span><span class="sxs-lookup"><span data-stu-id="181cf-147">V410</span></span>
-   <span data-ttu-id="181cf-148">YUY2</span><span class="sxs-lookup"><span data-stu-id="181cf-148">YUY2</span></span>
-   <span data-ttu-id="181cf-149">YV12</span><span class="sxs-lookup"><span data-stu-id="181cf-149">YV12</span></span>
-   <span data-ttu-id="181cf-150">YVYU</span><span class="sxs-lookup"><span data-stu-id="181cf-150">YVYU</span></span>

## <a name="properties"></a><span data-ttu-id="181cf-151">Propriétés</span><span class="sxs-lookup"><span data-stu-id="181cf-151">Properties</span></span>

-   [<span data-ttu-id="181cf-152">MFPKEY \_ COLORCONV \_ SRCLEFT</span><span class="sxs-lookup"><span data-stu-id="181cf-152">MFPKEY\_COLORCONV\_SRCLEFT</span></span>](mfpkey-colorconv-srcleft.md)
-   [<span data-ttu-id="181cf-153">MFPKEY \_ COLORCONV \_ SRCTOP</span><span class="sxs-lookup"><span data-stu-id="181cf-153">MFPKEY\_COLORCONV\_SRCTOP</span></span>](mfpkey-colorconv-srctop.md)
-   [<span data-ttu-id="181cf-154">MFPKEY \_ COLORCONV \_ DSTLEFT</span><span class="sxs-lookup"><span data-stu-id="181cf-154">MFPKEY\_COLORCONV\_DSTLEFT</span></span>](mfpkey-colorconv-dstleft.md)
-   [<span data-ttu-id="181cf-155">MFPKEY \_ COLORCONV \_ DSTTOP</span><span class="sxs-lookup"><span data-stu-id="181cf-155">MFPKEY\_COLORCONV\_DSTTOP</span></span>](mfpkey-colorconv-dsttop.md)
-   [<span data-ttu-id="181cf-156">largeur de MFPKEY \_ COLORCONV \_</span><span class="sxs-lookup"><span data-stu-id="181cf-156">MFPKEY\_COLORCONV\_WIDTH</span></span>](mfpkey-colorconv-width.md)
-   [<span data-ttu-id="181cf-157">\_hauteur MFPKEY COLORCONV \_</span><span class="sxs-lookup"><span data-stu-id="181cf-157">MFPKEY\_COLORCONV\_HEIGHT</span></span>](mfpkey-colorconv-height.md)
-   [<span data-ttu-id="181cf-158">MFPKEY \_ \_ mode COLORCONV</span><span class="sxs-lookup"><span data-stu-id="181cf-158">MFPKEY\_COLORCONV\_MODE</span></span>](mfpkey-colorconv-mode.md)

## <a name="remarks"></a><span data-ttu-id="181cf-159">Notes</span><span class="sxs-lookup"><span data-stu-id="181cf-159">Remarks</span></span>

<span data-ttu-id="181cf-160">Le convertisseur de couleur DSP est implémenté en tant qu’objet COM pouvant agir comme un objet DirectXMedia (DMO) ou une transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="181cf-160">The Color Converter DSP is implemented as a COM object that can act as a DirectXMedia Object (DMO) or a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="181cf-161">L’objet a un identificateur de classe unique (CLSID), qu’il agisse comme DMO ou MFT.</span><span class="sxs-lookup"><span data-stu-id="181cf-161">The object has a single class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span> <span data-ttu-id="181cf-162">Pour plus d’informations sur le moment où un DSP agit comme DMO ou MFT, consultez [processeurs de signal numérique](windowsmediadigitalsignalprocessors.md).</span><span class="sxs-lookup"><span data-stu-id="181cf-162">For information about when a DSP acts as a DMO or an MFT, see [Digital Signal Processors](windowsmediadigitalsignalprocessors.md).</span></span>

<span data-ttu-id="181cf-163">Les identificateurs globaux uniques (GUID) pour les sous-types de média RVB diffèrent selon qu’un DSP fait office de modèle DMO ou MFT.</span><span class="sxs-lookup"><span data-stu-id="181cf-163">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="181cf-164">Les GUID pour les sous-types de média non RVB sont les mêmes, qu’un DSP agisse comme DMO ou MFT.</span><span class="sxs-lookup"><span data-stu-id="181cf-164">The GUIDs for non-RGB media subtypes are the same, regardless of whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="181cf-165">Pour plus d’informations sur les GUID qui représentent des sous-types de médias, consultez [GUID de sous-type de vidéo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="181cf-165">For information about the GUIDs that represent media subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="181cf-166">Par défaut, ce DSP copie l’intégralité de l’image source dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="181cf-166">By default, this DSP copies the entire source image to the output buffer.</span></span> <span data-ttu-id="181cf-167">Si vous le souhaitez, vous pouvez spécifier des rectangles sources et de destination.</span><span class="sxs-lookup"><span data-stu-id="181cf-167">Optionally, you can specify source and destination rectangles.</span></span> <span data-ttu-id="181cf-168">Le DSP copie la partie de l’image source définie par le rectangle source et l’écrit dans le rectangle de destination de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="181cf-168">The DSP copies the portion of the source image defined by source rectangle, and writes it into the destination rectangle on the output buffer.</span></span> <span data-ttu-id="181cf-169">Le DSP n’effectue aucune mise à l’échelle ; les rectangles source et de destination doivent avoir la même taille.</span><span class="sxs-lookup"><span data-stu-id="181cf-169">The DSP does not perform any scaling; the source and destination rectangles must be the same size.</span></span> <span data-ttu-id="181cf-170">Les rectangles source et de destination ne peuvent pas dépasser les limites de la trame vidéo.</span><span class="sxs-lookup"><span data-stu-id="181cf-170">The source and destination rectangles cannot exceed the boundaries of the video frame.</span></span>

<span data-ttu-id="181cf-171">Toutes les propriétés, à l’exception du [**\_ \_ mode MFPKEY COLORCONV**](mfpkey-colorconv-mode.md) , doivent être définies dans un groupe.</span><span class="sxs-lookup"><span data-stu-id="181cf-171">All of the properties except [**MFPKEY\_COLORCONV\_MODE**](mfpkey-colorconv-mode.md) must be set in a group.</span></span> <span data-ttu-id="181cf-172">Si vous définissez l’une de ces propriétés, vous devez définir tous les autres.</span><span class="sxs-lookup"><span data-stu-id="181cf-172">If you set any of these properties, you must set all of the others.</span></span> <span data-ttu-id="181cf-173">Dans le cas contraire, les rectangles source et de destination peuvent être non valides, auquel cas les méthodes [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) et [**IMediaObject ::P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) retournent **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="181cf-173">Otherwise, the source and destination rectangles might be invalid, in which case both the [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) and [**IMediaObject::ProcessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) methods will return **E\_INVALIDARG**.</span></span>

<span data-ttu-id="181cf-174">Le convertisseur de couleur ne prend pas en charge toutes les combinaisons de format d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="181cf-174">The color converter does not support every combination of input format and output format.</span></span> <span data-ttu-id="181cf-175">En règle générale, vous devez définir le format de média que vous connaissez, en entrée ou en sortie, puis énumérer les formats disponibles sur le flux de données opposé.</span><span class="sxs-lookup"><span data-stu-id="181cf-175">Usually, you should set the media format that you know, either input or output, and then enumerate the available formats on the opposite stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="181cf-176">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="181cf-176">Requirements</span></span>



| <span data-ttu-id="181cf-177">Condition requise</span><span class="sxs-lookup"><span data-stu-id="181cf-177">Requirement</span></span> | <span data-ttu-id="181cf-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="181cf-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="181cf-179">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="181cf-179">Minimum supported client</span></span><br/> | <span data-ttu-id="181cf-180">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="181cf-180">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="181cf-181">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="181cf-181">Minimum supported server</span></span><br/> | <span data-ttu-id="181cf-182">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="181cf-182">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="181cf-183">En-tête</span><span class="sxs-lookup"><span data-stu-id="181cf-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="181cf-184"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="181cf-184"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="181cf-185">DLL</span><span class="sxs-lookup"><span data-stu-id="181cf-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="181cf-186"><dt>Colorcnv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="181cf-186"><dt>Colorcnv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="181cf-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="181cf-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="181cf-188">Processeurs de signaux numériques</span><span class="sxs-lookup"><span data-stu-id="181cf-188">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
