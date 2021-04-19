---
description: Le décodeur Windows Media MPEG-4 v3 décode les flux vidéo MPEG-4 v3.
ms.assetid: 5143b0cc-c171-46af-8d7f-4d029af71fb4
title: Décodeur Windows Media MPEG-4 v3 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ee98a0a3c4b221da6f2000e32d4c75bc3e3a93b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106539790"
---
# <a name="windows-media-mpeg-4-v3-decoder"></a><span data-ttu-id="e5be0-103">Décodeur Windows Media MPEG-4 v3</span><span class="sxs-lookup"><span data-stu-id="e5be0-103">Windows Media MPEG-4 V3 Decoder</span></span>

<span data-ttu-id="e5be0-104">Le décodeur Windows Media MPEG-4 v3 décode les flux vidéo MPEG-4 v3.</span><span class="sxs-lookup"><span data-stu-id="e5be0-104">The Windows Media MPEG-4 V3 decoder decodes MPEG-4 V3 video streams.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="e5be0-105">Identificateur de classe</span><span class="sxs-lookup"><span data-stu-id="e5be0-105">Class Identifier</span></span>

<span data-ttu-id="e5be0-106">L’identificateur de classe (CLSID) du décodeur Windows MPEG-4 v3 est représenté par la constante **CLSID \_ CMpeg43DecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="e5be0-106">The class identifier (CLSID) for the Windows MPEG-4 V3 decoder is represented by the constant **CLSID\_CMpeg43DecMediaObject**.</span></span> <span data-ttu-id="e5be0-107">Vous pouvez créer une instance du décodeur MPEG-4 v3 en appelant **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="e5be0-107">You can create an instance of the MPEG-4 V3 decoder by calling **CoCreateInstance**.</span></span>

## <a name="formats"></a><span data-ttu-id="e5be0-108">Formats</span><span class="sxs-lookup"><span data-stu-id="e5be0-108">Formats</span></span>

<span data-ttu-id="e5be0-109">Le décodeur Windows Media MPEG-4 v3 prend en charge les types de média d’entrée suivants.</span><span class="sxs-lookup"><span data-stu-id="e5be0-109">The Windows Media MPEG-4 V3 decoder supports the following input media types.</span></span>

-   <span data-ttu-id="e5be0-110">MEDIASUBTYPE \_ mp43</span><span class="sxs-lookup"><span data-stu-id="e5be0-110">MEDIASUBTYPE\_MP43</span></span>
-   <span data-ttu-id="e5be0-111">MEDIASUBTYPE \_ mp43</span><span class="sxs-lookup"><span data-stu-id="e5be0-111">MEDIASUBTYPE\_mp43</span></span>

<span data-ttu-id="e5be0-112">Le décodeur Windows Media MPEG-4 v3 prend en charge les sous-types de médias de sortie suivants lorsqu’il agit comme un objet de média DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="e5be0-112">The Windows Media MPEG-4 V3 decoder supports the following output media subtypes when it is acting as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="e5be0-113">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="e5be0-113">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="e5be0-114">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="e5be0-114">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="e5be0-115">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="e5be0-115">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="e5be0-116">MEDIASUBTYPE \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="e5be0-116">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="e5be0-117">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="e5be0-117">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="e5be0-118">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="e5be0-118">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="e5be0-119">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="e5be0-119">MEDIASUBTYPE\_RGB555</span></span>

<span data-ttu-id="e5be0-120">Le décodeur Windows Media MPEG-4 v3 prend en charge les sous-types de médias de sortie suivants lorsqu’il agit comme une Media Foundation transformation (MFT).</span><span class="sxs-lookup"><span data-stu-id="e5be0-120">The Windows Media MPEG-4 V3 decoder supports the following output media subtypes when it is acting as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="e5be0-121">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="e5be0-121">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="e5be0-122">MFVideoFormat \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="e5be0-122">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="e5be0-123">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="e5be0-123">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="e5be0-124">MFVideoFormat \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="e5be0-124">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="e5be0-125">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="e5be0-125">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="e5be0-126">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="e5be0-126">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="e5be0-127">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="e5be0-127">MFVideoFormat\_RGB555</span></span>

