---
description: L’interface IMediaDet récupère des informations sur un fichier multimédia, telles que le nombre de flux, le type de média, la durée et la fréquence d’images de chaque flux.
ms.assetid: 596fc84e-a88a-4e1b-aa48-b6dc9031db31
title: Interface IMediaDet (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ca5c87a1424872491aba5dcf4e01011872e9ff36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543587"
---
# <a name="imediadet-interface"></a><span data-ttu-id="e932d-103">Interface IMediaDet</span><span class="sxs-lookup"><span data-stu-id="e932d-103">IMediaDet interface</span></span>

> [!Note]  
> <span data-ttu-id="e932d-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="e932d-104">\[Deprecated.</span></span> <span data-ttu-id="e932d-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e932d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e932d-106">L' `IMediaDet` interface récupère des informations sur un fichier multimédia, telles que le nombre de flux, ainsi que le type de média, la durée et la fréquence d’images de chaque flux.</span><span class="sxs-lookup"><span data-stu-id="e932d-106">The `IMediaDet` interface retrieves information about a media file, such as the number of streams, and the media type, duration, and frame rate of each stream.</span></span> <span data-ttu-id="e932d-107">Il contient également des méthodes pour récupérer des frames individuels à partir d’un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="e932d-107">It also contains methods for retrieving individual frames from a video stream.</span></span> <span data-ttu-id="e932d-108">L’objet [détecteur de média (MediaDet)](media-detector--mediadet.md) expose cette interface.</span><span class="sxs-lookup"><span data-stu-id="e932d-108">The [Media Detector (MediaDet)](media-detector--mediadet.md) object exposes this interface.</span></span>

<span data-ttu-id="e932d-109">Pour obtenir des informations sur un fichier à l’aide de cette interface, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="e932d-109">To obtain information about a file using this interface, perform the following steps:</span></span>

1.  <span data-ttu-id="e932d-110">Créez une instance de l’objet MediaDet en appelant **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="e932d-110">Create an instance of the MediaDet object by calling **CoCreateInstance**.</span></span> <span data-ttu-id="e932d-111">L’ID de classe est CLSID \_ MediaDet.</span><span class="sxs-lookup"><span data-stu-id="e932d-111">The class ID is CLSID\_MediaDet.</span></span>
2.  <span data-ttu-id="e932d-112">Appelez [**IMediaDet ::p ut \_ filename**](imediadet-put-filename.md) pour spécifier le nom du fichier source.</span><span class="sxs-lookup"><span data-stu-id="e932d-112">Call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) to specify the name of the source file.</span></span>
3.  <span data-ttu-id="e932d-113">Appelez [**IMediaDet :: obtenir \_ OutputStreams**](imediadet-get-outputstreams.md) pour obtenir le nombre de flux de sortie dans la source.</span><span class="sxs-lookup"><span data-stu-id="e932d-113">Call [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) to obtain the number of output streams in the source.</span></span>
4.  <span data-ttu-id="e932d-114">Appelez [**IMediaDet ::p ut \_ CurrentStream**](imediadet-put-currentstream.md) pour spécifier un flux particulier.</span><span class="sxs-lookup"><span data-stu-id="e932d-114">Call [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md) to specify a particular stream.</span></span>
5.  <span data-ttu-id="e932d-115">Appelez l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e932d-115">Call any of the following methods:</span></span>
    -   [<span data-ttu-id="e932d-116">**IMediaDet :: obtient la \_ cadence**</span><span class="sxs-lookup"><span data-stu-id="e932d-116">**IMediaDet::get\_FrameRate**</span></span>](imediadet-get-framerate.md)
    -   [<span data-ttu-id="e932d-117">**IMediaDet :: obtient \_ StreamLength**</span><span class="sxs-lookup"><span data-stu-id="e932d-117">**IMediaDet::get\_StreamLength**</span></span>](imediadet-get-streamlength.md)
    -   [<span data-ttu-id="e932d-118">**IMediaDet :: obtient \_ StreamMediaType**</span><span class="sxs-lookup"><span data-stu-id="e932d-118">**IMediaDet::get\_StreamMediaType**</span></span>](imediadet-get-streammediatype.md)
    -   [<span data-ttu-id="e932d-119">**IMediaDet :: obtient \_ StreamType**</span><span class="sxs-lookup"><span data-stu-id="e932d-119">**IMediaDet::get\_StreamType**</span></span>](imediadet-get-streamtype.md)

