---
description: Utilisation du détecteur de média
ms.assetid: 462150d5-7315-4c2b-81b0-964a788ec47d
title: Utilisation du détecteur de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ebdb05eb47c7efabcc3234fb6ac2411a46e40d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106522269"
---
# <a name="using-the-media-detector"></a><span data-ttu-id="f0a2d-103">Utilisation du détecteur de média</span><span class="sxs-lookup"><span data-stu-id="f0a2d-103">Using the Media Detector</span></span>

<span data-ttu-id="f0a2d-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="f0a2d-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="f0a2d-105">Le détecteur de média est un objet d’assistance qui peut récupérer des informations sur un fichier, telles que le nombre de flux, leur type et leur durée.</span><span class="sxs-lookup"><span data-stu-id="f0a2d-105">The media detector is a helper object that can retrieve information about a file, such as the number of streams, their type, and their duration.</span></span> <span data-ttu-id="f0a2d-106">Elle contient également des méthodes permettant de récupérer des images de affiches à partir d’un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="f0a2d-106">It also contains methods for retrieving poster frames from a video stream.</span></span> <span data-ttu-id="f0a2d-107">Il expose l’interface [**IMediaDet**](imediadet.md) .</span><span class="sxs-lookup"><span data-stu-id="f0a2d-107">It exposes the [**IMediaDet**](imediadet.md) interface.</span></span>

<span data-ttu-id="f0a2d-108">Le détecteur de média fonctionne dans l’un des deux modes.</span><span class="sxs-lookup"><span data-stu-id="f0a2d-108">The media detector operates in one of two modes.</span></span> <span data-ttu-id="f0a2d-109">Lorsque vous créez une instance du détecteur de média, celle-ci n’est pas attachée à un fichier source particulier.</span><span class="sxs-lookup"><span data-stu-id="f0a2d-109">When you create an instance of the media detector, it is not attached to a particular source file.</span></span> <span data-ttu-id="f0a2d-110">Dans ce mode, vous pouvez récupérer des informations de flux à partir de plusieurs fichiers sources.</span><span class="sxs-lookup"><span data-stu-id="f0a2d-110">In this mode, you can retrieve stream information from multiple source files.</span></span> <span data-ttu-id="f0a2d-111">Toutefois, une fois que vous avez utilisé le détecteur de média pour obtenir un cadre d’affiche, celui-ci bascule en *mode de manipulation bitmap*.</span><span class="sxs-lookup"><span data-stu-id="f0a2d-111">However, once you use the media detector to obtain a poster frame, it switches to *bitmap grab mode*.</span></span> <span data-ttu-id="f0a2d-112">En mode de manipulation bitmap, le détecteur de média est attaché à un flux vidéo spécifique, et les méthodes d’informations de flux ne fonctionnent plus.</span><span class="sxs-lookup"><span data-stu-id="f0a2d-112">In bitmap grab mode, the media detector is attached to a specific video stream, and the stream information methods no longer work.</span></span> <span data-ttu-id="f0a2d-113">En outre, il n’existe aucun moyen de basculer le détecteur de média vers son mode de démarrage.</span><span class="sxs-lookup"><span data-stu-id="f0a2d-113">Moreover, there is no way to switch the media detector back to its starting mode.</span></span> <span data-ttu-id="f0a2d-114">Par conséquent, obtenez les informations de flux dont vous avez besoin avant de récupérer les images de poster, ou créez de nouvelles instances du détecteur de média pour chaque flux.</span><span class="sxs-lookup"><span data-stu-id="f0a2d-114">Therefore, obtain any stream information you need before retrieving poster frames, or else create new instances of the media detector for each stream.</span></span>

<span data-ttu-id="f0a2d-115">Pour obtenir des informations sur le flux, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="f0a2d-115">To obtain stream information, do the following:</span></span>

1.  <span data-ttu-id="f0a2d-116">Appelez [**IMediaDet ::p ut \_ filename**](imediadet-put-filename.md) avec le nom du fichier source.</span><span class="sxs-lookup"><span data-stu-id="f0a2d-116">Call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) with the name of the source file.</span></span>
2.  <span data-ttu-id="f0a2d-117">Appelez [**IMediaDet :: obtenir \_ OutputStreams**](imediadet-get-outputstreams.md) pour obtenir le nombre de flux dans la source.</span><span class="sxs-lookup"><span data-stu-id="f0a2d-117">Call [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) to obtain the number of streams in the source.</span></span>
3.  <span data-ttu-id="f0a2d-118">Spécifiez un numéro de flux avec [**IMediaDet ::p ut \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="f0a2d-118">Specify a stream number with [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span> <span data-ttu-id="f0a2d-119">Appelez ensuite une ou plusieurs des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f0a2d-119">Then call one or more of the following methods:</span></span>
    -   <span data-ttu-id="f0a2d-120">[**IMediaDet :: obtient \_ StreamType**](imediadet-get-streamtype.md): récupère le type de média du flux.</span><span class="sxs-lookup"><span data-stu-id="f0a2d-120">[**IMediaDet::get\_StreamType**](imediadet-get-streamtype.md): Retrieves the stream's media type.</span></span>
    -   <span data-ttu-id="f0a2d-121">[**IMediaDet :: obtient \_ StreamLength**](imediadet-get-streamlength.md): récupère la durée du flux.</span><span class="sxs-lookup"><span data-stu-id="f0a2d-121">[**IMediaDet::get\_StreamLength**](imediadet-get-streamlength.md): Retrieves the duration of the stream.</span></span>
    -   <span data-ttu-id="f0a2d-122">[**IMediaDet :: obtient \_ Cadence**](imediadet-get-framerate.md): récupère la fréquence d’images d’un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="f0a2d-122">[**IMediaDet::get\_FrameRate**](imediadet-get-framerate.md): Retrieves a video stream's frame rate.</span></span>

<span data-ttu-id="f0a2d-123">Pour obtenir un cadre d’affiche, spécifiez le numéro du flux, comme dans l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="f0a2d-123">To obtain a poster frame, specify the stream number, as in the previous step.</span></span> <span data-ttu-id="f0a2d-124">Ensuite, appelez [**IMediaDet :: GetBitmapBits**](imediadet-getbitmapbits.md), qui copie une image postérisée dans une mémoire tampon ou [**IMediaDet :: WriteBitmapBits**](imediadet-writebitmapbits.md), qui enregistre une image postérisée dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="f0a2d-124">Then call either [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md), which copies a poster frame into a buffer, or [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md), which saves a poster frame to a file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0a2d-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f0a2d-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0a2d-126">Utilisation des sources</span><span class="sxs-lookup"><span data-stu-id="f0a2d-126">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 



