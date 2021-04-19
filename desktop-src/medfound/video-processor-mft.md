---
description: La MFT du processeur vidéo est une Microsoft Media Foundation transformation (MFT) qui effectue la conversion colorspace, le redimensionnement vidéo, le désentrelacement, la conversion de la fréquence d’images, la rotation, le rognage, la décompression et la mise en miroir de la vue spatiale gauche et droite.
ms.assetid: 1476995A-9692-4B08-8EF7-7DB6321BEC24
title: MFT du processeur vidéo (Camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53783b42073414e4dc440546698bf295b404dcc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535383"
---
# <a name="video-processor-mft"></a><span data-ttu-id="cf7c6-103">MFT du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="cf7c6-103">Video Processor MFT</span></span>

<span data-ttu-id="cf7c6-104">La MFT du processeur vidéo est une Microsoft Media Foundation transformation (MFT) qui effectue la conversion colorspace, le redimensionnement vidéo, le désentrelacement, la conversion de la fréquence d’images, la rotation, le rognage, la décompression et la mise en miroir de la vue spatiale gauche et droite.</span><span class="sxs-lookup"><span data-stu-id="cf7c6-104">The video processor MFT is a Microsoft Media Foundation transform (MFT) that performs colorspace conversion, video resizing, deinterlacing, frame rate conversion, rotation, cropping, spatial left and right view unpacking, and mirroring.</span></span>

## <a name="clsid"></a><span data-ttu-id="cf7c6-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="cf7c6-105">CLSID</span></span>

<span data-ttu-id="cf7c6-106">CLSID \_ VideoProcessorMFT</span><span class="sxs-lookup"><span data-stu-id="cf7c6-106">CLSID\_VideoProcessorMFT</span></span>

## <a name="interfaces"></a><span data-ttu-id="cf7c6-107">Interfaces</span><span class="sxs-lookup"><span data-stu-id="cf7c6-107">Interfaces</span></span>

-   [<span data-ttu-id="cf7c6-108">**IMFRealTimeClientEx**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-108">**IMFRealTimeClientEx**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)
-   [<span data-ttu-id="cf7c6-109">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-109">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="cf7c6-110">**IMFVideoProcessorControl**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-110">**IMFVideoProcessorControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol)

## <a name="input-formats"></a><span data-ttu-id="cf7c6-111">Formats d’entrée</span><span class="sxs-lookup"><span data-stu-id="cf7c6-111">Input Formats</span></span>

-   <span data-ttu-id="cf7c6-112">**MFVideoFormat \_ ARGB32**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-112">**MFVideoFormat\_ARGB32**</span></span>
-   <span data-ttu-id="cf7c6-113">**MFVideoFormat \_ AYUV**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-113">**MFVideoFormat\_AYUV**</span></span>
-   <span data-ttu-id="cf7c6-114">**MFVideoFormat \_ I420**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-114">**MFVideoFormat\_I420**</span></span>
-   <span data-ttu-id="cf7c6-115">**MFVideoFormat \_ IYUV**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-115">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="cf7c6-116">**MFVideoFormat \_ NV11**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-116">**MFVideoFormat\_NV11**</span></span>
-   <span data-ttu-id="cf7c6-117">**MFVideoFormat \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-117">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="cf7c6-118">**MFVideoFormat \_ Rgb24**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-118">**MFVideoFormat\_RGB24**</span></span>
-   <span data-ttu-id="cf7c6-119">**MFVideoFormat \_ RGB32**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-119">**MFVideoFormat\_RGB32**</span></span>
-   <span data-ttu-id="cf7c6-120">**MFVideoFormat \_ RGB555**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-120">**MFVideoFormat\_RGB555**</span></span>
-   <span data-ttu-id="cf7c6-121">**MFVideoFormat \_ RGB565**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-121">**MFVideoFormat\_RGB565**</span></span>
-   <span data-ttu-id="cf7c6-122">**MFVideoFormat \_ RGB8**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-122">**MFVideoFormat\_RGB8**</span></span>
-   <span data-ttu-id="cf7c6-123">**MFVideoFormat \_ UYVY**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-123">**MFVideoFormat\_UYVY**</span></span>
-   <span data-ttu-id="cf7c6-124">**MFVideoFormat \_ V410**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-124">**MFVideoFormat\_v410**</span></span>
-   <span data-ttu-id="cf7c6-125">**MFVideoFormat \_ Y216**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-125">**MFVideoFormat\_Y216**</span></span>
-   <span data-ttu-id="cf7c6-126">**MFVideoFormat \_ Y41P**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-126">**MFVideoFormat\_Y41P**</span></span>
-   <span data-ttu-id="cf7c6-127">**MFVideoFormat \_ Y41T**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-127">**MFVideoFormat\_Y41T**</span></span>
-   <span data-ttu-id="cf7c6-128">**MFVideoFormat \_ Y42T**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-128">**MFVideoFormat\_Y42T**</span></span>
-   <span data-ttu-id="cf7c6-129">**MFVideoFormat \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-129">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="cf7c6-130">**MFVideoFormat \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-130">**MFVideoFormat\_YV12**</span></span>
-   <span data-ttu-id="cf7c6-131">**MFVideoFormat \_ YVYU**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-131">**MFVideoFormat\_YVYU**</span></span>

## <a name="output-formats"></a><span data-ttu-id="cf7c6-132">Formats de sortie</span><span class="sxs-lookup"><span data-stu-id="cf7c6-132">Output Formats</span></span>

-   <span data-ttu-id="cf7c6-133">**MFVideoFormat \_ ARGB32**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-133">**MFVideoFormat\_ARGB32**</span></span>
-   <span data-ttu-id="cf7c6-134">**MFVideoFormat \_ AYUV**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-134">**MFVideoFormat\_AYUV**</span></span>
-   <span data-ttu-id="cf7c6-135">**MFVideoFormat \_ I420**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-135">**MFVideoFormat\_I420**</span></span>
-   <span data-ttu-id="cf7c6-136">**MFVideoFormat \_ IYUV**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-136">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="cf7c6-137">**MFVideoFormat \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-137">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="cf7c6-138">**MFVideoFormat \_ Rgb24**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-138">**MFVideoFormat\_RGB24**</span></span>
-   <span data-ttu-id="cf7c6-139">**MFVideoFormat \_ RGB32**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-139">**MFVideoFormat\_RGB32**</span></span>
-   <span data-ttu-id="cf7c6-140">**MFVideoFormat \_ RGB555**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-140">**MFVideoFormat\_RGB555**</span></span>
-   <span data-ttu-id="cf7c6-141">**MFVideoFormat \_ RGB565**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-141">**MFVideoFormat\_RGB565**</span></span>
-   <span data-ttu-id="cf7c6-142">**MFVideoFormat \_ UYVY**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-142">**MFVideoFormat\_UYVY**</span></span>
-   <span data-ttu-id="cf7c6-143">**MFVideoFormat \_ Y216**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-143">**MFVideoFormat\_Y216**</span></span>
-   <span data-ttu-id="cf7c6-144">**MFVideoFormat \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-144">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="cf7c6-145">**MFVideoFormat \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-145">**MFVideoFormat\_YV12**</span></span>

<span data-ttu-id="cf7c6-146">Toutes les combinaisons de formats d’entrée et de sortie ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="cf7c6-146">Not every combination of input and output formats is supported.</span></span> <span data-ttu-id="cf7c6-147">Pour vérifier si une conversion est prise en charge, définissez le type d’entrée, puis appelez [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span><span class="sxs-lookup"><span data-stu-id="cf7c6-147">To test whether a conversion is supported, set the input type and then call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span></span>

<span data-ttu-id="cf7c6-148">Pour plus d’informations sur ces formats, consultez [GUID sous-type de vidéo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="cf7c6-148">For more information about these formats, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cf7c6-149">Notes</span><span class="sxs-lookup"><span data-stu-id="cf7c6-149">Remarks</span></span>

<span data-ttu-id="cf7c6-150">Une instance du processeur vidéo peut être créée de l’une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="cf7c6-150">An instance of the video processor can be created in one of the following ways:</span></span>

-   <span data-ttu-id="cf7c6-151">En appelant [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="cf7c6-151">By calling [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span> <span data-ttu-id="cf7c6-152">Le processeur vidéo est inscrit sous la catégorie de **\_ \_ \_ processeur vidéo de catégorie MFT** .</span><span class="sxs-lookup"><span data-stu-id="cf7c6-152">The video processor is registered under the **MFT\_CATEGORY\_VIDEO\_PROCESSOR** category.</span></span>
-   <span data-ttu-id="cf7c6-153">En appelant la fonction COM **CoCreateInstance** en lui transmettant le CLSID CLSID **\_ VideoProcessorMFT**.</span><span class="sxs-lookup"><span data-stu-id="cf7c6-153">By calling the COM function **CoCreateInstance** passing it the CLSID **CLSID\_VideoProcessorMFT**.</span></span>

<span data-ttu-id="cf7c6-154">Les remarques suivantes concernent l’utilisation des rectangles sources et des rectangles de destination dans la **MFT du processeur vidéo**.</span><span class="sxs-lookup"><span data-stu-id="cf7c6-154">The following remarks pertain to working with source rectangles and destination rectangles in the **Video Processor MFT**.</span></span> <span data-ttu-id="cf7c6-155">Les rectangles source et de destination sont définis avec [**IMFVideoProcessorControl :: SetDestinationRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setdestinationrectangle) et [**SetSourceRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setsourcerectangle) et parfois avec [**IMFMediaEngineEx :: UpdateVideoStream**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-updatevideostream).</span><span class="sxs-lookup"><span data-stu-id="cf7c6-155">Source and destination rectangles are set with [**IMFVideoProcessorControl::SetDestinationRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setdestinationrectangle) and [**SetSourceRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setsourcerectangle) and some times with [**IMFMediaEngineEx::UpdateVideoStream**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-updatevideostream).</span></span>

-   <span data-ttu-id="cf7c6-156">Le rectangle source doit être aligné et arrondi pour correspondre aux exigences du format de couleur du cadre entré sur le processeur vidéo.</span><span class="sxs-lookup"><span data-stu-id="cf7c6-156">The source rectangle should be aligned and rounded to match the requirements of the color format of the frame inputted to the video processor.</span></span> <span data-ttu-id="cf7c6-157">Cela est important, car les formats comme 420 et 422 ont des exigences relatives aux dimensions et aux décalages qui peuvent être créés et accessibles.</span><span class="sxs-lookup"><span data-stu-id="cf7c6-157">This is important because formats like 420 and 422 have requirements about the dimensions and offsets that can be created and accessed.</span></span> <span data-ttu-id="cf7c6-158">Par exemple, un rectangle source de {1, 0, 319, 240} (gauche, haut, droite, bas) sera arrondi à {2, 0, 320, 240} lorsque le format d’entrée est 420.</span><span class="sxs-lookup"><span data-stu-id="cf7c6-158">For example, a source rectangle of {1, 0, 319, 240} (left, top, right, bottom) will be rounded to {2, 0, 320, 240} when the input format is 420.</span></span>
-   <span data-ttu-id="cf7c6-159">Les rectangles de destination et source sont toujours fixés pour s’ajuster à l’intérieur de leurs images respectives : le rectangle source dans le frame source et le rectangle de destination dans le frame de destination.</span><span class="sxs-lookup"><span data-stu-id="cf7c6-159">Both the destination and source rectangle will always be clamped to fit inside their respective frames—the source rectangle to the source frame and the destination rectangle to the destination frame.</span></span> <span data-ttu-id="cf7c6-160">Cela signifie que les valeurs négatives ne sont pas significatives, elles sont toujours ancrées à 0.</span><span class="sxs-lookup"><span data-stu-id="cf7c6-160">This means that negative values are not meaningful—they will be always clamped to 0.</span></span>
-   <span data-ttu-id="cf7c6-161">Le rectangle source est dans le système de coordonnées du frame de destination, moins tout rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="cf7c6-161">The source rectangle is in the destination frame's coordinate system, minus any destination rectangle.</span></span> <span data-ttu-id="cf7c6-162">Cela signifie que les transformations telles que la rotation sont « annulées » sur le rectangle source.</span><span class="sxs-lookup"><span data-stu-id="cf7c6-162">This means that transformations like rotation are "undone" on the source rectangle.</span></span> <span data-ttu-id="cf7c6-163">Par conséquent, vous n’avez pas besoin de savoir si la vidéo a pivoté ou a été décompressée en 3D.</span><span class="sxs-lookup"><span data-stu-id="cf7c6-163">Therefore, you do not need to know if the video was rotated or 3D unpacked.</span></span> <span data-ttu-id="cf7c6-164">Par exemple, vous pouvez dessiner un rectangle en haut de la balise vidéo, prendre les coordonnées relatives (par rapport à la balise vidéo), les normaliser (plage 0 à 1) et les transmettre en tant que rectangle source et les faire fonctionner comme prévu, même si la vidéo est pivotée.</span><span class="sxs-lookup"><span data-stu-id="cf7c6-164">For example, you could draw a rectangle on top of the video tag, take the relative coordinates (relative to the video tag), normalize them (range 0 to 1) and pass them down as the source rectangle and they should work as expected, even if the video is being rotated.</span></span>

<span data-ttu-id="cf7c6-165">Le processeur vidéo prend en charge le traitement vidéo accéléré par GPU à l’aide de Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="cf7c6-165">The video processor supports GPU-accelerated video processing, using Microsoft Direct3D 11.</span></span> <span data-ttu-id="cf7c6-166">Pour plus d’informations, voir [MF \_ sa \_ d3d11 \_ Aware](mf-sa-d3d11-aware.md).</span><span class="sxs-lookup"><span data-stu-id="cf7c6-166">For more information, see [MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md).</span></span>

### <a name="stereoscopic-video"></a><span data-ttu-id="cf7c6-167">Vidéo stéréoscopique</span><span class="sxs-lookup"><span data-stu-id="cf7c6-167">Stereoscopic Video</span></span>

<span data-ttu-id="cf7c6-168">Le processeur vidéo prend en charge l’opération de décompression de vue sur les images vidéo 3D :</span><span class="sxs-lookup"><span data-stu-id="cf7c6-168">The video processor supports the view unpacking operation on 3D video frames:</span></span>

<span data-ttu-id="cf7c6-169">Si le frame d’entrée contient deux vues compressées dans le même frame, le processeur vidéo peut fractionner les vues en mémoires tampons distinctes, ou extraire la vue de base et ignorer la deuxième vue.</span><span class="sxs-lookup"><span data-stu-id="cf7c6-169">If the input frame contains two views packed in the same frame, the video processor can split the views into separate buffers, or extract the base view and discard the second view.</span></span> <span data-ttu-id="cf7c6-170">Pour activer la décompression de la vue, définissez l’attribut de [ \_ \_ \_ sortie 3DVIDEO MF Enable](mf-enable-3dvideo-output.md) sur **MF3DVideoOutputType \_ stéréo** ou **MF3DVideoOutputType \_ BaseView**.</span><span class="sxs-lookup"><span data-stu-id="cf7c6-170">To enable view unpacking, set the [MF\_ENABLE\_3DVIDEO\_OUTPUT](mf-enable-3dvideo-output.md) attribute to **MF3DVideoOutputType\_Stereo** or **MF3DVideoOutputType\_BaseView**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf7c6-171">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf7c6-171">Requirements</span></span>



| <span data-ttu-id="cf7c6-172">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf7c6-172">Requirement</span></span> | <span data-ttu-id="cf7c6-173">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf7c6-173">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf7c6-174">En-tête</span><span class="sxs-lookup"><span data-stu-id="cf7c6-174">Header</span></span><br/> | <dl> <span data-ttu-id="cf7c6-175"><dt>Camerauicontrol. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf7c6-175"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf7c6-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf7c6-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf7c6-177">Processeurs de signaux numériques</span><span class="sxs-lookup"><span data-stu-id="cf7c6-177">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




