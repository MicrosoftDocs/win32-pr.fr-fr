---
description: Ce didacticiel montre comment lire des fichiers multimédias à l’aide de l’objet Media session.
ms.assetid: cdd67082-8153-4f48-abc5-278be82ae082
title: Comment lire des fichiers multimédias avec Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163dba2f9f67139ce7477470889e13a54e2c8b5d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104558385"
---
# <a name="how-to-play-media-files-with-media-foundation"></a><span data-ttu-id="deac3-103">Comment lire des fichiers multimédias avec Media Foundation</span><span class="sxs-lookup"><span data-stu-id="deac3-103">How to Play Media Files with Media Foundation</span></span>

<span data-ttu-id="deac3-104">Ce didacticiel montre comment lire des fichiers multimédias à l’aide de l’objet [Media session](media-session.md) .</span><span class="sxs-lookup"><span data-stu-id="deac3-104">This tutorial shows how to play media files using the [Media Session](media-session.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="deac3-105">Prérequis</span><span class="sxs-lookup"><span data-stu-id="deac3-105">Prerequisites</span></span>

<span data-ttu-id="deac3-106">Avant de lire cette rubrique, vous devez être familiarisé avec les concepts de Media Foundation suivants :</span><span class="sxs-lookup"><span data-stu-id="deac3-106">Before reading this topic, you should be familiar with the following Media Foundation concepts:</span></span>

-   [<span data-ttu-id="deac3-107">Session multimédia</span><span class="sxs-lookup"><span data-stu-id="deac3-107">Media Session</span></span>](media-session.md)
-   [<span data-ttu-id="deac3-108">Résolveur source</span><span class="sxs-lookup"><span data-stu-id="deac3-108">Source Resolver</span></span>](source-resolver.md)
-   [<span data-ttu-id="deac3-109">Topologies</span><span class="sxs-lookup"><span data-stu-id="deac3-109">Topologies</span></span>](topologies.md)
-   [<span data-ttu-id="deac3-110">Générateurs d’événements de média</span><span class="sxs-lookup"><span data-stu-id="deac3-110">Media Event Generators</span></span>](media-event-generators.md)
-   [<span data-ttu-id="deac3-111">Descripteurs de présentation</span><span class="sxs-lookup"><span data-stu-id="deac3-111">Presentation Descriptors</span></span>](presentation-descriptors.md)

> [!Note]  
> <span data-ttu-id="deac3-112">Cette rubrique ne décrit pas comment lire des fichiers protégés par la gestion des droits numériques (DRM).</span><span class="sxs-lookup"><span data-stu-id="deac3-112">This topic does not describe how to play files that are protected by digital rights management (DRM).</span></span> <span data-ttu-id="deac3-113">Pour plus d’informations sur DRM dans Microsoft Media Foundation, consultez [Comment lire des fichiers multimédias protégés](how-to-play-protected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="deac3-113">For information about DRM in Microsoft Media Foundation, see [How to Play Protected Media Files](how-to-play-protected-media-files.md).</span></span>

 

## <a name="overview"></a><span data-ttu-id="deac3-114">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="deac3-114">Overview</span></span>

<span data-ttu-id="deac3-115">Les objets suivants sont utilisés pour lire un fichier multimédia avec la session multimédia :</span><span class="sxs-lookup"><span data-stu-id="deac3-115">The following objects are used to play a media file with the Media Session:</span></span>

-   <span data-ttu-id="deac3-116">Une *source de média* est un objet qui analyse un fichier multimédia ou une autre source de données multimédias.</span><span class="sxs-lookup"><span data-stu-id="deac3-116">A *media source* is an object that parses a media file or other source of media data.</span></span> <span data-ttu-id="deac3-117">La source du média crée des objets de *flux* pour chaque flux audio ou vidéo dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="deac3-117">The media source creates *stream* objects for each audio or video stream in the file.</span></span> <span data-ttu-id="deac3-118">Les *décodeurs* convertissent les données multimédias encodées en vidéo et audio non compressés.</span><span class="sxs-lookup"><span data-stu-id="deac3-118">*Decoders* convert encoded media data into uncompressed video and audio.</span></span>
-   <span data-ttu-id="deac3-119">Le programme de *résolution source* crée une source de média à partir d’une URL.</span><span class="sxs-lookup"><span data-stu-id="deac3-119">The *Source Resolver* creates a media source from a URL.</span></span>
-   <span data-ttu-id="deac3-120">Le [convertisseur vidéo amélioré](enhanced-video-renderer.md) (EVR) affiche la vidéo à l’écran.</span><span class="sxs-lookup"><span data-stu-id="deac3-120">The [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) renders video to the screen.</span></span>
-   <span data-ttu-id="deac3-121">Le [convertisseur audio de streaming](streaming-audio-renderer.md) (SAR) restitue l’audio sur un haut-parleur ou un autre périphérique de sortie audio.</span><span class="sxs-lookup"><span data-stu-id="deac3-121">The [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR) renders audio to a speaker or other audio output device.</span></span>
-   <span data-ttu-id="deac3-122">Une *topologie* définit le workflow des données de la source du média vers les EVR et SAR.</span><span class="sxs-lookup"><span data-stu-id="deac3-122">A *topology* defines the flow of data from the media source to the EVR and SAR.</span></span>
-   <span data-ttu-id="deac3-123">La *session multimédia* contrôle le workflow et envoie des événements d’État à l’application.</span><span class="sxs-lookup"><span data-stu-id="deac3-123">The *Media Session* controls the data flow and sends status events to the application.</span></span> <span data-ttu-id="deac3-124">Le diagramme suivant illustre ce processus.</span><span class="sxs-lookup"><span data-stu-id="deac3-124">The following diagram illustrates this process.</span></span>

![Diagramme montrant la lecture à l’aide de la session multimédia](images/session-playback.gif)

<span data-ttu-id="deac3-126">Voici un aperçu général des étapes nécessaires pour lire un fichier multimédia à l’aide de la session de média :</span><span class="sxs-lookup"><span data-stu-id="deac3-126">The following is a general outline of the steps needed to play a media file using the Media Session:</span></span>

1.  <span data-ttu-id="deac3-127">Appelez la fonction [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) pour initialiser la plateforme Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="deac3-127">Call the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function to initialize the Media Foundation platform.</span></span>
2.  <span data-ttu-id="deac3-128">Appelez [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) pour créer une nouvelle instance de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="deac3-128">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create a new instance of the Media Session.</span></span>
3.  <span data-ttu-id="deac3-129">Utilisez le programme de résolution source pour créer une source de média.</span><span class="sxs-lookup"><span data-stu-id="deac3-129">Use the source resolver to create a media source.</span></span> <span data-ttu-id="deac3-130">Pour plus d’informations, consultez [utilisation du programme de résolution source](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="deac3-130">For more information, see [Using the Source Resolver](using-the-source-resolver.md).</span></span>
4.  <span data-ttu-id="deac3-131">Créez une topologie qui connecte la source du média aux EVR et aux SAR.</span><span class="sxs-lookup"><span data-stu-id="deac3-131">Create a topology that connects the media source to the EVR and SAR.</span></span> <span data-ttu-id="deac3-132">Dans cette étape, l’application crée une topologie *partielle* qui n’inclut pas les décodeurs.</span><span class="sxs-lookup"><span data-stu-id="deac3-132">In this step, the application creates a *partial* topology that does not include the decoders.</span></span> <span data-ttu-id="deac3-133">Pour plus d’informations, consultez [création de topologies de lecture](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="deac3-133">For more information, see [Creating Playback Topologies](creating-playback-topologies.md).</span></span>
5.  <span data-ttu-id="deac3-134">Appelez [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) pour définir la topologie sur la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="deac3-134">Call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the topology on the Media Session.</span></span>
6.  <span data-ttu-id="deac3-135">Utilisez l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) pour récupérer les événements de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="deac3-135">Use the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface to get events from the Media Session.</span></span>
7.  <span data-ttu-id="deac3-136">Appelez [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) pour démarrer la lecture.</span><span class="sxs-lookup"><span data-stu-id="deac3-136">Call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) to start playback.</span></span> <span data-ttu-id="deac3-137">Une fois la lecture démarrée, vous pouvez la suspendre en appelant [**IMFMediaSession ::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)ou l’arrêter en appelant [**IMFMediaSession :: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span><span class="sxs-lookup"><span data-stu-id="deac3-137">After playback starts, you can pause it by calling [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause), or stop it by calling [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span></span>
8.  <span data-ttu-id="deac3-138">Lorsque l’application se ferme, libérer les ressources :</span><span class="sxs-lookup"><span data-stu-id="deac3-138">When the application exits, release resources:</span></span>

    1.  <span data-ttu-id="deac3-139">Appelez [**IMFMediaSession :: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) pour fermer la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="deac3-139">Call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the Media Session.</span></span> <span data-ttu-id="deac3-140">Cette méthode est asynchrone.</span><span class="sxs-lookup"><span data-stu-id="deac3-140">This method is asynchronous.</span></span> <span data-ttu-id="deac3-141">Une fois l’opération terminée, la session multimédia envoie un événement [MESessionClosed](mesessionclosed.md) .</span><span class="sxs-lookup"><span data-stu-id="deac3-141">When it completes, the Media Session sends an [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="deac3-142">Ensuite, il est possible d’effectuer les étapes restantes.</span><span class="sxs-lookup"><span data-stu-id="deac3-142">Then it is safe to perform the remaining steps.</span></span>
    2.  <span data-ttu-id="deac3-143">Appelez [**IMFMediaSource :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) pour arrêter la source du média.</span><span class="sxs-lookup"><span data-stu-id="deac3-143">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) to shut down the media source.</span></span>
    3.  <span data-ttu-id="deac3-144">Appelez [**IMFMediaSession :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) pour arrêter la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="deac3-144">Call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) to shut down the Media Session.</span></span>
    4.  <span data-ttu-id="deac3-145">Appelez [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) pour arrêter la plateforme Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="deac3-145">Call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to shut down the Media Foundation platform.</span></span>

<span data-ttu-id="deac3-146">Les sections suivantes présentent un exemple de code complet :</span><span class="sxs-lookup"><span data-stu-id="deac3-146">The following sections show a complete code example:</span></span>

-   [<span data-ttu-id="deac3-147">Étape 1 : déclarer la classe CPlayer</span><span class="sxs-lookup"><span data-stu-id="deac3-147">Step 1: Declare the CPlayer Class</span></span>](step-1--declare-the-cplayer-class.md)
-   [<span data-ttu-id="deac3-148">Étape 2 : créer l’objet CPlayer</span><span class="sxs-lookup"><span data-stu-id="deac3-148">Step 2: Create the CPlayer Object</span></span>](step-2--create-the-cplayer-object.md)
-   [<span data-ttu-id="deac3-149">Étape 3 : ouvrir un fichier multimédia</span><span class="sxs-lookup"><span data-stu-id="deac3-149">Step 3: Open a Media File</span></span>](step-3--open-a-media-file.md)
-   [<span data-ttu-id="deac3-150">Étape 4 : créer la session multimédia</span><span class="sxs-lookup"><span data-stu-id="deac3-150">Step 4: Create the Media Session</span></span>](step-4--create-the-media-session.md)
-   [<span data-ttu-id="deac3-151">Étape 5 : gérer les événements de session multimédia</span><span class="sxs-lookup"><span data-stu-id="deac3-151">Step 5: Handle Media Session Events</span></span>](step-5--handle-media-session-events.md)
-   [<span data-ttu-id="deac3-152">Étape 6 : contrôler la lecture</span><span class="sxs-lookup"><span data-stu-id="deac3-152">Step 6: Control Playback</span></span>](step-6--control-playback.md)
-   [<span data-ttu-id="deac3-153">Étape 7 : arrêter la session multimédia</span><span class="sxs-lookup"><span data-stu-id="deac3-153">Step 7: Shut Down the Media Session</span></span>](step-7--shut-down-the-media-session.md)
-   [<span data-ttu-id="deac3-154">Exemple de lecture de session multimédia</span><span class="sxs-lookup"><span data-stu-id="deac3-154">Media Session Playback Example</span></span>](media-session-playback-example.md)

## <a name="related-topics"></a><span data-ttu-id="deac3-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="deac3-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="deac3-156">Session multimédia</span><span class="sxs-lookup"><span data-stu-id="deac3-156">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="deac3-157">Lecture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="deac3-157">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