## <a name="remarks"></a><span data-ttu-id="e5be0-128">Notes</span><span class="sxs-lookup"><span data-stu-id="e5be0-128">Remarks</span></span>

<span data-ttu-id="e5be0-129">L’objet décodeur Windows Media MPEG-4 v3 expose l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) de sorte que l’objet puisse être utilisé en tant qu’objet de média DirectX (DMO) et expose l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) afin que l’objet puisse être utilisé en tant que transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="e5be0-129">The Windows Media MPEG-4 V3 decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="e5be0-130">L’objet a le même identificateur de classe (CLSID), qu’il agisse comme DMO ou MFT.</span><span class="sxs-lookup"><span data-stu-id="e5be0-130">The object has the same class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span>

<span data-ttu-id="e5be0-131">Le décodeur MPEG-4 v3 se comporte comme un DMO ou une table MFT en fonction des interfaces que vous obtenez et de la version de Windows en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e5be0-131">The MPEG-4 V3 decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="e5be0-132">Le tableau suivant répertorie les conditions dans lesquelles un décodeur MPEG-4 v3 se comporte comme une table DMO ou une table MFT.</span><span class="sxs-lookup"><span data-stu-id="e5be0-132">The following table shows the conditions under which an MPEG-4 V3 decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="e5be0-133">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="e5be0-133">Operating system</span></span>            | <span data-ttu-id="e5be0-134">Comportement du décodeur</span><span class="sxs-lookup"><span data-stu-id="e5be0-134">Decoder behavior</span></span>                                                                                                                                                    |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5be0-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e5be0-135">Windows XP</span></span>                  | <span data-ttu-id="e5be0-136">Le décodeur MPEG-4 v3 se comporte toujours comme un DMO.</span><span class="sxs-lookup"><span data-stu-id="e5be0-136">The MPEG-4 V3 decoder always behaves as a DMO.</span></span>                                                                                                                      |
| <span data-ttu-id="e5be0-137">Windows Vista et Windows 7</span><span class="sxs-lookup"><span data-stu-id="e5be0-137">Windows Vista and Windows 7</span></span> | <span data-ttu-id="e5be0-138">Par défaut, le décodeur MPEG-4 v3 se comporte comme un DMO.</span><span class="sxs-lookup"><span data-stu-id="e5be0-138">By default, the MPEG-4 V3 decoder behaves as a DMO.</span></span> <span data-ttu-id="e5be0-139">Si vous obtenez une interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) sur le décodeur MPEG-4 v3, elle se comporte comme une table MFT.</span><span class="sxs-lookup"><span data-stu-id="e5be0-139">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on the MPEG-4 V3 decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="e5be0-140">Les identificateurs globaux uniques (GUID) pour les sous-types de média RVB diffèrent selon qu’un décodeur agit comme DMO ou MFT.</span><span class="sxs-lookup"><span data-stu-id="e5be0-140">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="e5be0-141">Les GUID pour les sous-types de média non RVB sont les mêmes, qu’un décodeur agisse comme DMO ou MFT.</span><span class="sxs-lookup"><span data-stu-id="e5be0-141">The GUIDs for non-RGB media subtypes are the same, regardless of whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="e5be0-142">Pour plus d’informations sur les GUID qui représentent des sous-types de médias, consultez [GUID de sous-type de vidéo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="e5be0-142">For information about the GUIDs that represent media subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5be0-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5be0-143">Requirements</span></span>



| <span data-ttu-id="e5be0-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5be0-144">Requirement</span></span> | <span data-ttu-id="e5be0-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5be0-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5be0-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5be0-146">Minimum supported client</span></span><br/> | <span data-ttu-id="e5be0-147">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5be0-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e5be0-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5be0-148">Minimum supported server</span></span><br/> | <span data-ttu-id="e5be0-149">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5be0-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e5be0-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="e5be0-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5be0-151"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5be0-151"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="e5be0-152">DLL</span><span class="sxs-lookup"><span data-stu-id="e5be0-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5be0-153"><dt>MP43DECD.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5be0-153"><dt>MP43DECD.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5be0-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5be0-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5be0-155">Objets codec</span><span class="sxs-lookup"><span data-stu-id="e5be0-155">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
