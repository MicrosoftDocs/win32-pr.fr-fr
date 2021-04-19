---
description: Le décodeur d’écran Windows Media Video 9 décode les flux qui ont été encodés par l’encodeur d’écran Windows Media Video 9.
ms.assetid: 6688a830-7a54-4f58-947e-26013e191b5f
title: Décodeur d’écran Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9dcdce920fa39437edb769fd575a7d7a0d68fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524008"
---
# <a name="windows-media-video-9-screen-decoder"></a><span data-ttu-id="4f093-103">Décodeur d’écran Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="4f093-103">Windows Media Video 9 Screen Decoder</span></span>

<span data-ttu-id="4f093-104">Le décodeur d’écran Windows Media Video 9 décode les flux qui ont été encodés par l’encodeur d' [**écran Windows Media Video 9**](windowsmediavideo9screenencoder.md).</span><span class="sxs-lookup"><span data-stu-id="4f093-104">The Windows Media Video 9 Screen decoder decodes streams that were encoded by the [**Windows Media Video 9 Screen Encoder**](windowsmediavideo9screenencoder.md).</span></span>

## <a name="class-identifier"></a><span data-ttu-id="4f093-105">Identificateur de classe</span><span class="sxs-lookup"><span data-stu-id="4f093-105">Class Identifier</span></span>

<span data-ttu-id="4f093-106">L’identificateur de classe (CLSID) du décodeur d’écran Windows Media Video 9 est représenté par la constante **CLSID \_ CMSSCDecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="4f093-106">The class identifier (CLSID) for the Windows Media Video 9 Screen decoder is represented by the constant **CLSID\_CMSSCDecMediaObject**.</span></span> <span data-ttu-id="4f093-107">Vous pouvez créer une instance du décodeur en appelant **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="4f093-107">You can create an instance of the decoder by calling **CoCreateInstance**.</span></span>

## <a name="input-types"></a><span data-ttu-id="4f093-108">Types d’entrée</span><span class="sxs-lookup"><span data-stu-id="4f093-108">Input Types</span></span>

<span data-ttu-id="4f093-109">Le code à quatre caractères (FOURCC) pour Windows Media Video contenu encodé à l’écran version 9 est « MSS2 ».</span><span class="sxs-lookup"><span data-stu-id="4f093-109">The four-character code (FOURCC) for Windows Media Video Screen Version 9 encoded content is "MSS2".</span></span>

<span data-ttu-id="4f093-110">Les types d’entrée suivants sont pris en charge par le décodeur d’écran version 9.</span><span class="sxs-lookup"><span data-stu-id="4f093-110">The following input types are supported by the Version 9 Screen decoder.</span></span>

-   <span data-ttu-id="4f093-111">MEDIASUBTYPE \_ MSS2</span><span class="sxs-lookup"><span data-stu-id="4f093-111">MEDIASUBTYPE\_MSS2</span></span>

## <a name="output-types"></a><span data-ttu-id="4f093-112">Types de sortie</span><span class="sxs-lookup"><span data-stu-id="4f093-112">Output Types</span></span>

<span data-ttu-id="4f093-113">Les types de sortie suivants sont pris en charge par le décodeur d’écran version 9 lorsqu’il est utilisé en tant qu’objet de média DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="4f093-113">The following output types are supported by the Version 9 Screen decoder when it is being used as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="4f093-114">MEDIASUBTYPE \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="4f093-114">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="4f093-115">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="4f093-115">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="4f093-116">MEDIASUBTYPE \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="4f093-116">MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="4f093-117">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="4f093-117">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="4f093-118">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="4f093-118">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="4f093-119">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="4f093-119">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="4f093-120">Les types de sortie suivants sont pris en charge par le décodeur d’écran version 9 lorsqu’il est utilisé en tant que transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="4f093-120">The following output types are supported by the Version 9 Screen decoder when it is being used as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="4f093-121">MFVideoFormat \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="4f093-121">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="4f093-122">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="4f093-122">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="4f093-123">MFVideoFormat \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="4f093-123">MFVideoFormat\_ARGB32</span></span>
-   <span data-ttu-id="4f093-124">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="4f093-124">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="4f093-125">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="4f093-125">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="4f093-126">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="4f093-126">MFVideoFormat\_RGB8</span></span>

## <a name="remarks"></a><span data-ttu-id="4f093-127">Notes</span><span class="sxs-lookup"><span data-stu-id="4f093-127">Remarks</span></span>

