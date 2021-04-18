---
description: Cet article explique comment écrire un présentateur personnalisé pour le convertisseur vidéo amélioré (EVR).
ms.assetid: 1135b309-b158-4b70-9f76-5c93d0ad3250
title: Comment écrire un présentateur EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94933d9eb53b0b03105edc7056ace4fe73238d16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564888"
---
# <a name="how-to-write-an-evr-presenter"></a><span data-ttu-id="01b54-103">Comment écrire un présentateur EVR</span><span class="sxs-lookup"><span data-stu-id="01b54-103">How to Write an EVR Presenter</span></span>

<span data-ttu-id="01b54-104">Cet article explique comment écrire un présentateur personnalisé pour le convertisseur vidéo amélioré (EVR).</span><span class="sxs-lookup"><span data-stu-id="01b54-104">This article describes how to write a custom presenter for the enhanced video renderer (EVR).</span></span> <span data-ttu-id="01b54-105">Un présentateur personnalisé peut être utilisé avec DirectShow et Media Foundation ; les interfaces et le modèle objet sont les mêmes pour les deux technologies, bien que la séquence exacte d’opérations puisse varier.</span><span class="sxs-lookup"><span data-stu-id="01b54-105">A custom presenter can be used with both DirectShow and Media Foundation; the interfaces and object model are the same for both technologies, although the exact sequence of operations might vary.</span></span>

<span data-ttu-id="01b54-106">L’exemple de code de cette rubrique est adapté de l' [exemple EVRPresenter](evrpresenter-sample.md), fourni dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="01b54-106">The example code in this topic is adapted from the [EVRPresenter Sample](evrpresenter-sample.md), which is provided in the Windows SDK.</span></span>