<span data-ttu-id="e932d-120">Pour récupérer une image vidéo, appelez [**IMediaDet :: GetBitmapBits**](imediadet-getbitmapbits.md) ou [**IMediaDet :: WriteBitmapBits**](imediadet-writebitmapbits.md).</span><span class="sxs-lookup"><span data-stu-id="e932d-120">To retrieve a video frame, call [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) or [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md).</span></span> <span data-ttu-id="e932d-121">Le frame retourné est toujours au format RGB 24 bits.</span><span class="sxs-lookup"><span data-stu-id="e932d-121">The returned frame is always in 24-bit RGB format.</span></span>

> [!Note]  
> <span data-ttu-id="e932d-122">N’utilisez pas le même objet MediaDet avec plusieurs fichiers.</span><span class="sxs-lookup"><span data-stu-id="e932d-122">Do not use the same MediaDet object with multiple files.</span></span> <span data-ttu-id="e932d-123">Pour obtenir des informations ou des images vidéo à partir de plusieurs fichiers, utilisez des instances MediaDet distinctes.</span><span class="sxs-lookup"><span data-stu-id="e932d-123">To get information or video frames from more than one file, use separate MediaDet instances.</span></span>

 

<span data-ttu-id="e932d-124">L’interface **IMediaDet** ne prend pas en charge les formats [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) . vous ne pouvez donc pas utiliser cette interface pour obtenir des champs entrelacés ou des informations sur l’entrelacement.</span><span class="sxs-lookup"><span data-stu-id="e932d-124">The **IMediaDet** interface does not support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats, so you cannot use this interface to get interlaced fields or information about interlacing.</span></span> <span data-ttu-id="e932d-125">En outre, si le décodeur en amont prend en charge uniquement **VIDEOINFOHEADER2**, vous ne pouvez pas utiliser `IMediaDet` .</span><span class="sxs-lookup"><span data-stu-id="e932d-125">Also, if the upstream decoder supports only **VIDEOINFOHEADER2**, you cannot use `IMediaDet`.</span></span> <span data-ttu-id="e932d-126">Cela peut être le cas avec un décodeur MPEG-2, par exemple.</span><span class="sxs-lookup"><span data-stu-id="e932d-126">This might be the case with an MPEG-2 decoder, for example.</span></span> <span data-ttu-id="e932d-127">En outre, l' `IMediaDet` interface ignore tous les flux du fichier qui ne sont pas des données vidéo ou audio.</span><span class="sxs-lookup"><span data-stu-id="e932d-127">Also, the `IMediaDet` interface ignores any streams in the file that are not video or audio.</span></span> <span data-ttu-id="e932d-128">Par exemple, si le fichier contient un flux audio, un flux de données et un flux vidéo, la méthode **obtenir \_ OutputStreams** ne signale que deux flux (l’audio et la vidéo).</span><span class="sxs-lookup"><span data-stu-id="e932d-128">For example, if the file contains an audio stream, a data stream, and a video stream, the **get\_OutputStreams** method will report only two streams (the audio and video).</span></span>

## <a name="members"></a><span data-ttu-id="e932d-129">Membres</span><span class="sxs-lookup"><span data-stu-id="e932d-129">Members</span></span>

<span data-ttu-id="e932d-130">L’interface **IMediaDet** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e932d-130">The **IMediaDet** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e932d-131">**IMediaDet** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e932d-131">**IMediaDet** also has these types of members:</span></span>

