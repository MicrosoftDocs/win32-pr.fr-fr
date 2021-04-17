---
title: Lecture des fichiers avec le lecteur asynchrone
description: Lecture des fichiers avec le lecteur asynchrone
ms.assetid: 3cc72f8d-bf1f-416d-bc90-21dfb92a55aa
keywords:
- Windows Media Format SDK, lire des fichiers
- Windows Media Format SDK, lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- Fichiers ASF (Advanced Systems Format), lecture des fichiers
- ASF (format des systèmes avancés), lire les fichiers
- lecteurs asynchrones, interface IWMReaderCallback
- IWMReaderCallback, lecteurs asynchrones
- lecteurs asynchrones, lire des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0807c0701dd596f943010ad613b08ef9fe2c415c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381486"
---
# <a name="reading-files-with-the-asynchronous-reader"></a><span data-ttu-id="6b469-112">Lecture des fichiers avec le lecteur asynchrone</span><span class="sxs-lookup"><span data-stu-id="6b469-112">Reading Files with the Asynchronous Reader</span></span>

<span data-ttu-id="6b469-113">Le lecteur asynchrone lit le contenu des fichiers ASF en utilisant plusieurs threads et appels asynchrones.</span><span class="sxs-lookup"><span data-stu-id="6b469-113">The asynchronous reader reads the content from ASF files using multiple threads and asynchronous calls.</span></span> <span data-ttu-id="6b469-114">Les fonctionnalités prises en charge par le lecteur asynchrone conviennent parfaitement aux applications qui assurent le rendu du contenu aux utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="6b469-114">The features supported by the asynchronous reader make it well suited for applications that render content to end users.</span></span>

<span data-ttu-id="6b469-115">Les fonctionnalités les plus basiques de l’objet lecteur peuvent être décomposées selon les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="6b469-115">The most basic functionality of the reader object can be broken down into the following steps.</span></span> <span data-ttu-id="6b469-116">Dans ces étapes, « l’application » fait référence au programme que vous écrivez à l’aide du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6b469-116">In these steps "the application" refers to the program you write using the Windows Media Format SDK.</span></span>

1.  <span data-ttu-id="6b469-117">L’application implémente l’interface [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) pour gérer les messages à partir du lecteur.</span><span class="sxs-lookup"><span data-stu-id="6b469-117">The application implements the [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) interface to handle messages from the reader.</span></span> <span data-ttu-id="6b469-118">Cela comprend deux méthodes de rappel : **OnStatus**, qui reçoit les messages relatifs à l’état des différents aspects du lecteur et **OnSample**, qui reçoit des exemples non compressés du lecteur.</span><span class="sxs-lookup"><span data-stu-id="6b469-118">This includes two callback methods: **OnStatus**, which receives messages relating to the status of various aspects of the reader and **OnSample**, which receives uncompressed samples from the reader.</span></span>
2.  <span data-ttu-id="6b469-119">L’application transmet au lecteur le nom d’un fichier à lire.</span><span class="sxs-lookup"><span data-stu-id="6b469-119">The application passes to the reader the name of a file to read.</span></span> <span data-ttu-id="6b469-120">Lorsque le lecteur ouvre le fichier, il attribue un numéro de sortie à chaque flux.</span><span class="sxs-lookup"><span data-stu-id="6b469-120">When the reader opens the file, it assigns an output number to each stream.</span></span> <span data-ttu-id="6b469-121">Si le fichier utilise l’exclusion mutuelle, le lecteur assigne une seule sortie pour tous les flux qui s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="6b469-121">If the file uses mutual exclusion, the reader assigns a single output for all of the mutually exclusive streams.</span></span>
3.  <span data-ttu-id="6b469-122">L’application obtient des informations sur la configuration des différentes sorties à partir du lecteur.</span><span class="sxs-lookup"><span data-stu-id="6b469-122">The application gets information about the configuration of the various outputs from the reader.</span></span> <span data-ttu-id="6b469-123">Les informations collectées permettront à l’application de restituer correctement les exemples de supports.</span><span class="sxs-lookup"><span data-stu-id="6b469-123">The information gathered will enable the application to properly render media samples.</span></span>
4.  <span data-ttu-id="6b469-124">L’application demande au lecteur de commencer à lire les données à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="6b469-124">The application instructs the reader to begin reading data from the file.</span></span> <span data-ttu-id="6b469-125">Le lecteur commence à transmettre des échantillons non compressés au rappel **OnSample** un par un dans des mémoires tampons encapsulées dans des objets de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="6b469-125">The reader begins delivering uncompressed samples to the **OnSample** callback one at a time in buffers wrapped in buffer objects.</span></span> <span data-ttu-id="6b469-126">Les exemples fournis par le lecteur sont dans l’ordre de la présentation.</span><span class="sxs-lookup"><span data-stu-id="6b469-126">The samples delivered by the reader are in presentation-time order.</span></span> <span data-ttu-id="6b469-127">Le lecteur continue de fournir des échantillons jusqu’à ce qu’il soit arrêté par l’application ou jusqu’à ce que la fin du fichier soit atteinte.</span><span class="sxs-lookup"><span data-stu-id="6b469-127">The reader will continue delivering samples until stopped by the application or until the end of the file is reached.</span></span>
5.  <span data-ttu-id="6b469-128">L’application est chargée du rendu des données une fois qu’elles sont fournies par le lecteur.</span><span class="sxs-lookup"><span data-stu-id="6b469-128">The application is responsible for rendering data after it is delivered by the reader.</span></span> <span data-ttu-id="6b469-129">Le kit de développement logiciel (SDK) Windows Media format ne fournit pas de routines de rendu.</span><span class="sxs-lookup"><span data-stu-id="6b469-129">The Windows Media Format SDK does not provide any rendering routines.</span></span> <span data-ttu-id="6b469-130">En règle générale, les applications utilisent d’autres kits de développement logiciel (SDK) pour restituer des données, telles que le kit de développement logiciel (SDK) Microsoft DirectX® ou les fonctions multimédias du kit SDK de plateforme Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6b469-130">Typically, applications will use other SDKs to render data, such as the Microsoft DirectX® SDK, or the multimedia functions of the Microsoft Windows Platform SDK.</span></span>
6.  <span data-ttu-id="6b469-131">Lorsque la lecture est terminée, l’application demande au lecteur de fermer le fichier.</span><span class="sxs-lookup"><span data-stu-id="6b469-131">When reading is complete, the application instructs the reader to close the file.</span></span>