<span data-ttu-id="01b54-107">Cette rubrique contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="01b54-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="01b54-108">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="01b54-108">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="01b54-109">Modèle objet Presenter</span><span class="sxs-lookup"><span data-stu-id="01b54-109">Presenter Object Model</span></span>](#presenter-object-model)
    -   [<span data-ttu-id="01b54-110">Transmission de données à l’intérieur du EVR</span><span class="sxs-lookup"><span data-stu-id="01b54-110">Data Flow Inside the EVR</span></span>](#data-flow-inside-the-evr)
    -   [<span data-ttu-id="01b54-111">États du présentateur</span><span class="sxs-lookup"><span data-stu-id="01b54-111">Presenter States</span></span>](#presenter-states)
    -   [<span data-ttu-id="01b54-112">Interfaces presenter</span><span class="sxs-lookup"><span data-stu-id="01b54-112">Presenter Interfaces</span></span>](#presenter-interfaces)
    -   [<span data-ttu-id="01b54-113">Implémentation de IMFVideoDeviceID</span><span class="sxs-lookup"><span data-stu-id="01b54-113">Implementing IMFVideoDeviceID</span></span>](#implementing-imfvideodeviceid)
    -   [<span data-ttu-id="01b54-114">Implémentation de IMFTopologyServiceLookupClient</span><span class="sxs-lookup"><span data-stu-id="01b54-114">Implementing IMFTopologyServiceLookupClient</span></span>](#implementing-imftopologyservicelookupclient)
    -   [<span data-ttu-id="01b54-115">Implémentation de IMFVideoPresenter</span><span class="sxs-lookup"><span data-stu-id="01b54-115">Implementing IMFVideoPresenter</span></span>](#implementing-imfvideopresenter)
    -   [<span data-ttu-id="01b54-116">Implémentation de IMFClockStateSink</span><span class="sxs-lookup"><span data-stu-id="01b54-116">Implementing IMFClockStateSink</span></span>](#implementing-imfclockstatesink)
    -   [<span data-ttu-id="01b54-117">Implémentation de IMFRateSupport</span><span class="sxs-lookup"><span data-stu-id="01b54-117">Implementing IMFRateSupport</span></span>](#implementing-imfratesupport)
    -   [<span data-ttu-id="01b54-118">Envoi d’événements à EVR</span><span class="sxs-lookup"><span data-stu-id="01b54-118">Sending Events to the EVR</span></span>](#sending-events-to-the-evr)
-   [<span data-ttu-id="01b54-119">Négociation des formats</span><span class="sxs-lookup"><span data-stu-id="01b54-119">Negotiating Formats</span></span>](#negotiating-formats)
-   [<span data-ttu-id="01b54-120">Gestion de l’appareil Direct3D</span><span class="sxs-lookup"><span data-stu-id="01b54-120">Managing the Direct3D Device</span></span>](#managing-the-direct3d-device)
    -   [<span data-ttu-id="01b54-121">Allouer des surfaces Direct3D</span><span class="sxs-lookup"><span data-stu-id="01b54-121">Allocating Direct3D Surfaces</span></span>](#allocating-direct3d-surfaces)
    -   [<span data-ttu-id="01b54-122">Exemples de suivi</span><span class="sxs-lookup"><span data-stu-id="01b54-122">Tracking Samples</span></span>](#tracking-samples)
-   [<span data-ttu-id="01b54-123">Traitement de la sortie</span><span class="sxs-lookup"><span data-stu-id="01b54-123">Processing Output</span></span>](#processing-output)
    -   [<span data-ttu-id="01b54-124">Redessiner des frames</span><span class="sxs-lookup"><span data-stu-id="01b54-124">Repainting Frames</span></span>](#repainting-frames)
    -   [<span data-ttu-id="01b54-125">Exemples de planification</span><span class="sxs-lookup"><span data-stu-id="01b54-125">Scheduling Samples</span></span>](#scheduling-samples)
    -   [<span data-ttu-id="01b54-126">Présentation des exemples</span><span class="sxs-lookup"><span data-stu-id="01b54-126">Presenting Samples</span></span>](#presenting-samples)
    -   [<span data-ttu-id="01b54-127">Rectangles de source et de destination</span><span class="sxs-lookup"><span data-stu-id="01b54-127">Source and Destination Rectangles</span></span>](#source-and-destination-rectangles)
    -   [<span data-ttu-id="01b54-128">Fin de flux</span><span class="sxs-lookup"><span data-stu-id="01b54-128">End of Stream</span></span>](#end-of-stream)
-   [<span data-ttu-id="01b54-129">Pas à pas</span><span class="sxs-lookup"><span data-stu-id="01b54-129">Frame Stepping</span></span>](#frame-stepping)
    -   [<span data-ttu-id="01b54-130">Implémentation du pas à pas de frame</span><span class="sxs-lookup"><span data-stu-id="01b54-130">Implementing Frame Stepping</span></span>](#implementing-frame-stepping)
-   [<span data-ttu-id="01b54-131">Définition du présentateur sur le EVR</span><span class="sxs-lookup"><span data-stu-id="01b54-131">Setting the Presenter on the EVR</span></span>](#setting-the-presenter-on-the-evr)
    -   [<span data-ttu-id="01b54-132">Définition du présentateur dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="01b54-132">Setting the Presenter in DirectShow</span></span>](#setting-the-presenter-in-directshow)
    -   [<span data-ttu-id="01b54-133">Définition du présentateur dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="01b54-133">Setting the Presenter in Media Foundation</span></span>](#setting-the-presenter-in-media-foundation)
-   [<span data-ttu-id="01b54-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="01b54-134">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="01b54-135">Prérequis</span><span class="sxs-lookup"><span data-stu-id="01b54-135">Prerequisites</span></span>

<span data-ttu-id="01b54-136">Avant d’écrire un présentateur personnalisé, vous devez être familiarisé avec les technologies suivantes :</span><span class="sxs-lookup"><span data-stu-id="01b54-136">Before writing a custom presenter, you should be familiar with the following technologies:</span></span>

-   <span data-ttu-id="01b54-137">Convertisseur vidéo amélioré.</span><span class="sxs-lookup"><span data-stu-id="01b54-137">The enhanced video renderer.</span></span> <span data-ttu-id="01b54-138">Consultez [rendu vidéo amélioré](enhanced-video-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="01b54-138">See [Enhanced Video Renderer](enhanced-video-renderer.md).</span></span>
-   <span data-ttu-id="01b54-139">Graphiques Direct3D.</span><span class="sxs-lookup"><span data-stu-id="01b54-139">Direct3D graphics.</span></span> <span data-ttu-id="01b54-140">Vous n’avez pas besoin de comprendre les graphiques 3D pour écrire un présentateur, mais vous devez savoir comment créer un appareil Direct3D et gérer des surfaces Direct3D.</span><span class="sxs-lookup"><span data-stu-id="01b54-140">You don't need to understand 3-D graphics to write a presenter, but you must know how to create a Direct3D device and manage Direct3D surfaces.</span></span> <span data-ttu-id="01b54-141">Si vous n’êtes pas familiarisé avec Direct3D, lisez les sections « périphériques Direct3D » et « ressources Direct3D » dans la documentation du kit SDK DirectX Graphics.</span><span class="sxs-lookup"><span data-stu-id="01b54-141">If you aren't familiar with Direct3D, read the sections "Direct3D Devices" and "Direct3D Resources" in the DirectX Graphics SDK documentation.</span></span>
-   <span data-ttu-id="01b54-142">Les graphiques de filtre DirectShow ou le pipeline Media Foundation, selon la technologie que votre application utilisera pour afficher la vidéo.</span><span class="sxs-lookup"><span data-stu-id="01b54-142">DirectShow filter graphs or the Media Foundation pipeline, depending on which technology your application will use to render video.</span></span>
-   <span data-ttu-id="01b54-143">[Media Foundation transformations](media-foundation-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="01b54-143">[Media Foundation Transforms](media-foundation-transforms.md).</span></span> <span data-ttu-id="01b54-144">Le mélangeur EVR est une transformation Media Foundation, et le présenteur appelle des méthodes directement sur le mélangeur.</span><span class="sxs-lookup"><span data-stu-id="01b54-144">The EVR mixer is a Media Foundation transform, and the presenter calls methods directly on the mixer.</span></span>
-   <span data-ttu-id="01b54-145">Implémentation d’objets COM.</span><span class="sxs-lookup"><span data-stu-id="01b54-145">Implementing COM objects.</span></span> <span data-ttu-id="01b54-146">Le présentateur est un objet COM libre-thread dans le processus.</span><span class="sxs-lookup"><span data-stu-id="01b54-146">The presenter is an in-process, free-threaded COM object.</span></span>

## <a name="presenter-object-model"></a><span data-ttu-id="01b54-147">Modèle objet Presenter</span><span class="sxs-lookup"><span data-stu-id="01b54-147">Presenter Object Model</span></span>

<span data-ttu-id="01b54-148">Cette section contient une vue d’ensemble du modèle objet et des interfaces du présentateur.</span><span class="sxs-lookup"><span data-stu-id="01b54-148">This section contains an overview the presenter object model and interfaces.</span></span>

### <a name="data-flow-inside-the-evr"></a><span data-ttu-id="01b54-149">Transmission de données à l’intérieur du EVR</span><span class="sxs-lookup"><span data-stu-id="01b54-149">Data Flow Inside the EVR</span></span>

<span data-ttu-id="01b54-150">Le EVR utilise deux composants de plug-in pour afficher la vidéo : le *mélangeur* et le *présentateur*.</span><span class="sxs-lookup"><span data-stu-id="01b54-150">The EVR uses two plug-in components to render video: the *mixer* and the *presenter*.</span></span> <span data-ttu-id="01b54-151">Le mélangeur fusionne les flux vidéo et désentrelace la vidéo si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="01b54-151">The mixer blends the video streams and deinterlaces the video if needed.</span></span> <span data-ttu-id="01b54-152">Le présentateur dessine (ou *présente*) la vidéo sur l’écran et planifie le dessin de chaque image.</span><span class="sxs-lookup"><span data-stu-id="01b54-152">The presenter draws (or *presents*) the video onto the display and schedules when each frame is drawn.</span></span> <span data-ttu-id="01b54-153">Les applications peuvent remplacer l’un de ces objets par une implémentation personnalisée.</span><span class="sxs-lookup"><span data-stu-id="01b54-153">Applications can replace either of these objects with a custom implementation.</span></span>

<span data-ttu-id="01b54-154">Le EVR a un ou plusieurs flux d’entrée, et le mélangeur a un nombre correspondant de flux d’entrée.</span><span class="sxs-lookup"><span data-stu-id="01b54-154">The EVR has one or more input streams, and the mixer has a corresponding number of input streams.</span></span> <span data-ttu-id="01b54-155">Le flux 0 est toujours le *flux de référence*.</span><span class="sxs-lookup"><span data-stu-id="01b54-155">Stream 0 is always the *reference stream*.</span></span> <span data-ttu-id="01b54-156">Les autres flux sont des sous- *flux*, que le mixer alpha sur le flux de référence.</span><span class="sxs-lookup"><span data-stu-id="01b54-156">The other streams are *substreams*, which the mixer alpha-blends onto the reference stream.</span></span> <span data-ttu-id="01b54-157">Le flux de référence détermine le taux d’images maître pour la vidéo composite.</span><span class="sxs-lookup"><span data-stu-id="01b54-157">The reference stream determines the master frame-rate for the composited video.</span></span> <span data-ttu-id="01b54-158">Pour chaque frame de référence, la fenêtre de mixage prend le frame le plus récent de chaque sous-flux, les mélange alpha sur le frame de référence et génère un seul Frame composite.</span><span class="sxs-lookup"><span data-stu-id="01b54-158">For each reference frame, the mixer takes the most recent frame from each substream, alpha-blends them onto the reference frame, and outputs a single composited frame.</span></span> <span data-ttu-id="01b54-159">Le mélangeur effectue également une conversion de désentrelacement et de couleur de YUV en RVB si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="01b54-159">The mixer also performs deinterlacing and color conversion from YUV to RGB if needed.</span></span> <span data-ttu-id="01b54-160">Le EVR insère toujours le mixer dans le pipeline vidéo, quel que soit le nombre de flux d’entrée ou le format vidéo.</span><span class="sxs-lookup"><span data-stu-id="01b54-160">The EVR always inserts the mixer into the video pipeline, regardless of the number of input streams or the video format.</span></span> <span data-ttu-id="01b54-161">L’illustration suivante montre ce processus.</span><span class="sxs-lookup"><span data-stu-id="01b54-161">The following image illustrates this process.</span></span>

![Diagramme montrant le flux de référence et le sous-flux pointant vers le mélangeur, qui pointe vers le présentateur, qui pointe vers l’affichage](images/459338c4-cff8-4d20-bffd-ff1cbbe6f332.gif)

<span data-ttu-id="01b54-163">Le présentateur effectue les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="01b54-163">The presenter performs the following tasks:</span></span>

-   <span data-ttu-id="01b54-164">Définit le format de sortie sur le mélangeur.</span><span class="sxs-lookup"><span data-stu-id="01b54-164">Sets the output format on the mixer.</span></span> <span data-ttu-id="01b54-165">Avant le début de la diffusion en continu, le présentateur définit un type de média sur le flux de sortie de la console.</span><span class="sxs-lookup"><span data-stu-id="01b54-165">Before streaming begins, the presenter sets a media type on the mixer's output stream.</span></span> <span data-ttu-id="01b54-166">Ce type de média définit le format de l’image composite.</span><span class="sxs-lookup"><span data-stu-id="01b54-166">This media type defines the format of the composited image.</span></span>
-   <span data-ttu-id="01b54-167">Crée le périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="01b54-167">Creates the Direct3D device.</span></span>
-   <span data-ttu-id="01b54-168">Alloue des surfaces Direct3D.</span><span class="sxs-lookup"><span data-stu-id="01b54-168">Allocates Direct3D surfaces.</span></span> <span data-ttu-id="01b54-169">Le mélangeur BLITS les images composites sur ces surfaces.</span><span class="sxs-lookup"><span data-stu-id="01b54-169">The mixer blits the composited frames onto these surfaces.</span></span>
-   <span data-ttu-id="01b54-170">Obtient la sortie du mélangeur.</span><span class="sxs-lookup"><span data-stu-id="01b54-170">Gets the output from the mixer.</span></span>
-   <span data-ttu-id="01b54-171">Planifie la présentation des frames.</span><span class="sxs-lookup"><span data-stu-id="01b54-171">Schedules when the frames are presented.</span></span> <span data-ttu-id="01b54-172">Le EVR fournit l’horloge de présentation et le présentateur planifie les frames en fonction de cette horloge.</span><span class="sxs-lookup"><span data-stu-id="01b54-172">The EVR provides the presentation clock, and the presenter schedules frames according to this clock.</span></span>
-   <span data-ttu-id="01b54-173">Présente chaque frame à l’aide de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="01b54-173">Presents each frame using Direct3D.</span></span>
-   <span data-ttu-id="01b54-174">Effectue un pas à pas et un nettoyage de l’image.</span><span class="sxs-lookup"><span data-stu-id="01b54-174">Performs frame stepping and scrubbing.</span></span>

### <a name="presenter-states"></a><span data-ttu-id="01b54-175">États du présentateur</span><span class="sxs-lookup"><span data-stu-id="01b54-175">Presenter States</span></span>

<span data-ttu-id="01b54-176">À tout moment, le présentateur est dans l’un des États suivants :</span><span class="sxs-lookup"><span data-stu-id="01b54-176">At any time, the presenter is in one of following states:</span></span>

-   <span data-ttu-id="01b54-177">*Démarré*.</span><span class="sxs-lookup"><span data-stu-id="01b54-177">*Started*.</span></span> <span data-ttu-id="01b54-178">L’horloge de présentation de EVR est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="01b54-178">The EVR's presentation clock is running.</span></span> <span data-ttu-id="01b54-179">Le présentateur planifie des images vidéo pour la présentation à mesure qu’elles arrivent.</span><span class="sxs-lookup"><span data-stu-id="01b54-179">The presenter schedules video frames for presentation as they arrive.</span></span>
-   <span data-ttu-id="01b54-180">*Suspendu*.</span><span class="sxs-lookup"><span data-stu-id="01b54-180">*Paused*.</span></span> <span data-ttu-id="01b54-181">L’horloge de la présentation est suspendue.</span><span class="sxs-lookup"><span data-stu-id="01b54-181">The presentation clock is suspended.</span></span> <span data-ttu-id="01b54-182">Le présentateur ne présente aucun nouvel exemple, mais conserve sa file d’attente d’exemples planifiés.</span><span class="sxs-lookup"><span data-stu-id="01b54-182">The presenter does not present any new samples but maintains its queue of scheduled samples.</span></span> <span data-ttu-id="01b54-183">Si de nouveaux exemples sont reçus, le présentateur les ajoute à la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="01b54-183">If new samples are received, the presenter adds them to the queue.</span></span>
-   <span data-ttu-id="01b54-184">*Arrêté*.</span><span class="sxs-lookup"><span data-stu-id="01b54-184">*Stopped*.</span></span> <span data-ttu-id="01b54-185">L’horloge de la présentation est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="01b54-185">The presentation clock is stopped.</span></span> <span data-ttu-id="01b54-186">Le présentateur ignore tous les exemples qui ont été planifiés.</span><span class="sxs-lookup"><span data-stu-id="01b54-186">The presenter discards any samples that were scheduled.</span></span>
-   <span data-ttu-id="01b54-187">*Arrêtez*.</span><span class="sxs-lookup"><span data-stu-id="01b54-187">*Shut down*.</span></span> <span data-ttu-id="01b54-188">Le présentateur libère toutes les ressources liées à la diffusion en continu, telles que les surfaces Direct3D.</span><span class="sxs-lookup"><span data-stu-id="01b54-188">The presenter releases any resources related to streaming, such as Direct3D surfaces.</span></span> <span data-ttu-id="01b54-189">Il s’agit de l’état initial du présenteur et de l’état final avant la destruction du présentateur.</span><span class="sxs-lookup"><span data-stu-id="01b54-189">This is the presenter's initial state, and the final state before the presenter is destroyed.</span></span>

<span data-ttu-id="01b54-190">Dans l’exemple de code présenté dans cette rubrique, l’État présentateur est représenté par une énumération :</span><span class="sxs-lookup"><span data-stu-id="01b54-190">In the example code in this topic, the presenter state is represented by an enumeration:</span></span>


```C++
enum RENDER_STATE
{
    RENDER_STATE_STARTED = 1,
    RENDER_STATE_STOPPED,
    RENDER_STATE_PAUSED,
    RENDER_STATE_SHUTDOWN,  // Initial state.
};
```



<span data-ttu-id="01b54-191">Certaines opérations ne sont pas valides lorsque le présentateur est à l’état d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="01b54-191">Some operations are not valid while the presenter is in the shutdown state.</span></span> <span data-ttu-id="01b54-192">L’exemple de code vérifie cet État en appelant une méthode d’assistance :</span><span class="sxs-lookup"><span data-stu-id="01b54-192">The example code checks for this state by calling a helper method:</span></span>


```C++
    HRESULT CheckShutdown() const
    {
        if (m_RenderState == RENDER_STATE_SHUTDOWN)
        {
            return MF_E_SHUTDOWN;
        }
        else
        {
            return S_OK;
        }
    }
```



### <a name="presenter-interfaces"></a><span data-ttu-id="01b54-193">Interfaces presenter</span><span class="sxs-lookup"><span data-stu-id="01b54-193">Presenter Interfaces</span></span>

<span data-ttu-id="01b54-194">Un présentateur est requis pour implémenter les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="01b54-194">A presenter is required to implement the following interfaces:</span></span>



| <span data-ttu-id="01b54-195">Interface</span><span class="sxs-lookup"><span data-stu-id="01b54-195">Interface</span></span>                                                                | <span data-ttu-id="01b54-196">Description</span><span class="sxs-lookup"><span data-stu-id="01b54-196">Description</span></span>                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01b54-197">**IMFClockStateSink**</span><span class="sxs-lookup"><span data-stu-id="01b54-197">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)                           | <span data-ttu-id="01b54-198">Notifie le présenteur lorsque l’horloge du EVR change d’État.</span><span class="sxs-lookup"><span data-stu-id="01b54-198">Notifies the presenter when the EVR's clock changes state.</span></span> <span data-ttu-id="01b54-199">Consultez [implémentation de IMFClockStateSink](#implementing-imfclockstatesink).</span><span class="sxs-lookup"><span data-stu-id="01b54-199">See [Implementing IMFClockStateSink](#implementing-imfclockstatesink).</span></span>                                   |
| [<span data-ttu-id="01b54-200">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="01b54-200">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                   | <span data-ttu-id="01b54-201">Fournit un moyen pour l’application et d’autres composants dans le pipeline d’obtenir des interfaces du présentateur.</span><span class="sxs-lookup"><span data-stu-id="01b54-201">Provides a way for the application and other components in the pipeline to get interfaces from the presenter.</span></span>                                                       |
| [<span data-ttu-id="01b54-202">**IMFTopologyServiceLookupClient**</span><span class="sxs-lookup"><span data-stu-id="01b54-202">**IMFTopologyServiceLookupClient**</span></span>](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | <span data-ttu-id="01b54-203">Permet au présenteur d’accéder aux interfaces à partir du EVR ou du mélangeur.</span><span class="sxs-lookup"><span data-stu-id="01b54-203">Enables the presenter to get interfaces from the EVR or the mixer.</span></span> <span data-ttu-id="01b54-204">Consultez [implémentation de IMFTopologyServiceLookupClient](#implementing-imftopologyservicelookupclient).</span><span class="sxs-lookup"><span data-stu-id="01b54-204">See [Implementing IMFTopologyServiceLookupClient](#implementing-imftopologyservicelookupclient).</span></span> |
| [<span data-ttu-id="01b54-205">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="01b54-205">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | <span data-ttu-id="01b54-206">Garantit que le présentateur et le mélangeur utilisent des technologies compatibles.</span><span class="sxs-lookup"><span data-stu-id="01b54-206">Ensures that the presenter and the mixer use compatible technologies.</span></span> <span data-ttu-id="01b54-207">Consultez [implémentation de IMFVideoDeviceID](#implementing-imfvideodeviceid).</span><span class="sxs-lookup"><span data-stu-id="01b54-207">See [Implementing IMFVideoDeviceID](#implementing-imfvideodeviceid).</span></span>                          |
| [<span data-ttu-id="01b54-208">**IMFVideoPresenter**</span><span class="sxs-lookup"><span data-stu-id="01b54-208">**IMFVideoPresenter**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopresenter)                           | <span data-ttu-id="01b54-209">Traite les messages à partir du EVR.</span><span class="sxs-lookup"><span data-stu-id="01b54-209">Processes messages from the EVR.</span></span> <span data-ttu-id="01b54-210">Consultez [implémentation de IMFVideoPresenter](#implementing-imfvideopresenter).</span><span class="sxs-lookup"><span data-stu-id="01b54-210">See [Implementing IMFVideoPresenter](#implementing-imfvideopresenter).</span></span>                                                             |



 

<span data-ttu-id="01b54-211">Les interfaces suivantes sont facultatives :</span><span class="sxs-lookup"><span data-stu-id="01b54-211">The following interfaces are optional:</span></span>



| <span data-ttu-id="01b54-212">Interface</span><span class="sxs-lookup"><span data-stu-id="01b54-212">Interface</span></span>                                                | <span data-ttu-id="01b54-213">Description</span><span class="sxs-lookup"><span data-stu-id="01b54-213">Description</span></span>                                                                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01b54-214">**IEVRTrustedVideoPlugin**</span><span class="sxs-lookup"><span data-stu-id="01b54-214">**IEVRTrustedVideoPlugin**</span></span>](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | <span data-ttu-id="01b54-215">Permet au présentateur de travailler avec des médias protégés.</span><span class="sxs-lookup"><span data-stu-id="01b54-215">Enables the presenter to work with protected media.</span></span> <span data-ttu-id="01b54-216">Implémentez cette interface si votre présentateur est un composant approuvé conçu pour fonctionner dans le chemin d’accès au média protégé (PMP).</span><span class="sxs-lookup"><span data-stu-id="01b54-216">Implement this interface if your presenter is a trusted component designed to work in the protected media path (PMP).</span></span> |
| [<span data-ttu-id="01b54-217">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="01b54-217">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | <span data-ttu-id="01b54-218">Indique la plage de vitesses de lecture que le présenteur prend en charge.</span><span class="sxs-lookup"><span data-stu-id="01b54-218">Reports the range of playback rates that the presenter supports.</span></span> <span data-ttu-id="01b54-219">Consultez [implémentation de IMFRateSupport](#implementing-imfratesupport).</span><span class="sxs-lookup"><span data-stu-id="01b54-219">See [Implementing IMFRateSupport](#implementing-imfratesupport).</span></span>                                         |
| [<span data-ttu-id="01b54-220">**IMFVideoPositionMapper**</span><span class="sxs-lookup"><span data-stu-id="01b54-220">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | <span data-ttu-id="01b54-221">Mappe les coordonnées sur l’image vidéo de sortie à des coordonnées sur l’image vidéo d’entrée.</span><span class="sxs-lookup"><span data-stu-id="01b54-221">Maps coordinates on the output video frame to coordinates on the input video frame.</span></span>                                                                                       |
| [<span data-ttu-id="01b54-222">**IQualProp**</span><span class="sxs-lookup"><span data-stu-id="01b54-222">**IQualProp**</span></span>](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop)                         | <span data-ttu-id="01b54-223">Signale des informations sur les performances.</span><span class="sxs-lookup"><span data-stu-id="01b54-223">Reports performance information.</span></span> <span data-ttu-id="01b54-224">EVR utilise ces informations pour la gestion du contrôle qualité.</span><span class="sxs-lookup"><span data-stu-id="01b54-224">The EVR uses this information for quality-control management.</span></span> <span data-ttu-id="01b54-225">Cette interface est documentée dans le kit de développement logiciel (SDK) DirectShow.</span><span class="sxs-lookup"><span data-stu-id="01b54-225">This interface is documented in the DirectShow SDK.</span></span>                        |



 

<span data-ttu-id="01b54-226">Vous pouvez également fournir des interfaces pour que l’application communique avec le présentateur.</span><span class="sxs-lookup"><span data-stu-id="01b54-226">You can also provide interfaces for the application to communicate with the presenter.</span></span> <span data-ttu-id="01b54-227">Le présentateur standard implémente l’interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) à cet effet.</span><span class="sxs-lookup"><span data-stu-id="01b54-227">The standard presenter implements the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface for this purpose.</span></span> <span data-ttu-id="01b54-228">Vous pouvez implémenter cette interface ou définir les vôtres.</span><span class="sxs-lookup"><span data-stu-id="01b54-228">You can implement this interface or define your own.</span></span> <span data-ttu-id="01b54-229">L’application obtient les interfaces du présenteur en appelant [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) sur EVR.</span><span class="sxs-lookup"><span data-stu-id="01b54-229">The application obtains interfaces from the presenter by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the EVR.</span></span> <span data-ttu-id="01b54-230">Lorsque le GUID du service est **MR_VIDEO_RENDER_SERVICE**, EVR transmet la demande **GetService** au présenteur.</span><span class="sxs-lookup"><span data-stu-id="01b54-230">When the service GUID is **MR_VIDEO_RENDER_SERVICE**, the EVR passes the **GetService** request to the presenter.</span></span>

### <a name="implementing-imfvideodeviceid"></a><span data-ttu-id="01b54-231">Implémentation de IMFVideoDeviceID</span><span class="sxs-lookup"><span data-stu-id="01b54-231">Implementing IMFVideoDeviceID</span></span>

<span data-ttu-id="01b54-232">L’interface [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) contient une méthode, [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid), qui retourne un GUID de périphérique.</span><span class="sxs-lookup"><span data-stu-id="01b54-232">The [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) interface contains one method, [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid), which returns a device GUID.</span></span> <span data-ttu-id="01b54-233">Le GUID de l’appareil garantit que le présentateur et le mélangeur utilisent des technologies compatibles.</span><span class="sxs-lookup"><span data-stu-id="01b54-233">The device GUID ensures that the presenter and the mixer use compatible technologies.</span></span> <span data-ttu-id="01b54-234">Si les GUID d’appareil ne correspondent pas, l’initialisation du EVR échoue.</span><span class="sxs-lookup"><span data-stu-id="01b54-234">If the device GUIDs do not match, the EVR fails to initialize.</span></span>

<span data-ttu-id="01b54-235">Le mélangeur et le présentateur standard utilisent Direct3D 9, avec le GUID de l’appareil égal à **IID_IDirect3DDevice9**.</span><span class="sxs-lookup"><span data-stu-id="01b54-235">The standard mixer and presenter both use Direct3D 9, with the device GUID equal to **IID_IDirect3DDevice9**.</span></span> <span data-ttu-id="01b54-236">Si vous envisagez d’utiliser votre présentateur personnalisé avec le mélangeur standard, le GUID de l’appareil du présentateur doit être **IID_IDirect3DDevice9**.</span><span class="sxs-lookup"><span data-stu-id="01b54-236">If you intend to use your custom presenter with the standard mixer, the presenter's device GUID must be **IID_IDirect3DDevice9**.</span></span> <span data-ttu-id="01b54-237">Si vous remplacez les deux composants, vous pouvez définir un nouveau GUID d’appareil.</span><span class="sxs-lookup"><span data-stu-id="01b54-237">If you replace both components, you could define a new device GUID.</span></span> <span data-ttu-id="01b54-238">Pour le reste de cet article, il est supposé que le présentateur utilise Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="01b54-238">For the remainder of this article, it is assumed that the presenter uses Direct3D 9.</span></span> <span data-ttu-id="01b54-239">Voici l’implémentation standard de [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid):</span><span class="sxs-lookup"><span data-stu-id="01b54-239">Here is the standard implementation of [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid):</span></span>


```C++
HRESULT EVRCustomPresenter::GetDeviceID(IID* pDeviceID)
{
    if (pDeviceID == NULL)
    {
        return E_POINTER;
    }

    *pDeviceID = __uuidof(IDirect3DDevice9);
    return S_OK;
}
```



<span data-ttu-id="01b54-240">La méthode doit s’effectuer correctement même lorsque le présentateur est arrêté.</span><span class="sxs-lookup"><span data-stu-id="01b54-240">The method should succeed even when the presenter is shut down.</span></span>

### <a name="implementing-imftopologyservicelookupclient"></a><span data-ttu-id="01b54-241">Implémentation de IMFTopologyServiceLookupClient</span><span class="sxs-lookup"><span data-stu-id="01b54-241">Implementing IMFTopologyServiceLookupClient</span></span>

<span data-ttu-id="01b54-242">L’interface [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) permet au présenteur d’extraire des pointeurs d’interface à partir du EVR et du mélangeur comme suit :</span><span class="sxs-lookup"><span data-stu-id="01b54-242">The [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) interface enables the presenter to get interface pointers from the EVR and from the mixer as follows:</span></span>

1.  <span data-ttu-id="01b54-243">Quand le EVR Initialise le présentateur, il appelle la méthode [**IMFTopologyServiceLookupClient :: InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) du présentateur.</span><span class="sxs-lookup"><span data-stu-id="01b54-243">When the EVR initializes the presenter, it calls the presenter's [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method.</span></span> <span data-ttu-id="01b54-244">L’argument est un pointeur vers l’interface [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) de EVR.</span><span class="sxs-lookup"><span data-stu-id="01b54-244">The argument is a pointer to the EVR's [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) interface.</span></span>
2.  <span data-ttu-id="01b54-245">Le présentateur appelle [**IMFTopologyServiceLookup :: LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) pour récupérer les pointeurs d’interface à partir de EVR ou du mixer.</span><span class="sxs-lookup"><span data-stu-id="01b54-245">The presenter calls [**IMFTopologyServiceLookup::LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) to get interface pointers from either the EVR or the mixer.</span></span>

<span data-ttu-id="01b54-246">La méthode [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) est semblable à la méthode [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) .</span><span class="sxs-lookup"><span data-stu-id="01b54-246">The [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) method is similar to the [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) method.</span></span> <span data-ttu-id="01b54-247">Les deux méthodes prennent un GUID de service et un identificateur d’interface (IID) comme entrée, mais **LookupService** retourne un tableau de pointeurs d’interface, tandis que **GetService** retourne un pointeur unique.</span><span class="sxs-lookup"><span data-stu-id="01b54-247">Both methods take a service GUID and an interface identifier (IID) as input, but **LookupService** returns an array of interface pointers, while **GetService** returns a single pointer.</span></span> <span data-ttu-id="01b54-248">Dans la pratique, toutefois, vous pouvez toujours définir la taille du tableau sur 1.</span><span class="sxs-lookup"><span data-stu-id="01b54-248">In practice, however, you can always set the array size to 1.</span></span> <span data-ttu-id="01b54-249">L’objet interrogé dépend du GUID de service :</span><span class="sxs-lookup"><span data-stu-id="01b54-249">The object queried depends on the service GUID:</span></span>

-   <span data-ttu-id="01b54-250">Si le GUID du service est **MR_VIDEO_RENDER_SERVICE**, EVR est interrogé.</span><span class="sxs-lookup"><span data-stu-id="01b54-250">If the service GUID is **MR_VIDEO_RENDER_SERVICE**, the EVR is queried.</span></span>
-   <span data-ttu-id="01b54-251">Si le GUID du service est **MR_VIDEO_MIXER_SERVICE**, le mélangeur est interrogé.</span><span class="sxs-lookup"><span data-stu-id="01b54-251">If the service GUID is **MR_VIDEO_MIXER_SERVICE**, the mixer is queried.</span></span>

<span data-ttu-id="01b54-252">Dans votre implémentation de [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers), récupérez les interfaces suivantes à partir de EVR :</span><span class="sxs-lookup"><span data-stu-id="01b54-252">In your implementation of [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers), get the following interfaces from the EVR:</span></span>



| <span data-ttu-id="01b54-253">Interface EVR</span><span class="sxs-lookup"><span data-stu-id="01b54-253">EVR Interface</span></span>                                | <span data-ttu-id="01b54-254">Description</span><span class="sxs-lookup"><span data-stu-id="01b54-254">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01b54-255">**IMediaEventSink**</span><span class="sxs-lookup"><span data-stu-id="01b54-255">**IMediaEventSink**</span></span>](/windows/win32/api/strmif/nn-strmif-imediaeventsink) | <span data-ttu-id="01b54-256">Offre au présenteur un moyen d’envoyer des messages à EVR.</span><span class="sxs-lookup"><span data-stu-id="01b54-256">Provides a way for the presenter to send messages to the EVR.</span></span> <span data-ttu-id="01b54-257">Cette interface étant définie dans le kit de développement logiciel (SDK) DirectShow, les messages respectent le modèle pour les événements DirectShow, et non Media Foundation les événements.</span><span class="sxs-lookup"><span data-stu-id="01b54-257">This interface is defined in the DirectShow SDK, so the messages follow the pattern for DirectShow events, not Media Foundation events.</span></span><br/>                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="01b54-258">**IMFClock**</span><span class="sxs-lookup"><span data-stu-id="01b54-258">**IMFClock**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclock)                 | <span data-ttu-id="01b54-259">Représente l’horloge du EVR.</span><span class="sxs-lookup"><span data-stu-id="01b54-259">Represents the EVR's clock.</span></span> <span data-ttu-id="01b54-260">Le présentateur utilise cette interface pour planifier des exemples à des fins de présentation.</span><span class="sxs-lookup"><span data-stu-id="01b54-260">The presenter uses this interface to schedule samples for presentation.</span></span> <span data-ttu-id="01b54-261">Le EVR peut s’exécuter sans horloge. cette interface peut donc ne pas être disponible.</span><span class="sxs-lookup"><span data-stu-id="01b54-261">The EVR can run without a clock, so this interface might not be available.</span></span> <span data-ttu-id="01b54-262">Si ce n’est pas le cas, ignorez le code d’erreur de [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice).</span><span class="sxs-lookup"><span data-stu-id="01b54-262">If not, ignore the error code from [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice).</span></span><br/> <span data-ttu-id="01b54-263">L’horloge implémente également l’interface [**IMFTimer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer) .</span><span class="sxs-lookup"><span data-stu-id="01b54-263">The clock also implements the [**IMFTimer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer) interface.</span></span> <span data-ttu-id="01b54-264">Dans le pipeline Media Foundation, l’horloge implémente l’interface [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) .</span><span class="sxs-lookup"><span data-stu-id="01b54-264">In the Media Foundation pipeline, the clock implements the [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) interface.</span></span> <span data-ttu-id="01b54-265">Elle n’implémente pas cette interface dans DirectShow.</span><span class="sxs-lookup"><span data-stu-id="01b54-265">It does not implement this interface in DirectShow.</span></span><br/> |



 

<span data-ttu-id="01b54-266">Récupérez les interfaces suivantes à partir du mélangeur :</span><span class="sxs-lookup"><span data-stu-id="01b54-266">Get the following interfaces from the mixer:</span></span>



| <span data-ttu-id="01b54-267">Interface de mixage</span><span class="sxs-lookup"><span data-stu-id="01b54-267">Mixer Interface</span></span>                              | <span data-ttu-id="01b54-268">Description</span><span class="sxs-lookup"><span data-stu-id="01b54-268">Description</span></span>                                                |
|----------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="01b54-269">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="01b54-269">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)         | <span data-ttu-id="01b54-270">Permet au présenteur de communiquer avec le mélangeur.</span><span class="sxs-lookup"><span data-stu-id="01b54-270">Enables the presenter to communicate with the mixer.</span></span>       |
| [<span data-ttu-id="01b54-271">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="01b54-271">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) | <span data-ttu-id="01b54-272">Permet au présenteur de valider le GUID de l’appareil du mélangeur.</span><span class="sxs-lookup"><span data-stu-id="01b54-272">Enables the presenter to validate the mixer's device GUID.</span></span> |



 

<span data-ttu-id="01b54-273">Le code suivant implémente la méthode [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) :</span><span class="sxs-lookup"><span data-stu-id="01b54-273">The following code implements the [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method :</span></span>


```C++
HRESULT EVRCustomPresenter::InitServicePointers(
    IMFTopologyServiceLookup *pLookup
    )
{
    if (pLookup == NULL)
    {
        return E_POINTER;
    }

    HRESULT             hr = S_OK;
    DWORD               dwObjectCount = 0;

    EnterCriticalSection(&m_ObjectLock);

    // Do not allow initializing when playing or paused.
    if (IsActive())
    {
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    // Ask for the clock. Optional, because the EVR might not have a clock.
    dwObjectCount = 1;

    (void)pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL,   // Not used.
        0,                          // Reserved.
        MR_VIDEO_RENDER_SERVICE,    // Service to look up.
        IID_PPV_ARGS(&m_pClock),    // Interface to retrieve.
        &dwObjectCount              // Number of elements retrieved.
        );

    // Ask for the mixer. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_MIXER_SERVICE, IID_PPV_ARGS(&m_pMixer), &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Make sure that we can work with this mixer.
    hr = ConfigureMixer(m_pMixer);
    if (FAILED(hr))
    {
        goto done;
    }

    // Ask for the EVR's event-sink interface. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_RENDER_SERVICE, IID_PPV_ARGS(&m_pMediaEventSink),
        &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Successfully initialized. Set the state to "stopped."
    m_RenderState = RENDER_STATE_STOPPED;

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



<span data-ttu-id="01b54-274">Lorsque les pointeurs d’interface obtenus à partir de [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) ne sont plus valides, EVR appelle [**IMFTopologyServiceLookupClient :: ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers).</span><span class="sxs-lookup"><span data-stu-id="01b54-274">When the interface pointers obtained from [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) are no longer valid, the EVR calls [**IMFTopologyServiceLookupClient::ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers).</span></span> <span data-ttu-id="01b54-275">Dans cette méthode, libérez tous les pointeurs d’interface et définissez l’état du présentateur sur arrêt :</span><span class="sxs-lookup"><span data-stu-id="01b54-275">Inside this method, release all interface pointers and set the presenter state to shut down:</span></span>


```C++
HRESULT EVRCustomPresenter::ReleaseServicePointers()
{
    // Enter the shut-down state.
    EnterCriticalSection(&m_ObjectLock);

    m_RenderState = RENDER_STATE_SHUTDOWN;

    LeaveCriticalSection(&m_ObjectLock);

    // Flush any samples that were scheduled.
    Flush();

    // Clear the media type and release related resources.
    SetMediaType(NULL);

    // Release all services that were acquired from InitServicePointers.
    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    return S_OK;
}
```



<span data-ttu-id="01b54-276">EVR appelle [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) pour diverses raisons, notamment :</span><span class="sxs-lookup"><span data-stu-id="01b54-276">The EVR calls [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) for various reasons, including:</span></span>

-   <span data-ttu-id="01b54-277">La déconnexion ou la reconnexion des broches (DirectShow), ou l’ajout ou la suppression de récepteurs de flux (Media Foundation).</span><span class="sxs-lookup"><span data-stu-id="01b54-277">Disconnecting or reconnecting pins (DirectShow), or adding or removing stream sinks (Media Foundation).</span></span>
-   <span data-ttu-id="01b54-278">Modification du format.</span><span class="sxs-lookup"><span data-stu-id="01b54-278">Changing format.</span></span>
-   <span data-ttu-id="01b54-279">Définition d’une nouvelle horloge.</span><span class="sxs-lookup"><span data-stu-id="01b54-279">Setting a new clock.</span></span>
-   <span data-ttu-id="01b54-280">Arrêt final du EVR.</span><span class="sxs-lookup"><span data-stu-id="01b54-280">Final shutdown of the EVR.</span></span>

<span data-ttu-id="01b54-281">Pendant la durée de vie du présentateur, le EVR peut appeler [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) et [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="01b54-281">During the lifetime of the presenter, the EVR might call [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) and [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) several times.</span></span>

### <a name="implementing-imfvideopresenter"></a><span data-ttu-id="01b54-282">Implémentation de IMFVideoPresenter</span><span class="sxs-lookup"><span data-stu-id="01b54-282">Implementing IMFVideoPresenter</span></span>

<span data-ttu-id="01b54-283">L’interface [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) hérite de [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) et ajoute deux méthodes :</span><span class="sxs-lookup"><span data-stu-id="01b54-283">The [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) interface inherits [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) and adds two methods:</span></span>



| <span data-ttu-id="01b54-284">Méthode</span><span class="sxs-lookup"><span data-stu-id="01b54-284">Method</span></span>                                                               | <span data-ttu-id="01b54-285">Description</span><span class="sxs-lookup"><span data-stu-id="01b54-285">Description</span></span>                                            |
|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="01b54-286">**GetCurrentMediaType**</span><span class="sxs-lookup"><span data-stu-id="01b54-286">**GetCurrentMediaType**</span></span>](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) | <span data-ttu-id="01b54-287">Retourne le type de média des images vidéo composite.</span><span class="sxs-lookup"><span data-stu-id="01b54-287">Returns the media type of the composited video frames.</span></span> |
| [<span data-ttu-id="01b54-288">**ProcessMessage**</span><span class="sxs-lookup"><span data-stu-id="01b54-288">**ProcessMessage**</span></span>](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage)           | <span data-ttu-id="01b54-289">Signale au présenteur d’effectuer diverses actions.</span><span class="sxs-lookup"><span data-stu-id="01b54-289">Signals the presenter to perform various actions.</span></span>      |



 

<span data-ttu-id="01b54-290">La méthode [**GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) retourne le type de média du présentateur.</span><span class="sxs-lookup"><span data-stu-id="01b54-290">The [**GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) method returns the presenter's media type.</span></span> <span data-ttu-id="01b54-291">(Pour plus d’informations sur la définition du type de support, consultez [négociation de formats](#negotiating-formats).) Le type de média est retourné en tant que pointeur d’interface [**IMFVideoMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype) .</span><span class="sxs-lookup"><span data-stu-id="01b54-291">(For details about setting the media type, see [Negotiating Formats](#negotiating-formats).) The media type is returned as an [**IMFVideoMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype) interface pointer.</span></span> <span data-ttu-id="01b54-292">L’exemple suivant suppose que le présenteur stocke le type de média comme un pointeur [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="01b54-292">The following example assumes that the presenter stores the media type as an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) pointer.</span></span> <span data-ttu-id="01b54-293">Pour accéder à l’interface **IMFVideoMediaType** à partir du type de média, appelez **QueryInterface**:</span><span class="sxs-lookup"><span data-stu-id="01b54-293">To get the **IMFVideoMediaType** interface from the media type, call **QueryInterface**:</span></span>


```C++
HRESULT EVRCustomPresenter::GetCurrentMediaType(
    IMFVideoMediaType** ppMediaType
    )
{
    HRESULT hr = S_OK;

    if (ppMediaType == NULL)
    {
        return E_POINTER;
    }

    *ppMediaType = NULL;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    if (m_pMediaType == NULL)
    {
        hr = MF_E_NOT_INITIALIZED;
        goto done;
    }

    hr = m_pMediaType->QueryInterface(IID_PPV_ARGS(ppMediaType));

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



<span data-ttu-id="01b54-294">La méthode [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) est le mécanisme principal de EVR pour communiquer avec le présentateur.</span><span class="sxs-lookup"><span data-stu-id="01b54-294">The [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) method is the primary mechanism for the EVR to communicate with the presenter.</span></span> <span data-ttu-id="01b54-295">Les messages suivants sont définis.</span><span class="sxs-lookup"><span data-stu-id="01b54-295">The following messages are defined.</span></span> <span data-ttu-id="01b54-296">Les détails de l’implémentation de chaque message sont donnés dans le reste de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="01b54-296">The details of implementing each message are given in the remainder of this topic.</span></span>



| <span data-ttu-id="01b54-297">Message</span><span class="sxs-lookup"><span data-stu-id="01b54-297">Message</span></span>                                | <span data-ttu-id="01b54-298">Description</span><span class="sxs-lookup"><span data-stu-id="01b54-298">Description</span></span>                                                                                                                                                                                                                                        |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01b54-299">**MFVP_MESSAGE_INVALIDATEMEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="01b54-299">**MFVP_MESSAGE_INVALIDATEMEDIATYPE**</span></span> | <span data-ttu-id="01b54-300">Le type de média de sortie du mélangeur n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="01b54-300">The mixer's output media type is invalid.</span></span> <span data-ttu-id="01b54-301">Le présentateur doit négocier un nouveau type de média avec le mélangeur.</span><span class="sxs-lookup"><span data-stu-id="01b54-301">The presenter should negotiate a new media type with the mixer.</span></span> <span data-ttu-id="01b54-302">Consultez la page [négociation de formats](#negotiating-formats).</span><span class="sxs-lookup"><span data-stu-id="01b54-302">See [Negotiating Formats](#negotiating-formats).</span></span>                                                                                         |
| <span data-ttu-id="01b54-303">**MFVP_MESSAGE_BEGINSTREAMING**</span><span class="sxs-lookup"><span data-stu-id="01b54-303">**MFVP_MESSAGE_BEGINSTREAMING**</span></span>      | <span data-ttu-id="01b54-304">La diffusion en continu a démarré.</span><span class="sxs-lookup"><span data-stu-id="01b54-304">Streaming has started.</span></span> <span data-ttu-id="01b54-305">Aucune action particulière n’est requise par ce message, mais vous pouvez l’utiliser pour allouer des ressources.</span><span class="sxs-lookup"><span data-stu-id="01b54-305">No particular action is required by this message, but you can use it to allocate resources.</span></span>                                                                                                                                 |
| <span data-ttu-id="01b54-306">**MFVP_MESSAGE_ENDSTREAMING**</span><span class="sxs-lookup"><span data-stu-id="01b54-306">**MFVP_MESSAGE_ENDSTREAMING**</span></span>        | <span data-ttu-id="01b54-307">La diffusion en continu est terminée.</span><span class="sxs-lookup"><span data-stu-id="01b54-307">Streaming has ended.</span></span> <span data-ttu-id="01b54-308">Libère toutes les ressources que vous avez allouées en réponse au message de **MFVP_MESSAGE_BEGINSTREAMING** .</span><span class="sxs-lookup"><span data-stu-id="01b54-308">Release any resources that you allocated in response to the **MFVP_MESSAGE_BEGINSTREAMING** message.</span></span>                                                                                                                        |
| <span data-ttu-id="01b54-309">**MFVP_MESSAGE_PROCESSINPUTNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="01b54-309">**MFVP_MESSAGE_PROCESSINPUTNOTIFY**</span></span>  | <span data-ttu-id="01b54-310">Le mélangeur a reçu un nouvel exemple d’entrée et peut être en mesure de générer un nouveau frame de sortie.</span><span class="sxs-lookup"><span data-stu-id="01b54-310">The mixer has received a new input sample and might be able to generate a new output frame.</span></span> <span data-ttu-id="01b54-311">Le présentateur doit appeler [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) sur le mixer.</span><span class="sxs-lookup"><span data-stu-id="01b54-311">The presenter should call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="01b54-312">Consultez [traitement](#processing-output)de la sortie.</span><span class="sxs-lookup"><span data-stu-id="01b54-312">See [Processing Output](#processing-output).</span></span> |
| <span data-ttu-id="01b54-313">**MFVP_MESSAGE_ENDOFSTREAM**</span><span class="sxs-lookup"><span data-stu-id="01b54-313">**MFVP_MESSAGE_ENDOFSTREAM**</span></span>         | <span data-ttu-id="01b54-314">La présentation est terminée.</span><span class="sxs-lookup"><span data-stu-id="01b54-314">The presentation has ended.</span></span> <span data-ttu-id="01b54-315">Voir la [fin du flux](#end-of-stream).</span><span class="sxs-lookup"><span data-stu-id="01b54-315">See [End of Stream](#end-of-stream).</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="01b54-316">**MFVP_MESSAGE_FLUSH**</span><span class="sxs-lookup"><span data-stu-id="01b54-316">**MFVP_MESSAGE_FLUSH**</span></span>               | <span data-ttu-id="01b54-317">EVR vide les données dans son pipeline de rendu.</span><span class="sxs-lookup"><span data-stu-id="01b54-317">The EVR is flushing the data in its rendering pipeline.</span></span> <span data-ttu-id="01b54-318">Le présentateur doit ignorer toutes les images vidéo qui sont planifiées pour la présentation.</span><span class="sxs-lookup"><span data-stu-id="01b54-318">The presenter should discard any video frames that are scheduled for presentation.</span></span>                                                                                                         |
| <span data-ttu-id="01b54-319">**MFVP_MESSAGE_STEP**</span><span class="sxs-lookup"><span data-stu-id="01b54-319">**MFVP_MESSAGE_STEP**</span></span>                | <span data-ttu-id="01b54-320">Demande au présentateur d’effectuer un pas à pas détaillé dans les N frames.</span><span class="sxs-lookup"><span data-stu-id="01b54-320">Requests the presenter to step forward N frames.</span></span> <span data-ttu-id="01b54-321">Le présentateur doit ignorer les N-1 frames suivants et afficher le nième Frame.</span><span class="sxs-lookup"><span data-stu-id="01b54-321">The presenter should discard the next N-1 frames and display the Nth frame.</span></span> <span data-ttu-id="01b54-322">Consultez [exécution pas à pas de la trame](#frame-stepping).</span><span class="sxs-lookup"><span data-stu-id="01b54-322">See [Frame Stepping](#frame-stepping).</span></span>                                                                                |
| <span data-ttu-id="01b54-323">**MFVP_MESSAGE_CANCELSTEP**</span><span class="sxs-lookup"><span data-stu-id="01b54-323">**MFVP_MESSAGE_CANCELSTEP**</span></span>          | <span data-ttu-id="01b54-324">Annule le pas à pas de la trame.</span><span class="sxs-lookup"><span data-stu-id="01b54-324">Cancels frame stepping.</span></span>                                                                                                                                                                                                                            |



 

### <a name="implementing-imfclockstatesink"></a><span data-ttu-id="01b54-325">Implémentation de IMFClockStateSink</span><span class="sxs-lookup"><span data-stu-id="01b54-325">Implementing IMFClockStateSink</span></span>

<span data-ttu-id="01b54-326">Le présentateur doit implémenter l’interface [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) dans le cadre de son implémentation de [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter), qui hérite de **IMFClockStateSink**.</span><span class="sxs-lookup"><span data-stu-id="01b54-326">The presenter must implement the [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) interface as part of its implementation of [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter), which inherits **IMFClockStateSink**.</span></span> <span data-ttu-id="01b54-327">EVR utilise cette interface pour notifier le présenteur chaque fois que l’horloge du EVR change d’État.</span><span class="sxs-lookup"><span data-stu-id="01b54-327">The EVR uses this interface to notify the presenter whenever the EVR's clock changes state.</span></span> <span data-ttu-id="01b54-328">Pour plus d’informations sur les États d’horloge, consultez [Présentation Clock](presentation-clock.md).</span><span class="sxs-lookup"><span data-stu-id="01b54-328">For more information about the clock states, see [Presentation Clock](presentation-clock.md).</span></span>

<span data-ttu-id="01b54-329">Voici quelques recommandations pour implémenter les méthodes dans cette interface.</span><span class="sxs-lookup"><span data-stu-id="01b54-329">Here are some guidelines for implementing the methods in this interface.</span></span> <span data-ttu-id="01b54-330">Toutes les méthodes doivent échouer si le présenteur est arrêté.</span><span class="sxs-lookup"><span data-stu-id="01b54-330">All of the methods should fail if the presenter is shut down.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="01b54-331"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="01b54-331"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="01b54-332">Définissez l’État présentateur sur démarré.</span><span class="sxs-lookup"><span data-stu-id="01b54-332">Set the presenter state to started.</span></span></li>
<li><span data-ttu-id="01b54-333">Si le <em>llClockStartOffset</em> n’est pas <strong>PRESENTATION_CURRENT_POSITION</strong>, videz la file d’attente du présentateur des exemples.</span><span class="sxs-lookup"><span data-stu-id="01b54-333">If the <em>llClockStartOffset</em> is not <strong>PRESENTATION_CURRENT_POSITION</strong>, flush the presenter's queue of samples.</span></span> <span data-ttu-id="01b54-334">(Cela équivaut à recevoir un message de <strong>MFVP_MESSAGE_FLUSH</strong> .)</span><span class="sxs-lookup"><span data-stu-id="01b54-334">(This is equivalent to receiving an <strong>MFVP_MESSAGE_FLUSH</strong> message.)</span></span></li>
<li><span data-ttu-id="01b54-335">Si une demande d’étape de frame précédente est toujours en attente, traitez la demande (consultez <a href="#frame-stepping">exécution pas à pas de la trame</a>).</span><span class="sxs-lookup"><span data-stu-id="01b54-335">If a previous frame-step request is still pending, process the request (see <a href="#frame-stepping">Frame Stepping</a>).</span></span> <span data-ttu-id="01b54-336">Sinon, essayez de traiter la sortie à partir du mélangeur (consultez traitement de la <a href="#processing-output">sortie</a>.</span><span class="sxs-lookup"><span data-stu-id="01b54-336">Otherwise, try to process output from the mixer (see <a href="#processing-output">Processing Output</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b54-337"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>OnClockStop</strong></a></span><span class="sxs-lookup"><span data-stu-id="01b54-337"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>OnClockStop</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="01b54-338">Définissez l’État présentateur sur arrêté.</span><span class="sxs-lookup"><span data-stu-id="01b54-338">Set the presenter state to stopped.</span></span></li>
<li><span data-ttu-id="01b54-339">Videz la file d’attente du présentateur des exemples.</span><span class="sxs-lookup"><span data-stu-id="01b54-339">Flush the presenter's queue of samples.</span></span></li>
<li><span data-ttu-id="01b54-340">Annulez toute opération de l’étape de frame en attente.</span><span class="sxs-lookup"><span data-stu-id="01b54-340">Cancel any pending frame-step operation.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b54-341"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>OnClockPause</strong></a></span><span class="sxs-lookup"><span data-stu-id="01b54-341"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>OnClockPause</strong></a></span></span></td>
<td><span data-ttu-id="01b54-342">Affectez à l’État présentateur la valeur Paused.</span><span class="sxs-lookup"><span data-stu-id="01b54-342">Set the presenter state to paused.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b54-343"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>OnClockRestart</strong></a></span><span class="sxs-lookup"><span data-stu-id="01b54-343"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>OnClockRestart</strong></a></span></span></td>
<td><span data-ttu-id="01b54-344">Traitez le même que <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a> , mais ne videz pas la file d’attente des exemples.</span><span class="sxs-lookup"><span data-stu-id="01b54-344">Treat the same as <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a> but do not flush the queue of samples.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b54-345"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>OnClockSetRate</strong></a></span><span class="sxs-lookup"><span data-stu-id="01b54-345"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>OnClockSetRate</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="01b54-346">Si le taux passe de zéro à différent de zéro, annulez l’exécution pas à pas de la trame.</span><span class="sxs-lookup"><span data-stu-id="01b54-346">If the rate is changing from zero to nonzero, cancel frame stepping.</span></span></li>
<li><span data-ttu-id="01b54-347">Stockez le nouveau taux d’horloge.</span><span class="sxs-lookup"><span data-stu-id="01b54-347">Store the new clock rate.</span></span> <span data-ttu-id="01b54-348">Le taux d’horloge affecte le moment où les exemples sont présentés.</span><span class="sxs-lookup"><span data-stu-id="01b54-348">The clock rate affects when samples are presented.</span></span> <span data-ttu-id="01b54-349">Pour plus d’informations, consultez <a href="#scheduling-samples">planification des exemples</a>.</span><span class="sxs-lookup"><span data-stu-id="01b54-349">For more information, see <a href="#scheduling-samples">Scheduling Samples</a>.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="implementing-imfratesupport"></a><span data-ttu-id="01b54-350">Implémentation de IMFRateSupport</span><span class="sxs-lookup"><span data-stu-id="01b54-350">Implementing IMFRateSupport</span></span>

<span data-ttu-id="01b54-351">Pour prendre en charge des vitesses de lecture autres que 1 × vitesse, le présentateur doit implémenter l’interface [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) .</span><span class="sxs-lookup"><span data-stu-id="01b54-351">To support playback rates other than 1× speed, the presenter must implement the [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface.</span></span> <span data-ttu-id="01b54-352">Voici quelques recommandations pour implémenter les méthodes dans cette interface.</span><span class="sxs-lookup"><span data-stu-id="01b54-352">Here are some guidelines for implementing the methods in this interface.</span></span> <span data-ttu-id="01b54-353">Toutes les méthodes doivent échouer après l’arrêt du présentateur.</span><span class="sxs-lookup"><span data-stu-id="01b54-353">All of the methods should fail after the presenter is shut down.</span></span> <span data-ttu-id="01b54-354">Pour plus d’informations sur cette interface, consultez la page contrôle de la [fréquence](rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="01b54-354">For more information about this interface, see [Rate Control](rate-control.md).</span></span>



|                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01b54-355">**GetSlowestRate**</span><span class="sxs-lookup"><span data-stu-id="01b54-355">**GetSlowestRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate)   | <span data-ttu-id="01b54-356">Retourne zéro pour indiquer qu’il n’y a pas de vitesse de lecture minimale.</span><span class="sxs-lookup"><span data-stu-id="01b54-356">Return zero to indicate no minimum playback rate.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="01b54-357">**GetFastestRate**</span><span class="sxs-lookup"><span data-stu-id="01b54-357">**GetFastestRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)   | <span data-ttu-id="01b54-358">Pour une lecture non fine, la vitesse de lecture ne doit pas dépasser la fréquence d’actualisation du moniteur :  =  *taux de rafraîchissement* maximal (Hz)/fréquence d' *images vidéo* (FPS).</span><span class="sxs-lookup"><span data-stu-id="01b54-358">For non-thinned playback, the playback rate should not exceed the refresh rate of the monitor: *maximum rate* = *refresh rate* (Hz) / *video frame rate* (fps).</span></span> <span data-ttu-id="01b54-359">La fréquence d’images vidéo est spécifiée dans le type de média du présentateur.</span><span class="sxs-lookup"><span data-stu-id="01b54-359">The video frame rate is specified in the presenter's media type.</span></span> <br/> <span data-ttu-id="01b54-360">Pour une lecture fine, le taux de lecture est illimité ; retourne la valeur **FLT_MAX**.</span><span class="sxs-lookup"><span data-stu-id="01b54-360">For thinned playback, the playback rate is unbounded; return the value **FLT_MAX**.</span></span> <span data-ttu-id="01b54-361">Dans la pratique, la source et le décodeur seront les facteurs de limitation lors de la lecture fine.</span><span class="sxs-lookup"><span data-stu-id="01b54-361">In practice, the source and the decoder will be the limiting factors during thinned playback.</span></span> <br/> <span data-ttu-id="01b54-362">Pour la lecture inversée, retourne la valeur négative du taux maximal.</span><span class="sxs-lookup"><span data-stu-id="01b54-362">For reverse playback, return the negative of the maximum rate.</span></span><br/> |
| [<span data-ttu-id="01b54-363">**IsRateSupported**</span><span class="sxs-lookup"><span data-stu-id="01b54-363">**IsRateSupported**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) | <span data-ttu-id="01b54-364">Retourne **MF_E_UNSUPPORTED_RATE** si la valeur absolue de *flRate* dépasse la vitesse de lecture maximale du présentateur.</span><span class="sxs-lookup"><span data-stu-id="01b54-364">Return **MF_E_UNSUPPORTED_RATE** if the absolute value of *flRate* exceeds the presenter's maximum playback rate.</span></span> <span data-ttu-id="01b54-365">Calculez la vitesse de lecture maximale comme décrit pour [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate).</span><span class="sxs-lookup"><span data-stu-id="01b54-365">Calculate the maximum playback rate as described for [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate).</span></span>                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="01b54-366">L’exemple suivant montre comment implémenter la méthode [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate) :</span><span class="sxs-lookup"><span data-stu-id="01b54-366">The following example shows how to implement the [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate) method:</span></span>


```C++
float EVRCustomPresenter::GetMaxRate(BOOL bThin)
{
    // Non-thinned:
    // If we have a valid frame rate and a monitor refresh rate, the maximum
    // playback rate is equal to the refresh rate. Otherwise, the maximum rate
    // is unbounded (FLT_MAX).

    // Thinned: The maximum rate is unbounded.

    float   fMaxRate = FLT_MAX;
    MFRatio fps = { 0, 0 };
    UINT    MonitorRateHz = 0;

    if (!bThin && (m_pMediaType != NULL))
    {
        GetFrameRate(m_pMediaType, &fps);
        MonitorRateHz = m_pD3DPresentEngine->RefreshRate();

        if (fps.Denominator && fps.Numerator && MonitorRateHz)
        {
            // Max Rate = Refresh Rate / Frame Rate
            fMaxRate = (float)MulDiv(
                MonitorRateHz, fps.Denominator, fps.Numerator);
        }
    }

    return fMaxRate;
}
```



<span data-ttu-id="01b54-367">L’exemple précédent appelle une méthode d’assistance, GetMaxRate, pour calculer la vitesse maximale de lecture en avant :</span><span class="sxs-lookup"><span data-stu-id="01b54-367">The previous example calls a helper method, GetMaxRate, to calculate the maximum forward playback rate:</span></span>

<span data-ttu-id="01b54-368">L’exemple suivant montre comment implémenter la méthode [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) :</span><span class="sxs-lookup"><span data-stu-id="01b54-368">The following example shows how to implement the [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) method:</span></span>


```C++
HRESULT EVRCustomPresenter::IsRateSupported(
    BOOL bThin,
    float fRate,
    float *pfNearestSupportedRate
    )
{
    EnterCriticalSection(&m_ObjectLock);

    float   fMaxRate = 0.0f;
    float   fNearestRate = fRate;  // If we support fRate, that is the nearest.

    HRESULT hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    // Find the maximum forward rate.
    // Note: We have no minimum rate (that is, we support anything down to 0).
    fMaxRate = GetMaxRate(bThin);

    if (fabsf(fRate) > fMaxRate)
    {
        // The (absolute) requested rate exceeds the maximum rate.
        hr = MF_E_UNSUPPORTED_RATE;

        // The nearest supported rate is fMaxRate.
        fNearestRate = fMaxRate;
        if (fRate < 0)
        {
            // Negative for reverse playback.
            fNearestRate = -fNearestRate;
        }
    }

    // Return the nearest supported rate.
    if (pfNearestSupportedRate != NULL)
    {
        *pfNearestSupportedRate = fNearestRate;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



### <a name="sending-events-to-the-evr"></a><span data-ttu-id="01b54-369">Envoi d’événements à EVR</span><span class="sxs-lookup"><span data-stu-id="01b54-369">Sending Events to the EVR</span></span>

<span data-ttu-id="01b54-370">Le présentateur doit notifier le EVR de divers événements.</span><span class="sxs-lookup"><span data-stu-id="01b54-370">The presenter must notify the EVR of various events.</span></span> <span data-ttu-id="01b54-371">Pour ce faire, il utilise l’interface [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) de EVR, obtenue lorsque le EVR appelle la méthode [**IMFTopologyServiceLookupClient :: InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) du présentateur.</span><span class="sxs-lookup"><span data-stu-id="01b54-371">To do so, it uses the EVR's [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) interface, obtained when the EVR calls the presenter's [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method.</span></span> <span data-ttu-id="01b54-372">(L’interface **IMediaEventSink** est à l’origine une interface DirectShow, mais elle est utilisée à la fois dans le EVR DirectShow et dans le Media Foundation.) Le code suivant montre comment envoyer un événement à EVR :</span><span class="sxs-lookup"><span data-stu-id="01b54-372">(The **IMediaEventSink** interface is originally a DirectShow interface, but is used in both the DirectShow EVR and the Media Foundation.) The following code shows how to send an event to the EVR:</span></span>


```C++
    // NotifyEvent: Send an event to the EVR through its IMediaEventSink interface.
    void NotifyEvent(long EventCode, LONG_PTR Param1, LONG_PTR Param2)
    {
        if (m_pMediaEventSink)
        {
            m_pMediaEventSink->Notify(EventCode, Param1, Param2);
        }
    }
```



<span data-ttu-id="01b54-373">Le tableau suivant répertorie les événements que le présenteur envoie, ainsi que les paramètres d’événement.</span><span class="sxs-lookup"><span data-stu-id="01b54-373">The following table lists the events that the presenter sends, along with the event parameters.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01b54-374">Événement</span><span class="sxs-lookup"><span data-stu-id="01b54-374">Event</span></span></th>
<th><span data-ttu-id="01b54-375">Description</span><span class="sxs-lookup"><span data-stu-id="01b54-375">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="01b54-376"><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></span><span class="sxs-lookup"><span data-stu-id="01b54-376"><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></span></span></td>
<td><span data-ttu-id="01b54-377">Le présentateur a terminé le rendu de toutes les trames après le message de MFVP_MESSAGE_ENDOFSTREAM.</span><span class="sxs-lookup"><span data-stu-id="01b54-377">The presenter has finished rendering all frames after the MFVP_MESSAGE_ENDOFSTREAM message.</span></span><br/>
<ul>
<li><span data-ttu-id="01b54-378"><em>Param1</em>: HRESULT indiquant l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="01b54-378"><em>Param1</em>: HRESULT indicating the status of the operation.</span></span></li>
<li><span data-ttu-id="01b54-379"><em>Param2</em>: non utilisé.</span><span class="sxs-lookup"><span data-stu-id="01b54-379"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="01b54-380">Pour plus d’informations, consultez <a href="#end-of-stream">fin de flux</a>.</span><span class="sxs-lookup"><span data-stu-id="01b54-380">For more information, see <a href="#end-of-stream">End of Stream</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b54-381"><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="01b54-381"><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></span></span></td>
<td><span data-ttu-id="01b54-382">L’appareil Direct3D a changé.</span><span class="sxs-lookup"><span data-stu-id="01b54-382">The Direct3D device has changed.</span></span><br/>
<ul>
<li><span data-ttu-id="01b54-383"><em>Param1</em>: non utilisé.</span><span class="sxs-lookup"><span data-stu-id="01b54-383"><em>Param1</em>: Not used.</span></span></li>
<li><span data-ttu-id="01b54-384"><em>Param2</em>: non utilisé.</span><span class="sxs-lookup"><span data-stu-id="01b54-384"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="01b54-385">Pour plus d’informations, consultez <a href="#managing-the-direct3d-device">gestion du périphérique Direct3D</a>.</span><span class="sxs-lookup"><span data-stu-id="01b54-385">For more information, see <a href="#managing-the-direct3d-device">Managing the Direct3D Device</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b54-386"><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="01b54-386"><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></span></span></td>
<td><span data-ttu-id="01b54-387">Une erreur s’est produite et nécessite l’arrêt de la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="01b54-387">An error has occurred that requires streaming to stop.</span></span><br/>
<ul>
<li><span data-ttu-id="01b54-388"><em>Param1</em>: <strong>HRESULT</strong> indiquant l’erreur qui s’est produite.</span><span class="sxs-lookup"><span data-stu-id="01b54-388"><em>Param1</em>: <strong>HRESULT</strong> indicating the error that occurred.</span></span></li>
<li><span data-ttu-id="01b54-389"><em>Param2</em>: non utilisé.</span><span class="sxs-lookup"><span data-stu-id="01b54-389"><em>Param2</em>: Not used.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b54-390"><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="01b54-390"><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></span></span></td>
<td><span data-ttu-id="01b54-391">Spécifie la durée pendant laquelle le présentateur prend le rendu de chaque image.</span><span class="sxs-lookup"><span data-stu-id="01b54-391">Specifies the amount of time that the presenter is taking to render each frame.</span></span> <span data-ttu-id="01b54-392">(Facultatif.)</span><span class="sxs-lookup"><span data-stu-id="01b54-392">(Optional.)</span></span><br/>
<ul>
<li><span data-ttu-id="01b54-393"><em>Param1</em>: pointeur vers une valeur <strong>LongLong</strong> constante qui contient la durée de traitement de la trame, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="01b54-393"><em>Param1</em>: Pointer to a constant <strong>LONGLONG</strong> value that contains the amount of time to process the frame, in 100-nanosecond units.</span></span></li>
<li><span data-ttu-id="01b54-394"><em>Param2</em>: non utilisé.</span><span class="sxs-lookup"><span data-stu-id="01b54-394"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="01b54-395">Pour plus d’informations, consultez traitement de la <a href="#processing-output">sortie</a>.</span><span class="sxs-lookup"><span data-stu-id="01b54-395">For more information, see <a href="#processing-output">Processing Output</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b54-396"><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="01b54-396"><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></span></span></td>
<td><span data-ttu-id="01b54-397">Spécifie le temps de décalage actuel dans les échantillons de rendu.</span><span class="sxs-lookup"><span data-stu-id="01b54-397">Specifies the current lag time in rendering samples.</span></span> <span data-ttu-id="01b54-398">Si la valeur est positive, les exemples sont en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="01b54-398">If the value is positive, samples are behind schedule.</span></span> <span data-ttu-id="01b54-399">Si la valeur est négative, les échantillons sont en avance sur Schedule.</span><span class="sxs-lookup"><span data-stu-id="01b54-399">If the value is negative, samples are ahead of schedule.</span></span> <span data-ttu-id="01b54-400">(Facultatif.)</span><span class="sxs-lookup"><span data-stu-id="01b54-400">(Optional.)</span></span><br/>
<ul>
<li><span data-ttu-id="01b54-401"><em>Param1</em>: pointeur vers une valeur <strong>LongLong</strong> constante qui contient le temps de retard, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="01b54-401"><em>Param1</em>: Pointer to a constant <strong>LONGLONG</strong> value that contains the lag time, in 100-nanosecond units.</span></span></li>
<li><span data-ttu-id="01b54-402"><em>Param2</em>: non utilisé.</span><span class="sxs-lookup"><span data-stu-id="01b54-402"><em>Param2</em>: Not used.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01b54-403"><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></span><span class="sxs-lookup"><span data-stu-id="01b54-403"><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></span></span></td>
<td><span data-ttu-id="01b54-404">Envoyé immédiatement après <strong>EC_STEP_COMPLETE</strong> si la vitesse de lecture est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="01b54-404">Sent immediately after <strong>EC_STEP_COMPLETE</strong> if the playback rate is zero.</span></span> <span data-ttu-id="01b54-405">Cet événement contient l’horodatage du frame qui a été affiché.</span><span class="sxs-lookup"><span data-stu-id="01b54-405">This event contains the time stamp of the frame that was displayed.</span></span><br/>
<ul>
<li><span data-ttu-id="01b54-406"><em>Param1</em>: 32 bits inférieurs de l’horodatage.</span><span class="sxs-lookup"><span data-stu-id="01b54-406"><em>Param1</em>: Lower 32 bits of the time stamp.</span></span></li>
<li><span data-ttu-id="01b54-407"><em>Param2</em>: 32 bits supérieurs de l’horodatage.</span><span class="sxs-lookup"><span data-stu-id="01b54-407"><em>Param2</em>: Upper 32 bits of the time stamp.</span></span></li>
</ul>
<span data-ttu-id="01b54-408">Pour plus d’informations, consultez <a href="#frame-stepping">exécution pas à pas de la trame</a>.</span><span class="sxs-lookup"><span data-stu-id="01b54-408">For more information, see <a href="#frame-stepping">Frame Stepping</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01b54-409"><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></span><span class="sxs-lookup"><span data-stu-id="01b54-409"><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></span></span></td>
<td><span data-ttu-id="01b54-410">Le présentateur a terminé ou annulé une étape de frame.</span><span class="sxs-lookup"><span data-stu-id="01b54-410">The presenter has completed or canceled a frame step.</span></span><br/>
<ul>
<li><span data-ttu-id="01b54-411"><em>Param1</em>: non utilisé.</span><span class="sxs-lookup"><span data-stu-id="01b54-411"><em>Param1</em>: Not used.</span></span></li>
<li><span data-ttu-id="01b54-412"><em>Param2</em>: non utilisé.</span><span class="sxs-lookup"><span data-stu-id="01b54-412"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="01b54-413">Pour plus d’informations, consultez <a href="#frame-stepping">exécution pas à pas de la trame</a>.</span><span class="sxs-lookup"><span data-stu-id="01b54-413">For more information, see <a href="#frame-stepping">Frame Stepping</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="01b54-414">Une version précédente de la documentation A décrit <em>param1</em> de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="01b54-414">A previous version of the documentation described <em>Param1</em> incorrectly.</span></span> <span data-ttu-id="01b54-415">Ce paramètre n’est pas utilisé pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="01b54-415">This parameter is not used for this event.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="negotiating-formats"></a><span data-ttu-id="01b54-416">Négociation des formats</span><span class="sxs-lookup"><span data-stu-id="01b54-416">Negotiating Formats</span></span>

<span data-ttu-id="01b54-417">Chaque fois que le présentateur reçoit un message de **MFVP_MESSAGE_INVALIDATEMEDIATYPE** à partir du EVR, il doit définir le format de sortie sur le mélangeur, comme suit :</span><span class="sxs-lookup"><span data-stu-id="01b54-417">Whenever the presenter receives an **MFVP_MESSAGE_INVALIDATEMEDIATYPE** message from the EVR, it must set the output format on the mixer, as follows:</span></span>

1.  <span data-ttu-id="01b54-418">Appelez [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) sur le mélangeur pour obtenir un type de sortie possible.</span><span class="sxs-lookup"><span data-stu-id="01b54-418">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) on the mixer to get a possible output type.</span></span> <span data-ttu-id="01b54-419">Ce type décrit un format que le mélangeur peut produire en fonction des flux d’entrée et des fonctionnalités de traitement vidéo du périphérique graphique.</span><span class="sxs-lookup"><span data-stu-id="01b54-419">This type describes a format that the mixer can produce given the input streams and the video processing capabilities of the graphics device.</span></span>
2.  <span data-ttu-id="01b54-420">Vérifiez si le présentateur peut utiliser ce type de média comme format de rendu.</span><span class="sxs-lookup"><span data-stu-id="01b54-420">Check whether the presenter can use this media type as its rendering format.</span></span> <span data-ttu-id="01b54-421">Voici quelques éléments à vérifier, bien que votre implémentation puisse avoir ses propres exigences :</span><span class="sxs-lookup"><span data-stu-id="01b54-421">Here are some things to check, although your implementation might have its own requirements:</span></span>

    -   <span data-ttu-id="01b54-422">La vidéo doit être décompressée.</span><span class="sxs-lookup"><span data-stu-id="01b54-422">The video must be uncompressed.</span></span>
    -   <span data-ttu-id="01b54-423">La vidéo ne doit comporter que des images progressives.</span><span class="sxs-lookup"><span data-stu-id="01b54-423">The video must have progressive frames only.</span></span> <span data-ttu-id="01b54-424">Vérifiez que l’attribut [**MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) est égal à **MFVideoInterlace_Progressive**.</span><span class="sxs-lookup"><span data-stu-id="01b54-424">Check that the [**MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) attribute equals **MFVideoInterlace_Progressive**.</span></span>
    -   <span data-ttu-id="01b54-425">Le format doit être compatible avec le périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="01b54-425">The format must be compatible with the Direct3D device.</span></span>

    <span data-ttu-id="01b54-426">Si le type n’est pas acceptable, revenez à l’étape 1 et récupérez le type proposé suivant de la console.</span><span class="sxs-lookup"><span data-stu-id="01b54-426">If the type is not acceptable, return to step 1 and get the mixer's next proposed type.</span></span>

3.  <span data-ttu-id="01b54-427">Créez un nouveau type de média qui est un clone du type d’origine, puis modifiez les attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="01b54-427">Create a new media type that is a clone of the original type and then change the following attributes:</span></span>

    -   <span data-ttu-id="01b54-428">Définissez l’attribut [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) égal à la largeur et à la hauteur souhaitées pour les surfaces Direct3D que vous allez allouer.</span><span class="sxs-lookup"><span data-stu-id="01b54-428">Set the [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) attribute equal to the width and height that you want for the Direct3D surfaces you will allocate.</span></span>
    -   <span data-ttu-id="01b54-429">Affectez la valeur **false** à l’attribut [**MF_MT_PAN_SCAN_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="01b54-429">Set the [**MF_MT_PAN_SCAN_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) attribute to **FALSE**.</span></span>
    -   <span data-ttu-id="01b54-430">Affectez à l’attribut [**MF_MT_PIXEL_ASPECT_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) égal au-dessus de l’affichage (généralement 1:1).</span><span class="sxs-lookup"><span data-stu-id="01b54-430">Set the [**MF_MT_PIXEL_ASPECT_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) attribute equal to the PAR of the display (typically 1:1).</span></span>
    -   <span data-ttu-id="01b54-431">Affectez à l’ouverture géométrique (attribut [**MF_MT_GEOMETRIC_APERTURE**](mf-mt-geometric-aperture-attribute.md) ) une valeur égale à un rectangle dans la surface Direct3D.</span><span class="sxs-lookup"><span data-stu-id="01b54-431">Set the geometric aperture ([**MF_MT_GEOMETRIC_APERTURE**](mf-mt-geometric-aperture-attribute.md) attribute) equal to a rectangle within the Direct3D surface.</span></span> <span data-ttu-id="01b54-432">Lorsque le mélangeur génère un frame de sortie, il BLITS l’image source sur ce rectangle.</span><span class="sxs-lookup"><span data-stu-id="01b54-432">When the mixer generates an output frame, it blits the source image onto this rectangle.</span></span> <span data-ttu-id="01b54-433">L’ouverture géométrique peut être aussi grande que la surface, ou elle peut être un sous-rectangle dans la surface.</span><span class="sxs-lookup"><span data-stu-id="01b54-433">The geometric aperture can be as large as the surface, or it can be a subrectangle within the surface.</span></span> <span data-ttu-id="01b54-434">Pour plus d’informations, consultez [rectangles source et destination](#source-and-destination-rectangles).</span><span class="sxs-lookup"><span data-stu-id="01b54-434">For more information, see [Source and Destination Rectangles](#source-and-destination-rectangles).</span></span>

4.  <span data-ttu-id="01b54-435">Pour vérifier si le mélangeur accepte le type de sortie modifié, appelez [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) avec l’indicateur **MFT_SET_TYPE_TEST_ONLY** .</span><span class="sxs-lookup"><span data-stu-id="01b54-435">To test whether the mixer will accept the modified output type, call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) with the **MFT_SET_TYPE_TEST_ONLY** flag.</span></span> <span data-ttu-id="01b54-436">Si le mélangeur rejette le type, revenez à l’étape 1 pour obtenir le type suivant.</span><span class="sxs-lookup"><span data-stu-id="01b54-436">If the mixer rejects the type, go back to step 1 and get the next type.</span></span>
5.  <span data-ttu-id="01b54-437">Allouez un pool de surfaces Direct3D, comme décrit dans [allocation de surfaces Direct3D](#allocating-direct3d-surfaces).</span><span class="sxs-lookup"><span data-stu-id="01b54-437">Allocate a pool of Direct3D surfaces, as described in [Allocating Direct3D Surfaces](#allocating-direct3d-surfaces).</span></span> <span data-ttu-id="01b54-438">Le mélangeur utilise ces surfaces lorsqu’il dessine les images vidéo composite.</span><span class="sxs-lookup"><span data-stu-id="01b54-438">The mixer will use these surfaces when it draws the composited video frames.</span></span>
6.  <span data-ttu-id="01b54-439">Définissez le type de sortie sur le mélangeur en appelant [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) sans indicateurs.</span><span class="sxs-lookup"><span data-stu-id="01b54-439">Set the output type on the mixer by calling [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) with no flags.</span></span> <span data-ttu-id="01b54-440">Si le premier appel à **SetOutputType** a réussi à l’étape 4, la méthode doit être réexécutée.</span><span class="sxs-lookup"><span data-stu-id="01b54-440">If the first call to **SetOutputType** succeeded in step 4, the method should succeed again.</span></span>

<span data-ttu-id="01b54-441">Si le mélangeur est en dehors des types, la méthode [**GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) retourne **MF_E_NO_MORE_TYPES**.</span><span class="sxs-lookup"><span data-stu-id="01b54-441">If the mixer runs out of types, the [**GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method returns **MF_E_NO_MORE_TYPES**.</span></span> <span data-ttu-id="01b54-442">Si le présenteur ne parvient pas à trouver un type de sortie approprié pour le mélangeur, le flux ne peut pas être rendu.</span><span class="sxs-lookup"><span data-stu-id="01b54-442">If the presenter cannot find a suitable output type for the mixer, the stream cannot be rendered.</span></span> <span data-ttu-id="01b54-443">Dans ce cas, DirectShow ou Media Foundation peuvent essayer un autre format de flux.</span><span class="sxs-lookup"><span data-stu-id="01b54-443">In that case, DirectShow or Media Foundation might try another stream format.</span></span> <span data-ttu-id="01b54-444">Par conséquent, le présentateur peut recevoir plusieurs messages de **MFVP_MESSAGE_INVALIDATEMEDIATYPE** dans une ligne jusqu’à ce qu’un type valide soit trouvé.</span><span class="sxs-lookup"><span data-stu-id="01b54-444">Therefore, the presenter might receive several **MFVP_MESSAGE_INVALIDATEMEDIATYPE** messages in a row until a valid type is found.</span></span>

<span data-ttu-id="01b54-445">Le mélangeur cadres automatiquement la vidéo, en tenant compte des proportions en pixels (PAR) de la source et de la destination.</span><span class="sxs-lookup"><span data-stu-id="01b54-445">The mixer automatically letterboxes the video, taking into account the pixel aspect ratio (PAR) of the source and destination.</span></span> <span data-ttu-id="01b54-446">Pour de meilleurs résultats, la largeur et la hauteur de la surface et l’ouverture géométrique doivent être égales à la taille réelle dans laquelle vous souhaitez que la vidéo apparaisse sur l’affichage.</span><span class="sxs-lookup"><span data-stu-id="01b54-446">For best results, the surface width and height and the geometric aperture should be equal to the actual size that you want the video to appear on the display.</span></span> <span data-ttu-id="01b54-447">L’illustration suivante montre ce processus.</span><span class="sxs-lookup"><span data-stu-id="01b54-447">The following image illustrates this process.</span></span>

![Diagramme montrant un minutage composite menant à une surface Direct3D, qui mène à une fenêtre](images/b746edca-8830-4c88-aa59-0067b020d4af.gif)

<span data-ttu-id="01b54-449">Le code suivant illustre le plan du processus.</span><span class="sxs-lookup"><span data-stu-id="01b54-449">The following code shows the outline of the process.</span></span> <span data-ttu-id="01b54-450">Certaines étapes sont placées dans les fonctions d’assistance, dont les détails exacts dépendent des exigences de votre présentateur.</span><span class="sxs-lookup"><span data-stu-id="01b54-450">Some of the steps are placed in helper functions, the exact details of which will depend on the requirements of your presenter.</span></span>


```C++
HRESULT EVRCustomPresenter::RenegotiateMediaType()
{
    HRESULT hr = S_OK;
    BOOL bFoundMediaType = FALSE;

    IMFMediaType *pMixerType = NULL;
    IMFMediaType *pOptimalType = NULL;
    IMFVideoMediaType *pVideoType = NULL;

    if (!m_pMixer)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Loop through all of the mixer's proposed output types.
    DWORD iTypeIndex = 0;
    while (!bFoundMediaType && (hr != MF_E_NO_MORE_TYPES))
    {
        SafeRelease(&pMixerType);
        SafeRelease(&pOptimalType);

        // Step 1. Get the next media type supported by mixer.
        hr = m_pMixer->GetOutputAvailableType(0, iTypeIndex++, &pMixerType);
        if (FAILED(hr))
        {
            break;
        }

        // From now on, if anything in this loop fails, try the next type,
        // until we succeed or the mixer runs out of types.

        // Step 2. Check if we support this media type.
        if (SUCCEEDED(hr))
        {
            // Note: None of the modifications that we make later in CreateOptimalVideoType
            // will affect the suitability of the type, at least for us. (Possibly for the mixer.)
            hr = IsMediaTypeSupported(pMixerType);
        }

        // Step 3. Adjust the mixer's type to match our requirements.
        if (SUCCEEDED(hr))
        {
            hr = CreateOptimalVideoType(pMixerType, &pOptimalType);
        }

        // Step 4. Check if the mixer will accept this media type.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, MFT_SET_TYPE_TEST_ONLY);
        }

        // Step 5. Try to set the media type on ourselves.
        if (SUCCEEDED(hr))
        {
            hr = SetMediaType(pOptimalType);
        }

        // Step 6. Set output media type on mixer.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, 0);

            assert(SUCCEEDED(hr)); // This should succeed unless the MFT lied in the previous call.

            // If something went wrong, clear the media type.
            if (FAILED(hr))
            {
                SetMediaType(NULL);
            }
        }

        if (SUCCEEDED(hr))
        {
            bFoundMediaType = TRUE;
        }
    }

    SafeRelease(&pMixerType);
    SafeRelease(&pOptimalType);
    SafeRelease(&pVideoType);

    return hr;
}
```



<span data-ttu-id="01b54-451">Pour plus d’informations sur les types de média vidéo, consultez [Video Media types](video-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="01b54-451">For more information about video media types, see [Video Media Types](video-media-types.md).</span></span>

## <a name="managing-the-direct3d-device"></a><span data-ttu-id="01b54-452">Gestion de l’appareil Direct3D</span><span class="sxs-lookup"><span data-stu-id="01b54-452">Managing the Direct3D Device</span></span>

<span data-ttu-id="01b54-453">Le présentateur crée le périphérique Direct3D et gère toute perte d’appareil pendant la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="01b54-453">The presenter creates the Direct3D device and handles any device loss during streaming.</span></span> <span data-ttu-id="01b54-454">Le présentateur héberge également le gestionnaire de périphériques Direct3D, qui permet à d’autres composants d’utiliser le même appareil.</span><span class="sxs-lookup"><span data-stu-id="01b54-454">The presenter also hosts the Direct3D device manager, which provides a way for other components to use the same device.</span></span> <span data-ttu-id="01b54-455">Par exemple, le mélangeur utilise le périphérique Direct3D pour mélanger les sous-flux, le désentrelacement et effectuer des ajustements de couleurs.</span><span class="sxs-lookup"><span data-stu-id="01b54-455">For example, the mixer uses the Direct3D device to mix substreams, deinterlace, and perform color adjustments.</span></span> <span data-ttu-id="01b54-456">Les décodeurs peuvent utiliser l’appareil Direct3D pour le décodage accéléré vidéo.</span><span class="sxs-lookup"><span data-stu-id="01b54-456">Decoders can use the Direct3D device for video-accelerated decoding.</span></span> <span data-ttu-id="01b54-457">(Pour plus d’informations sur l’accélération vidéo, consultez [DirectX Video acceleration 2,0](directx-video-acceleration-2-0.md).)</span><span class="sxs-lookup"><span data-stu-id="01b54-457">(For more information about video acceleration, see [DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md).)</span></span>

<span data-ttu-id="01b54-458">Pour configurer le périphérique Direct3D, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="01b54-458">To set up the Direct3D device, perform the following steps:</span></span>

1.  <span data-ttu-id="01b54-459">Créez l’objet Direct3D en appelant **Direct3DCreate9** ou **Direct3DCreate9Ex**.</span><span class="sxs-lookup"><span data-stu-id="01b54-459">Create the Direct3D object by calling **Direct3DCreate9** or **Direct3DCreate9Ex**.</span></span>
2.  <span data-ttu-id="01b54-460">Créez l’appareil en appelant **IDirect3D9 :: CreateDevice** ou **IDirect3D9Ex :: CreateDevice**.</span><span class="sxs-lookup"><span data-stu-id="01b54-460">Create the device by calling **IDirect3D9::CreateDevice** or **IDirect3D9Ex::CreateDevice**.</span></span>
3.  <span data-ttu-id="01b54-461">Créez le gestionnaire de périphériques en appelant [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span><span class="sxs-lookup"><span data-stu-id="01b54-461">Create the device manager by calling [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span></span>
4.  <span data-ttu-id="01b54-462">Définissez l’appareil sur le gestionnaire de périphériques en appelant [**IDirect3DDeviceManager9 :: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span><span class="sxs-lookup"><span data-stu-id="01b54-462">Set the device on the device manager by calling [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span></span>

<span data-ttu-id="01b54-463">Si un autre composant de pipeline a besoin du gestionnaire de périphériques, il appelle [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) sur le EVR, en spécifiant **MR_VIDEO_ACCELERATION_SERVICE** pour le GUID du service.</span><span class="sxs-lookup"><span data-stu-id="01b54-463">If another pipeline component needs the device manager, it calls [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the EVR, specifying **MR_VIDEO_ACCELERATION_SERVICE** for the service GUID.</span></span> <span data-ttu-id="01b54-464">Le EVR transmet la requête au présentateur.</span><span class="sxs-lookup"><span data-stu-id="01b54-464">The EVR passes the request to the presenter.</span></span> <span data-ttu-id="01b54-465">Une fois que l’objet a obtenu le pointeur [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) , il peut obtenir un handle vers l’appareil en appelant [**IDirect3DDeviceManager9 :: OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle).</span><span class="sxs-lookup"><span data-stu-id="01b54-465">After the object gets the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) pointer, it can get a handle to the device by calling [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle).</span></span> <span data-ttu-id="01b54-466">Lorsque l’objet doit utiliser l’appareil, il passe le handle de l’appareil à la méthode [**IDirect3DDeviceManager9 :: LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) , qui retourne un pointeur **IDirect3DDevice9** .</span><span class="sxs-lookup"><span data-stu-id="01b54-466">When the object needs to use the device, it passes the device handle to the [**IDirect3DDeviceManager9::LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) method, which returns an **IDirect3DDevice9** pointer.</span></span>

<span data-ttu-id="01b54-467">Une fois l’appareil créé, si le présentateur détruit l’appareil et en crée un nouveau, le présentateur doit appeler à nouveau [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) .</span><span class="sxs-lookup"><span data-stu-id="01b54-467">After the device is created, if the presenter destroys the device and creates a new one, the presenter must call [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) again.</span></span> <span data-ttu-id="01b54-468">La méthode **ResetDevice** invalide tous les descripteurs d’appareil existants, ce qui amène [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) à retourner **DXVA2_E_NEW_VIDEO_DEVICE**.</span><span class="sxs-lookup"><span data-stu-id="01b54-468">The **ResetDevice** method invalidates any existing device handles, which causes [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) to return **DXVA2_E_NEW_VIDEO_DEVICE**.</span></span> <span data-ttu-id="01b54-469">Ce code d’erreur signale à d’autres objets utilisant l’appareil qu’ils doivent ouvrir un nouveau descripteur d’appareil.</span><span class="sxs-lookup"><span data-stu-id="01b54-469">This error code signals to other objects using the device that they should open a new device handle.</span></span> <span data-ttu-id="01b54-470">Pour plus d’informations sur l’utilisation du gestionnaire de périphériques, consultez [Direct3D gestionnaire de périphériques](direct3d-device-manager.md).</span><span class="sxs-lookup"><span data-stu-id="01b54-470">For more information about using the device manager, see [Direct3D Device Manager](direct3d-device-manager.md).</span></span>

<span data-ttu-id="01b54-471">Le présentateur peut créer l’appareil en mode fenêtre ou exclusif en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="01b54-471">The presenter can create the device in windowed mode or full-screen exclusive mode.</span></span> <span data-ttu-id="01b54-472">Pour le mode fenêtre, vous devez fournir à l’application un moyen de spécifier la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="01b54-472">For windowed mode, you should provide a way for the application to specify the video window.</span></span> <span data-ttu-id="01b54-473">Le présentateur standard implémente la méthode [**IMFVideoDisplayControl :: SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) à cet effet.</span><span class="sxs-lookup"><span data-stu-id="01b54-473">The standard presenter implements the [**IMFVideoDisplayControl::SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) method for this purpose.</span></span> <span data-ttu-id="01b54-474">Vous devez créer l’appareil lorsque le présentateur est créé pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="01b54-474">You must create the device when the presenter is first created.</span></span> <span data-ttu-id="01b54-475">En règle générale, vous ne connaissez pas tous les paramètres de l’appareil à ce stade, tels que la fenêtre ou le format de la mémoire tampon d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="01b54-475">Typically, you won't know all of the device parameters at this time, such as the window or the back buffer format.</span></span> <span data-ttu-id="01b54-476">Vous pouvez créer un appareil temporaire et le remplacer ultérieurement&\# ; n’oubliez pas d’appeler [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) sur le gestionnaire de périphériques.</span><span class="sxs-lookup"><span data-stu-id="01b54-476">You can create a temporary device and replace it later&\#;just remember to call [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) on the device manager.</span></span>

<span data-ttu-id="01b54-477">Si vous créez un nouveau périphérique ou si vous appelez **IDirect3DDevice9 :: Reset** ou **IDirect3DDevice9Ex :: ResetEx** sur un appareil existant, envoyez un événement [**EC_DISPLAY_CHANGED**](../directshow/ec-display-changed.md) au EVR.</span><span class="sxs-lookup"><span data-stu-id="01b54-477">If you create a new device, or if you call **IDirect3DDevice9::Reset** or **IDirect3DDevice9Ex::ResetEx** on an existing device, send an [**EC_DISPLAY_CHANGED**](../directshow/ec-display-changed.md) event to the EVR.</span></span> <span data-ttu-id="01b54-478">Cet événement avertit EVR de renégocier le type de média.</span><span class="sxs-lookup"><span data-stu-id="01b54-478">This event notifies the EVR to renegotiate the media type.</span></span> <span data-ttu-id="01b54-479">EVR ignore les paramètres d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="01b54-479">The EVR ignores the event parameters for this event.</span></span>

### <a name="allocating-direct3d-surfaces"></a><span data-ttu-id="01b54-480">Allouer des surfaces Direct3D</span><span class="sxs-lookup"><span data-stu-id="01b54-480">Allocating Direct3D Surfaces</span></span>

<span data-ttu-id="01b54-481">Une fois que le présentateur a défini le type de média, il peut allouer les surfaces Direct3D qui seront utilisées par le mélangeur pour écrire les images vidéo.</span><span class="sxs-lookup"><span data-stu-id="01b54-481">After the presenter sets the media type, it can allocate the Direct3D surfaces, which the mixer will use to write the video frames.</span></span> <span data-ttu-id="01b54-482">La surface doit correspondre au type de média du présentateur :</span><span class="sxs-lookup"><span data-stu-id="01b54-482">The surface must match the presenter's media type:</span></span>

-   <span data-ttu-id="01b54-483">Le format de surface doit correspondre au sous-type de média.</span><span class="sxs-lookup"><span data-stu-id="01b54-483">The surface format must match the media subtype.</span></span> <span data-ttu-id="01b54-484">Par exemple, si le sous-type est **MFVideoFormat_RGB24**, le format de surface doit être **D3DFMT_X8R8G8B8**.</span><span class="sxs-lookup"><span data-stu-id="01b54-484">For example, if the subtype is **MFVideoFormat_RGB24**, the surface format must be **D3DFMT_X8R8G8B8**.</span></span> <span data-ttu-id="01b54-485">Pour plus d’informations sur les sous-types et les formats Direct3D, consultez [GUID sous-type de vidéo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="01b54-485">For more information about subtypes and Direct3D formats, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>
-   <span data-ttu-id="01b54-486">La largeur et la hauteur de la surface doivent correspondre aux dimensions spécifiées dans l’attribut [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) du type de média.</span><span class="sxs-lookup"><span data-stu-id="01b54-486">The surface width and height must match the dimensions given in the [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) attribute of the media type.</span></span>

<span data-ttu-id="01b54-487">La méthode recommandée pour allouer des surfaces varie selon que le présentateur s’exécute en mode fenêtre ou plein écran.</span><span class="sxs-lookup"><span data-stu-id="01b54-487">The recommended way to allocate surfaces depends on whether the presenter runs windowed or full-screen.</span></span>

<span data-ttu-id="01b54-488">Si le périphérique Direct3D est fenêtre, vous pouvez créer plusieurs chaînes de permutation, chacune avec une seule mémoire tampon d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="01b54-488">If the Direct3D device is windowed, you can create several swap chains, each with a single back buffer.</span></span> <span data-ttu-id="01b54-489">À l’aide de cette approche, vous pouvez présenter chaque surface indépendamment, car la présentation d’une chaîne de permutation n’interfère pas avec les autres chaînes de permutation.</span><span class="sxs-lookup"><span data-stu-id="01b54-489">Using this approach, you can present each surface independently, because presenting one swap chain will not interfere with the other swap chains.</span></span> <span data-ttu-id="01b54-490">Le mélangeur peut écrire des données sur une surface, tandis qu’une autre surface est planifiée pour la présentation.</span><span class="sxs-lookup"><span data-stu-id="01b54-490">The mixer can write data to a surface while another surface is scheduled for presentation.</span></span>

<span data-ttu-id="01b54-491">Tout d’abord, déterminez le nombre de chaînes de permutation à créer.</span><span class="sxs-lookup"><span data-stu-id="01b54-491">First, decide how many swap chains to create.</span></span> <span data-ttu-id="01b54-492">Un minimum de trois est recommandé.</span><span class="sxs-lookup"><span data-stu-id="01b54-492">A minimum of three is recommended.</span></span> <span data-ttu-id="01b54-493">Pour chaque chaîne de permutation, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="01b54-493">For each swap chain, do the following:</span></span>

1.  <span data-ttu-id="01b54-494">Appelez **IDirect3DDevice9 :: CreateAdditionalSwapChain** pour créer la chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="01b54-494">Call **IDirect3DDevice9::CreateAdditionalSwapChain** to create the swap chain.</span></span>
2.  <span data-ttu-id="01b54-495">Appelez **IDirect3DSwapChain9 :: GetBackBuffer** pour obtenir un pointeur vers la surface de mémoire tampon d’arrière-plan de la chaîne d’échange.</span><span class="sxs-lookup"><span data-stu-id="01b54-495">Call **IDirect3DSwapChain9::GetBackBuffer** to get a pointer to the swap chain's back buffer surface.</span></span>
3.  <span data-ttu-id="01b54-496">Appelez [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) et transmettez un pointeur vers l’aire.</span><span class="sxs-lookup"><span data-stu-id="01b54-496">Call [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) and pass in a pointer to the surface.</span></span> <span data-ttu-id="01b54-497">Cette fonction retourne un pointeur vers un objet d’exemple vidéo.</span><span class="sxs-lookup"><span data-stu-id="01b54-497">This function returns a pointer to a video sample object.</span></span> <span data-ttu-id="01b54-498">L’exemple d’objet Video implémente l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , et le présenteur utilise cette interface pour remettre la surface au mélangeur lorsque le présenteur appelle la méthode [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) du mixer.</span><span class="sxs-lookup"><span data-stu-id="01b54-498">The video sample object implements the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, and the presenter uses this interface to deliver the surface to the mixer when the presenter calls the mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method.</span></span> <span data-ttu-id="01b54-499">Pour plus d’informations sur l’exemple d’objet vidéo, consultez [Video Samples](video-samples.md)(en anglais).</span><span class="sxs-lookup"><span data-stu-id="01b54-499">For more information about the video sample object, see [Video Samples](video-samples.md).</span></span>
4.  <span data-ttu-id="01b54-500">Stocke le pointeur [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) dans une file d’attente.</span><span class="sxs-lookup"><span data-stu-id="01b54-500">Store the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointer in a queue.</span></span> <span data-ttu-id="01b54-501">Le présentateur extraira les exemples de cette file d’attente pendant le traitement, comme décrit dans traitement de la [sortie](#processing-output).</span><span class="sxs-lookup"><span data-stu-id="01b54-501">The presenter will pull samples from this queue during processing as described in [Processing Output](#processing-output).</span></span>
5.  <span data-ttu-id="01b54-502">Conservez une référence au pointeur **IDirect3DSwapChain9** pour que la chaîne de permutation ne soit pas libérée.</span><span class="sxs-lookup"><span data-stu-id="01b54-502">Keep a reference to the **IDirect3DSwapChain9** pointer so the swap chain is not released.</span></span>

<span data-ttu-id="01b54-503">En mode exclusif plein écran, l’appareil ne peut pas avoir plus d’une chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="01b54-503">In full-screen exclusive mode, the device cannot have more than one swap chain.</span></span> <span data-ttu-id="01b54-504">Cette chaîne de permutation est créée implicitement lorsque vous créez l’appareil plein écran.</span><span class="sxs-lookup"><span data-stu-id="01b54-504">This swap chain is created implicitly when you create the full-screen device.</span></span> <span data-ttu-id="01b54-505">La chaîne de permutation peut avoir plus d’une mémoire tampon d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="01b54-505">The swap chain can have more than one back buffer.</span></span> <span data-ttu-id="01b54-506">Malheureusement, toutefois, si vous présentez une mémoire tampon d’arrière-plan pendant que vous écrivez à une autre mémoire tampon d’arrière-plan dans la même chaîne de permutation, il n’existe aucun moyen simple de coordonner les deux opérations.</span><span class="sxs-lookup"><span data-stu-id="01b54-506">Unfortunately, however, if you present one back buffer while you write to another back buffer in the same swap chain, there is no easy way to coordinate the two operations.</span></span> <span data-ttu-id="01b54-507">Cela est dû à la façon dont Direct3D implémente la symétrie de surface.</span><span class="sxs-lookup"><span data-stu-id="01b54-507">This is because of the way Direct3D implements surface flipping.</span></span> <span data-ttu-id="01b54-508">Lorsque vous appelez la présente, le pilote Graphics met à jour les pointeurs surface dans la mémoire graphique.</span><span class="sxs-lookup"><span data-stu-id="01b54-508">When you call Present, the graphics driver updates the surface pointers in graphics memory.</span></span> <span data-ttu-id="01b54-509">Si vous maintenez des pointeurs **IDirect3DSurface9** quand vous appelez la méthode **present**, ceux-ci pointeront vers des mémoires tampons différentes après le retour de l’appel **présent** .</span><span class="sxs-lookup"><span data-stu-id="01b54-509">If you are holding any **IDirect3DSurface9** pointers when you call **Present**, they will point to different buffers after the **Present** call returns.</span></span>

<span data-ttu-id="01b54-510">L’option la plus simple consiste à créer un exemple de vidéo pour la chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="01b54-510">The simplest option is to create one video sample for the swap chain.</span></span> <span data-ttu-id="01b54-511">Si vous choisissez cette option, suivez les mêmes étapes que pour le mode fenêtre.</span><span class="sxs-lookup"><span data-stu-id="01b54-511">If you choose this option, follow the same steps given for windowed mode.</span></span> <span data-ttu-id="01b54-512">La seule différence est que la file d’attente de l’exemple contient un seul échantillon vidéo.</span><span class="sxs-lookup"><span data-stu-id="01b54-512">The only difference is that the sample queue contains a single video sample.</span></span> <span data-ttu-id="01b54-513">Une autre option consiste à créer des surfaces hors écran, puis à les confondre avec la mémoire tampon d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="01b54-513">Another option is to create offscreen surfaces and then blit them to the back buffer.</span></span> <span data-ttu-id="01b54-514">Les surfaces que vous créez doivent prendre en charge la méthode [**IDirectXVideoProcessor :: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) , que le mélangeur utilise pour compositiser les frames de sortie.</span><span class="sxs-lookup"><span data-stu-id="01b54-514">The surfaces that you create must support the [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) method, which the mixer uses to composite the output frames.</span></span>

### <a name="tracking-samples"></a><span data-ttu-id="01b54-515">Exemples de suivi</span><span class="sxs-lookup"><span data-stu-id="01b54-515">Tracking Samples</span></span>

<span data-ttu-id="01b54-516">Lorsque le présentateur alloue d’abord les échantillons vidéo, il les place dans une file d’attente.</span><span class="sxs-lookup"><span data-stu-id="01b54-516">When the presenter first allocates the video samples, it places them in a queue.</span></span> <span data-ttu-id="01b54-517">Le présentateur dessine à partir de cette file d’attente chaque fois qu’il doit obtenir un nouveau Frame à partir du mélangeur.</span><span class="sxs-lookup"><span data-stu-id="01b54-517">The presenter draws from this queue whenever it needs to get a new frame from the mixer.</span></span> <span data-ttu-id="01b54-518">Une fois le mixage en sortie, le présentateur déplace l’exemple dans une deuxième file d’attente.</span><span class="sxs-lookup"><span data-stu-id="01b54-518">After the mixer outputs the frame, the presenter moves the sample into a second queue.</span></span> <span data-ttu-id="01b54-519">La deuxième file d’attente est destinée aux exemples qui attendent leurs temps de présentation planifiés.</span><span class="sxs-lookup"><span data-stu-id="01b54-519">The second queue is for samples that are waiting for their scheduled presentation times.</span></span>

<span data-ttu-id="01b54-520">Pour faciliter le suivi de l’état de chaque exemple, l’objet Video Sample implémente l’interface [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) .</span><span class="sxs-lookup"><span data-stu-id="01b54-520">To make it easier to track the status of each sample, the video sample object implements the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) interface.</span></span> <span data-ttu-id="01b54-521">Vous pouvez utiliser cette interface comme suit :</span><span class="sxs-lookup"><span data-stu-id="01b54-521">You can use this interface as follows:</span></span>

1.  <span data-ttu-id="01b54-522">Implémentez l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) dans votre présentateur.</span><span class="sxs-lookup"><span data-stu-id="01b54-522">Implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface in your presenter.</span></span>
2.  <span data-ttu-id="01b54-523">Avant de placer un exemple dans la file d’attente planifiée, interrogez l’exemple d’objet vidéo de l’interface [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) .</span><span class="sxs-lookup"><span data-stu-id="01b54-523">Before you place a sample in the scheduled queue, query the video sample object for the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) interface.</span></span>

3.  <span data-ttu-id="01b54-524">Appelez [**IMFTrackedSample :: SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) avec un pointeur vers votre interface de rappel.</span><span class="sxs-lookup"><span data-stu-id="01b54-524">Call [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) with a pointer to your callback interface.</span></span>
4.  <span data-ttu-id="01b54-525">Lorsque l’exemple est prêt pour la présentation, supprimez-le de la file d’attente planifiée, présentez-le et publiez toutes les références à l’exemple.</span><span class="sxs-lookup"><span data-stu-id="01b54-525">When the sample is ready for presentation, remove it from the scheduled queue, present it, and release all references to the sample.</span></span>
5.  <span data-ttu-id="01b54-526">L’exemple appelle le rappel.</span><span class="sxs-lookup"><span data-stu-id="01b54-526">The sample invokes the callback.</span></span> <span data-ttu-id="01b54-527">(L’exemple d’objet n’est pas supprimé dans ce cas, car il contient un décompte de références sur lui-même jusqu’à ce que le rappel soit appelé.)</span><span class="sxs-lookup"><span data-stu-id="01b54-527">(The sample object is not deleted in this case because it holds a reference count on itself until the callback is invoked.)</span></span>
6.  <span data-ttu-id="01b54-528">Dans le rappel, retournez l’exemple à la file d’attente disponible.</span><span class="sxs-lookup"><span data-stu-id="01b54-528">Inside the callback, return the sample to the available queue.</span></span>

<span data-ttu-id="01b54-529">Il n’est pas nécessaire qu’un présentateur utilise [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) pour suivre les exemples ; vous pouvez implémenter n’importe quelle technique qui fonctionne le mieux pour votre conception.</span><span class="sxs-lookup"><span data-stu-id="01b54-529">A presenter is not required to use [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) to track samples; you can implement any technique that works best for your design.</span></span> <span data-ttu-id="01b54-530">L’un des avantages de **IMFTrackedSample** est que vous pouvez déplacer les fonctions de planification et de rendu du présentateur dans des objets d’assistance, et ces objets n’ont pas besoin d’un mécanisme spécial pour rappeler le présentateur lorsqu’ils déposent des exemples vidéo, car l’exemple d’objet fournit ce mécanisme.</span><span class="sxs-lookup"><span data-stu-id="01b54-530">One advantage of **IMFTrackedSample** is that you can move the presenter's scheduling and rendering functions into helper objects, and these objects do not need any special mechanism for calling back to the presenter when they release video samples because the sample object provides that mechanism.</span></span>

<span data-ttu-id="01b54-531">Le code suivant montre comment définir le rappel :</span><span class="sxs-lookup"><span data-stu-id="01b54-531">The following code shows how to set the callback:</span></span>


```C++
HRESULT EVRCustomPresenter::TrackSample(IMFSample *pSample)
{
    IMFTrackedSample *pTracked = NULL;

    HRESULT hr = pSample->QueryInterface(IID_PPV_ARGS(&pTracked));

    if (SUCCEEDED(hr))
    {
        hr = pTracked->SetAllocator(&m_SampleFreeCB, NULL);
    }

    SafeRelease(&pTracked);
    return hr;
}
```



<span data-ttu-id="01b54-532">Dans le rappel, appelez [**IMFAsyncResult :: GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) sur l’objet de résultat asynchrone pour récupérer un pointeur vers l’exemple :</span><span class="sxs-lookup"><span data-stu-id="01b54-532">In the callback, call [**IMFAsyncResult::GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) on the asynchronous result object to retrieve a pointer to the sample:</span></span>


```C++
HRESULT EVRCustomPresenter::OnSampleFree(IMFAsyncResult *pResult)
{
    IUnknown *pObject = NULL;
    IMFSample *pSample = NULL;
    IUnknown *pUnk = NULL;

    // Get the sample from the async result object.
    HRESULT hr = pResult->GetObject(&pObject);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pObject->QueryInterface(IID_PPV_ARGS(&pSample));
    if (FAILED(hr))
    {
        goto done;
    }

    // If this sample was submitted for a frame-step, the frame step operation
    // is complete.

    if (m_FrameStep.state == FRAMESTEP_SCHEDULED)
    {
        // Query the sample for IUnknown and compare it to our cached value.
        hr = pSample->QueryInterface(IID_PPV_ARGS(&pUnk));
        if (FAILED(hr))
        {
            goto done;
        }

        if (m_FrameStep.pSampleNoRef == (DWORD_PTR)pUnk)
        {
            // Notify the EVR.
            hr = CompleteFrameStep(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Note: Although pObject is also an IUnknown pointer, it is not
        // guaranteed to be the exact pointer value returned through
        // QueryInterface. Therefore, the second QueryInterface call is
        // required.
    }

    /*** Begin lock **_/

    EnterCriticalSection(&m_ObjectLock);

    UINT32 token = MFGetAttributeUINT32(
        pSample, MFSamplePresenter_SampleCounter, (UINT32)-1);

    if (token == m_TokenCounter)
    {
        // Return the sample to the sample pool.
        hr = m_SamplePool.ReturnSample(pSample);
        if (SUCCEEDED(hr))
        {
            // A free sample is available. Process more data if possible.
            (void)ProcessOutputLoop();
        }
    }

    LeaveCriticalSection(&m_ObjectLock);

    /_*_ End lock _*_/

done:
    if (FAILED(hr))
    {
        NotifyEvent(EC_ERRORABORT, hr, 0);
    }
    SafeRelease(&pObject);
    SafeRelease(&pSample);
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="processing-output"></a><span data-ttu-id="01b54-533">Traitement de la sortie</span><span class="sxs-lookup"><span data-stu-id="01b54-533">Processing Output</span></span>

<span data-ttu-id="01b54-534">Chaque fois que la console reçoit un nouvel exemple d’entrée, EVR envoie un message _ *MFVP_MESSAGE_PROCESSINPUTNOTIFY*\* au présenteur.</span><span class="sxs-lookup"><span data-stu-id="01b54-534">Whenever the mixer receives a new input sample, the EVR sends an _ *MFVP_MESSAGE_PROCESSINPUTNOTIFY*\* message to the presenter.</span></span> <span data-ttu-id="01b54-535">Ce message indique que le mélangeur peut avoir une nouvelle image vidéo à remettre.</span><span class="sxs-lookup"><span data-stu-id="01b54-535">This message indicates that the mixer might have a new video frame to deliver.</span></span> <span data-ttu-id="01b54-536">En réponse, le présentateur appelle [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) sur le mélangeur.</span><span class="sxs-lookup"><span data-stu-id="01b54-536">In response, the presenter calls [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="01b54-537">Si la méthode est réussie, le présentateur planifie l’exemple pour la présentation.</span><span class="sxs-lookup"><span data-stu-id="01b54-537">If the method succeeds, the presenter schedules the sample for presentation.</span></span>

<span data-ttu-id="01b54-538">Pour extraire la sortie du mélangeur, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="01b54-538">To get output from the mixer, perform the following steps:</span></span>

1.  <span data-ttu-id="01b54-539">Vérifiez l’état de l’horloge.</span><span class="sxs-lookup"><span data-stu-id="01b54-539">Check the clock state.</span></span> <span data-ttu-id="01b54-540">Si l’horloge est suspendue, ignorez le **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message, sauf s’il s’agit de la première image vidéo.</span><span class="sxs-lookup"><span data-stu-id="01b54-540">If the clock is paused, ignore the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message unless this is the first video frame.</span></span> <span data-ttu-id="01b54-541">Si l’horloge est en cours d’exécution, ou s’il s’agit de la première image vidéo, continuez.</span><span class="sxs-lookup"><span data-stu-id="01b54-541">If the clock is running, or if this is the first video frame, continue.</span></span>
2.  <span data-ttu-id="01b54-542">Obtenir un exemple à partir de la file d’attente des exemples disponibles.</span><span class="sxs-lookup"><span data-stu-id="01b54-542">Get a sample from the queue of available samples.</span></span> <span data-ttu-id="01b54-543">Si la file d’attente est vide, cela signifie que tous les échantillons alloués sont actuellement planifiés pour la présentation.</span><span class="sxs-lookup"><span data-stu-id="01b54-543">If the queue is empty, it means that all allocated samples are currently scheduled for presenting.</span></span> <span data-ttu-id="01b54-544">Dans ce cas, ignorez le message **MFVP_MESSAGE_PROCESSINPUTNOTIFY** pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="01b54-544">In that case, ignore the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message at this time.</span></span> <span data-ttu-id="01b54-545">Lorsque l’exemple suivant devient disponible, répétez les étapes répertoriées ici.</span><span class="sxs-lookup"><span data-stu-id="01b54-545">When the next sample becomes available, repeat the steps listed here.</span></span>
3.  <span data-ttu-id="01b54-546">(Facultatif.) Si l’horloge est disponible, obtient l’heure actuelle de l’horloge (*T1*) en appelant [**IMFClock :: GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span><span class="sxs-lookup"><span data-stu-id="01b54-546">(Optional.) If the clock is available, get the current clock time (*T1*) by calling [**IMFClock::GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span></span>
4.  <span data-ttu-id="01b54-547">Appelez [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) sur le mixer.</span><span class="sxs-lookup"><span data-stu-id="01b54-547">Call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="01b54-548">Si **ProcessOutput** fonctionne, l’exemple contient une image vidéo.</span><span class="sxs-lookup"><span data-stu-id="01b54-548">If **ProcessOutput** succeeds, the sample contains a video frame.</span></span> <span data-ttu-id="01b54-549">Si la méthode échoue, vérifiez le code de retour.</span><span class="sxs-lookup"><span data-stu-id="01b54-549">If the method fails, check the return code.</span></span> <span data-ttu-id="01b54-550">Les codes d’erreur suivants de **ProcessOutput** ne sont pas des échecs critiques :</span><span class="sxs-lookup"><span data-stu-id="01b54-550">The following error codes from **ProcessOutput** are not critical failures:</span></span>

    

    | <span data-ttu-id="01b54-551">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="01b54-551">Error code</span></span>                              | <span data-ttu-id="01b54-552">Description</span><span class="sxs-lookup"><span data-stu-id="01b54-552">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
    |-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="01b54-553">**MF_E_TRANSFORM_NEED_MORE_INPUT**</span><span class="sxs-lookup"><span data-stu-id="01b54-553">**MF_E_TRANSFORM_NEED_MORE_INPUT**</span></span> | <span data-ttu-id="01b54-554">Le mélangeur a besoin d’une plus grande entrée avant de produire une nouvelle trame de sortie.</span><span class="sxs-lookup"><span data-stu-id="01b54-554">The mixer needs more input before it can produce a new output frame.</span></span><br/> <span data-ttu-id="01b54-555">Si vous obtenez ce code d’erreur, vérifiez si le EVR a atteint la fin du flux et répond en conséquence, comme décrit dans [fin de flux](#end-of-stream).</span><span class="sxs-lookup"><span data-stu-id="01b54-555">If you get this error code, check whether the EVR has reached the end of the stream and respond accordingly, as described in [End of Stream](#end-of-stream).</span></span> <span data-ttu-id="01b54-556">Sinon, ignorez ce **MF_E_TRANSFORM_NEED_MORE_INPUT** message.</span><span class="sxs-lookup"><span data-stu-id="01b54-556">Otherwise, ignore this **MF_E_TRANSFORM_NEED_MORE_INPUT** message.</span></span> <span data-ttu-id="01b54-557">Le EVR envoie un autre lorsque le mélangeur obtient davantage d’entrées.</span><span class="sxs-lookup"><span data-stu-id="01b54-557">The EVR will send another one when the mixer gets more input.</span></span><br/> |
    | <span data-ttu-id="01b54-558">**MF_E_TRANSFORM_STREAM_CHANGE**</span><span class="sxs-lookup"><span data-stu-id="01b54-558">**MF_E_TRANSFORM_STREAM_CHANGE**</span></span>    | <span data-ttu-id="01b54-559">Le type de sortie du mélangeur est devenu non valide, peut-être en raison d’un changement de format en amont.</span><span class="sxs-lookup"><span data-stu-id="01b54-559">The mixer's output type has become invalid, possibly due to a format change upstream.</span></span><br/> <span data-ttu-id="01b54-560">Si vous recevez ce code d’erreur, attribuez la valeur **null** au type de média du présentateur.</span><span class="sxs-lookup"><span data-stu-id="01b54-560">If you get this error code, set the presenter's media type to **NULL**.</span></span> <span data-ttu-id="01b54-561">EVR demande un nouveau format.</span><span class="sxs-lookup"><span data-stu-id="01b54-561">The EVR will request a new format.</span></span><br/>                                                                                                                                                                         |
    | <span data-ttu-id="01b54-562">**MF_E_TRANSFORM_TYPE_NOT_SET**</span><span class="sxs-lookup"><span data-stu-id="01b54-562">**MF_E_TRANSFORM_TYPE_NOT_SET**</span></span>    | <span data-ttu-id="01b54-563">Le mélangeur requiert un nouveau type de média.</span><span class="sxs-lookup"><span data-stu-id="01b54-563">The mixer requires a new media type.</span></span><br/> <span data-ttu-id="01b54-564">Si vous recevez ce code d’erreur, renégociez le type de sortie du mélangeur comme décrit dans [négociation des formats](#negotiating-formats).</span><span class="sxs-lookup"><span data-stu-id="01b54-564">If you get this error code, renegotiate the mixer's output type as described in [Negotiating Formats](#negotiating-formats).</span></span><br/>                                                                                                                                                                                                        |

    

     

    <span data-ttu-id="01b54-565">Si [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) fonctionne, continuez.</span><span class="sxs-lookup"><span data-stu-id="01b54-565">If [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) succeeds, continue.</span></span>

5.  <span data-ttu-id="01b54-566">(Facultatif.) Si l’horloge est disponible, obtient l’heure actuelle de l’horloge (*T2*).</span><span class="sxs-lookup"><span data-stu-id="01b54-566">(Optional.) If the clock is available, get the current clock time (*T2*).</span></span> <span data-ttu-id="01b54-567">La latence introduite par le mélangeur est (*T2*  -  *T1*).</span><span class="sxs-lookup"><span data-stu-id="01b54-567">The amount of latency introduced by the mixer is (*T2* - *T1*).</span></span> <span data-ttu-id="01b54-568">Envoie un événement **EC_PROCESSING_LATENCY** avec cette valeur au EVR.</span><span class="sxs-lookup"><span data-stu-id="01b54-568">Send an **EC_PROCESSING_LATENCY** event with this value to the EVR.</span></span> <span data-ttu-id="01b54-569">EVR utilise cette valeur pour le contrôle de la qualité.</span><span class="sxs-lookup"><span data-stu-id="01b54-569">The EVR uses this value for quality control.</span></span> <span data-ttu-id="01b54-570">Si aucune horloge n’est disponible, il n’y a aucune raison d’envoyer l’événement **EC_PROCESSING_LATENCY** .</span><span class="sxs-lookup"><span data-stu-id="01b54-570">If no clock is available, there is no reason to send the **EC_PROCESSING_LATENCY** event.</span></span>
6.  <span data-ttu-id="01b54-571">(Facultatif.) Interrogez l’exemple pour [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) et appelez [**IMFTrackedSample :: SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) comme décrit dans exemples de [suivi](#tracking-samples).</span><span class="sxs-lookup"><span data-stu-id="01b54-571">(Optional.) Query the sample for [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) and call [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) as described in [Tracking Samples](#tracking-samples).</span></span>
7.  <span data-ttu-id="01b54-572">Planifiez l’exemple pour la présentation.</span><span class="sxs-lookup"><span data-stu-id="01b54-572">Schedule the sample for presentation.</span></span>

<span data-ttu-id="01b54-573">Cette séquence d’étapes peut se terminer avant que le présentateur ne récupère une sortie à partir du mélangeur.</span><span class="sxs-lookup"><span data-stu-id="01b54-573">This sequence of steps can terminate before the presenter gets any output from the mixer.</span></span> <span data-ttu-id="01b54-574">Pour vous assurer qu’aucune demande n’est supprimée, vous devez répéter les mêmes étapes dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="01b54-574">To ensure that no requests are dropped, you should repeat the same steps when the following occur:</span></span>

-   <span data-ttu-id="01b54-575">La méthode [**IMFClockStateSink :: OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) ou **IMFClockStateSink :: OnClockStart** du présentateur est appelée.</span><span class="sxs-lookup"><span data-stu-id="01b54-575">The presenter's [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) or **IMFClockStateSink::OnClockStart** method is called.</span></span> <span data-ttu-id="01b54-576">Cela permet de gérer le cas où le mélangeur ignore l’entrée, car l’horloge est suspendue (étape 1).</span><span class="sxs-lookup"><span data-stu-id="01b54-576">This handles the case where the mixer ignores input because the clock is paused (step 1).</span></span>
-   <span data-ttu-id="01b54-577">Le rappel [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) est appelé.</span><span class="sxs-lookup"><span data-stu-id="01b54-577">The [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback is invoked.</span></span> <span data-ttu-id="01b54-578">Cela permet de gérer le cas où le mélangeur reçoit l’entrée, mais tous les exemples vidéo du présentateur sont en cours d’utilisation (étape 2).</span><span class="sxs-lookup"><span data-stu-id="01b54-578">This handles the case where the mixer receives input but all of the presenter's video samples are in use (step 2).</span></span>

<span data-ttu-id="01b54-579">Les exemples de code suivants illustrent ces étapes plus en détail.</span><span class="sxs-lookup"><span data-stu-id="01b54-579">The next several code examples show these steps in more detail.</span></span> <span data-ttu-id="01b54-580">Le présentateur appelle la `ProcessInputNotify` méthode (illustrée dans l’exemple suivant) lorsqu’il obtient le message de **MFVP_MESSAGE_PROCESSINPUTNOTIFY** .</span><span class="sxs-lookup"><span data-stu-id="01b54-580">The presenter calls the `ProcessInputNotify` method (shown in the following example) when it gets the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message.</span></span>


```C++
//-----------------------------------------------------------------------------
// ProcessInputNotify
//
// Attempts to get a new output sample from the mixer.
//
// This method is called when the EVR sends an MFVP_MESSAGE_PROCESSINPUTNOTIFY
// message, which indicates that the mixer has a new input sample.
//
// Note: If there are multiple input streams, the mixer might not deliver an
// output sample for every input sample.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessInputNotify()
{
    HRESULT hr = S_OK;

    // Set the flag that says the mixer has a new sample.
    m_bSampleNotify = TRUE;

    if (m_pMediaType == NULL)
    {
        // We don't have a valid media type yet.
        hr = MF_E_TRANSFORM_TYPE_NOT_SET;
    }
    else
    {
        // Try to process an output sample.
        ProcessOutputLoop();
    }
    return hr;
}
```



<span data-ttu-id="01b54-581">Cette `ProcessInputNotify` méthode définit un indicateur booléen pour enregistrer le fait que le mélangeur a une nouvelle entrée.</span><span class="sxs-lookup"><span data-stu-id="01b54-581">This `ProcessInputNotify` method sets a Boolean flag to record the fact that the mixer has new input.</span></span> <span data-ttu-id="01b54-582">Elle appelle ensuite la `ProcessOutputLoop` méthode, illustrée dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="01b54-582">Then it calls the `ProcessOutputLoop` method, shown in the next example.</span></span> <span data-ttu-id="01b54-583">Cette méthode tente d’extraire autant d’échantillons que possible du mélangeur :</span><span class="sxs-lookup"><span data-stu-id="01b54-583">This method attempts to pull as many samples as possible from the mixer:</span></span>


```C++
void EVRCustomPresenter::ProcessOutputLoop()
{
    HRESULT hr = S_OK;

    // Process as many samples as possible.
    while (hr == S_OK)
    {
        // If the mixer doesn't have a new input sample, break from the loop.
        if (!m_bSampleNotify)
        {
            hr = MF_E_TRANSFORM_NEED_MORE_INPUT;
            break;
        }

        // Try to process a sample.
        hr = ProcessOutput();

        // NOTE: ProcessOutput can return S_FALSE to indicate it did not
        // process a sample. If so, break out of the loop.
    }

    if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
    {
        // The mixer has run out of input data. Check for end-of-stream.
        CheckEndOfStream();
    }
}
```



<span data-ttu-id="01b54-584">La `ProcessOutput` méthode, illustrée dans l’exemple suivant, tente d’obtenir une image vidéo unique à partir du mixer.</span><span class="sxs-lookup"><span data-stu-id="01b54-584">The `ProcessOutput` method, shown in the next example, attempts to get a single video frame from the mixer.</span></span> <span data-ttu-id="01b54-585">Si aucune image vidéo n’est disponible, `ProcessSample` retourne S_FALSE ou un code d’erreur, l’un des deux qui interrompt la boucle dans `ProcessOutputLoop` .</span><span class="sxs-lookup"><span data-stu-id="01b54-585">If no video frame is available, `ProcessSample` returns S_FALSE or an error code, either of which interrupts the loop in `ProcessOutputLoop`.</span></span> <span data-ttu-id="01b54-586">La majeure partie du travail est effectuée à l’intérieur de la `ProcessOutput` méthode :</span><span class="sxs-lookup"><span data-stu-id="01b54-586">Most of the work is done inside the `ProcessOutput` method:</span></span>


```C++
//-----------------------------------------------------------------------------
// ProcessOutput
//
// Attempts to get a new output sample from the mixer.
//
// Called in two situations:
// (1) ProcessOutputLoop, if the mixer has a new input sample.
// (2) Repainting the last frame.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessOutput()
{
    assert(m_bSampleNotify || m_bRepaint);  // See note above.

    HRESULT     hr = S_OK;
    DWORD       dwStatus = 0;
    LONGLONG    mixerStartTime = 0, mixerEndTime = 0;
    MFTIME      systemTime = 0;
    BOOL        bRepaint = m_bRepaint; // Temporarily store this state flag.

    MFT_OUTPUT_DATA_BUFFER dataBuffer;
    ZeroMemory(&dataBuffer, sizeof(dataBuffer));

    IMFSample *pSample = NULL;

    // If the clock is not running, we present the first sample,
    // and then don't present any more until the clock starts.

    if ((m_RenderState != RENDER_STATE_STARTED) &&  // Not running.
         !m_bRepaint &&             // Not a repaint request.
         m_bPrerolled               // At least one sample has been presented.
         )
    {
        return S_FALSE;
    }

    // Make sure we have a pointer to the mixer.
    if (m_pMixer == NULL)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Try to get a free sample from the video sample pool.
    hr = m_SamplePool.GetSample(&pSample);
    if (hr == MF_E_SAMPLEALLOCATOR_EMPTY)
    {
        // No free samples. Try again when a sample is released.
        return S_FALSE;
    }
    else if (FAILED(hr))
    {
        return hr;
    }

    // From now on, we have a valid video sample pointer, where the mixer will
    // write the video data.
    assert(pSample != NULL);

    // (If the following assertion fires, it means we are not managing the sample pool correctly.)
    assert(MFGetAttributeUINT32(pSample, MFSamplePresenter_SampleCounter, (UINT32)-1) == m_TokenCounter);

    if (m_bRepaint)
    {
        // Repaint request. Ask the mixer for the most recent sample.
        SetDesiredSampleTime(
            pSample,
            m_scheduler.LastSampleTime(),
            m_scheduler.FrameDuration()
            );

        m_bRepaint = FALSE; // OK to clear this flag now.
    }
    else
    {
        // Not a repaint request. Clear the desired sample time; the mixer will
        // give us the next frame in the stream.
        ClearDesiredSampleTime(pSample);

        if (m_pClock)
        {
            // Latency: Record the starting time for ProcessOutput.
            (void)m_pClock->GetCorrelatedTime(0, &mixerStartTime, &systemTime);
        }
    }

    // Now we are ready to get an output sample from the mixer.
    dataBuffer.dwStreamID = 0;
    dataBuffer.pSample = pSample;
    dataBuffer.dwStatus = 0;

    hr = m_pMixer->ProcessOutput(0, 1, &dataBuffer, &dwStatus);

    if (FAILED(hr))
    {
        // Return the sample to the pool.
        HRESULT hr2 = m_SamplePool.ReturnSample(pSample);
        if (FAILED(hr2))
        {
            hr = hr2;
            goto done;
        }
        // Handle some known error codes from ProcessOutput.
        if (hr == MF_E_TRANSFORM_TYPE_NOT_SET)
        {
            // The mixer's format is not set. Negotiate a new format.
            hr = RenegotiateMediaType();
        }
        else if (hr == MF_E_TRANSFORM_STREAM_CHANGE)
        {
            // There was a dynamic media type change. Clear our media type.
            SetMediaType(NULL);
        }
        else if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
        {
            // The mixer needs more input.
            // We have to wait for the mixer to get more input.
            m_bSampleNotify = FALSE;
        }
    }
    else
    {
        // We got an output sample from the mixer.

        if (m_pClock && !bRepaint)
        {
            // Latency: Record the ending time for the ProcessOutput operation,
            // and notify the EVR of the latency.

            (void)m_pClock->GetCorrelatedTime(0, &mixerEndTime, &systemTime);

            LONGLONG latencyTime = mixerEndTime - mixerStartTime;
            NotifyEvent(EC_PROCESSING_LATENCY, (LONG_PTR)&latencyTime, 0);
        }

        // Set up notification for when the sample is released.
        hr = TrackSample(pSample);
        if (FAILED(hr))
        {
            goto done;
        }

        // Schedule the sample.
        if ((m_FrameStep.state == FRAMESTEP_NONE) || bRepaint)
        {
            hr = DeliverSample(pSample, bRepaint);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else
        {
            // We are frame-stepping (and this is not a repaint request).
            hr = DeliverFrameStepSample(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        m_bPrerolled = TRUE; // We have presented at least one sample now.
    }

done:
    SafeRelease(&pSample);

    // Important: Release any events returned from the ProcessOutput method.
    SafeRelease(&dataBuffer.pEvents);
    return hr;
}
```



<span data-ttu-id="01b54-587">Voici quelques remarques sur cet exemple :</span><span class="sxs-lookup"><span data-stu-id="01b54-587">Some remarks about this example:</span></span>

-   <span data-ttu-id="01b54-588">La variable *m_SamplePool* est supposée être un objet de collection qui contient la file d’attente des exemples vidéo disponibles.</span><span class="sxs-lookup"><span data-stu-id="01b54-588">The *m_SamplePool* variable is assumed to be a collection object that holds the queue of available video samples.</span></span> <span data-ttu-id="01b54-589">La méthode de l’objet `GetSample` retourne **MF_E_SAMPLEALLOCATOR_EMPTY** si la file d’attente est vide.</span><span class="sxs-lookup"><span data-stu-id="01b54-589">The object's `GetSample` method returns **MF_E_SAMPLEALLOCATOR_EMPTY** if the queue is empty.</span></span>
-   <span data-ttu-id="01b54-590">Si la méthode [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) du mixer retourne MF_E_TRANSFORM_NEED_MORE_INPUT, cela signifie que le mélangeur ne peut pas produire plus de sortie, de sorte que le présenteur efface l’indicateur *m_fSampleNotify* .</span><span class="sxs-lookup"><span data-stu-id="01b54-590">If the mixer's [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method returns MF_E_TRANSFORM_NEED_MORE_INPUT, it means the mixer cannot produce any more output, so the presenter clears the *m_fSampleNotify* flag.</span></span>
-   <span data-ttu-id="01b54-591">La `TrackSample` méthode, qui définit le rappel [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) , est présentée dans la section [exemples de suivi](#tracking-samples).</span><span class="sxs-lookup"><span data-stu-id="01b54-591">The `TrackSample` method, which sets the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback, is shown in the section [Tracking Samples](#tracking-samples).</span></span>

### <a name="repainting-frames"></a><span data-ttu-id="01b54-592">Redessiner des frames</span><span class="sxs-lookup"><span data-stu-id="01b54-592">Repainting Frames</span></span>

<span data-ttu-id="01b54-593">Il peut arriver que le présentateur doive redessiner l’image vidéo la plus récente.</span><span class="sxs-lookup"><span data-stu-id="01b54-593">Occasionally the presenter might need to repaint the most recent video frame.</span></span> <span data-ttu-id="01b54-594">Par exemple, le présentateur standard repeint le frame dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="01b54-594">For example, the standard presenter repaints the frame in the following situations:</span></span>

-   <span data-ttu-id="01b54-595">En mode fenêtre, en réponse à **WM_PAINT** messages reçus par la fenêtre de l’application.</span><span class="sxs-lookup"><span data-stu-id="01b54-595">In windowed mode, in response to **WM_PAINT** messages received by the application's window.</span></span> <span data-ttu-id="01b54-596">Consultez [**IMFVideoDisplayControl :: RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="01b54-596">See [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span></span>
-   <span data-ttu-id="01b54-597">Si le rectangle de destination change quand l’application appelle [**IMFVideoDisplayControl :: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="01b54-597">If the destination rectangle changes when the application calls [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>

<span data-ttu-id="01b54-598">Utilisez les étapes suivantes pour demander au mélangeur de recréer la trame la plus récente :</span><span class="sxs-lookup"><span data-stu-id="01b54-598">Use the following steps to request the mixer to re-create the most recent frame:</span></span>

1.  <span data-ttu-id="01b54-599">Obtient un échantillon vidéo de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="01b54-599">Get a video sample from the queue.</span></span>
2.  <span data-ttu-id="01b54-600">Interrogez l’exemple de l’interface [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample) .</span><span class="sxs-lookup"><span data-stu-id="01b54-600">Query the sample for the [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample) interface.</span></span>
3.  <span data-ttu-id="01b54-601">Appelez [**IMFDesiredSample :: SetDesiredSampleTimeAndDuration**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration).</span><span class="sxs-lookup"><span data-stu-id="01b54-601">Call [**IMFDesiredSample::SetDesiredSampleTimeAndDuration**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration).</span></span> <span data-ttu-id="01b54-602">Spécifiez l’horodatage de la trame vidéo la plus récente.</span><span class="sxs-lookup"><span data-stu-id="01b54-602">Specify the time stamp of the most recent video frame.</span></span> <span data-ttu-id="01b54-603">(Vous devrez mettre en cache cette valeur et la mettre à jour pour chaque frame.)</span><span class="sxs-lookup"><span data-stu-id="01b54-603">(You will need to cache this value and update it for each frame.)</span></span>
4.  <span data-ttu-id="01b54-604">Appelez [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) sur le mixer.</span><span class="sxs-lookup"><span data-stu-id="01b54-604">Call [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span>

<span data-ttu-id="01b54-605">Quand vous repeignez un frame, vous pouvez ignorer l’horloge de présentation et présenter immédiatement le cadre.</span><span class="sxs-lookup"><span data-stu-id="01b54-605">When repainting a frame, you can ignore the presentation clock and present the frame immediately.</span></span>

### <a name="scheduling-samples"></a><span data-ttu-id="01b54-606">Exemples de planification</span><span class="sxs-lookup"><span data-stu-id="01b54-606">Scheduling Samples</span></span>

<span data-ttu-id="01b54-607">Les trames vidéo peuvent atteindre le EVR à tout moment.</span><span class="sxs-lookup"><span data-stu-id="01b54-607">Video frames can reach the EVR at any time.</span></span> <span data-ttu-id="01b54-608">Le présentateur est responsable de la présentation de chaque frame à l’heure correcte, en fonction de l’horodatage du frame.</span><span class="sxs-lookup"><span data-stu-id="01b54-608">The presenter is responsible for presenting each frame at the correct time, based on the time stamp of the frame.</span></span> <span data-ttu-id="01b54-609">Lorsque le présenteur obtient un nouvel exemple à partir du mélangeur, il place l’exemple dans la file d’attente planifiée.</span><span class="sxs-lookup"><span data-stu-id="01b54-609">When the presenter gets a new sample from the mixer, it puts the sample on the scheduled queue.</span></span> <span data-ttu-id="01b54-610">Sur un thread distinct, le présentateur obtient continuellement le premier échantillon du début de la file d’attente et détermine s’il faut :</span><span class="sxs-lookup"><span data-stu-id="01b54-610">On a separate thread, the presenter continually gets the first sample from the head of the queue and determines whether to:</span></span>

-   <span data-ttu-id="01b54-611">Présentez l’exemple.</span><span class="sxs-lookup"><span data-stu-id="01b54-611">Present the sample.</span></span>
-   <span data-ttu-id="01b54-612">Conservez l’exemple dans la file d’attente, car il est précoce.</span><span class="sxs-lookup"><span data-stu-id="01b54-612">Keep the sample on the queue because it is early.</span></span>
-   <span data-ttu-id="01b54-613">Ignorez l’exemple, car il est tardif.</span><span class="sxs-lookup"><span data-stu-id="01b54-613">Discard the sample because it is late.</span></span> <span data-ttu-id="01b54-614">Bien que vous deviez éviter de supprimer des frames si possible, vous devrez peut-être le faire si le présentateur est continuellement en retard.</span><span class="sxs-lookup"><span data-stu-id="01b54-614">Although you should avoid dropping frames if possible, you might need to if the presenter is continually falling behind.</span></span>

<span data-ttu-id="01b54-615">Pour obtenir l’horodatage d’une image vidéo, appelez [**IMFSample :: GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) sur l’exemple vidéo.</span><span class="sxs-lookup"><span data-stu-id="01b54-615">To get the time stamp for a video frame, call [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) on the video sample.</span></span> <span data-ttu-id="01b54-616">L’horodatage est relatif à l’horloge de présentation de EVR.</span><span class="sxs-lookup"><span data-stu-id="01b54-616">The time stamp is relative to the EVR's presentation clock.</span></span> <span data-ttu-id="01b54-617">Pour connaître l’heure actuelle de l’horloge, appelez [**IMFClock :: GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span><span class="sxs-lookup"><span data-stu-id="01b54-617">To get the current clock time, call [**IMFClock::GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span></span> <span data-ttu-id="01b54-618">Si le EVR n’a pas d’horloge de présentation, ou si un exemple n’a pas d’horodatage, vous pouvez présenter l’exemple immédiatement après l’avoir obtenu.</span><span class="sxs-lookup"><span data-stu-id="01b54-618">If the EVR does not have a presentation clock, or if a sample does not have a time stamp, you can present the sample immediately after you get it.</span></span>

<span data-ttu-id="01b54-619">Pour connaître la durée de chaque exemple, appelez [**IMFSample :: GetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration).</span><span class="sxs-lookup"><span data-stu-id="01b54-619">To get the duration of each sample, call [**IMFSample::GetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration).</span></span> <span data-ttu-id="01b54-620">Si l’exemple n’a pas de durée, vous pouvez utiliser la fonction [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) pour calculer la durée à partir de la fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="01b54-620">If the sample does not have a duration, you can use the [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) function to calculate the duration from the frame rate.</span></span>

<span data-ttu-id="01b54-621">Lorsque vous planifiez des exemples, gardez à l’esprit les points suivants :</span><span class="sxs-lookup"><span data-stu-id="01b54-621">When you schedule samples, keep in mind the following:</span></span>

-   <span data-ttu-id="01b54-622">Si la vitesse de lecture est plus rapide ou plus lente que la vitesse normale, l’horloge s’exécute à une vitesse plus rapide ou plus lente.</span><span class="sxs-lookup"><span data-stu-id="01b54-622">If the playback rate is faster or slower than normal speed, the clock runs at a faster or slower rate.</span></span> <span data-ttu-id="01b54-623">Cela signifie que l’horodatage d’un échantillon donne toujours l’heure cible correcte relative à l’horloge de la présentation.</span><span class="sxs-lookup"><span data-stu-id="01b54-623">That means the time stamp on a sample always gives the correct target time relative to the presentation clock.</span></span> <span data-ttu-id="01b54-624">Toutefois, si vous traduisez les temps de présentation dans une autre période (par exemple, le compteur de performances haute résolution), vous devez mettre à l’échelle les heures en fonction de la fréquence d’horloge.</span><span class="sxs-lookup"><span data-stu-id="01b54-624">However, if you translate presentation times into some other clock time (for example, the high-resolution performace counter), then you must scale the times based on the clock speed.</span></span> <span data-ttu-id="01b54-625">Si la vitesse de l’horloge change, EVR appelle la méthode [**IMFClockStateSink :: OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) du présentateur.</span><span class="sxs-lookup"><span data-stu-id="01b54-625">If the clock speed changes, the EVR calls the presenter's [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) method.</span></span>
-   <span data-ttu-id="01b54-626">La vitesse de lecture peut être négative pour la lecture inversée.</span><span class="sxs-lookup"><span data-stu-id="01b54-626">The playback rate can be negative for reverse playback.</span></span> <span data-ttu-id="01b54-627">Lorsque la vitesse de lecture est négative, l’horloge de la présentation s’exécute en arrière.</span><span class="sxs-lookup"><span data-stu-id="01b54-627">When the playback rate is negative, the presentation clock runs backward.</span></span> <span data-ttu-id="01b54-628">En d’autres termes, l’heure *n* + 1 se produit avant l’heure *n*.</span><span class="sxs-lookup"><span data-stu-id="01b54-628">In other words, time *N* + 1 occurs before time *N*.</span></span>

<span data-ttu-id="01b54-629">L’exemple suivant calcule le début ou la fin d’un exemple, par rapport à l’horloge de présentation :</span><span class="sxs-lookup"><span data-stu-id="01b54-629">The following example calculates how early or late a sample is, relative to the presentation clock:</span></span>


```C++
    LONGLONG hnsPresentationTime = 0;
    LONGLONG hnsTimeNow = 0;
    MFTIME   hnsSystemTime = 0;

    BOOL bPresentNow = TRUE;
    LONG lNextSleep = 0;

    if (m_pClock)
    {
        // Get the sample's time stamp. It is valid for a sample to
        // have no time stamp.
        hr = pSample->GetSampleTime(&hnsPresentationTime);

        // Get the clock time. (But if the sample does not have a time stamp,
        // we don't need the clock time.)
        if (SUCCEEDED(hr))
        {
            hr = m_pClock->GetCorrelatedTime(0, &hnsTimeNow, &hnsSystemTime);
        }

        // Calculate the time until the sample's presentation time.
        // A negative value means the sample is late.
        LONGLONG hnsDelta = hnsPresentationTime - hnsTimeNow;
        if (m_fRate < 0)
        {
            // For reverse playback, the clock runs backward. Therefore, the
            // delta is reversed.
            hnsDelta = - hnsDelta;
        }
```



<span data-ttu-id="01b54-630">L’horloge de présentation est généralement pilotée par l’horloge système ou le convertisseur audio.</span><span class="sxs-lookup"><span data-stu-id="01b54-630">The presentation clock is usually driven by the system clock or the audio renderer.</span></span> <span data-ttu-id="01b54-631">(Le convertisseur audio dérive l’heure à partir de la vitesse à laquelle la carte son consomme des données audio.) En général, l’horloge de la présentation n’est pas synchronisée avec la fréquence d’actualisation de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="01b54-631">(The audio renderer derives the time from the rate at which the sound card consumes audio.) In general, the presentation clock is not synchronized with the refresh rate of the monitor.</span></span>

<span data-ttu-id="01b54-632">Si vos paramètres de présentation Direct3D spécifient **D3DPRESENT_INTERVAL_DEFAULT** ou **D3DPRESENT_INTERVAL_ONE** pour l’intervalle de présentation, l’opération **actuelle** attend le retraçage vertical de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="01b54-632">If your Direct3D presentation parameters specify **D3DPRESENT_INTERVAL_DEFAULT** or **D3DPRESENT_INTERVAL_ONE** for the presentation interval, the **Present** operation waits for the monitor's vertical retrace.</span></span> <span data-ttu-id="01b54-633">Il s’agit d’un moyen simple d’éviter les déchirures, mais réduit la précision de votre algorithme de planification.</span><span class="sxs-lookup"><span data-stu-id="01b54-633">This is an easy way to prevent tearing, but reduces the accuracy of your scheduling algorithm.</span></span> <span data-ttu-id="01b54-634">À l’inverse, si l’intervalle de présentation est **D3DPRESENT_INTERVAL_IMMEDIATE**, la méthode **présente** s’exécute immédiatement, ce qui entraîne une suppression, à moins que votre algorithme de planification ne soit suffisamment précis pour que vous appeliez **présent** uniquement pendant la période de retrace verticale.</span><span class="sxs-lookup"><span data-stu-id="01b54-634">Conversely, if the presentation interval is **D3DPRESENT_INTERVAL_IMMEDIATE**, the **Present** method executes immediately, which causes tearing unless your scheduling algorithm is accurate enough that you call **Present** only during the vertical retrace period.</span></span>

<span data-ttu-id="01b54-635">Les fonctions suivantes peuvent vous aider à obtenir des informations de temporisation précises :</span><span class="sxs-lookup"><span data-stu-id="01b54-635">The following functions can help you get accurate timing information:</span></span>

-   <span data-ttu-id="01b54-636">**IDirect3DDevice9 :: GetRasterStatus** retourne des informations sur le raster, y compris la ligne de numérisation actuelle et si le raster est dans la période vide verticale.</span><span class="sxs-lookup"><span data-stu-id="01b54-636">**IDirect3DDevice9::GetRasterStatus** returns information about the raster, including the current scan line and whether the raster is in the vertical blank period.</span></span>
-   <span data-ttu-id="01b54-637">**DwmGetCompositionTimingInfo** retourne les informations de minutage du gestionnaire de fenêtrage.</span><span class="sxs-lookup"><span data-stu-id="01b54-637">**DwmGetCompositionTimingInfo** returns timing information for the desktop window manager.</span></span> <span data-ttu-id="01b54-638">Ces informations sont utiles si la composition du Bureau est activée.</span><span class="sxs-lookup"><span data-stu-id="01b54-638">This information is useful if desktop composition is enabled.</span></span>

### <a name="presenting-samples"></a><span data-ttu-id="01b54-639">Présentation des exemples</span><span class="sxs-lookup"><span data-stu-id="01b54-639">Presenting Samples</span></span>

<span data-ttu-id="01b54-640">Cette section part du principe que vous avez créé une chaîne de permutation distincte pour chaque surface, comme décrit dans [allocation de surfaces Direct3D](#allocating-direct3d-surfaces).</span><span class="sxs-lookup"><span data-stu-id="01b54-640">This section assumes that you created a separate swap chain for each surface as described in [Allocating Direct3D Surfaces](#allocating-direct3d-surfaces).</span></span> <span data-ttu-id="01b54-641">Pour présenter un exemple, récupérez la chaîne de permutation de l’exemple de vidéo comme suit :</span><span class="sxs-lookup"><span data-stu-id="01b54-641">To present a sample, get the swap chain from the video sample as follows:</span></span>

1.  <span data-ttu-id="01b54-642">Appelez [**IMFSample :: GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) sur l’exemple de vidéo pour récupérer la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="01b54-642">Call [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) on the video sample to get the buffer.</span></span>
2.  <span data-ttu-id="01b54-643">Interrogez la mémoire tampon de l’interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="01b54-643">Query the buffer for the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
3.  <span data-ttu-id="01b54-644">Appelez [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) pour accéder à l’interface **IDirect3DSurface9** de la surface Direct3D.</span><span class="sxs-lookup"><span data-stu-id="01b54-644">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get the **IDirect3DSurface9** interface of the Direct3D surface.</span></span> <span data-ttu-id="01b54-645">(Vous pouvez combiner cette étape et l’étape précédente en une en appelant [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).)</span><span class="sxs-lookup"><span data-stu-id="01b54-645">(You can combine this step and the previous step into one by calling [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).)</span></span>
4.  <span data-ttu-id="01b54-646">Appelez **IDirect3DSurface9 :: GetContainer** sur la surface pour obtenir un pointeur vers la chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="01b54-646">Call **IDirect3DSurface9::GetContainer** on the surface to get a pointer to the swap chain.</span></span>
5.  <span data-ttu-id="01b54-647">Appelez **IDirect3DSwapChain9 ::P renvoyée** sur la chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="01b54-647">Call **IDirect3DSwapChain9::Present** on the swap chain.</span></span>

<span data-ttu-id="01b54-648">Le code suivant illustre ces étapes :</span><span class="sxs-lookup"><span data-stu-id="01b54-648">The following code shows these steps:</span></span>


```C++
HRESULT D3DPresentEngine::PresentSample(IMFSample* pSample, LONGLONG llTarget)
{
    HRESULT hr = S_OK;

    IMFMediaBuffer* pBuffer = NULL;
    IDirect3DSurface9* pSurface = NULL;
    IDirect3DSwapChain9* pSwapChain = NULL;

    if (pSample)
    {
        // Get the buffer from the sample.
        hr = pSample->GetBufferByIndex(0, &pBuffer);
        if (FAILED(hr))
        {
            goto done;
        }

        // Get the surface from the buffer.
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(&pSurface));
        if (FAILED(hr))
        {
            goto done;
        }
    }
    else if (m_pSurfaceRepaint)
    {
        // Redraw from the last surface.
        pSurface = m_pSurfaceRepaint;
        pSurface->AddRef();
    }

    if (pSurface)
    {
        // Get the swap chain from the surface.
        hr = pSurface->GetContainer(IID_PPV_ARGS(&pSwapChain));
        if (FAILED(hr))
        {
            goto done;
        }

        // Present the swap chain.
        hr = PresentSwapChain(pSwapChain, pSurface);
        if (FAILED(hr))
        {
            goto done;
        }

        // Store this pointer in case we need to repaint the surface.
        CopyComPointer(m_pSurfaceRepaint, pSurface);
    }
    else
    {
        // No surface. All we can do is paint a black rectangle.
        PaintFrameWithGDI();
    }

done:
    SafeRelease(&pSwapChain);
    SafeRelease(&pSurface);
    SafeRelease(&pBuffer);

    if (FAILED(hr))
    {
        if (hr == D3DERR_DEVICELOST || hr == D3DERR_DEVICENOTRESET || hr == D3DERR_DEVICEHUNG)
        {
            // We failed because the device was lost. Fill the destination rectangle.
            PaintFrameWithGDI();

            // Ignore. We need to reset or re-create the device, but this method
            // is probably being called from the scheduler thread, which is not the
            // same thread that created the device. The Reset(Ex) method must be
            // called from the thread that created the device.

            // The presenter will detect the state when it calls CheckDeviceState()
            // on the next sample.
            hr = S_OK;
        }
    }
    return hr;
}
```



### <a name="source-and-destination-rectangles"></a><span data-ttu-id="01b54-649">Rectangles de source et de destination</span><span class="sxs-lookup"><span data-stu-id="01b54-649">Source and Destination Rectangles</span></span>

<span data-ttu-id="01b54-650">Le *rectangle source* est la partie de l’image vidéo à afficher.</span><span class="sxs-lookup"><span data-stu-id="01b54-650">The *source rectangle* is the portion of the video frame to display.</span></span> <span data-ttu-id="01b54-651">Elle est définie par rapport à un système de coordonnées normalisé, dans lequel la totalité de la trame vidéo occupe un rectangle avec des coordonnées {0, 0, 1, 1}.</span><span class="sxs-lookup"><span data-stu-id="01b54-651">It is defined relative to a normalized coordinate system, in which the entire video frame occupies a rectangle with coordinates {0, 0, 1, 1}.</span></span> <span data-ttu-id="01b54-652">Le *rectangle de destination* est la zone dans la surface de destination dans laquelle la vidéo est dessinée.</span><span class="sxs-lookup"><span data-stu-id="01b54-652">The *destination rectangle* is the area within the destination surface where the video frame is drawn.</span></span> <span data-ttu-id="01b54-653">Le présentateur standard permet à une application de définir ces rectangles en appelant [**IMFVideoDisplayControl :: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="01b54-653">The standard presenter enables an application to set these rectangles by calling [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>

<span data-ttu-id="01b54-654">Il existe plusieurs options pour l’application des rectangles source et de destination.</span><span class="sxs-lookup"><span data-stu-id="01b54-654">There are several options for applying source and destination rectangles.</span></span> <span data-ttu-id="01b54-655">La première option consiste à laisser le mélangeur les appliquer :</span><span class="sxs-lookup"><span data-stu-id="01b54-655">The first option is to let the mixer apply them:</span></span>

-   <span data-ttu-id="01b54-656">Définissez le rectangle source à l’aide de l’attribut [**VIDEO_ZOOM_RECT**](video-zoom-rect-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="01b54-656">Set the source rectangle using the [**VIDEO_ZOOM_RECT**](video-zoom-rect-attribute.md) attribute.</span></span> <span data-ttu-id="01b54-657">Le mélangeur applique le rectangle source lorsqu’il BLITS la vidéo à la surface de destination.</span><span class="sxs-lookup"><span data-stu-id="01b54-657">The mixer will apply the source rectangle when it blits the video to the destination surface.</span></span> <span data-ttu-id="01b54-658">Le rectangle source par défaut du mélangeur est le cadre entier.</span><span class="sxs-lookup"><span data-stu-id="01b54-658">The mixer's default source rectangle is the entire frame.</span></span>
-   <span data-ttu-id="01b54-659">Définissez le rectangle de destination en tant qu’ouverture géométrique dans le type de sortie du mélangeur.</span><span class="sxs-lookup"><span data-stu-id="01b54-659">Set the destination rectangle as the geometric aperture in the mixer's output type.</span></span> <span data-ttu-id="01b54-660">Pour plus d’informations, consultez la page relative à la [négociation des formats](#negotiating-formats).</span><span class="sxs-lookup"><span data-stu-id="01b54-660">For more information, see [Negotiating Formats](#negotiating-formats).</span></span>

<span data-ttu-id="01b54-661">La deuxième option consiste à appliquer les rectangles quand vous **IDirect3DSwapChain9 ::P renvoyé** en spécifiant les paramètres *pSourceRect* et *pDestRect* dans la méthode **présente** .</span><span class="sxs-lookup"><span data-stu-id="01b54-661">The second option is to apply the rectangles when you **IDirect3DSwapChain9::Present** by specifying the *pSourceRect* and *pDestRect* parameters in the **Present** method.</span></span> <span data-ttu-id="01b54-662">Vous pouvez combiner ces options.</span><span class="sxs-lookup"><span data-stu-id="01b54-662">You can combine these options.</span></span> <span data-ttu-id="01b54-663">Par exemple, vous pouvez définir le rectangle source sur le mélangeur, mais appliquer le rectangle de destination dans la méthode **présente** .</span><span class="sxs-lookup"><span data-stu-id="01b54-663">For example, you could set the source rectangle on the mixer but apply the destination rectangle in the **Present** method.</span></span>

<span data-ttu-id="01b54-664">Si l’application modifie le rectangle de destination ou redimensionne la fenêtre, vous devrez peut-être allouer de nouvelles surfaces.</span><span class="sxs-lookup"><span data-stu-id="01b54-664">If the application changes the destination rectangle or resizes the window, you might need to allocate new surfaces.</span></span> <span data-ttu-id="01b54-665">Dans ce cas, vous devez veiller à synchroniser cette opération avec votre thread de planification.</span><span class="sxs-lookup"><span data-stu-id="01b54-665">If so, you must be careful to synchronize this operation with your scheduling thread.</span></span> <span data-ttu-id="01b54-666">Videz la file d’attente de planification et ignorez les anciens exemples avant d’allouer de nouvelles surfaces.</span><span class="sxs-lookup"><span data-stu-id="01b54-666">Flush the scheduling queue and discard the old samples before allocating new surfaces.</span></span>

### <a name="end-of-stream"></a><span data-ttu-id="01b54-667">Fin de flux</span><span class="sxs-lookup"><span data-stu-id="01b54-667">End of Stream</span></span>

<span data-ttu-id="01b54-668">Lorsque chaque flux d’entrée sur le EVR est terminé, EVR envoie un message **MFVP_MESSAGE_ENDOFSTREAM** au présenteur.</span><span class="sxs-lookup"><span data-stu-id="01b54-668">When every input stream on the EVR has ended, the EVR sends an **MFVP_MESSAGE_ENDOFSTREAM** message to the presenter.</span></span> <span data-ttu-id="01b54-669">Toutefois, lorsque vous recevez le message, il se peut qu’il reste quelques images vidéo à traiter.</span><span class="sxs-lookup"><span data-stu-id="01b54-669">At the point when you receive the message, however, there might be a few video frames remaining to be processed.</span></span> <span data-ttu-id="01b54-670">Avant de répondre au message de fin de flux, vous devez décharger toute la sortie du mélangeur et présenter tous les autres frames.</span><span class="sxs-lookup"><span data-stu-id="01b54-670">Before you respond to the end-of-stream message, you must drain all of the output from the mixer and present all of the remaining frames.</span></span> <span data-ttu-id="01b54-671">Une fois la dernière image présentée, envoyez un événement **EC_COMPLETE** à l’EVR.</span><span class="sxs-lookup"><span data-stu-id="01b54-671">After the last frame is presented, send an **EC_COMPLETE** event to the EVR.</span></span>

<span data-ttu-id="01b54-672">L’exemple suivant montre une méthode qui envoie l’événement **EC_COMPLETE** si différentes conditions sont remplies.</span><span class="sxs-lookup"><span data-stu-id="01b54-672">The next example shows a method that sends the **EC_COMPLETE** event if various conditions are met.</span></span> <span data-ttu-id="01b54-673">Sinon, elle retourne S_OK sans envoyer l’événement :</span><span class="sxs-lookup"><span data-stu-id="01b54-673">Otherwise, it returns S_OK without sending the event:</span></span>


```C++
HRESULT EVRCustomPresenter::CheckEndOfStream()
{
    if (!m_bEndStreaming)
    {
        // The EVR did not send the MFVP_MESSAGE_ENDOFSTREAM message.
        return S_OK;
    }

    if (m_bSampleNotify)
    {
        // The mixer still has input.
        return S_OK;
    }

    if (m_SamplePool.AreSamplesPending())
    {
        // Samples are still scheduled for rendering.
        return S_OK;
    }

    // Everything is complete. Now we can tell the EVR that we are done.
    NotifyEvent(EC_COMPLETE, (LONG_PTR)S_OK, 0);
    m_bEndStreaming = FALSE;
    return S_OK;
}
```



<span data-ttu-id="01b54-674">Cette méthode vérifie les États suivants :</span><span class="sxs-lookup"><span data-stu-id="01b54-674">This method checks the following states:</span></span>

-   <span data-ttu-id="01b54-675">Si la variable *m_fSampleNotify* a la **valeur true**, cela signifie que le mélangeur a une ou plusieurs trames qui n’ont pas encore été traitées.</span><span class="sxs-lookup"><span data-stu-id="01b54-675">If the *m_fSampleNotify* variable is **TRUE**, it means the mixer has one or more frames that have not been processed yet.</span></span> <span data-ttu-id="01b54-676">(Pour plus d’informations, consultez traitement de la [sortie](#processing-output).)</span><span class="sxs-lookup"><span data-stu-id="01b54-676">(For details, see [Processing Output](#processing-output).)</span></span>
-   <span data-ttu-id="01b54-677">La variable *m_fEndStreaming* est un indicateur booléen dont la valeur initiale est **false**.</span><span class="sxs-lookup"><span data-stu-id="01b54-677">The *m_fEndStreaming* variable is a Boolean flag whose initial value **FALSE**.</span></span> <span data-ttu-id="01b54-678">Le présentateur affecte la **valeur true** à l’indicateur lorsque EVR envoie le MESSAGE de **MFVP_MESSAGE_ENDOFSTREAM** .</span><span class="sxs-lookup"><span data-stu-id="01b54-678">The presenter sets the flag to **TRUE** when the EVR sends the **MFVP_MESSAGE_ENDOFSTREAM** message.</span></span>
-   <span data-ttu-id="01b54-679">La `AreSamplesPending` méthode est supposée retourner la **valeur true** tant qu’un ou plusieurs frames sont en attente dans la file d’attente planifiée.</span><span class="sxs-lookup"><span data-stu-id="01b54-679">The `AreSamplesPending` method is assumed to return **TRUE** as long as one or more frames are waiting in the scheduled queue.</span></span>

<span data-ttu-id="01b54-680">Dans la méthode [**IMFVideoPresenter ::P rocessmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) , affectez la valeur **true** à *M_FENDSTREAMING* et appelez `CheckEndOfStream` lorsque le EVR envoie le message **MFVP_MESSAGE_ENDOFSTREAM** :</span><span class="sxs-lookup"><span data-stu-id="01b54-680">In the [**IMFVideoPresenter::ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) method, set *m_fEndStreaming* to **TRUE** and call `CheckEndOfStream` when the EVR sends the **MFVP_MESSAGE_ENDOFSTREAM** message:</span></span>


```C++
HRESULT EVRCustomPresenter::ProcessMessage(
    MFVP_MESSAGE_TYPE eMessage,
    ULONG_PTR ulParam
    )
{
    HRESULT hr = S_OK;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    switch (eMessage)
    {
    // Flush all pending samples.
    case MFVP_MESSAGE_FLUSH:
        hr = Flush();
        break;

    // Renegotiate the media type with the mixer.
    case MFVP_MESSAGE_INVALIDATEMEDIATYPE:
        hr = RenegotiateMediaType();
        break;

    // The mixer received a new input sample.
    case MFVP_MESSAGE_PROCESSINPUTNOTIFY:
        hr = ProcessInputNotify();
        break;

    // Streaming is about to start.
    case MFVP_MESSAGE_BEGINSTREAMING:
        hr = BeginStreaming();
        break;

    // Streaming has ended. (The EVR has stopped.)
    case MFVP_MESSAGE_ENDSTREAMING:
        hr = EndStreaming();
        break;

    // All input streams have ended.
    case MFVP_MESSAGE_ENDOFSTREAM:
        // Set the EOS flag.
        m_bEndStreaming = TRUE;
        // Check if it's time to send the EC_COMPLETE event to the EVR.
        hr = CheckEndOfStream();
        break;

    // Frame-stepping is starting.
    case MFVP_MESSAGE_STEP:
        hr = PrepareFrameStep(LODWORD(ulParam));
        break;

    // Cancels frame-stepping.
    case MFVP_MESSAGE_CANCELSTEP:
        hr = CancelFrameStep();
        break;

    default:
        hr = E_INVALIDARG; // Unknown message. This case should never occur.
        break;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



<span data-ttu-id="01b54-681">En outre, appelez `CheckEndOfStream` si la méthode [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) du mixer retourne **MF_E_TRANSFORM_NEED_MORE_INPUT**.</span><span class="sxs-lookup"><span data-stu-id="01b54-681">In addition, call `CheckEndOfStream` if the mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method returns **MF_E_TRANSFORM_NEED_MORE_INPUT**.</span></span> <span data-ttu-id="01b54-682">Ce code d’erreur indique que le mélangeur n’a plus d’exemples d’entrée (voir [traitement de sortie](#processing-output)).</span><span class="sxs-lookup"><span data-stu-id="01b54-682">This error code indicates that the mixer has no more input samples (see [Processing Output](#processing-output)).</span></span>

## <a name="frame-stepping"></a><span data-ttu-id="01b54-683">Pas à pas</span><span class="sxs-lookup"><span data-stu-id="01b54-683">Frame Stepping</span></span>

<span data-ttu-id="01b54-684">Le EVR est conçu pour prendre en charge le pas à pas détaillé dans DirectShow et le nettoyage dans Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="01b54-684">The EVR is designed to support frame stepping in DirectShow and scrubbing in Media Foundation.</span></span> <span data-ttu-id="01b54-685">L’exécution pas à pas et le nettoyage des images sont similaires d’un plan conceptuel.</span><span class="sxs-lookup"><span data-stu-id="01b54-685">Frame stepping and scrubbing are conceptually similar.</span></span> <span data-ttu-id="01b54-686">Dans les deux cas, l’application demande une image vidéo à la fois.</span><span class="sxs-lookup"><span data-stu-id="01b54-686">In both cases, the application requests one video frame at a time.</span></span> <span data-ttu-id="01b54-687">En interne, le présenteur utilise le même mécanisme pour implémenter les deux fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="01b54-687">Internally, the presenter uses the same mechanism to implement both features.</span></span>

<span data-ttu-id="01b54-688">Le pas à pas détaillé dans DirectShow fonctionne comme suit :</span><span class="sxs-lookup"><span data-stu-id="01b54-688">Frame stepping in DirectShow works as follows:</span></span>

-   <span data-ttu-id="01b54-689">L’application appelle [**IVideoFrameStep :: Step**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step).</span><span class="sxs-lookup"><span data-stu-id="01b54-689">The application calls [**IVideoFrameStep::Step**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step).</span></span> <span data-ttu-id="01b54-690">Le nombre d’étapes est indiqué dans le paramètre *dwSteps* .</span><span class="sxs-lookup"><span data-stu-id="01b54-690">The number of steps is given in the *dwSteps* parameter.</span></span> <span data-ttu-id="01b54-691">EVR envoie un message **MFVP_MESSAGE_STEP** au présenteur, où le paramètre de message (*ulParam*) est le nombre d’étapes.</span><span class="sxs-lookup"><span data-stu-id="01b54-691">The EVR sends an **MFVP_MESSAGE_STEP** message to the presenter, where the message parameter (*ulParam*) is the number of steps.</span></span>
-   <span data-ttu-id="01b54-692">Si l’application appelle [**IVideoFrameStep :: CancelStep**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) ou modifie l’état du graphique (en cours d’exécution, suspendu ou arrêté), le EVR envoie un MESSAGE de **MFVP_MESSAGE_CANCELSTEP** .</span><span class="sxs-lookup"><span data-stu-id="01b54-692">If the application calls [**IVideoFrameStep::CancelStep**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) or changes the graph state (running, paused, or stopped), the EVR sends an **MFVP_MESSAGE_CANCELSTEP** message.</span></span>

<span data-ttu-id="01b54-693">Le nettoyage dans Media Foundation fonctionne comme suit :</span><span class="sxs-lookup"><span data-stu-id="01b54-693">Scrubbing in Media Foundation works as follows:</span></span>

-   <span data-ttu-id="01b54-694">L’application définit la vitesse de lecture sur zéro en appelant [**IMFRateControl ::**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)se.</span><span class="sxs-lookup"><span data-stu-id="01b54-694">The application sets the playback rate to zero by calling [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).</span></span>
-   <span data-ttu-id="01b54-695">Pour afficher un nouveau Frame, l’application appelle [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) avec la position souhaitée.</span><span class="sxs-lookup"><span data-stu-id="01b54-695">To render a new frame, the application calls [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) with the desired position.</span></span> <span data-ttu-id="01b54-696">EVR envoie un message de **MFVP_MESSAGE_STEP** avec *ulParam* égal à 1.</span><span class="sxs-lookup"><span data-stu-id="01b54-696">The EVR sends an **MFVP_MESSAGE_STEP** message with *ulParam* equal to 1.</span></span>
-   <span data-ttu-id="01b54-697">Pour arrêter le nettoyage, l’application définit la vitesse de lecture sur une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="01b54-697">To stop scrubbing, the application sets the playback rate to a nonzero value.</span></span> <span data-ttu-id="01b54-698">EVR envoie le message **MFVP_MESSAGE_CANCELSTEP** .</span><span class="sxs-lookup"><span data-stu-id="01b54-698">The EVR sends the **MFVP_MESSAGE_CANCELSTEP** message.</span></span>

<span data-ttu-id="01b54-699">Après avoir reçu le message **MFVP_MESSAGE_STEP** , le présentateur attend l’arrivée du frame cible.</span><span class="sxs-lookup"><span data-stu-id="01b54-699">After receiving the **MFVP_MESSAGE_STEP** message, the presenter waits for the target frame to arrive.</span></span> <span data-ttu-id="01b54-700">Si le nombre d’étapes est *N*, le présentateur ignore les exemples (*n* -1) suivants et présente le *N* ième échantillon.</span><span class="sxs-lookup"><span data-stu-id="01b54-700">If the number of steps is *N*, the presenter discards the next (*N* - 1) samples and presents the *N* th sample.</span></span> <span data-ttu-id="01b54-701">Lorsque le présenteur termine l’étape de frame, il envoie un événement [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) à l’EVR avec *LParam1* défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="01b54-701">When the presenter completes the frame step, it sends an [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) event to the EVR with *lParam1* set to **FALSE**.</span></span> <span data-ttu-id="01b54-702">En outre, si la vitesse de lecture est égale à zéro, le présentateur envoie un événement [**EC_SCRUB_TIME**](../directshow/ec-scrub-time.md) .</span><span class="sxs-lookup"><span data-stu-id="01b54-702">In addition, if the playback rate is zero, the presenter sends an [**EC_SCRUB_TIME**](../directshow/ec-scrub-time.md) event.</span></span> <span data-ttu-id="01b54-703">Si le EVR annule le pas à pas de la trame pendant qu’une opération de l’étape de frame est toujours en attente, le présentateur envoie un événement **EC_STEP_COMPLETE** avec *LParam1* défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="01b54-703">If the EVR cancels frame stepping while a frame-step operation is still pending, the presenter sends an **EC_STEP_COMPLETE** event with *lParam1* set to **TRUE**.</span></span>

<span data-ttu-id="01b54-704">L’application peut effectuer un frame ou un nettoyage à plusieurs moments. le présentateur peut donc recevoir plusieurs messages de **MFVP_MESSAGE_STEP** avant d’obtenir un message **MFVP_MESSAGE_CANCELSTEP** .</span><span class="sxs-lookup"><span data-stu-id="01b54-704">The application can frame step or scrub multiple times, so the presenter might receive multiple **MFVP_MESSAGE_STEP** messages before it gets an **MFVP_MESSAGE_CANCELSTEP** message.</span></span> <span data-ttu-id="01b54-705">En outre, le présentateur peut recevoir le message de **MFVP_MESSAGE_STEP** avant le démarrage de l’horloge ou pendant l’exécution de l’horloge.</span><span class="sxs-lookup"><span data-stu-id="01b54-705">Also, the presenter can receive the **MFVP_MESSAGE_STEP** message before the clock starts or while the clock is running.</span></span>

### <a name="implementing-frame-stepping"></a><span data-ttu-id="01b54-706">Implémentation du pas à pas de frame</span><span class="sxs-lookup"><span data-stu-id="01b54-706">Implementing Frame Stepping</span></span>

<span data-ttu-id="01b54-707">Cette section décrit un algorithme permettant d’implémenter l’exécution pas à pas de frame.</span><span class="sxs-lookup"><span data-stu-id="01b54-707">This section describes an algorithm to implement frame stepping.</span></span> <span data-ttu-id="01b54-708">L’algorithme d’exécution pas à pas de Frame utilise les variables suivantes :</span><span class="sxs-lookup"><span data-stu-id="01b54-708">The frame stepping algorithm uses the following variables:</span></span>

-   <span data-ttu-id="01b54-709">*step_count*.</span><span class="sxs-lookup"><span data-stu-id="01b54-709">*step_count*.</span></span> <span data-ttu-id="01b54-710">Entier non signé qui spécifie le nombre d’étapes dans l’opération de pas à pas de l’image en cours.</span><span class="sxs-lookup"><span data-stu-id="01b54-710">An unsigned integer that specifies the number of steps in the current frame stepping operation.</span></span>
-   <span data-ttu-id="01b54-711">*step_queue*.</span><span class="sxs-lookup"><span data-stu-id="01b54-711">*step_queue*.</span></span> <span data-ttu-id="01b54-712">Une file d’attente de pointeurs [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .</span><span class="sxs-lookup"><span data-stu-id="01b54-712">A queue of [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointers.</span></span>
-   <span data-ttu-id="01b54-713">*step_state*.</span><span class="sxs-lookup"><span data-stu-id="01b54-713">*step_state*.</span></span> <span data-ttu-id="01b54-714">À tout moment, le présentateur peut être dans l’un des États suivants en ce qui concerne le pas à pas détaillé de la trame :</span><span class="sxs-lookup"><span data-stu-id="01b54-714">At any time, the presenter can be in one of the following states with respect to frame stepping:</span></span> 

    | <span data-ttu-id="01b54-715">State</span><span class="sxs-lookup"><span data-stu-id="01b54-715">State</span></span>         | <span data-ttu-id="01b54-716">Description</span><span class="sxs-lookup"><span data-stu-id="01b54-716">Description</span></span>                                                                                                                                                                                                     |
    |---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="01b54-717">NOT_STEPPING</span><span class="sxs-lookup"><span data-stu-id="01b54-717">NOT_STEPPING</span></span> | <span data-ttu-id="01b54-718">Pas de cadre pas à pas.</span><span class="sxs-lookup"><span data-stu-id="01b54-718">Not frame stepping.</span></span>                                                                                                                                                                                             |
    | <span data-ttu-id="01b54-719">WAITING</span><span class="sxs-lookup"><span data-stu-id="01b54-719">WAITING</span></span>       | <span data-ttu-id="01b54-720">Le présentateur a reçu le message **MFVP_MESSAGE_STEP** , mais l’horloge n’a pas démarré.</span><span class="sxs-lookup"><span data-stu-id="01b54-720">The presenter has received the **MFVP_MESSAGE_STEP** message, but the clock has not started.</span></span>                                                                                                                  |
    | <span data-ttu-id="01b54-721">PENDING</span><span class="sxs-lookup"><span data-stu-id="01b54-721">PENDING</span></span>       | <span data-ttu-id="01b54-722">Le présentateur a reçu le message **MFVP_MESSAGE_STEP** et l’horloge a démarré, mais le présentateur attend de recevoir le frame cible.</span><span class="sxs-lookup"><span data-stu-id="01b54-722">The presenter has received the **MFVP_MESSAGE_STEP** message and the clock has started, but the presenter is waiting to receive the target frame.</span></span>                                                             |
    | <span data-ttu-id="01b54-723">PLANIFIÉE</span><span class="sxs-lookup"><span data-stu-id="01b54-723">SCHEDULED</span></span>     | <span data-ttu-id="01b54-724">Le présentateur a reçu le frame cible et l’a planifié pour la présentation, mais le cadre n’a pas été présenté.</span><span class="sxs-lookup"><span data-stu-id="01b54-724">The presenter has received the target frame and has scheduled it for presentation, but the frame has not been presented.</span></span>                                                                                        |
    | <span data-ttu-id="01b54-725">Remplissez</span><span class="sxs-lookup"><span data-stu-id="01b54-725">COMPLETE</span></span>      | <span data-ttu-id="01b54-726">Le présentateur a présenté le frame cible et a envoyé l’événement [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) et attend le MESSAGE de **MFVP_MESSAGE_STEP** ou de **MFVP_MESSAGE_CANCELSTEP** suivant.</span><span class="sxs-lookup"><span data-stu-id="01b54-726">The presenter has presented the target frame and sent the [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) event, and is waiting for the next **MFVP_MESSAGE_STEP** or **MFVP_MESSAGE_CANCELSTEP** message.</span></span> |

    

     

    <span data-ttu-id="01b54-727">Ces États sont indépendants des États de présenteur répertoriés dans la section [États du présentateur](#presenter-states).</span><span class="sxs-lookup"><span data-stu-id="01b54-727">These states are independent of the presenter states listed in the section [Presenter States](#presenter-states).</span></span>

<span data-ttu-id="01b54-728">Les procédures suivantes sont définies pour l’algorithme de pas à pas :</span><span class="sxs-lookup"><span data-stu-id="01b54-728">The following procedures are defined for the frame-stepping algorithm:</span></span>

<span data-ttu-id="01b54-729">Procédure PrepareFrameStep</span><span class="sxs-lookup"><span data-stu-id="01b54-729">PrepareFrameStep Procedure</span></span>

1.  <span data-ttu-id="01b54-730">Incrémente *step_count*.</span><span class="sxs-lookup"><span data-stu-id="01b54-730">Increment *step_count*.</span></span>
2.  <span data-ttu-id="01b54-731">Définissez *step_state* sur Waiting.</span><span class="sxs-lookup"><span data-stu-id="01b54-731">Set *step_state* to WAITING.</span></span>
3.  <span data-ttu-id="01b54-732">Si l’horloge est en cours d’exécution, appelez StartFrameStep.</span><span class="sxs-lookup"><span data-stu-id="01b54-732">If the clock is running, call StartFrameStep.</span></span>

<span data-ttu-id="01b54-733">Procédure StartFrameStep</span><span class="sxs-lookup"><span data-stu-id="01b54-733">StartFrameStep Procedure</span></span>

1.  <span data-ttu-id="01b54-734">Si *step_state* est égal à en attente, affectez la valeur en attente à *step_state* .</span><span class="sxs-lookup"><span data-stu-id="01b54-734">If *step_state* equals WAITING, set *step_state* to PENDING.</span></span> <span data-ttu-id="01b54-735">Pour chaque exemple dans *step_queue*, appelez DeliverFrameStepSample.</span><span class="sxs-lookup"><span data-stu-id="01b54-735">For each sample in *step_queue*, call DeliverFrameStepSample.</span></span>
2.  <span data-ttu-id="01b54-736">Si *step_state* est égal à NOT_STEPPING, supprimez les exemples de *step_queue* et planifiez-les pour la présentation.</span><span class="sxs-lookup"><span data-stu-id="01b54-736">If *step_state* equals NOT_STEPPING, remove any samples from *step_queue* and schedule them for presentation.</span></span>

<span data-ttu-id="01b54-737">Procédure CompleteFrameStep</span><span class="sxs-lookup"><span data-stu-id="01b54-737">CompleteFrameStep Procedure</span></span>

1.  <span data-ttu-id="01b54-738">Définissez *step_state* sur terminé.</span><span class="sxs-lookup"><span data-stu-id="01b54-738">Set *step_state* to COMPLETE.</span></span>
2.  <span data-ttu-id="01b54-739">Envoyez l’événement EC_STEP_COMPLETE avec *lParam1*  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="01b54-739">Send the EC_STEP_COMPLETE event with *lParam1* = **FALSE**.</span></span>
3.  <span data-ttu-id="01b54-740">Si la fréquence d’horloge est égale à zéro, envoyez l’événement **EC_SCRUB_TIME** avec l’heure de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="01b54-740">If the clock rate is zero, send the **EC_SCRUB_TIME** event with the sample time.</span></span>

<span data-ttu-id="01b54-741">Procédure DeliverFrameStepSample</span><span class="sxs-lookup"><span data-stu-id="01b54-741">DeliverFrameStepSample Procedure</span></span>

1.  <span data-ttu-id="01b54-742">Si la fréquence d’horloge est égale à zéro et *échantillonner*  +  la *durée* de l’exemple de temps  <  *horloge*, ignorez l’exemple.</span><span class="sxs-lookup"><span data-stu-id="01b54-742">If the clock rate is zero and *sample time* + *sample duration* < *clock time*, discard the sample.</span></span> <span data-ttu-id="01b54-743">Quitter.</span><span class="sxs-lookup"><span data-stu-id="01b54-743">Exit.</span></span>
2.  <span data-ttu-id="01b54-744">Si *step_state* est égal à planifié ou terminé, ajoutez l’exemple à *step_queue*.</span><span class="sxs-lookup"><span data-stu-id="01b54-744">If *step_state* equals SCHEDULED or COMPLETE, add the sample to *step_queue*.</span></span> <span data-ttu-id="01b54-745">Quitter.</span><span class="sxs-lookup"><span data-stu-id="01b54-745">Exit.</span></span>
3.  <span data-ttu-id="01b54-746">Décrémenter *step_count*.</span><span class="sxs-lookup"><span data-stu-id="01b54-746">Decrement *step_count*.</span></span>
4.  <span data-ttu-id="01b54-747">Si *step_count* > 0, ignorez l’exemple.</span><span class="sxs-lookup"><span data-stu-id="01b54-747">If *step_count* > 0, discard the sample.</span></span> <span data-ttu-id="01b54-748">Quitter.</span><span class="sxs-lookup"><span data-stu-id="01b54-748">Exit.</span></span>
5.  <span data-ttu-id="01b54-749">Si *step_state* est égal à Waiting, ajoutez l’exemple à *step_queue*.</span><span class="sxs-lookup"><span data-stu-id="01b54-749">If *step_state* equals WAITING, add the sample to *step_queue*.</span></span> <span data-ttu-id="01b54-750">Quitter.</span><span class="sxs-lookup"><span data-stu-id="01b54-750">Exit.</span></span>
6.  <span data-ttu-id="01b54-751">Planifiez l’exemple pour la présentation.</span><span class="sxs-lookup"><span data-stu-id="01b54-751">Schedule the sample for presentation.</span></span>
7.  <span data-ttu-id="01b54-752">Définissez *step_state* sur planifié.</span><span class="sxs-lookup"><span data-stu-id="01b54-752">Set *step_state* to SCHEDULED.</span></span>

<span data-ttu-id="01b54-753">Procédure CancelFrameStep</span><span class="sxs-lookup"><span data-stu-id="01b54-753">CancelFrameStep Procedure</span></span>

1.  <span data-ttu-id="01b54-754">Définissez *step_state* sur NOT_STEPPING</span><span class="sxs-lookup"><span data-stu-id="01b54-754">Set *step_state* to NOT_STEPPING</span></span>
2.  <span data-ttu-id="01b54-755">Réinitialisez *step_count* à zéro.</span><span class="sxs-lookup"><span data-stu-id="01b54-755">Reset *step_count* to zero.</span></span>
3.  <span data-ttu-id="01b54-756">Si la valeur précédente de *step_state* était en attente, en attente ou planifiée, envoyez EC_STEP_COMPLETE avec *lParam1*  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="01b54-756">If the previous value of *step_state* was WAITING, PENDING, or SCHEDULED, send EC_STEP_COMPLETE with *lParam1* = **TRUE**.</span></span>

<span data-ttu-id="01b54-757">Appelez ces procédures comme suit :</span><span class="sxs-lookup"><span data-stu-id="01b54-757">Call these procedures as follows:</span></span>



| <span data-ttu-id="01b54-758">Message ou méthode presenter</span><span class="sxs-lookup"><span data-stu-id="01b54-758">Presenter message or method</span></span>                                                   | <span data-ttu-id="01b54-759">Procédure</span><span class="sxs-lookup"><span data-stu-id="01b54-759">Procedure</span></span>           |
|-------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="01b54-760">MESSAGE **MFVP_MESSAGE_STEP**</span><span class="sxs-lookup"><span data-stu-id="01b54-760">**MFVP_MESSAGE_STEP** message</span></span>                                               | `PrepareFrameStep`  |
| <span data-ttu-id="01b54-761">MESSAGE **MFVP_MESSAGE_STEP**</span><span class="sxs-lookup"><span data-stu-id="01b54-761">**MFVP_MESSAGE_STEP** message</span></span>                                               | `CancelStep`        |
| [<span data-ttu-id="01b54-762">**IMFClockStateSink::OnClockStart**</span><span class="sxs-lookup"><span data-stu-id="01b54-762">**IMFClockStateSink::OnClockStart**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)     | `StartFrameStep`    |
| [<span data-ttu-id="01b54-763">**IMFClockStateSink::OnClockRestart**</span><span class="sxs-lookup"><span data-stu-id="01b54-763">**IMFClockStateSink::OnClockRestart**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) | `StartFrameStep`    |
| <span data-ttu-id="01b54-764">Rappel [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)</span><span class="sxs-lookup"><span data-stu-id="01b54-764">[**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback</span></span>                         | `CompleteFrameStep` |
| [<span data-ttu-id="01b54-765">**IMFClockStateSink::OnClockStop**</span><span class="sxs-lookup"><span data-stu-id="01b54-765">**IMFClockStateSink::OnClockStop**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)       | `CancelFrameStep`   |
| [<span data-ttu-id="01b54-766">**IMFClockStateSink::OnClockSetRate**</span><span class="sxs-lookup"><span data-stu-id="01b54-766">**IMFClockStateSink::OnClockSetRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) | `CancelFrameStep`   |



 

<span data-ttu-id="01b54-767">L’organigramme suivant présente les procédures pas à pas.</span><span class="sxs-lookup"><span data-stu-id="01b54-767">The following flow chart shows the frame-stepping procedures.</span></span>

![organigramme indiquant les chemins qui commencent par mfvp \- message \- Step et mfvp \- message \- processinputnotify et se terminent par « State = Complete »](images/d9baaa67-a9b1-4e27-9a32-08a45b0677d3.gif)

## <a name="setting-the-presenter-on-the-evr"></a><span data-ttu-id="01b54-769">Définition du présentateur sur le EVR</span><span class="sxs-lookup"><span data-stu-id="01b54-769">Setting the Presenter on the EVR</span></span>

<span data-ttu-id="01b54-770">Après avoir implémenté le présentateur, l’étape suivante consiste à configurer le EVR pour l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="01b54-770">After implementing the presenter, the next step is to configure the EVR to use it.</span></span>

### <a name="setting-the-presenter-in-directshow"></a><span data-ttu-id="01b54-771">Définition du présentateur dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="01b54-771">Setting the Presenter in DirectShow</span></span>

<span data-ttu-id="01b54-772">Dans une application DirectShow, définissez le présentateur sur le EVR comme suit :</span><span class="sxs-lookup"><span data-stu-id="01b54-772">In a DirectShow application, set the presenter on the EVR as follows:</span></span>

1.  <span data-ttu-id="01b54-773">Créez le filtre EVR en appelant **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="01b54-773">Create the EVR filter by calling **CoCreateInstance**.</span></span> <span data-ttu-id="01b54-774">Le CLSID est **CLSID_EnhancedVideoRenderer**.</span><span class="sxs-lookup"><span data-stu-id="01b54-774">The CLSID is **CLSID_EnhancedVideoRenderer**.</span></span>
2.  <span data-ttu-id="01b54-775">Ajoutez le EVR au graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="01b54-775">Add the EVR to the filter graph.</span></span>
3.  <span data-ttu-id="01b54-776">Créez une instance de votre présentateur.</span><span class="sxs-lookup"><span data-stu-id="01b54-776">Create an instance of your presenter.</span></span> <span data-ttu-id="01b54-777">Votre présentateur peut prendre en charge la création d’objets COM standard via **IClassFactory**, mais ce n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="01b54-777">Your presenter can support standard COM object creation through **IClassFactory**, but this is not mandatory.</span></span>
4.  <span data-ttu-id="01b54-778">Interrogez le filtre EVR pour l’interface [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) .</span><span class="sxs-lookup"><span data-stu-id="01b54-778">Query the EVR filter for the [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) interface.</span></span>
5.  <span data-ttu-id="01b54-779">Appelez [**IMFVideoRenderer :: InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span><span class="sxs-lookup"><span data-stu-id="01b54-779">Call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span>

### <a name="setting-the-presenter-in-media-foundation"></a><span data-ttu-id="01b54-780">Définition du présentateur dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="01b54-780">Setting the Presenter in Media Foundation</span></span>

<span data-ttu-id="01b54-781">Dans Media Foundation, vous avez plusieurs options, selon que vous créez le récepteur multimédia EVR ou l’objet d’activation EVR.</span><span class="sxs-lookup"><span data-stu-id="01b54-781">In Media Foundation, you have several options, depending on whether you create the EVR media sink or the EVR activation object.</span></span> <span data-ttu-id="01b54-782">Pour plus d’informations sur les objets d’activation, consultez [objets d’activation](activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="01b54-782">For more information about activation objects, see [Activation Objects](activation-objects.md).</span></span>

<span data-ttu-id="01b54-783">Pour le récepteur multimédia EVR, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="01b54-783">For the EVR media sink, do the following:</span></span>

1.  <span data-ttu-id="01b54-784">Appelez [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) pour créer le récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="01b54-784">Call [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) to create the media sink.</span></span>
2.  <span data-ttu-id="01b54-785">Créez une instance de votre présentateur.</span><span class="sxs-lookup"><span data-stu-id="01b54-785">Create an instance of your presenter.</span></span>
3.  <span data-ttu-id="01b54-786">Interrogez le récepteur multimédia EVR pour l’interface [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) .</span><span class="sxs-lookup"><span data-stu-id="01b54-786">Query the EVR media sink for the [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) interface.</span></span>
4.  <span data-ttu-id="01b54-787">Appelez [**IMFVideoRenderer :: InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span><span class="sxs-lookup"><span data-stu-id="01b54-787">Call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span>

<span data-ttu-id="01b54-788">Pour l’objet d’activation EVR, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="01b54-788">For the EVR activation object, do the following:</span></span>

1.  <span data-ttu-id="01b54-789">Appelez [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) pour créer l’objet d’activation.</span><span class="sxs-lookup"><span data-stu-id="01b54-789">Call [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) to create the activation object.</span></span>
2.  <span data-ttu-id="01b54-790">Définissez l’un des attributs suivants sur l’objet d’activation :</span><span class="sxs-lookup"><span data-stu-id="01b54-790">Set one of the following attributes on the activation object:</span></span> 

    | <span data-ttu-id="01b54-791">Attribut</span><span class="sxs-lookup"><span data-stu-id="01b54-791">Attribute</span></span>                                                                                                         | <span data-ttu-id="01b54-792">Description</span><span class="sxs-lookup"><span data-stu-id="01b54-792">Description</span></span>                                                                                                                                                                                                                               |
    |-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="01b54-793">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE**</span><span class="sxs-lookup"><span data-stu-id="01b54-793">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE**</span></span>](mf-activate-custom-video-presenter-activate-attribute.md) | <span data-ttu-id="01b54-794">Pointeur vers un objet d’activation pour le présentateur.</span><span class="sxs-lookup"><span data-stu-id="01b54-794">Pointer to an activation object for the presenter.</span></span><br/> <span data-ttu-id="01b54-795">Avec cet indicateur, vous devez fournir un objet d’activation pour votre présentateur.</span><span class="sxs-lookup"><span data-stu-id="01b54-795">With this flag, you must provide an activation object for your presenter.</span></span> <span data-ttu-id="01b54-796">L’objet d’activation doit implémenter l’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="01b54-796">The activation object must implement the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span><br/> |
    | [<span data-ttu-id="01b54-797">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID**</span><span class="sxs-lookup"><span data-stu-id="01b54-797">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID**</span></span>](mf-activate-custom-video-presenter-clsid-attribute.md)       | <span data-ttu-id="01b54-798">CLSID du présentateur.</span><span class="sxs-lookup"><span data-stu-id="01b54-798">CLSID of the presenter.</span></span><br/> <span data-ttu-id="01b54-799">Avec cet indicateur, votre présentateur doit prendre en charge la création d’objets COM standard via **IClassFactory**.</span><span class="sxs-lookup"><span data-stu-id="01b54-799">With this flag, your presenter must support standard COM object creation through **IClassFactory**.</span></span><br/>                                                                                         |

    

     

3.  <span data-ttu-id="01b54-800">Si vous le souhaitez, définissez l’attribut [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md) sur l’objet d’activation.</span><span class="sxs-lookup"><span data-stu-id="01b54-800">Optionally, set the [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md) attribute on the activation object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01b54-801">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="01b54-801">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01b54-802">Convertisseur vidéo amélioré</span><span class="sxs-lookup"><span data-stu-id="01b54-802">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="01b54-803">Exemple EVRPresenter</span><span class="sxs-lookup"><span data-stu-id="01b54-803">EVRPresenter Sample</span></span>](evrpresenter-sample.md)
</dt> </dl>

 

 
