---
description: Utilisation de sources multimédias avec la session multimédia
ms.assetid: b50d3d6e-728b-4ba5-9b79-413d2108ade1
title: Utilisation de sources multimédias avec la session multimédia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf08edf1d68ea11b05e8f8db83e247bc844cd85c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953386"
---
# <a name="using-media-sources-with-the-media-session"></a><span data-ttu-id="72aac-103">Utilisation de sources multimédias avec la session multimédia</span><span class="sxs-lookup"><span data-stu-id="72aac-103">Using Media Sources with the Media Session</span></span>

<span data-ttu-id="72aac-104">Si vous utilisez la session multimédia pour contrôler la lecture, l’ensemble de méthodes que vous devez appeler sur une source de média est limité.</span><span class="sxs-lookup"><span data-stu-id="72aac-104">If you are using the Media Session to control playback, the set of methods that you should call on a media source is restricted.</span></span> <span data-ttu-id="72aac-105">Cette section décrit comment utiliser la source de média conjointement avec la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="72aac-105">This section describes how to use media source in conjunction with the Media Session.</span></span>

<span data-ttu-id="72aac-106">Voici les étapes de base que votre application doit effectuer :</span><span class="sxs-lookup"><span data-stu-id="72aac-106">Here are the basic steps your application will perform:</span></span>

1.  <span data-ttu-id="72aac-107">Créez la source du média.</span><span class="sxs-lookup"><span data-stu-id="72aac-107">Create the media source.</span></span> <span data-ttu-id="72aac-108">Pour créer une source de média, utilisez le programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="72aac-108">To create a media source, use the source resolver.</span></span> <span data-ttu-id="72aac-109">Pour plus d’informations, consultez la page programme de [résolution source](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="72aac-109">For more information, see [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="72aac-110">Le programme de résolution source retourne un pointeur vers l’interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) de la source.</span><span class="sxs-lookup"><span data-stu-id="72aac-110">The source resolver returns a pointer to the source's [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span> <span data-ttu-id="72aac-111">(Si vous avez écrit une source de média personnalisée, vous pouvez fournir une méthode de création personnalisée à la place.)</span><span class="sxs-lookup"><span data-stu-id="72aac-111">(If you have written a custom media source, you can provide a custom creation method instead.)</span></span>

2.  <span data-ttu-id="72aac-112">Configurez la présentation.</span><span class="sxs-lookup"><span data-stu-id="72aac-112">Configure the presentation.</span></span> <span data-ttu-id="72aac-113">Pour configurer la présentation de la source, appelez [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="72aac-113">To configure the source's presentation, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="72aac-114">Vous pouvez modifier cette copie, mais les modifications ne sont pas actives tant que la lecture n’a pas commencé.</span><span class="sxs-lookup"><span data-stu-id="72aac-114">You can modify this copy, but the changes do not become active until the playback starts.</span></span> <span data-ttu-id="72aac-115">Ne modifiez pas le descripteur de présentation pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="72aac-115">Do not modify the presentation descriptor during playback.</span></span> <span data-ttu-id="72aac-116">Pour plus d’informations, consultez [descripteurs de présentation](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="72aac-116">For more information, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

3.  <span data-ttu-id="72aac-117">Créez une topologie qui contient la source du média.</span><span class="sxs-lookup"><span data-stu-id="72aac-117">Create a topology that contains the media source.</span></span> <span data-ttu-id="72aac-118">Pour plus d’informations, consultez [topologies](topologies.md).</span><span class="sxs-lookup"><span data-stu-id="72aac-118">For more information, see [Topologies](topologies.md).</span></span>

4.  <span data-ttu-id="72aac-119">Utilisez la session multimédia pour contrôler la lecture.</span><span class="sxs-lookup"><span data-stu-id="72aac-119">Use the Media Session to control playback.</span></span> <span data-ttu-id="72aac-120">La session multimédia appelle des méthodes sur la source du média.</span><span class="sxs-lookup"><span data-stu-id="72aac-120">The Media Session calls methods on the media source.</span></span> <span data-ttu-id="72aac-121">Pour l’instant, l’application ne doit pas appeler de méthode sur la source du média.</span><span class="sxs-lookup"><span data-stu-id="72aac-121">The application should not call any methods on the media source at this time.</span></span>

5.  <span data-ttu-id="72aac-122">Avant de libérer la source du média, appelez [**IMFMediaSource :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) pour arrêter la source.</span><span class="sxs-lookup"><span data-stu-id="72aac-122">Before releasing the media source, call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) to shut down the source.</span></span>

    > [!Note]  
    > <span data-ttu-id="72aac-123">Si vous utilisez la source de Sequencer, la source de Sequencer gère l’arrêt des sources de segment.</span><span class="sxs-lookup"><span data-stu-id="72aac-123">If you are using the sequencer source, the sequencer source handles shutting down the segment sources.</span></span> <span data-ttu-id="72aac-124">Pour plus d’informations, consultez [Sequencer source](sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="72aac-124">For more information, see [Sequencer Source](sequencer-source.md).</span></span>

     

<span data-ttu-id="72aac-125">Si vous utilisez la session multimédia, les seules méthodes que vous devez appeler sur la source du média sont [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor), [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics)et [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span><span class="sxs-lookup"><span data-stu-id="72aac-125">If you use the Media Session, the only methods that you should call on the media source are [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor), [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics), and [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span> <span data-ttu-id="72aac-126">En particulier :</span><span class="sxs-lookup"><span data-stu-id="72aac-126">In particular:</span></span>

-   <span data-ttu-id="72aac-127">N’appelez pas [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), [**Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause)ou [**Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop); ces méthodes doivent être appelées uniquement par la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="72aac-127">Do not call [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), [**Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause), or [**Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop); these methods should be called only by the Media Session.</span></span>

-   <span data-ttu-id="72aac-128">N’appelez aucune méthode [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) .</span><span class="sxs-lookup"><span data-stu-id="72aac-128">Do not call any [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) methods.</span></span>

-   <span data-ttu-id="72aac-129">Ne récupérez pas d’événements directement à partir de la source du média ou de l’un des flux.</span><span class="sxs-lookup"><span data-stu-id="72aac-129">Do not retrieve events directly from the media source or any of the streams.</span></span> <span data-ttu-id="72aac-130">La session multimédia doit recevoir ces événements pour que le pipeline fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="72aac-130">The Media Session must receive these events for the pipeline to function correctly.</span></span> <span data-ttu-id="72aac-131">La session multimédia transfère tous les événements qui sont requis par l’application.</span><span class="sxs-lookup"><span data-stu-id="72aac-131">The Media Session forwards any events that are needed by the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72aac-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="72aac-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72aac-133">Session multimédia</span><span class="sxs-lookup"><span data-stu-id="72aac-133">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 



