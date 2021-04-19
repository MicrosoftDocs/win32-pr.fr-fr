---
description: Le décodeur MPEG4 v1/v2 Windows Media décode les flux vidéo MPEG4 v1/v2.
ms.assetid: 63b32972-1003-4291-bfdd-cc0cb8d65430
title: Décodeur Windows Media MPEG4 v1/v2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b14cf22e29c1266ac9bb3593375ee4485d79df2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106537163"
---
# <a name="windows-media-mpeg4-v1v2-decoder"></a><span data-ttu-id="d7a8f-103">Décodeur Windows Media MPEG4 v1/v2</span><span class="sxs-lookup"><span data-stu-id="d7a8f-103">Windows Media MPEG4 V1/V2 Decoder</span></span>

<span data-ttu-id="d7a8f-104">Le décodeur MPEG4 v1/v2 Windows Media décode les flux vidéo MPEG4 v1/v2.</span><span class="sxs-lookup"><span data-stu-id="d7a8f-104">The Windows Media MPEG4 V1/V2 decoder decodes MPEG4 V1/V2 video streams.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="d7a8f-105">Identificateur de classe</span><span class="sxs-lookup"><span data-stu-id="d7a8f-105">Class Identifier</span></span>

<span data-ttu-id="d7a8f-106">L’identificateur de classe (CLSID) du décodeur MPEG4 v1/v2 Windows Media est représenté par la constante **CLSID \_ CMpeg4DecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="d7a8f-106">The class identifier (CLSID) for the Windows Media MPEG4 V1/V2 decoder is represented by the constant **CLSID\_CMpeg4DecMediaObject**.</span></span> <span data-ttu-id="d7a8f-107">Vous pouvez créer une instance du décodeur MPEG4 v1/v2 en appelant **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="d7a8f-107">You can create an instance of the MPEG4 V1/V2 decoder by calling **CoCreateInstance**.</span></span>

## <a name="formats"></a><span data-ttu-id="d7a8f-108">Formats</span><span class="sxs-lookup"><span data-stu-id="d7a8f-108">Formats</span></span>

<span data-ttu-id="d7a8f-109">Le décodeur MPEG4 v1/v2 Windows Media prend en charge les types de média d’entrée suivants.</span><span class="sxs-lookup"><span data-stu-id="d7a8f-109">The Windows Media MPEG4 V1/V2 decoder supports the following input media types.</span></span>

-   <span data-ttu-id="d7a8f-110">MEDIASUBTYPE \_ MPG4</span><span class="sxs-lookup"><span data-stu-id="d7a8f-110">MEDIASUBTYPE\_MPG4</span></span>
-   <span data-ttu-id="d7a8f-111">MEDIASUBTYPE \_ MPG4</span><span class="sxs-lookup"><span data-stu-id="d7a8f-111">MEDIASUBTYPE\_mpg4</span></span>
-   <span data-ttu-id="d7a8f-112">MEDIASUBTYPE \_ MP42</span><span class="sxs-lookup"><span data-stu-id="d7a8f-112">MEDIASUBTYPE\_MP42</span></span>
-   <span data-ttu-id="d7a8f-113">MEDIASUBTYPE \_ MP42</span><span class="sxs-lookup"><span data-stu-id="d7a8f-113">MEDIASUBTYPE\_mp42</span></span>

<span data-ttu-id="d7a8f-114">Le décodeur MPEG4 Windows Media MPEG4/v2 prend en charge les sous-types de médias de sortie suivants lorsqu’il agit comme un objet de média DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="d7a8f-114">The Windows Media MPEG4 V1/V2 decoder supports the following output media subtypes when it is acting as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="d7a8f-115">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="d7a8f-115">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="d7a8f-116">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="d7a8f-116">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="d7a8f-117">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="d7a8f-117">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="d7a8f-118">MEDIASUBTYPE \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="d7a8f-118">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="d7a8f-119">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="d7a8f-119">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="d7a8f-120">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="d7a8f-120">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="d7a8f-121">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="d7a8f-121">MEDIASUBTYPE\_RGB555</span></span>

<span data-ttu-id="d7a8f-122">Le décodeur MPEG4 Windows Media MPEG4/v2 prend en charge les sous-types de médias de sortie suivants lorsqu’il agit comme une Media Foundation transformation (MFT).</span><span class="sxs-lookup"><span data-stu-id="d7a8f-122">The Windows Media MPEG4 V1/V2 decoder supports the following output media subtypes when it is acting as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="d7a8f-123">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="d7a8f-123">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="d7a8f-124">MFVideoFormat \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="d7a8f-124">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="d7a8f-125">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="d7a8f-125">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="d7a8f-126">MFVideoFormat \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="d7a8f-126">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="d7a8f-127">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="d7a8f-127">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="d7a8f-128">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="d7a8f-128">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="d7a8f-129">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="d7a8f-129">MFVideoFormat\_RGB555</span></span>

