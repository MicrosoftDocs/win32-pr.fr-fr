---
description: Descripteurs de présentation
ms.assetid: 714c8bda-5ce1-47e2-ba73-9304e26b3129
title: Descripteurs de présentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44f1581e35fe6d875c691efdd5ef5736c1aa5215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527358"
---
# <a name="presentation-descriptors"></a><span data-ttu-id="92a55-103">Descripteurs de présentation</span><span class="sxs-lookup"><span data-stu-id="92a55-103">Presentation Descriptors</span></span>

<span data-ttu-id="92a55-104">Une *Présentation* est un ensemble de flux multimédia associés qui partagent un temps de présentation commun.</span><span class="sxs-lookup"><span data-stu-id="92a55-104">A *presentation* is a set of related media streams that share a common presentation time.</span></span> <span data-ttu-id="92a55-105">Par exemple, une présentation peut comporter des flux audio et vidéo provenant d’un film.</span><span class="sxs-lookup"><span data-stu-id="92a55-105">For example, a presentation might consist of the audio and video streams from a movie.</span></span> <span data-ttu-id="92a55-106">Un *descripteur de présentation* est un objet qui contient la description d’une présentation particulière.</span><span class="sxs-lookup"><span data-stu-id="92a55-106">A *presentation descriptor* is an object that contains the description of a particular presentation.</span></span> <span data-ttu-id="92a55-107">Les descripteurs de présentation sont utilisés pour configurer les sources multimédias et certains récepteurs multimédias.</span><span class="sxs-lookup"><span data-stu-id="92a55-107">Presentation descriptors are used to configure media sources and some media sinks.</span></span>

<span data-ttu-id="92a55-108">Chaque descripteur de présentation contient une liste d’un ou plusieurs *descripteurs de flux*.</span><span class="sxs-lookup"><span data-stu-id="92a55-108">Each presentation descriptor contains a list of one or more *stream descriptors*.</span></span> <span data-ttu-id="92a55-109">Ils décrivent les flux dans la présentation.</span><span class="sxs-lookup"><span data-stu-id="92a55-109">These describe the streams in the presentation.</span></span> <span data-ttu-id="92a55-110">Les flux peuvent être sélectionnés ou désélectionnés.</span><span class="sxs-lookup"><span data-stu-id="92a55-110">Streams can be either selected or deselected.</span></span> <span data-ttu-id="92a55-111">Seuls les flux sélectionnés produisent des données.</span><span class="sxs-lookup"><span data-stu-id="92a55-111">Only the selected streams produce data.</span></span> <span data-ttu-id="92a55-112">Les flux désélectionnés ne sont pas actifs et ne produisent aucune donnée.</span><span class="sxs-lookup"><span data-stu-id="92a55-112">Deselected streams are not active and do not produce any data.</span></span> <span data-ttu-id="92a55-113">Chaque descripteur de flux a un *Gestionnaire de type de média*, qui est utilisé pour modifier le type de média du flux ou obtenir le type de média actuel du flux.</span><span class="sxs-lookup"><span data-stu-id="92a55-113">Each stream descriptor has a *media type handler*, which is used to change the stream's media type or get the stream's current media type.</span></span> <span data-ttu-id="92a55-114">(Pour plus d’informations sur les types de médias, consultez [types de média](media-types.md).)</span><span class="sxs-lookup"><span data-stu-id="92a55-114">(For more information about media types, see [Media Types](media-types.md).)</span></span>

<span data-ttu-id="92a55-115">Le tableau suivant présente les interfaces principales exposées par chacun de ces objets.</span><span class="sxs-lookup"><span data-stu-id="92a55-115">The following table shows the primary interfaces that each of these objects exposes.</span></span>



| <span data-ttu-id="92a55-116">Object</span><span class="sxs-lookup"><span data-stu-id="92a55-116">Object</span></span>                  | <span data-ttu-id="92a55-117">Interface</span><span class="sxs-lookup"><span data-stu-id="92a55-117">Interface</span></span>                                                      |
|-------------------------|----------------------------------------------------------------|
| <span data-ttu-id="92a55-118">Descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="92a55-118">Presentation descriptor</span></span> | [<span data-ttu-id="92a55-119">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="92a55-119">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) |
| <span data-ttu-id="92a55-120">Descripteur de flux</span><span class="sxs-lookup"><span data-stu-id="92a55-120">Stream descriptor</span></span>       | [<span data-ttu-id="92a55-121">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="92a55-121">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)             |
| <span data-ttu-id="92a55-122">Gestionnaire de type de média</span><span class="sxs-lookup"><span data-stu-id="92a55-122">Media type handler</span></span>      | [<span data-ttu-id="92a55-123">**IMFMediaTypeHandler**</span><span class="sxs-lookup"><span data-stu-id="92a55-123">**IMFMediaTypeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)             |



 

