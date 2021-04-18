---
description: Événements de source de média
ms.assetid: c7b6ea86-e919-45b8-a1f9-bd18c3aed163
title: Événements de source de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c40755a32f610b33ef3a5c66d3acb448223813
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106527263"
---
# <a name="media-source-events"></a><span data-ttu-id="308b6-103">Événements de source de média</span><span class="sxs-lookup"><span data-stu-id="308b6-103">Media Source Events</span></span>

<span data-ttu-id="308b6-104">Cette rubrique répertorie les événements qui sont envoyés par les sources de média et les flux multimédias.</span><span class="sxs-lookup"><span data-stu-id="308b6-104">This topic lists the events that are sent by media sources and media streams.</span></span> <span data-ttu-id="308b6-105">Les sources multimédias peuvent également envoyer des événements personnalisés qui ne sont pas répertoriés ici.</span><span class="sxs-lookup"><span data-stu-id="308b6-105">Media sources can also send custom events not listed here.</span></span>

## <a name="media-source-events"></a><span data-ttu-id="308b6-106">Événements de source de média</span><span class="sxs-lookup"><span data-stu-id="308b6-106">Media Source Events</span></span>



| <span data-ttu-id="308b6-107">Événement</span><span class="sxs-lookup"><span data-stu-id="308b6-107">Event</span></span>                                                                      | <span data-ttu-id="308b6-108">Description</span><span class="sxs-lookup"><span data-stu-id="308b6-108">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="308b6-109">Événement MEEndOfPresentation</span><span class="sxs-lookup"><span data-stu-id="308b6-109">MEEndOfPresentation Event</span></span>](meendofpresentation.md)                       | <span data-ttu-id="308b6-110">La présentation s’est terminée.</span><span class="sxs-lookup"><span data-stu-id="308b6-110">The presentation ended.</span></span> <span data-ttu-id="308b6-111">Tous les flux de la présentation ont atteint la fin du flux.</span><span class="sxs-lookup"><span data-stu-id="308b6-111">All streams in the presentation have reached the end of the stream.</span></span>      |
| [<span data-ttu-id="308b6-112">Événement MENewStream</span><span class="sxs-lookup"><span data-stu-id="308b6-112">MENewStream Event</span></span>](menewstream.md)                                       | <span data-ttu-id="308b6-113">Un nouveau flux a été créé.</span><span class="sxs-lookup"><span data-stu-id="308b6-113">A new stream was created.</span></span> <span data-ttu-id="308b6-114">L’événement contient un pointeur vers le flux.</span><span class="sxs-lookup"><span data-stu-id="308b6-114">The event contains a pointer to the stream.</span></span>                            |
| [<span data-ttu-id="308b6-115">Événement MESourceCharacteristicsChanged</span><span class="sxs-lookup"><span data-stu-id="308b6-115">MESourceCharacteristicsChanged Event</span></span>](mesourcecharacteristicschanged.md) | <span data-ttu-id="308b6-116">Les caractéristiques de la source ont changé.</span><span class="sxs-lookup"><span data-stu-id="308b6-116">The characteristics of the source have changed.</span></span> <span data-ttu-id="308b6-117">(Facultatif.)</span><span class="sxs-lookup"><span data-stu-id="308b6-117">(Optional.)</span></span>                                      |
| [<span data-ttu-id="308b6-118">Événement MESourceMetadataChanged</span><span class="sxs-lookup"><span data-stu-id="308b6-118">MESourceMetadataChanged Event</span></span>](mesourcemetadatachanged.md)               | <span data-ttu-id="308b6-119">Les métadonnées de la source ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="308b6-119">The source's metadata has changed.</span></span> <span data-ttu-id="308b6-120">(Facultatif.)</span><span class="sxs-lookup"><span data-stu-id="308b6-120">(Optional.)</span></span>                                                   |
| [<span data-ttu-id="308b6-121">Événement MESourcePaused</span><span class="sxs-lookup"><span data-stu-id="308b6-121">MESourcePaused Event</span></span>](mesourcepaused.md)                                 | <span data-ttu-id="308b6-122">La source a été suspendue.</span><span class="sxs-lookup"><span data-stu-id="308b6-122">The source was paused.</span></span> <span data-ttu-id="308b6-123">Toutes les sources ne prennent pas en charge la suspension.</span><span class="sxs-lookup"><span data-stu-id="308b6-123">Not all sources support pausing.</span></span>                                          |
| [<span data-ttu-id="308b6-124">Événement MESourceRateChanged</span><span class="sxs-lookup"><span data-stu-id="308b6-124">MESourceRateChanged Event</span></span>](mesourceratechanged.md)                       | <span data-ttu-id="308b6-125">La vitesse de lecture de la source a changé.</span><span class="sxs-lookup"><span data-stu-id="308b6-125">The source's playback rate has changed.</span></span> <span data-ttu-id="308b6-126">(Facultatif ; s’applique si la source prend en charge le contrôle de fréquence.)</span><span class="sxs-lookup"><span data-stu-id="308b6-126">(Optional; applies if the source supports rate control.)</span></span> |
| [<span data-ttu-id="308b6-127">Événement MESourceRateChangeRequested</span><span class="sxs-lookup"><span data-stu-id="308b6-127">MESourceRateChangeRequested Event</span></span>](mesourceratechangerequested.md)       | <span data-ttu-id="308b6-128">La source demande un nouveau taux de lecture.</span><span class="sxs-lookup"><span data-stu-id="308b6-128">The source is requesting a new playback rate.</span></span> <span data-ttu-id="308b6-129">(Facultatif.)</span><span class="sxs-lookup"><span data-stu-id="308b6-129">(Optional.)</span></span>                                        |
| [<span data-ttu-id="308b6-130">Événement MESourceSeeked</span><span class="sxs-lookup"><span data-stu-id="308b6-130">MESourceSeeked Event</span></span>](mesourceseeked.md)                                 | <span data-ttu-id="308b6-131">La source a été recherchée.</span><span class="sxs-lookup"><span data-stu-id="308b6-131">The source was seeked.</span></span> <span data-ttu-id="308b6-132">Toutes les sources ne prennent pas en charge la recherche.</span><span class="sxs-lookup"><span data-stu-id="308b6-132">Not all sources support seeking.</span></span>                                          |
| [<span data-ttu-id="308b6-133">Événement MESourceStarted</span><span class="sxs-lookup"><span data-stu-id="308b6-133">MESourceStarted Event</span></span>](mesourcestarted.md)                               | <span data-ttu-id="308b6-134">La source a été démarrée.</span><span class="sxs-lookup"><span data-stu-id="308b6-134">The source was started.</span></span>                                                                          |
| [<span data-ttu-id="308b6-135">Événement MESourceStopped</span><span class="sxs-lookup"><span data-stu-id="308b6-135">MESourceStopped Event</span></span>](mesourcestopped.md)                               | <span data-ttu-id="308b6-136">La source a été arrêtée.</span><span class="sxs-lookup"><span data-stu-id="308b6-136">The source was stopped.</span></span>                                                                          |
| [<span data-ttu-id="308b6-137">Événement MEUpdatedStream</span><span class="sxs-lookup"><span data-stu-id="308b6-137">MEUpdatedStream Event</span></span>](meupdatedstream.md)                               | <span data-ttu-id="308b6-138">Un flux existant a été cherché ou redémarré.</span><span class="sxs-lookup"><span data-stu-id="308b6-138">An existing stream was seeked or re-started.</span></span> <span data-ttu-id="308b6-139">L’événement contient un pointeur vers le flux.</span><span class="sxs-lookup"><span data-stu-id="308b6-139">The event contains a pointer to the stream.</span></span>         |



 