## <a name="remarks"></a><span data-ttu-id="d7a8f-130">Notes</span><span class="sxs-lookup"><span data-stu-id="d7a8f-130">Remarks</span></span>

<span data-ttu-id="d7a8f-131">L’objet décodeur Windows Media MPEG4 v1/v2 expose l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) afin que l’objet puisse être utilisé en tant qu’objet de média DirectX (DMO) et expose l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) afin que l’objet puisse être utilisé en tant que transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="d7a8f-131">The Windows Media MPEG4 V1/V2 decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="d7a8f-132">L’objet a le même identificateur de classe (CLSID), qu’il agisse comme DMO ou MFT.</span><span class="sxs-lookup"><span data-stu-id="d7a8f-132">The object has the same class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span>

<span data-ttu-id="d7a8f-133">Un décodeur MPEG4 v1/v2 se comporte comme un DMO ou une table MFT en fonction des interfaces que vous obtenez et de la version de Windows en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d7a8f-133">An MPEG4 V1/V2 decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="d7a8f-134">Le tableau suivant indique les conditions dans lesquelles un décodeur MPEG4 v1/v2 se comporte comme une version DMO ou une table MFT.</span><span class="sxs-lookup"><span data-stu-id="d7a8f-134">The following table shows the conditions under which an MPEG4 V1/V2 decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="d7a8f-135">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="d7a8f-135">Operating system</span></span>            | <span data-ttu-id="d7a8f-136">Comportement du décodeur</span><span class="sxs-lookup"><span data-stu-id="d7a8f-136">Decoder behavior</span></span>                                                                                                                                                                |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7a8f-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d7a8f-137">Windows XP</span></span>                  | <span data-ttu-id="d7a8f-138">Un décodeur MPEG4 v1/v2 se comporte toujours comme un DMO.</span><span class="sxs-lookup"><span data-stu-id="d7a8f-138">An MPEG4 V1/V2 decoder always behaves as a DMO.</span></span>                                                                                                                                 |
| <span data-ttu-id="d7a8f-139">Windows Vista et Windows 7</span><span class="sxs-lookup"><span data-stu-id="d7a8f-139">Windows Vista and Windows 7</span></span> | <span data-ttu-id="d7a8f-140">Par défaut, un décodeur MPEG4 v1/v2 se comporte comme un DMO.</span><span class="sxs-lookup"><span data-stu-id="d7a8f-140">By default, an MPEG4 V1/V2 decoder behaves as a DMO.</span></span> <span data-ttu-id="d7a8f-141">Si vous obtenez une interface de GUID de sous- [type de vidéo](video-subtype-guids.md) sur un décodeur MPEG4 v1/v2, elle se comporte comme une table MFT.</span><span class="sxs-lookup"><span data-stu-id="d7a8f-141">If you obtain an [Video Subtype GUIDs](video-subtype-guids.md) interface on an MPEG4 V1/V2 decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="d7a8f-142">Les identificateurs globaux uniques (GUID) pour les sous-types de média RVB diffèrent selon qu’un décodeur agit comme DMO ou MFT.</span><span class="sxs-lookup"><span data-stu-id="d7a8f-142">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="d7a8f-143">Les GUID pour les sous-types de média non RVB sont les mêmes, qu’un décodeur agisse comme DMO ou MFT.</span><span class="sxs-lookup"><span data-stu-id="d7a8f-143">The GUIDs for non-RGB media subtypes are the same, regardless of whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="d7a8f-144">Pour plus d’informations sur les GUID qui représentent des sous-types de vidéos, consultez [GUID de sous-type de vidéo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="d7a8f-144">For information about the GUIDs that represent video subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d7a8f-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7a8f-145">Requirements</span></span>



| <span data-ttu-id="d7a8f-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7a8f-146">Requirement</span></span> | <span data-ttu-id="d7a8f-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7a8f-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7a8f-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7a8f-148">Minimum supported client</span></span><br/> | <span data-ttu-id="d7a8f-149">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7a8f-149">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d7a8f-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7a8f-150">Minimum supported server</span></span><br/> | <span data-ttu-id="d7a8f-151">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7a8f-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d7a8f-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7a8f-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7a8f-153"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7a8f-153"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="d7a8f-154">DLL</span><span class="sxs-lookup"><span data-stu-id="d7a8f-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7a8f-155"><dt>MPG4DECD.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7a8f-155"><dt>MPG4DECD.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7a8f-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7a8f-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7a8f-157">Objets codec</span><span class="sxs-lookup"><span data-stu-id="d7a8f-157">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