## <a name="media-source-presentations"></a><span data-ttu-id="92a55-124">Présentations sources multimédias</span><span class="sxs-lookup"><span data-stu-id="92a55-124">Media Source Presentations</span></span>

<span data-ttu-id="92a55-125">Chaque source de média fournit un descripteur de présentation qui décrit la configuration par défaut de la source.</span><span class="sxs-lookup"><span data-stu-id="92a55-125">Every media source provides a presentation descriptor that describes the default configuration for the source.</span></span> <span data-ttu-id="92a55-126">Dans la configuration par défaut, au moins un flux est sélectionné, et chaque flux sélectionné a un type de média.</span><span class="sxs-lookup"><span data-stu-id="92a55-126">In the default configuration, at least one stream is selected, and every selected stream has a media type.</span></span> <span data-ttu-id="92a55-127">Pour récupérer le descripteur de présentation, appelez [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="92a55-127">To get the presentation descriptor, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="92a55-128">La méthode retourne un pointeur [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="92a55-128">The method returns an [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) pointer.</span></span>

<span data-ttu-id="92a55-129">Vous pouvez modifier le descripteur de présentation de la source pour sélectionner un autre ensemble de flux.</span><span class="sxs-lookup"><span data-stu-id="92a55-129">You can modify the source's presentation descriptor to select a different set of streams.</span></span> <span data-ttu-id="92a55-130">Ne modifiez pas le descripteur de présentation, sauf si la source du média est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="92a55-130">Do not modify the presentation descriptor unless the media source is stopped.</span></span> <span data-ttu-id="92a55-131">Les modifications sont appliquées quand vous appelez [**IMFMediaSource :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) pour démarrer la source.</span><span class="sxs-lookup"><span data-stu-id="92a55-131">The changes are applied when you call [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) to start the source.</span></span>

<span data-ttu-id="92a55-132">Pour connaître le nombre de flux, appelez [**IMFPresentationDescriptor :: GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount).</span><span class="sxs-lookup"><span data-stu-id="92a55-132">To get the number of streams, call [**IMFPresentationDescriptor::GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount).</span></span> <span data-ttu-id="92a55-133">Pour obtenir le descripteur de flux pour un flux, appelez [**IMFPresentationDescriptor :: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) et transmettez l’index du flux.</span><span class="sxs-lookup"><span data-stu-id="92a55-133">To get the stream descriptor for a stream, call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) and pass in the index of the stream.</span></span> <span data-ttu-id="92a55-134">Les flux sont indexés à partir de zéro.</span><span class="sxs-lookup"><span data-stu-id="92a55-134">Streams are indexed from zero.</span></span> <span data-ttu-id="92a55-135">La méthode **GetStreamDescriptorByIndex** retourne un pointeur [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="92a55-135">The **GetStreamDescriptorByIndex** method returns an [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) pointer.</span></span> <span data-ttu-id="92a55-136">Elle retourne également un indicateur booléen qui indique si le flux est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="92a55-136">It also returns a Boolean flag indicating whether the stream is selected.</span></span> <span data-ttu-id="92a55-137">Si le flux est sélectionné, la source du média produit des données pour ce flux.</span><span class="sxs-lookup"><span data-stu-id="92a55-137">If the stream is selected, the media source produces data for that stream.</span></span> <span data-ttu-id="92a55-138">Dans le cas contraire, la source ne produit pas de données pour ce flux.</span><span class="sxs-lookup"><span data-stu-id="92a55-138">Otherwise, the source does not produce any data for that stream.</span></span> <span data-ttu-id="92a55-139">Pour sélectionner un flux, appelez [**IMFPresentationDescriptor :: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) avec l’index du flux.</span><span class="sxs-lookup"><span data-stu-id="92a55-139">To select a stream, call [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) with the index of the stream.</span></span> <span data-ttu-id="92a55-140">Pour désélectionner un flux, appelez [**IMFPresentationDescriptor ::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).</span><span class="sxs-lookup"><span data-stu-id="92a55-140">To deselect a stream, call [**IMFPresentationDescriptor::DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).</span></span>

<span data-ttu-id="92a55-141">Le code suivant montre comment obtenir le descripteur de présentation à partir d’une source multimédia et comment énumérer les flux.</span><span class="sxs-lookup"><span data-stu-id="92a55-141">The following code shows how to get the presentation descriptor from a media source and enumerate the streams.</span></span>


```C++
HRESULT hr = S_OK;
DWORD cStreams = 0;
BOOL  fSelected = FALSE;

IMFPresentationDescriptor *pPresentation = NULL;
IMFStreamDescriptor *pStreamDesc = NULL;

hr = pSource->CreatePresentationDescriptor(&pPresentation);

if (SUCCEEDED(hr))
{
    hr = pPresentation->GetStreamDescriptorCount(&cStreams);
}

if (SUCCEEDED(hr))
{
    for (DWORD iStream = 0; iStream < cStreams; iStream++)
    {
        hr = pPresentation->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);

        if (FAILED(hr))
        {
            break;
        }

        /*  Use the stream descriptor. (Not shown.) */

        SAFE_RELEASE(pStreamDesc);
    }
}
SAFE_RELEASE(pPresentation);
SAFE_RELEASE(pStreamDesc);
```



## <a name="media-type-handlers"></a><span data-ttu-id="92a55-142">Gestionnaires de type de média</span><span class="sxs-lookup"><span data-stu-id="92a55-142">Media Type Handlers</span></span>

<span data-ttu-id="92a55-143">Pour modifier le type de média du flux ou pour récupérer le type de média actuel du flux, utilisez le gestionnaire de type de média du descripteur de flux.</span><span class="sxs-lookup"><span data-stu-id="92a55-143">To change the stream's media type or to get the stream's current media type, use the stream descriptor's media type handler.</span></span> <span data-ttu-id="92a55-144">Appelez [**IMFStreamDescriptor :: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) pour accéder au gestionnaire de type de média.</span><span class="sxs-lookup"><span data-stu-id="92a55-144">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) to get the media type handler.</span></span> <span data-ttu-id="92a55-145">Cette méthode retourne un pointeur [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) .</span><span class="sxs-lookup"><span data-stu-id="92a55-145">This method returns an [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) pointer.</span></span>

<span data-ttu-id="92a55-146">Si vous souhaitez simplement connaître le type de données dans le flux, par exemple audio ou vidéo, appelez [**IMFMediaTypeHandler :: GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype).</span><span class="sxs-lookup"><span data-stu-id="92a55-146">If you simply want to know what kind of data is in the stream, such as audio or video, call [**IMFMediaTypeHandler::GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype).</span></span> <span data-ttu-id="92a55-147">Cette méthode retourne le GUID pour le type de média principal.</span><span class="sxs-lookup"><span data-stu-id="92a55-147">This method returns the GUID for the major media type.</span></span> <span data-ttu-id="92a55-148">Par exemple, une application de lecture connecte généralement un flux audio au convertisseur audio et un flux vidéo au convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="92a55-148">For example, a playback application typically connects an audio stream to the audio renderer and a video stream to the video renderer.</span></span> <span data-ttu-id="92a55-149">Si vous utilisez la session de média ou le chargeur de topologie pour créer une topologie, le GUID de type principal peut être les seules informations de format dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="92a55-149">If you use the Media Session or the topology loader to build a topology, the major type GUID might be the only format information that you need.</span></span>

<span data-ttu-id="92a55-150">Si votre application a besoin d’informations plus détaillées sur le format actuel, appelez [**IMFMediaTypeHandler :: GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype).</span><span class="sxs-lookup"><span data-stu-id="92a55-150">If your application needs more detailed information about the current format, call [**IMFMediaTypeHandler::GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype).</span></span> <span data-ttu-id="92a55-151">Cette méthode retourne un pointeur vers l’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) du type de média.</span><span class="sxs-lookup"><span data-stu-id="92a55-151">This method returns a pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface of the media type.</span></span> <span data-ttu-id="92a55-152">Utilisez cette interface pour récupérer les détails du format.</span><span class="sxs-lookup"><span data-stu-id="92a55-152">Use this interface to get the details of the format.</span></span>

<span data-ttu-id="92a55-153">Le gestionnaire de type de média contient également une liste de types de média pris en charge pour le flux.</span><span class="sxs-lookup"><span data-stu-id="92a55-153">The media type handler also contains a list of supported media types for the stream.</span></span> <span data-ttu-id="92a55-154">Pour connaître la taille de la liste, appelez [**IMFMediaTypeHandler :: GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount).</span><span class="sxs-lookup"><span data-stu-id="92a55-154">To get the size of the list, call [**IMFMediaTypeHandler::GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount).</span></span> <span data-ttu-id="92a55-155">Pour obtenir un type de média à partir de la liste, appelez [**IMFMediaTypeHandler :: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) avec l’index du type de média.</span><span class="sxs-lookup"><span data-stu-id="92a55-155">To get a media type from the list, call [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) with the index of the media type.</span></span> <span data-ttu-id="92a55-156">Les types de média sont retournés dans l’ordre de préférence approximatif.</span><span class="sxs-lookup"><span data-stu-id="92a55-156">Media types are returned in the approximate order of preference.</span></span> <span data-ttu-id="92a55-157">Par exemple, pour les formats audio, des taux d’échantillonnage plus élevés sont préférés par rapport aux taux d’échantillonnage inférieurs.</span><span class="sxs-lookup"><span data-stu-id="92a55-157">For example, for audio formats, higher sample rates are preferred over lower sample rates.</span></span> <span data-ttu-id="92a55-158">Toutefois, il n’existe aucune règle définitive qui régit le classement. vous devez donc le traiter simplement comme une indication.</span><span class="sxs-lookup"><span data-stu-id="92a55-158">However, there is no definitive rule that governs the ordering, so you should treat it simply as a guideline.</span></span>

<span data-ttu-id="92a55-159">La liste des types pris en charge peut ne pas contenir tous les types de médias pris en charge par le flux.</span><span class="sxs-lookup"><span data-stu-id="92a55-159">The list of supported types might not contain every possible media type that the stream supports.</span></span> <span data-ttu-id="92a55-160">Pour vérifier si un type de média particulier est pris en charge, appelez [**IMFMediaTypeHandler :: IsMediaTypeSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported).</span><span class="sxs-lookup"><span data-stu-id="92a55-160">To test whether a particular media type is supported, call [**IMFMediaTypeHandler::IsMediaTypeSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported).</span></span> <span data-ttu-id="92a55-161">Pour définir le type de média, appelez [**IMFMediaTypeHandler :: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype).</span><span class="sxs-lookup"><span data-stu-id="92a55-161">To set the media type, call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype).</span></span> <span data-ttu-id="92a55-162">Si la méthode est réussie, le flux contient des données conformes au format spécifié.</span><span class="sxs-lookup"><span data-stu-id="92a55-162">If the method succeeds, the stream will contain data that conforms to the specified format.</span></span> <span data-ttu-id="92a55-163">La méthode **SetCurrentMediaType** ne modifie pas la liste des types préférés.</span><span class="sxs-lookup"><span data-stu-id="92a55-163">The **SetCurrentMediaType** method does not change the list of preferred types.</span></span>