<span data-ttu-id="4f093-128">Un objet décodeur d’écran expose l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) afin que l’objet puisse être utilisé en tant qu’objet de média DirectX (DMO) et expose l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) afin que l’objet puisse être utilisé en tant que transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="4f093-128">A screen decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="4f093-129">Un décodeur d’écran se comporte comme un DMO ou une table MFT selon les interfaces que vous obtenez et la version de Windows en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4f093-129">A screen decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="4f093-130">Le tableau suivant indique les conditions sous lesquelles un décodeur d’écran se comporte comme un DMO ou une table MFT.</span><span class="sxs-lookup"><span data-stu-id="4f093-130">The following table shows the conditions under which a screen decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="4f093-131">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="4f093-131">Operating system</span></span>            | <span data-ttu-id="4f093-132">Comportement du décodeur</span><span class="sxs-lookup"><span data-stu-id="4f093-132">Decoder behavior</span></span>                                                                                                                                                        |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f093-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4f093-133">Windows XP</span></span>                  | <span data-ttu-id="4f093-134">Un décodeur d’écran Windows Media se comporte toujours comme un DMO.</span><span class="sxs-lookup"><span data-stu-id="4f093-134">A Windows Media Screen decoder always behaves as a DMO.</span></span>                                                                                                                 |
| <span data-ttu-id="4f093-135">Windows Vista et Windows 7</span><span class="sxs-lookup"><span data-stu-id="4f093-135">Windows Vista and Windows 7</span></span> | <span data-ttu-id="4f093-136">Par défaut, un décodeur d’écran Windows Media se comporte comme un DMO.</span><span class="sxs-lookup"><span data-stu-id="4f093-136">By default, a Windows Media Screen decoder behaves as a DMO.</span></span> <span data-ttu-id="4f093-137">Si vous obtenez une interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) sur un décodeur d’écran, celui-ci se comporte comme une table MFT.</span><span class="sxs-lookup"><span data-stu-id="4f093-137">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a screen decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="4f093-138">Vous pouvez utiliser le même CLSID (CLSID \_ CMSSCDecMediaObject) pour créer le décodeur d’écran de la version 7 et le décodeur d’écran de la version 9.</span><span class="sxs-lookup"><span data-stu-id="4f093-138">You can use the same CLSID (CLSID\_CMSSCDecMediaObject) to create the Version 7 Screen decoder and the Version 9 Screen decoder.</span></span> <span data-ttu-id="4f093-139">Le contenu encodé FOURCC pour Windows Media Video écran version 7 est « MSS1 ».</span><span class="sxs-lookup"><span data-stu-id="4f093-139">The FOURCC for Windows Media Video Screen Version 7 encoded content is "MSS1".</span></span> <span data-ttu-id="4f093-140">Le décodeur d’écran de la version 7 prend en charge le \_ type d’entrée MEDIASUBTYPE MSS1.</span><span class="sxs-lookup"><span data-stu-id="4f093-140">The Version 7 Screen decoder supports the MEDIASUBTYPE\_MSS1 input type.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f093-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f093-141">Requirements</span></span>



| <span data-ttu-id="4f093-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f093-142">Requirement</span></span> | <span data-ttu-id="4f093-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f093-143">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f093-144">Client</span><span class="sxs-lookup"><span data-stu-id="4f093-144">Client</span></span><br/> | <span data-ttu-id="4f093-145">Windows XP, Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="4f093-145">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="4f093-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f093-146">Header</span></span><br/> | <dl> <span data-ttu-id="4f093-147"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f093-147"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="4f093-148">DLL</span><span class="sxs-lookup"><span data-stu-id="4f093-148">DLL</span></span><br/>    | <dl> <span data-ttu-id="4f093-149"><dt>Wmvsdecd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f093-149"><dt>Wmvsdecd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f093-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f093-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f093-151">Objets codec</span><span class="sxs-lookup"><span data-stu-id="4f093-151">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="4f093-152">Implémentation du codec</span><span class="sxs-lookup"><span data-stu-id="4f093-152">Codec Implementation</span></span>](codecimplementation.md)
</dt> <dt>

[<span data-ttu-id="4f093-153">Utilisation du codec d’écran Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="4f093-153">Using the Windows Media Video 9 Screen Codec</span></span>](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[<span data-ttu-id="4f093-154">Encodeur d’écran Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="4f093-154">Windows Media Video 9 Screen Encoder</span></span>](windowsmediavideo9screenencoder.md)
</dt> </dl>

 

 