<span data-ttu-id="6b469-132">Ces étapes sont illustrées dans l’exemple d’application AudioPlayer, entre autres.</span><span class="sxs-lookup"><span data-stu-id="6b469-132">These steps are illustrated in the AudioPlayer sample application, among others.</span></span> <span data-ttu-id="6b469-133">Pour plus d’informations, consultez [exemples d’applications](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="6b469-133">For more information, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="6b469-134">Le lecteur prend également en charge des fonctionnalités plus avancées.</span><span class="sxs-lookup"><span data-stu-id="6b469-134">The reader also supports more advanced functionality.</span></span> <span data-ttu-id="6b469-135">Le lecteur vous permet d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="6b469-135">The reader enables you to do the following:</span></span>

-   <span data-ttu-id="6b469-136">Suspendre la lecture d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="6b469-136">Pause playback of a file.</span></span>
-   <span data-ttu-id="6b469-137">Récupérez les statistiques de performances des lecteurs.</span><span class="sxs-lookup"><span data-stu-id="6b469-137">Retrieve reader performance statistics.</span></span>
-   <span data-ttu-id="6b469-138">Contrôle de la sélection de flux pour les flux mutuellement exclusifs.</span><span class="sxs-lookup"><span data-stu-id="6b469-138">Control stream selection for mutually exclusive streams.</span></span>
-   <span data-ttu-id="6b469-139">Allouez manuellement les tampons pour la sortie.</span><span class="sxs-lookup"><span data-stu-id="6b469-139">Manually allocate buffers for output.</span></span>
-   <span data-ttu-id="6b469-140">Fournissez votre propre horloge.</span><span class="sxs-lookup"><span data-stu-id="6b469-140">Provide your own clock.</span></span>
-   <span data-ttu-id="6b469-141">Récupérez l’état des opérations sur les fichiers (mise en mémoire tampon, téléchargement ou enregistrement).</span><span class="sxs-lookup"><span data-stu-id="6b469-141">Retrieve the status of file operations (buffering, download, or save).</span></span>
-   <span data-ttu-id="6b469-142">Ouvrez un fichier à l’aide de l’interface COM standard, **IStream**.</span><span class="sxs-lookup"><span data-stu-id="6b469-142">Open a file using the standard COM interface, **IStream**.</span></span>
-   <span data-ttu-id="6b469-143">Recherchez des points spécifiques dans un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="6b469-143">Seek to specific points in an ASF file.</span></span>
-   <span data-ttu-id="6b469-144">Lire les données de profil dans l’en-tête du fichier.</span><span class="sxs-lookup"><span data-stu-id="6b469-144">Read profile data from the header of the file.</span></span>

<span data-ttu-id="6b469-145">Les sections suivantes décrivent en détail l’utilisation de l’objet Reader.</span><span class="sxs-lookup"><span data-stu-id="6b469-145">The following sections describe the use of the reader object in detail.</span></span>

-   [<span data-ttu-id="6b469-146">Pour implémenter des messages de lecture dans le rappel OnStatus</span><span class="sxs-lookup"><span data-stu-id="6b469-146">To Implement Reader Messages in the OnStatus Callback</span></span>](to-implement-reader-messages-in-the-onstatus-callback.md)
-   [<span data-ttu-id="6b469-147">Pour implémenter le rappel OnSample</span><span class="sxs-lookup"><span data-stu-id="6b469-147">To Implement the OnSample Callback</span></span>](to-implement-the-onsample-callback.md)
-   [<span data-ttu-id="6b469-148">Pour créer un lecteur et ouvrir un fichier</span><span class="sxs-lookup"><span data-stu-id="6b469-148">To Create a Reader and Open a File</span></span>](to-create-a-reader-and-open-a-file.md)
-   [<span data-ttu-id="6b469-149">Pour récupérer des exemples de médias avec le lecteur asynchrone</span><span class="sxs-lookup"><span data-stu-id="6b469-149">To Retrieve Media Samples with the Asynchronous Reader</span></span>](to-retrieve-media-samples-with-the-asynchronous-reader.md)
-   [<span data-ttu-id="6b469-150">Pour effectuer une recherche par heure à l’aide du lecteur asynchrone</span><span class="sxs-lookup"><span data-stu-id="6b469-150">To Seek By Time Using the Asynchronous Reader</span></span>](to-seek-by-time-using-the-asynchronous-reader.md)
-   [<span data-ttu-id="6b469-151">Pour rechercher par numéro de frame à l’aide du lecteur asynchrone</span><span class="sxs-lookup"><span data-stu-id="6b469-151">To Seek By Frame Number Using the Asynchronous Reader</span></span>](to-seek-by-frame-number-using-the-asynchronous-reader.md)
-   [<span data-ttu-id="6b469-152">Pour effectuer une recherche par code temporel SMPTE à l’aide du lecteur asynchrone</span><span class="sxs-lookup"><span data-stu-id="6b469-152">To Seek By SMPTE Time Code Using the Asynchronous Reader</span></span>](to-seek-by-smpte-time-code-using-the-asynchronous-reader.md)
-   [<span data-ttu-id="6b469-153">Pour rechercher des marqueurs</span><span class="sxs-lookup"><span data-stu-id="6b469-153">To Seek to Markers</span></span>](to-seek-to-markers.md)
-   [<span data-ttu-id="6b469-154">Pour suspendre ou arrêter la lecture</span><span class="sxs-lookup"><span data-stu-id="6b469-154">To Pause or Stop Playback</span></span>](to-pause-or-stop-playback.md)
-   [<span data-ttu-id="6b469-155">Pour accéder aux statistiques de performances des lecteurs</span><span class="sxs-lookup"><span data-stu-id="6b469-155">To Get Reader Performance Statistics</span></span>](to-get-reader-performance-statistics.md)
-   [<span data-ttu-id="6b469-156">Pour utiliser la sélection manuelle de flux</span><span class="sxs-lookup"><span data-stu-id="6b469-156">To Use Manual Stream Selection</span></span>](to-use-manual-stream-selection.md)
-   [<span data-ttu-id="6b469-157">Pour distribuer des exemples compressés avec le lecteur asynchrone</span><span class="sxs-lookup"><span data-stu-id="6b469-157">To Deliver Compressed Samples with the Asynchronous Reader</span></span>](to-deliver-compressed-samples-with-the-asynchronous-reader.md)

## <a name="related-topics"></a><span data-ttu-id="6b469-158">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6b469-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b469-159">**Lecture des fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="6b469-159">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="6b469-160">**Lecteur, objet**</span><span class="sxs-lookup"><span data-stu-id="6b469-160">**Reader Object**</span></span>](reader-object.md)
</dt> </dl>

 

 