## <a name="media-stream-events"></a><span data-ttu-id="308b6-140">Événements de flux multimédia</span><span class="sxs-lookup"><span data-stu-id="308b6-140">Media Stream Events</span></span>



| <span data-ttu-id="308b6-141">Événement</span><span class="sxs-lookup"><span data-stu-id="308b6-141">Event</span></span>                                                    | <span data-ttu-id="308b6-142">Description</span><span class="sxs-lookup"><span data-stu-id="308b6-142">Description</span></span>                                                                                                                    |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="308b6-143">Événement MEEndOfStream</span><span class="sxs-lookup"><span data-stu-id="308b6-143">MEEndOfStream Event</span></span>](meendofstream.md)                 | <span data-ttu-id="308b6-144">Le flux s’est terminé.</span><span class="sxs-lookup"><span data-stu-id="308b6-144">The stream ended.</span></span>                                                                                                              |
| [<span data-ttu-id="308b6-145">Événement MEError</span><span class="sxs-lookup"><span data-stu-id="308b6-145">MEError Event</span></span>](meerror.md)                             | <span data-ttu-id="308b6-146">Une erreur s’est produite lors de la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="308b6-146">An error has occurred during streaming.</span></span> <span data-ttu-id="308b6-147">Utilisez cet événement pour les erreurs qui ne sont pas liées à l’un des autres événements répertoriés ici.</span><span class="sxs-lookup"><span data-stu-id="308b6-147">Use this event for errors that are not related to any of the other events listed here.</span></span> |
| [<span data-ttu-id="308b6-148">Événement MEMediaSample</span><span class="sxs-lookup"><span data-stu-id="308b6-148">MEMediaSample Event</span></span>](memediasample.md)                 | <span data-ttu-id="308b6-149">Le flux a généré un nouvel exemple.</span><span class="sxs-lookup"><span data-stu-id="308b6-149">The stream has generated a new sample.</span></span>                                                                                         |
| [<span data-ttu-id="308b6-150">Événement MEStreamFormatChanged</span><span class="sxs-lookup"><span data-stu-id="308b6-150">MEStreamFormatChanged Event</span></span>](mestreamformatchanged.md) | <span data-ttu-id="308b6-151">Le type de média a changé.</span><span class="sxs-lookup"><span data-stu-id="308b6-151">The media type has changed.</span></span> <span data-ttu-id="308b6-152">(Facultatif.)</span><span class="sxs-lookup"><span data-stu-id="308b6-152">(Optional.)</span></span>                                                                                        |
| [<span data-ttu-id="308b6-153">Événement MEStreamPaused</span><span class="sxs-lookup"><span data-stu-id="308b6-153">MEStreamPaused Event</span></span>](mestreampaused.md)               | <span data-ttu-id="308b6-154">Le flux a été suspendu.</span><span class="sxs-lookup"><span data-stu-id="308b6-154">The stream was paused.</span></span>                                                                                                         |
| [<span data-ttu-id="308b6-155">Événement MEStreamSeeked</span><span class="sxs-lookup"><span data-stu-id="308b6-155">MEStreamSeeked Event</span></span>](mestreamseeked.md)               | <span data-ttu-id="308b6-156">Le flux a été cherché.</span><span class="sxs-lookup"><span data-stu-id="308b6-156">The stream was seeked.</span></span>                                                                                                         |
| [<span data-ttu-id="308b6-157">Événement MEStreamStarted</span><span class="sxs-lookup"><span data-stu-id="308b6-157">MEStreamStarted Event</span></span>](mestreamstarted.md)             | <span data-ttu-id="308b6-158">Le flux a été démarré.</span><span class="sxs-lookup"><span data-stu-id="308b6-158">The stream was started.</span></span>                                                                                                        |
| [<span data-ttu-id="308b6-159">Événement MEStreamStopped</span><span class="sxs-lookup"><span data-stu-id="308b6-159">MEStreamStopped Event</span></span>](mestreamstopped.md)             | <span data-ttu-id="308b6-160">Le flux a été arrêté.</span><span class="sxs-lookup"><span data-stu-id="308b6-160">The stream was stopped.</span></span>                                                                                                        |
| [<span data-ttu-id="308b6-161">Événement MEStreamThinMode</span><span class="sxs-lookup"><span data-stu-id="308b6-161">MEStreamThinMode Event</span></span>](mestreamthinmode.md)           | <span data-ttu-id="308b6-162">Le mode de réduction a démarré ou s’est arrêté.</span><span class="sxs-lookup"><span data-stu-id="308b6-162">Thinning mode has started or stopped.</span></span> <span data-ttu-id="308b6-163">(Facultatif.)</span><span class="sxs-lookup"><span data-stu-id="308b6-163">(Optional.)</span></span>                                                                              |
| [<span data-ttu-id="308b6-164">Événement MEStreamTick</span><span class="sxs-lookup"><span data-stu-id="308b6-164">MEStreamTick Event</span></span>](mestreamtick.md)                   | <span data-ttu-id="308b6-165">Il y a un intervalle dans le flux.</span><span class="sxs-lookup"><span data-stu-id="308b6-165">There is a gap in the stream.</span></span> <span data-ttu-id="308b6-166">(Facultatif.)</span><span class="sxs-lookup"><span data-stu-id="308b6-166">(Optional.)</span></span>                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="308b6-167">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="308b6-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="308b6-168">Sources multimédias</span><span class="sxs-lookup"><span data-stu-id="308b6-168">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 



