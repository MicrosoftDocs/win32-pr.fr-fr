---
description: Appareils mobiles Windows prend en charge les propriétés vidéo suivantes.
ms.assetid: e6df5b2d-ceb8-4de0-b60b-9102c77143fe
title: Propriétés de la vidéo (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Video
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1f44f32ab19c5ad10cc9c8dd5bdb8816ccc944f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525198"
---
# <a name="video-properties"></a><span data-ttu-id="40ac5-103">Propriétés de la vidéo</span><span class="sxs-lookup"><span data-stu-id="40ac5-103">Video Properties</span></span>

<span data-ttu-id="40ac5-104">Appareils mobiles Windows prend en charge les propriétés vidéo suivantes.</span><span class="sxs-lookup"><span data-stu-id="40ac5-104">Windows Portable Devices supports the following video properties.</span></span>



| <span data-ttu-id="40ac5-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="40ac5-105">Property</span></span>                                         | <span data-ttu-id="40ac5-106">VarType</span><span class="sxs-lookup"><span data-stu-id="40ac5-106">VarType</span></span>        | <span data-ttu-id="40ac5-107">Description</span><span class="sxs-lookup"><span data-stu-id="40ac5-107">Description</span></span>                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40ac5-108">**\_auteur de vidéo wpd \_**</span><span class="sxs-lookup"><span data-stu-id="40ac5-108">**WPD\_VIDEO\_AUTHOR**</span></span>                           | <span data-ttu-id="40ac5-109">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="40ac5-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="40ac5-110">Auteur du fichier vidéo.</span><span class="sxs-lookup"><span data-stu-id="40ac5-110">The author of the video file.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="40ac5-111">**\_vitesse de \_ transmission vidéo wpd**</span><span class="sxs-lookup"><span data-stu-id="40ac5-111">**WPD\_VIDEO\_BITRATE**</span></span>                          | <span data-ttu-id="40ac5-112">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="40ac5-112">**VT\_UI4**</span></span>    | <span data-ttu-id="40ac5-113">Vitesse de transmission du fichier vidéo.</span><span class="sxs-lookup"><span data-stu-id="40ac5-113">The bit rate of the video file.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="40ac5-114">**taille de la \_ \_ mémoire tampon vidéo wpd \_**</span><span class="sxs-lookup"><span data-stu-id="40ac5-114">**WPD\_VIDEO\_BUFFER\_SIZE**</span></span>                     | <span data-ttu-id="40ac5-115">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="40ac5-115">**VT\_UI4**</span></span>    | <span data-ttu-id="40ac5-116">Valeur qui spécifie la taille de mémoire tampon vidéo requise pour restituer ce fichier.</span><span class="sxs-lookup"><span data-stu-id="40ac5-116">A value that specifies the required video buffer size to render this file.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="40ac5-117">**\_crédits vidéo \_ wpd**</span><span class="sxs-lookup"><span data-stu-id="40ac5-117">**WPD\_VIDEO\_CREDITS**</span></span>                          | <span data-ttu-id="40ac5-118">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="40ac5-118">**VT\_LPWSTR**</span></span> | <span data-ttu-id="40ac5-119">Les crédits qui répertorient le cast et l’équipage de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="40ac5-119">The credits listing the cast and crew for the video.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="40ac5-120">**\_ \_ code FourCC vidéo \_ wpd**</span><span class="sxs-lookup"><span data-stu-id="40ac5-120">**WPD\_VIDEO\_FOURCC\_CODE**</span></span>                     | <span data-ttu-id="40ac5-121">**\_DWORD VT**</span><span class="sxs-lookup"><span data-stu-id="40ac5-121">**VT\_DWORD**</span></span>  | <span data-ttu-id="40ac5-122">Code FourCC inscrit qui indique le codec utilisé pour le fichier vidéo.</span><span class="sxs-lookup"><span data-stu-id="40ac5-122">The registered FourCC code that indicates the codec that was used for the video file.</span></span> <span data-ttu-id="40ac5-123">Pour obtenir la liste des formats FourCC, consultez l’article sur les [codes FourCC et les formats Wave inscrits](https://msdn2.microsoft.com/library/ms867195.aspx) sur le site Web MSDN.</span><span class="sxs-lookup"><span data-stu-id="40ac5-123">For a listing of FourCC formats, see the article [Registered FOURCC Codes and WAVE Formats](https://msdn2.microsoft.com/library/ms867195.aspx) on the MSDN Web site.</span></span> |
| <span data-ttu-id="40ac5-124">**\_fréquence d’images vidéo wpd \_**</span><span class="sxs-lookup"><span data-stu-id="40ac5-124">**WPD\_VIDEO\_FRAMERATE**</span></span>                        | <span data-ttu-id="40ac5-125">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="40ac5-125">**VT\_UI4**</span></span>    | <span data-ttu-id="40ac5-126">Fréquence d’images du fichier vidéo, en images/seconde x 1 000.</span><span class="sxs-lookup"><span data-stu-id="40ac5-126">The frame rate of the video file, in frames/second x 1,000.</span></span> <span data-ttu-id="40ac5-127">Par exemple, une fréquence d’images de 29,97 est représentée sous la forme 29970.</span><span class="sxs-lookup"><span data-stu-id="40ac5-127">For example, a frame rate of 29.97 is represented as 29970.</span></span>                                                                                                                                 |
| <span data-ttu-id="40ac5-128">**\_genre vidéo \_ wpd**</span><span class="sxs-lookup"><span data-stu-id="40ac5-128">**WPD\_VIDEO\_GENRE**</span></span>                            | <span data-ttu-id="40ac5-129">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="40ac5-129">**VT\_LPWSTR**</span></span> | <span data-ttu-id="40ac5-130">Genre de ce fichier vidéo.</span><span class="sxs-lookup"><span data-stu-id="40ac5-130">The genre of this video file.</span></span> <span data-ttu-id="40ac5-131">Il n’existe aucune définition de genre standard.</span><span class="sxs-lookup"><span data-stu-id="40ac5-131">There are no standard genre definitions.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="40ac5-132">**DISTANCE de l’image de la \_ clé vidéo wpd \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="40ac5-132">**WPD\_VIDEO\_KEY\_FRAME\_DISTANCE**</span></span>             | <span data-ttu-id="40ac5-133">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="40ac5-133">**VT\_UI4**</span></span>    | <span data-ttu-id="40ac5-134">Intervalle, en millisecondes, entre les images clés.</span><span class="sxs-lookup"><span data-stu-id="40ac5-134">The interval between key frames, in milliseconds.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="40ac5-135">**\_paramètre de \_ qualité \_ vidéo wpd**</span><span class="sxs-lookup"><span data-stu-id="40ac5-135">**WPD\_VIDEO\_QUALITY\_SETTING**</span></span>                 | <span data-ttu-id="40ac5-136">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="40ac5-136">**VT\_UI4**</span></span>    | <span data-ttu-id="40ac5-137">Paramètre de qualité du fichier vidéo.</span><span class="sxs-lookup"><span data-stu-id="40ac5-137">The quality setting for the video file.</span></span> <span data-ttu-id="40ac5-138">Cela dépend du codec.</span><span class="sxs-lookup"><span data-stu-id="40ac5-138">This is codec-dependent.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="40ac5-139">**\_numéro de \_ \_ canal RECORDEDTV vidéo wpd \_**</span><span class="sxs-lookup"><span data-stu-id="40ac5-139">**WPD\_VIDEO\_RECORDEDTV\_CHANNEL\_NUMBER**</span></span>      | <span data-ttu-id="40ac5-140">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="40ac5-140">**VT\_UI4**</span></span>    | <span data-ttu-id="40ac5-141">Numéro du canal de télévision à partir duquel la vidéo a été enregistrée.</span><span class="sxs-lookup"><span data-stu-id="40ac5-141">The television channel number the video was recorded from.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="40ac5-142">**\_Description du \_ \_ programme RECORDEDTV vidéo wpd \_**</span><span class="sxs-lookup"><span data-stu-id="40ac5-142">**WPD\_VIDEO\_RECORDEDTV\_PROGRAM\_DESCRIPTION**</span></span> | <span data-ttu-id="40ac5-143">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="40ac5-143">**VT\_LPWSTR**</span></span> | <span data-ttu-id="40ac5-144">Description du programme de télévision enregistré.</span><span class="sxs-lookup"><span data-stu-id="40ac5-144">A description of the recorded television program.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="40ac5-145">**\_RECORDEDTV vidéo \_ wpd \_ répéter**</span><span class="sxs-lookup"><span data-stu-id="40ac5-145">**WPD\_VIDEO\_RECORDEDTV\_REPEAT**</span></span>               | <span data-ttu-id="40ac5-146">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="40ac5-146">**VT\_BOOL**</span></span>   | <span data-ttu-id="40ac5-147">Valeur booléenne qui spécifie si le programme de télévision était une répétition affichée.</span><span class="sxs-lookup"><span data-stu-id="40ac5-147">A Boolean value that specifies whether the television program was a repeat showing.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="40ac5-148">**\_nom de \_ la \_ station RECORDEDTV vidéo \_ wpd**</span><span class="sxs-lookup"><span data-stu-id="40ac5-148">**WPD\_VIDEO\_RECORDEDTV\_STATION\_NAME**</span></span>        | <span data-ttu-id="40ac5-149">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="40ac5-149">**VT\_LPWSTR**</span></span> | <span data-ttu-id="40ac5-150">Station de télévision à partir de laquelle la vidéo a été enregistrée.</span><span class="sxs-lookup"><span data-stu-id="40ac5-150">The television station that the video was recorded from.</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="40ac5-151">**\_type d' \_ analyse \_ vidéo wpd**</span><span class="sxs-lookup"><span data-stu-id="40ac5-151">**WPD\_VIDEO\_SCAN\_TYPE**</span></span>                       | <span data-ttu-id="40ac5-152">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="40ac5-152">**VT\_UI4**</span></span>    | <span data-ttu-id="40ac5-153">Énumérateur [**de \_ \_ \_ types d’analyses vidéo wpd**](wpd-video-scan-types.md) qui spécifie l’entrelacement du fichier vidéo.</span><span class="sxs-lookup"><span data-stu-id="40ac5-153">A [**WPD\_VIDEO\_SCAN\_TYPES**](wpd-video-scan-types.md) enumerator that specifies the interlacing of the video file.</span></span>                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="40ac5-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40ac5-154">Requirements</span></span>



| <span data-ttu-id="40ac5-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40ac5-155">Requirement</span></span> | <span data-ttu-id="40ac5-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="40ac5-156">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="40ac5-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="40ac5-157">Header</span></span><br/> | <dl> <span data-ttu-id="40ac5-158"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="40ac5-158"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40ac5-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40ac5-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40ac5-160">**Propriétés et attributs WPD**</span><span class="sxs-lookup"><span data-stu-id="40ac5-160">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