-   [<span data-ttu-id="e932d-132">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e932d-132">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e932d-133">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e932d-133">Methods</span></span>

<span data-ttu-id="e932d-134">L’interface **IMediaDet** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e932d-134">The **IMediaDet** interface has these methods.</span></span>



| <span data-ttu-id="e932d-135">Méthode</span><span class="sxs-lookup"><span data-stu-id="e932d-135">Method</span></span>                                                        | <span data-ttu-id="e932d-136">Description</span><span class="sxs-lookup"><span data-stu-id="e932d-136">Description</span></span>                                                                                                |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e932d-137">**EnterBitmapGrabMode**</span><span class="sxs-lookup"><span data-stu-id="e932d-137">**EnterBitmapGrabMode**</span></span>](imediadet-enterbitmapgrabmode.md)  | <span data-ttu-id="e932d-138">Bascule le détecteur de média en mode de manipulation bitmap et recherche le graphique de filtre à une heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e932d-138">Switches the media detector to bitmap grab mode and seeks the filter graph to a specified time.</span></span><br/> |
| [<span data-ttu-id="e932d-139">**Obtient \_ CurrentStream**</span><span class="sxs-lookup"><span data-stu-id="e932d-139">**get\_CurrentStream**</span></span>](imediadet-get-currentstream.md)     | <span data-ttu-id="e932d-140">Récupère le numéro de flux actuellement utilisé par le détecteur de média.</span><span class="sxs-lookup"><span data-stu-id="e932d-140">Retrieves the stream number currently used by the media detector.</span></span><br/>                               |
| [<span data-ttu-id="e932d-141">**récupérer le \_ nom de fichier**</span><span class="sxs-lookup"><span data-stu-id="e932d-141">**get\_Filename**</span></span>](imediadet-get-filename.md)               | <span data-ttu-id="e932d-142">Récupère le nom du fichier source actuellement utilisé par le détecteur de média.</span><span class="sxs-lookup"><span data-stu-id="e932d-142">Retrieves the name of the source file currently used by the media detector.</span></span><br/>                     |
| [<span data-ttu-id="e932d-143">**recevoir le \_ filtre**</span><span class="sxs-lookup"><span data-stu-id="e932d-143">**get\_Filter**</span></span>](imediadet-get-filter.md)                   | <span data-ttu-id="e932d-144">Récupère un pointeur vers le filtre source actuellement utilisé par le détecteur de média.</span><span class="sxs-lookup"><span data-stu-id="e932d-144">Retrieves a pointer to the source filter currently used by the media detector.</span></span><br/>                  |
| [<span data-ttu-id="e932d-145">**recevoir une \_ cadence**</span><span class="sxs-lookup"><span data-stu-id="e932d-145">**get\_FrameRate**</span></span>](imediadet-get-framerate.md)             | <span data-ttu-id="e932d-146">Récupère la fréquence d’images du flux actuel.</span><span class="sxs-lookup"><span data-stu-id="e932d-146">Retrieves the frame rate of the current stream.</span></span><br/>                                                 |
| [<span data-ttu-id="e932d-147">**Obtient \_ OutputStreams**</span><span class="sxs-lookup"><span data-stu-id="e932d-147">**get\_OutputStreams**</span></span>](imediadet-get-outputstreams.md)     | <span data-ttu-id="e932d-148">Récupère le nombre de flux audio et vidéo contenus dans la source du média.</span><span class="sxs-lookup"><span data-stu-id="e932d-148">Retrieves the number of audio and video streams contained in the media source.</span></span><br/>                  |
| [<span data-ttu-id="e932d-149">**Obtient \_ StreamLength**</span><span class="sxs-lookup"><span data-stu-id="e932d-149">**get\_StreamLength**</span></span>](imediadet-get-streamlength.md)       | <span data-ttu-id="e932d-150">Récupère la durée du flux actuel.</span><span class="sxs-lookup"><span data-stu-id="e932d-150">Retrieves the duration of the current stream.</span></span><br/>                                                   |
| [<span data-ttu-id="e932d-151">**Obtient \_ StreamMediaType**</span><span class="sxs-lookup"><span data-stu-id="e932d-151">**get\_StreamMediaType**</span></span>](imediadet-get-streammediatype.md) | <span data-ttu-id="e932d-152">Récupère le type de média du flux actuel.</span><span class="sxs-lookup"><span data-stu-id="e932d-152">Retrieves the media type of the current stream.</span></span><br/>                                                 |
| [<span data-ttu-id="e932d-153">**Obtient \_ StreamType**</span><span class="sxs-lookup"><span data-stu-id="e932d-153">**get\_StreamType**</span></span>](imediadet-get-streamtype.md)           | <span data-ttu-id="e932d-154">Récupère l’identificateur global unique (GUID) pour le type de média du flux actuel.</span><span class="sxs-lookup"><span data-stu-id="e932d-154">Retrieves the globally unique identifier (GUID) for the media type of the current stream.</span></span><br/>       |
| [<span data-ttu-id="e932d-155">**Obtient \_ StreamTypeB**</span><span class="sxs-lookup"><span data-stu-id="e932d-155">**get\_StreamTypeB**</span></span>](imediadet-get-streamtypeb.md)         | <span data-ttu-id="e932d-156">Récupère une chaîne représentant le GUID du type de média pour le flux actuel.</span><span class="sxs-lookup"><span data-stu-id="e932d-156">Retrieves a string representing the GUID of the media type for the current stream.</span></span><br/>              |
| [<span data-ttu-id="e932d-157">**GetBitmapBits**</span><span class="sxs-lookup"><span data-stu-id="e932d-157">**GetBitmapBits**</span></span>](imediadet-getbitmapbits.md)              | <span data-ttu-id="e932d-158">Récupère une image vidéo à l’heure du média spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e932d-158">Retrieves a video frame at the specified media time.</span></span><br/>                                            |
| [<span data-ttu-id="e932d-159">**GetSampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="e932d-159">**GetSampleGrabber**</span></span>](imediadet-getsamplegrabber.md)        | <span data-ttu-id="e932d-160">Récupère un pointeur vers l’interface [**ISampleGrabber**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="e932d-160">Retrieves a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span><br/>                  |
| [<span data-ttu-id="e932d-161">**put \_ CurrentStream**</span><span class="sxs-lookup"><span data-stu-id="e932d-161">**put\_CurrentStream**</span></span>](imediadet-put-currentstream.md)     | <span data-ttu-id="e932d-162">Spécifie le numéro de flux du détecteur de média à utiliser.</span><span class="sxs-lookup"><span data-stu-id="e932d-162">Specifies the stream number for the media detector to use.</span></span><br/>                                      |
| [<span data-ttu-id="e932d-163">**Placer le \_ nom de fichier**</span><span class="sxs-lookup"><span data-stu-id="e932d-163">**put\_Filename**</span></span>](imediadet-put-filename.md)               | <span data-ttu-id="e932d-164">Spécifie le nom du fichier source pour le détecteur de média à utiliser.</span><span class="sxs-lookup"><span data-stu-id="e932d-164">Specifies the name of the source file for the media detector to use.</span></span><br/>                            |
| [<span data-ttu-id="e932d-165">**Placer le \_ filtre**</span><span class="sxs-lookup"><span data-stu-id="e932d-165">**put\_Filter**</span></span>](imediadet-put-filter.md)                   | <span data-ttu-id="e932d-166">Spécifie un filtre source pour le détecteur de média à utiliser.</span><span class="sxs-lookup"><span data-stu-id="e932d-166">Specifies a source filter for the media detector to use.</span></span><br/>                                        |
| [<span data-ttu-id="e932d-167">**WriteBitmapBits**</span><span class="sxs-lookup"><span data-stu-id="e932d-167">**WriteBitmapBits**</span></span>](imediadet-writebitmapbits.md)          | <span data-ttu-id="e932d-168">Récupère une image vidéo à l’heure du média spécifiée et l’écrit dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="e932d-168">Retrieves a video frame at the specified media time and writes it to a file.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="e932d-169">Notes</span><span class="sxs-lookup"><span data-stu-id="e932d-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e932d-170">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="e932d-170">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e932d-171">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e932d-171">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e932d-172">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e932d-172">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e932d-173">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e932d-173">Requirements</span></span>



| <span data-ttu-id="e932d-174">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e932d-174">Requirement</span></span> | <span data-ttu-id="e932d-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="e932d-175">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e932d-176">En-tête</span><span class="sxs-lookup"><span data-stu-id="e932d-176">Header</span></span><br/>  | <dl> <span data-ttu-id="e932d-177"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e932d-177"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e932d-178">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e932d-178">Library</span></span><br/> | <dl> <span data-ttu-id="e932d-179"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e932d-179"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
