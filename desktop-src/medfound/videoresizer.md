---
description: Redimensionne un flux vidéo.
ms.assetid: 4acd6366-1abf-43f3-b6c9-4ea17a335cec
title: Dimensionnement vidéo DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7826f21cadc6d30bc2b8b04bbcc741c2bf31bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519578"
---
# <a name="video-resizer-dsp"></a><span data-ttu-id="84ac7-103">Dimensionnement vidéo DSP</span><span class="sxs-lookup"><span data-stu-id="84ac7-103">Video Resizer DSP</span></span>

<span data-ttu-id="84ac7-104">Redimensionne un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="84ac7-104">Resizes a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="84ac7-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="84ac7-105">CLSID</span></span>

<span data-ttu-id="84ac7-106">CLSID \_ CResizerDMO</span><span class="sxs-lookup"><span data-stu-id="84ac7-106">CLSID\_CResizerDMO</span></span>

## <a name="interfaces"></a><span data-ttu-id="84ac7-107">Interfaces</span><span class="sxs-lookup"><span data-stu-id="84ac7-107">Interfaces</span></span>

-   [<span data-ttu-id="84ac7-108">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="84ac7-108">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [<span data-ttu-id="84ac7-109">**IMFRealTimeClient**</span><span class="sxs-lookup"><span data-stu-id="84ac7-109">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="84ac7-110">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="84ac7-110">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="84ac7-111">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="84ac7-111">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [<span data-ttu-id="84ac7-112">**IWMResizerProps**</span><span class="sxs-lookup"><span data-stu-id="84ac7-112">**IWMResizerProps**</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops)

## <a name="formats"></a><span data-ttu-id="84ac7-113">Formats</span><span class="sxs-lookup"><span data-stu-id="84ac7-113">Formats</span></span>

<span data-ttu-id="84ac7-114">Le redimensionnement vidéo DSP prend en charge les sous-types de médias d’entrée/sortie suivants lorsqu’il agit comme un objet de média DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="84ac7-114">The Video Resizer DSP supports the following input/output media subtypes when it is acting as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="84ac7-115">MEDIASUBTYPE \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="84ac7-115">MEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="84ac7-116">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="84ac7-116">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="84ac7-117">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="84ac7-117">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="84ac7-118">MEDIASUBTYPE \_ I420</span><span class="sxs-lookup"><span data-stu-id="84ac7-118">MEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="84ac7-119">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="84ac7-119">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="84ac7-120">MEDIASUBTYPE \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="84ac7-120">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="84ac7-121">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="84ac7-121">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="84ac7-122">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="84ac7-122">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="84ac7-123">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="84ac7-123">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="84ac7-124">MEDIASUBTYPE \_ AYUV</span><span class="sxs-lookup"><span data-stu-id="84ac7-124">MEDIASUBTYPE\_AYUV</span></span>
-   <span data-ttu-id="84ac7-125">MEDIASUBTYPE \_ V216</span><span class="sxs-lookup"><span data-stu-id="84ac7-125">MEDIASUBTYPE\_V216</span></span>
-   <span data-ttu-id="84ac7-126">MEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="84ac7-126">MEDIASUBTYPE\_YV12</span></span>

<span data-ttu-id="84ac7-127">Le redimensionnement vidéo DSP prend en charge les sous-types de médias d’entrée/sortie suivants lorsqu’il joue le rôle d’une transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="84ac7-127">The Video Resizer DSP supports the following input/output media subtypes when it is acting as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="84ac7-128">MFVideoFormat \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="84ac7-128">MFVideoFormat\_IYUV</span></span>
-   <span data-ttu-id="84ac7-129">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="84ac7-129">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="84ac7-130">MFVideoFormat \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="84ac7-130">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="84ac7-131">MFVideoFormat \_ I420</span><span class="sxs-lookup"><span data-stu-id="84ac7-131">MFVideoFormat\_I420</span></span>
-   <span data-ttu-id="84ac7-132">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="84ac7-132">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="84ac7-133">MFVideoFormat \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="84ac7-133">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="84ac7-134">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="84ac7-134">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="84ac7-135">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="84ac7-135">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="84ac7-136">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="84ac7-136">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="84ac7-137">MFVideoFormat \_ AYUV</span><span class="sxs-lookup"><span data-stu-id="84ac7-137">MFVideoFormat\_AYUV</span></span>
-   <span data-ttu-id="84ac7-138">MFVideoFormat \_ V216</span><span class="sxs-lookup"><span data-stu-id="84ac7-138">MFVideoFormat\_V216</span></span>
-   <span data-ttu-id="84ac7-139">MFVideoFormat \_ YV12</span><span class="sxs-lookup"><span data-stu-id="84ac7-139">MFVideoFormat\_YV12</span></span>

## <a name="properties"></a><span data-ttu-id="84ac7-140">Propriétés</span><span class="sxs-lookup"><span data-stu-id="84ac7-140">Properties</span></span>

-   [<span data-ttu-id="84ac7-141">MFPKEY \_ REdimensionner \_ SRC à \_ gauche</span><span class="sxs-lookup"><span data-stu-id="84ac7-141">MFPKEY\_RESIZE\_SRC\_LEFT</span></span>](mfpkey-resize-src-left.md)
-   [<span data-ttu-id="84ac7-142">MFPKEY \_ REdimensionner \_ SRC en \_ haut</span><span class="sxs-lookup"><span data-stu-id="84ac7-142">MFPKEY\_RESIZE\_SRC\_TOP</span></span>](mfpkey-resize-src-top.md)
-   [<span data-ttu-id="84ac7-143">MFPKEY \_ REdimensionner la \_ \_ largeur SRC</span><span class="sxs-lookup"><span data-stu-id="84ac7-143">MFPKEY\_RESIZE\_SRC\_WIDTH</span></span>](mfpkey-resize-src-width.md)
-   [<span data-ttu-id="84ac7-144">MFPKEY \_ REdimensionner la \_ \_ hauteur SRC</span><span class="sxs-lookup"><span data-stu-id="84ac7-144">MFPKEY\_RESIZE\_SRC\_HEIGHT</span></span>](mfpkey-resize-src-height.md)
-   [<span data-ttu-id="84ac7-145">MFPKEY \_ REdimensionner l' \_ heure d’été à \_ gauche</span><span class="sxs-lookup"><span data-stu-id="84ac7-145">MFPKEY\_RESIZE\_DST\_LEFT</span></span>](mfpkey-resize-dst-left.md)
-   [<span data-ttu-id="84ac7-146">MFPKEY \_ REdimensionner l' \_ heure d’été en \_ haut</span><span class="sxs-lookup"><span data-stu-id="84ac7-146">MFPKEY\_RESIZE\_DST\_TOP</span></span>](mfpkey-resize-dst-top.md)
-   [<span data-ttu-id="84ac7-147">largeur de l' \_ heure d’été de REdimensionnement MFPKEY \_ \_</span><span class="sxs-lookup"><span data-stu-id="84ac7-147">MFPKEY\_RESIZE\_DST\_WIDTH</span></span>](mfpkey-resize-dst-width.md)
-   [<span data-ttu-id="84ac7-148">\_hauteur MFPKEY REdimensionner l' \_ heure d’été \_</span><span class="sxs-lookup"><span data-stu-id="84ac7-148">MFPKEY\_RESIZE\_DST\_HEIGHT</span></span>](mfpkey-resize-dst-height.md)
-   [<span data-ttu-id="84ac7-149">\_qualité de REdimensionnement MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="84ac7-149">MFPKEY\_RESIZE\_QUALITY</span></span>](mfpkey-resize-quality.md)
-   [<span data-ttu-id="84ac7-150">\_entrelacement de REdimensionnement MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="84ac7-150">MFPKEY\_RESIZE\_INTERLACE</span></span>](mfpkey-resize-interlace.md)
-   [<span data-ttu-id="84ac7-151">MFPKEY \_ REdimensionner \_ GEOMAPX</span><span class="sxs-lookup"><span data-stu-id="84ac7-151">MFPKEY\_RESIZE\_GEOMAPX</span></span>](mfpkey-resize-geomapx.md)
-   [<span data-ttu-id="84ac7-152">MFPKEY \_ REdimensionner \_ GEOMAPY</span><span class="sxs-lookup"><span data-stu-id="84ac7-152">MFPKEY\_RESIZE\_GEOMAPY</span></span>](mfpkey-resize-geomapy.md)
-   [<span data-ttu-id="84ac7-153">MFPKEY \_ REdimensionner \_ GEOMAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="84ac7-153">MFPKEY\_RESIZE\_GEOMAPWIDTH</span></span>](mfpkey-resize-geomapwidth.md)
-   [<span data-ttu-id="84ac7-154">MFPKEY \_ REdimensionner \_ GEOMAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="84ac7-154">MFPKEY\_RESIZE\_GEOMAPHEIGHT</span></span>](mfpkey-resize-geomapheight.md)
-   [<span data-ttu-id="84ac7-155">MFPKEY \_ REdimensionner \_ MINAPX</span><span class="sxs-lookup"><span data-stu-id="84ac7-155">MFPKEY\_RESIZE\_MINAPX</span></span>](mfpkey-resize-minapx.md)
-   [<span data-ttu-id="84ac7-156">MFPKEY \_ REdimensionner \_ MINAPY</span><span class="sxs-lookup"><span data-stu-id="84ac7-156">MFPKEY\_RESIZE\_MINAPY</span></span>](mfpkey-resize-minapy.md)
-   [<span data-ttu-id="84ac7-157">MFPKEY \_ REdimensionner \_ MINAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="84ac7-157">MFPKEY\_RESIZE\_MINAPWIDTH</span></span>](mfpkey-resize-minapwidth.md)
-   [<span data-ttu-id="84ac7-158">MFPKEY \_ REdimensionner \_ MINAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="84ac7-158">MFPKEY\_RESIZE\_MINAPHEIGHT</span></span>](mfpkey-resize-minapheight.md)
-   [<span data-ttu-id="84ac7-159">MFPKEY \_ REdimensionner \_ PANSCANAPX</span><span class="sxs-lookup"><span data-stu-id="84ac7-159">MFPKEY\_RESIZE\_PANSCANAPX</span></span>](mfpkey-resize-panscanapx.md)
-   [<span data-ttu-id="84ac7-160">MFPKEY \_ REdimensionner \_ PANSCANAPY</span><span class="sxs-lookup"><span data-stu-id="84ac7-160">MFPKEY\_RESIZE\_PANSCANAPY</span></span>](mfpkey-resize-panscanapy.md)
-   [<span data-ttu-id="84ac7-161">MFPKEY \_ REdimensionner \_ PANSCANAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="84ac7-161">MFPKEY\_RESIZE\_PANSCANAPWIDTH</span></span>](mfpkey-resize-panscanapwidth.md)
-   [<span data-ttu-id="84ac7-162">MFPKEY \_ REdimensionner \_ PANSCANAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="84ac7-162">MFPKEY\_RESIZE\_PANSCANAPHEIGHT</span></span>](mfpkey-resize-panscanapheight.md)
-   [<span data-ttu-id="84ac7-163">MFPKEY \_ PIXELASPECTRATIO</span><span class="sxs-lookup"><span data-stu-id="84ac7-163">MFPKEY\_PIXELASPECTRATIO</span></span>](mfpkey-pixelaspectratio.md)

## <a name="remarks"></a><span data-ttu-id="84ac7-164">Notes</span><span class="sxs-lookup"><span data-stu-id="84ac7-164">Remarks</span></span>

<span data-ttu-id="84ac7-165">Le rôle d’application vidéo redimensionnement DSP est implémenté en tant qu’objet COM pouvant agir comme DMO ou MFT.</span><span class="sxs-lookup"><span data-stu-id="84ac7-165">The Video Resizer DSP is implemented as a COM object that can act as a DMO or an MFT.</span></span> <span data-ttu-id="84ac7-166">L’objet a un identificateur de classe unique (CLSID), qu’il agisse comme DMO ou MFT.</span><span class="sxs-lookup"><span data-stu-id="84ac7-166">The object has a single class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span> <span data-ttu-id="84ac7-167">Pour plus d’informations sur le moment où un DSP agit comme DMO ou MFT, consultez [processeurs de signal numérique](windowsmediadigitalsignalprocessors.md).</span><span class="sxs-lookup"><span data-stu-id="84ac7-167">For information about when a DSP acts as a DMO or an MFT, see [Digital Signal Processors](windowsmediadigitalsignalprocessors.md).</span></span>

<span data-ttu-id="84ac7-168">Les identificateurs globaux uniques (GUID) pour les sous-types de média RVB diffèrent selon qu’un DSP fait office de modèle DMO ou MFT.</span><span class="sxs-lookup"><span data-stu-id="84ac7-168">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="84ac7-169">Les GUID pour les sous-types de média non RVB sont les mêmes, qu’un DSP agisse comme DMO ou MFT.</span><span class="sxs-lookup"><span data-stu-id="84ac7-169">The GUIDs for non-RGB media subtypes are the same, regardless of whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="84ac7-170">Pour plus d’informations sur les GUID qui représentent des sous-types de médias, consultez [GUID de sous-type de vidéo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="84ac7-170">For information about the GUIDs that represent media subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="84ac7-171">Ce DSP peut effectuer des opérations de rognage et de mise à l’échelle sur l’image vidéo.</span><span class="sxs-lookup"><span data-stu-id="84ac7-171">This DSP can perform both cropping and scaling on the video image.</span></span> <span data-ttu-id="84ac7-172">Le format du type de sortie doit correspondre au format du type d’entrée.</span><span class="sxs-lookup"><span data-stu-id="84ac7-172">The format of the output type must match the format of the input type.</span></span> <span data-ttu-id="84ac7-173">Le DSP n’effectue pas de conversions de l’espace colorimétrique.</span><span class="sxs-lookup"><span data-stu-id="84ac7-173">The DSP does not perform color-space conversions.</span></span>

<span data-ttu-id="84ac7-174">Avant de définir le type de sortie, vous pouvez définir l’une des régions suivantes à l’aide des propriétés listées dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="84ac7-174">Before setting the output type, you can define any of the following regions by using the properties listed in this table.</span></span>



| <span data-ttu-id="84ac7-175">Région</span><span class="sxs-lookup"><span data-stu-id="84ac7-175">Region</span></span>                   | <span data-ttu-id="84ac7-176">Propriétés</span><span class="sxs-lookup"><span data-stu-id="84ac7-176">Properties</span></span>                                                                                                                                                       |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84ac7-177">Rectangle source</span><span class="sxs-lookup"><span data-stu-id="84ac7-177">Source rectangle</span></span>         | <span data-ttu-id="84ac7-178">MFPKEY \_ REdimensionner \_ SRC à \_ gauche</span><span class="sxs-lookup"><span data-stu-id="84ac7-178">MFPKEY\_RESIZE\_SRC\_LEFT</span></span><br/> <span data-ttu-id="84ac7-179">MFPKEY \_ REdimensionner \_ SRC en \_ haut</span><span class="sxs-lookup"><span data-stu-id="84ac7-179">MFPKEY\_RESIZE\_SRC\_TOP</span></span><br/> <span data-ttu-id="84ac7-180">MFPKEY \_ REdimensionner la \_ \_ largeur SRC</span><span class="sxs-lookup"><span data-stu-id="84ac7-180">MFPKEY\_RESIZE\_SRC\_WIDTH</span></span><br/> <span data-ttu-id="84ac7-181">MFPKEY \_ REdimensionner la \_ \_ hauteur SRC</span><span class="sxs-lookup"><span data-stu-id="84ac7-181">MFPKEY\_RESIZE\_SRC\_HEIGHT</span></span><br/>            |
| <span data-ttu-id="84ac7-182">Rectangle de destination</span><span class="sxs-lookup"><span data-stu-id="84ac7-182">Destination rectangle</span></span>    | <span data-ttu-id="84ac7-183">MFPKEY \_ REdimensionner l' \_ heure d’été à \_ gauche</span><span class="sxs-lookup"><span data-stu-id="84ac7-183">MFPKEY\_RESIZE\_DST\_LEFT</span></span><br/> <span data-ttu-id="84ac7-184">MFPKEY \_ REdimensionner l' \_ heure d’été en \_ haut</span><span class="sxs-lookup"><span data-stu-id="84ac7-184">MFPKEY\_RESIZE\_DST\_TOP</span></span><br/> <span data-ttu-id="84ac7-185">largeur de l' \_ heure d’été de REdimensionnement MFPKEY \_ \_</span><span class="sxs-lookup"><span data-stu-id="84ac7-185">MFPKEY\_RESIZE\_DST\_WIDTH</span></span><br/> <span data-ttu-id="84ac7-186">\_hauteur MFPKEY REdimensionner l' \_ heure d’été \_</span><span class="sxs-lookup"><span data-stu-id="84ac7-186">MFPKEY\_RESIZE\_DST\_HEIGHT</span></span><br/>            |
| <span data-ttu-id="84ac7-187">Ouverture géométrique</span><span class="sxs-lookup"><span data-stu-id="84ac7-187">Geometric aperture</span></span>       | <span data-ttu-id="84ac7-188">MFPKEY \_ REdimensionner \_ GEOMAPX</span><span class="sxs-lookup"><span data-stu-id="84ac7-188">MFPKEY\_RESIZE\_GEOMAPX</span></span><br/> <span data-ttu-id="84ac7-189">MFPKEY \_ REdimensionner \_ GEOMAPY</span><span class="sxs-lookup"><span data-stu-id="84ac7-189">MFPKEY\_RESIZE\_GEOMAPY</span></span><br/> <span data-ttu-id="84ac7-190">MFPKEY \_ REdimensionner \_ GEOMAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="84ac7-190">MFPKEY\_RESIZE\_GEOMAPWIDTH</span></span><br/> <span data-ttu-id="84ac7-191">MFPKEY \_ REdimensionner \_ GEOMAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="84ac7-191">MFPKEY\_RESIZE\_GEOMAPHEIGHT</span></span><br/>             |
| <span data-ttu-id="84ac7-192">Ouverture minimale de l’affichage</span><span class="sxs-lookup"><span data-stu-id="84ac7-192">Minimum display aperture</span></span> | <span data-ttu-id="84ac7-193">MFPKEY \_ REdimensionner \_ MINAPX</span><span class="sxs-lookup"><span data-stu-id="84ac7-193">MFPKEY\_RESIZE\_MINAPX</span></span><br/> <span data-ttu-id="84ac7-194">MFPKEY \_ REdimensionner \_ MINAPY</span><span class="sxs-lookup"><span data-stu-id="84ac7-194">MFPKEY\_RESIZE\_MINAPY</span></span><br/> <span data-ttu-id="84ac7-195">MFPKEY \_ REdimensionner \_ MINAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="84ac7-195">MFPKEY\_RESIZE\_MINAPWIDTH</span></span><br/> <span data-ttu-id="84ac7-196">MFPKEY \_ REdimensionner \_ MINAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="84ac7-196">MFPKEY\_RESIZE\_MINAPHEIGHT</span></span><br/>                 |
| <span data-ttu-id="84ac7-197">Région Pan/Scan</span><span class="sxs-lookup"><span data-stu-id="84ac7-197">Pan/scan region</span></span>          | <span data-ttu-id="84ac7-198">MFPKEY \_ REdimensionner \_ PANSCANAPX</span><span class="sxs-lookup"><span data-stu-id="84ac7-198">MFPKEY\_RESIZE\_PANSCANAPX</span></span><br/> <span data-ttu-id="84ac7-199">MFPKEY \_ REdimensionner \_ PANSCANAPY</span><span class="sxs-lookup"><span data-stu-id="84ac7-199">MFPKEY\_RESIZE\_PANSCANAPY</span></span><br/> <span data-ttu-id="84ac7-200">MFPKEY \_ REdimensionner \_ PANSCANAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="84ac7-200">MFPKEY\_RESIZE\_PANSCANAPWIDTH</span></span><br/> <span data-ttu-id="84ac7-201">MFPKEY \_ REdimensionner \_ PANSCANAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="84ac7-201">MFPKEY\_RESIZE\_PANSCANAPHEIGHT</span></span><br/> |



 

<span data-ttu-id="84ac7-202">Dans chaque cas, vous devez définir toutes les propriétés associées pour que le paramètre prenne effet.</span><span class="sxs-lookup"><span data-stu-id="84ac7-202">In each case, you must set all of the associated properties for the setting to take effect.</span></span>

<span data-ttu-id="84ac7-203">Le DSP copie la partie de l’image source définie par le rectangle source et l’étire ou le compresse sur le rectangle de destination de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="84ac7-203">The DSP copies the portion of the source image defined by source rectangle, and stretches or compresses it onto the destination rectangle on the output buffer.</span></span> <span data-ttu-id="84ac7-204">Les rectangles source et de destination n’ont pas besoin d’être de la même taille.</span><span class="sxs-lookup"><span data-stu-id="84ac7-204">The source and destination rectangles do not need to be the same size.</span></span> <span data-ttu-id="84ac7-205">La taille de trame dans le type de média de sortie doit être suffisamment grande pour contenir le rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="84ac7-205">The frame size in the output media type must be large enough to hold the destination rectangle.</span></span>

<span data-ttu-id="84ac7-206">L’ouverture géométrique, la zone d’affichage minimale et la région de panoramique/numérisation n’affectent pas la manière dont le DSP redimensionne la vidéo.</span><span class="sxs-lookup"><span data-stu-id="84ac7-206">The geometric aperture, minimum display aperture, and pan/scan region do not affect how the DSP resizes the video.</span></span> <span data-ttu-id="84ac7-207">Toutefois, ils peuvent affecter la façon dont le composant en aval interprète la trame vidéo.</span><span class="sxs-lookup"><span data-stu-id="84ac7-207">However, they might affect how the downstream component interprets the video frame.</span></span> <span data-ttu-id="84ac7-208">En particulier, le convertisseur vidéo amélioré (EVR) utilise ces valeurs lorsqu’il calcule les proportions de l’image et la zone d’affichage.</span><span class="sxs-lookup"><span data-stu-id="84ac7-208">In particular, the enhanced video renderer (EVR) uses these values when it calculates the picture aspect ratio and the display area.</span></span>

<span data-ttu-id="84ac7-209">Si vous utilisez Media Foundation types de média, vous pouvez définir l’ouverture géométrique, l’ouverture minimale d’affichage et les régions Pan/Scan directement dans le type de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="84ac7-209">If you are using Media Foundation media types, you can set the geometric aperture, minimum display aperture, and pan/scan regions directly in the output media type.</span></span> <span data-ttu-id="84ac7-210">Dans le cas contraire, si vous utilisez des types de média DMO, définissez-les à l’aide des propriétés.</span><span class="sxs-lookup"><span data-stu-id="84ac7-210">Otherwise, if you are using DMO media types, set them using the properties.</span></span>

<span data-ttu-id="84ac7-211">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="84ac7-211">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="84ac7-212">**\_ \_ ouverture géométrique MF \_ MF**</span><span class="sxs-lookup"><span data-stu-id="84ac7-212">**MF\_MT\_GEOMETRIC\_APERTURE**</span></span>](mf-mt-geometric-aperture-attribute.md)
-   [<span data-ttu-id="84ac7-213">**\_ouverture de \_ l' \_ affichage \_ de la version MF**</span><span class="sxs-lookup"><span data-stu-id="84ac7-213">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
-   [<span data-ttu-id="84ac7-214">**\_ouverture de \_ l' \_ analyse \_ panoramique MF MT**</span><span class="sxs-lookup"><span data-stu-id="84ac7-214">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)

## <a name="requirements"></a><span data-ttu-id="84ac7-215">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84ac7-215">Requirements</span></span>



| <span data-ttu-id="84ac7-216">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84ac7-216">Requirement</span></span> | <span data-ttu-id="84ac7-217">Valeur</span><span class="sxs-lookup"><span data-stu-id="84ac7-217">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84ac7-218">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84ac7-218">Minimum supported client</span></span><br/> | <span data-ttu-id="84ac7-219">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84ac7-219">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="84ac7-220">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84ac7-220">Minimum supported server</span></span><br/> | <span data-ttu-id="84ac7-221">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84ac7-221">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="84ac7-222">En-tête</span><span class="sxs-lookup"><span data-stu-id="84ac7-222">Header</span></span><br/>                   | <dl> <span data-ttu-id="84ac7-223"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="84ac7-223"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="84ac7-224">DLL</span><span class="sxs-lookup"><span data-stu-id="84ac7-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84ac7-225"><dt>Vidreszr.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84ac7-225"><dt>Vidreszr.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84ac7-226">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84ac7-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84ac7-227">Processeurs de signaux numériques</span><span class="sxs-lookup"><span data-stu-id="84ac7-227">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