<span data-ttu-id="92a55-164">Le code suivant montre comment récupérer le gestionnaire de type de média, comment énumérer les types de média préférés et comment définir le type de média.</span><span class="sxs-lookup"><span data-stu-id="92a55-164">The following code shows how to get the media type handler, enumerate the preferred media types, and set the media type.</span></span> <span data-ttu-id="92a55-165">Cet exemple suppose que l’application possède un algorithme, non illustré ici, pour la sélection du type de média.</span><span class="sxs-lookup"><span data-stu-id="92a55-165">This example assumes that the application has some algorithm, not shown here, for selecting the media type.</span></span> <span data-ttu-id="92a55-166">Les spécificités dépendent beaucoup de votre application.</span><span class="sxs-lookup"><span data-stu-id="92a55-166">The specifics will depend greatly on your application.</span></span>


```C++
HRESULT hr = S_OK;
DWORD cTypes = 0;
BOOL  bTypeOK = FALSE;

IMFMediaTypeHandler *pHandler = NULL;
IMFMediaType *pMediaType = NULL;

hr = pStreamDesc->GetMediaTypeHandler(&pHandler);

if (SUCCEEDED(hr))
{
    hr = pHandler->GetMediaTypeCount(&cTypes);
}

if (SUCCEEDED(hr))
{
    for (DWORD iType = 0; iType < cTypes; iType++)
    {   
        hr = pHandler->GetMediaTypeByIndex(iType, &pMediaType);

        if (FAILED(hr))
        {
            break;
        }

        /* Examine the media type. (Not shown.)  */

        /* If this media type is acceptable, set the media type. */

        if (bTypeOK)
        {
            hr = pHandler->SetCurrentMediaType(pMediaType);
            break;
        }

        SAFE_RELEASE(pMediaType);
    }
}    

SAFE_RELEASE(pMediaType);
SAFE_RELEASE(pHandler);
```



## <a name="related-topics"></a><span data-ttu-id="92a55-167">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="92a55-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92a55-168">Sources multimédias</span><span class="sxs-lookup"><span data-stu-id="92a55-168">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="92a55-169">API de plateforme Media Foundation</span><span class="sxs-lookup"><span data-stu-id="92a55-169">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



