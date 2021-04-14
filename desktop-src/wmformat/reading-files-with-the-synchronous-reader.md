---
title: Lecture des fichiers avec le lecteur synchrone
description: Lecture des fichiers avec le lecteur synchrone
ms.assetid: 18c6c0cd-478f-4325-b23e-571c33779a96
keywords:
- Windows Media Format SDK, lire des fichiers
- Windows Media Format SDK, lecteurs synchrones
- ASF (Advanced Systems Format), lecteurs synchrones
- ASF (format des systèmes avancés), lecteurs synchrones
- Fichiers ASF (Advanced Systems Format), lecture des fichiers
- ASF (format des systèmes avancés), lire les fichiers
- lecteurs synchrones, interface IWMReaderCallback
- IWMReaderCallback, lecteurs synchrones
- lecteurs synchrones, lire des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893a1bd324cdc91968e423f2084bfdba5ef57c8e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381485"
---
# <a name="reading-files-with-the-synchronous-reader"></a><span data-ttu-id="6ddc6-112">Lecture des fichiers avec le lecteur synchrone</span><span class="sxs-lookup"><span data-stu-id="6ddc6-112">Reading Files with the Synchronous Reader</span></span>

<span data-ttu-id="6ddc6-113">Vous pouvez utiliser le lecteur synchrone pour lire un fichier ASF à l’aide d’appels synchrones au lieu des méthodes asynchrones dans l’objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-113">You can use the synchronous reader to read an ASF file using synchronous calls instead of the asynchronous methods in the reader object.</span></span> <span data-ttu-id="6ddc6-114">L’utilisation d’appels synchrones réduit le nombre de threads requis pour lire un fichier.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-114">Using synchronous calls reduces the number of threads required to read a file.</span></span> <span data-ttu-id="6ddc6-115">Le lecteur asynchrone utilise plusieurs threads pour le traitement des flux.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-115">The asynchronous reader uses multiple threads for processing streams.</span></span> <span data-ttu-id="6ddc6-116">Pour les fichiers contenant plusieurs flux, le nombre de threads utilisés peut devenir très élevé.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-116">For files with multiple streams, the number of threads used can become very large.</span></span> <span data-ttu-id="6ddc6-117">Le lecteur synchrone n’utilise qu’un seul thread.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-117">The synchronous reader uses only one thread.</span></span>

<span data-ttu-id="6ddc6-118">Le lecteur synchrone a été conçu pour répondre aux besoins des applications de création de contenu et de modification de fichiers.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-118">The synchronous reader was designed to meet the needs of content creation and file editing applications.</span></span> <span data-ttu-id="6ddc6-119">Vous pouvez utiliser le lecteur synchrone pour d’autres applications, mais ses fonctionnalités sont limitées.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-119">You can use the synchronous reader for other applications, but its functionality is limited.</span></span>

<span data-ttu-id="6ddc6-120">Le lecteur synchrone peut ouvrir des fichiers locaux ou des fichiers sur un réseau à l’aide du nom de chemin d’accès UNC (par exemple, « \\ \\ someshare \\ somedirectory \\ somefile. wmv »).</span><span class="sxs-lookup"><span data-stu-id="6ddc6-120">The synchronous reader can open files that are local, or files on a network using the UNC path name (such as "\\\\someshare\\somedirectory\\somefile.wmv").</span></span> <span data-ttu-id="6ddc6-121">Vous ne pouvez pas diffuser des fichiers vers le lecteur synchrone ou ouvrir des fichiers à partir d’un emplacement Internet.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-121">You cannot stream files to the synchronous reader, or open files from an Internet location.</span></span> <span data-ttu-id="6ddc6-122">Le lecteur synchrone prend également en charge l’utilisation de l’interface com **IStream** comme source.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-122">The synchronous reader also provides support for using the **IStream** COM interface as a source.</span></span>

<span data-ttu-id="6ddc6-123">Le lecteur synchrone offre plus de polyvalence pour récupérer des exemples d’un fichier ASF que le lecteur asynchrone.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-123">The synchronous reader provides more versatility for retrieving samples from an ASF file than the asynchronous reader.</span></span> <span data-ttu-id="6ddc6-124">Le lecteur synchrone peut fournir des échantillons par numéro de flux, ainsi que par sortie.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-124">The synchronous reader can deliver samples by stream number as well as by output.</span></span> <span data-ttu-id="6ddc6-125">Les exemples fournis par le numéro de flux peuvent être compressés ou non.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-125">Samples delivered by stream number can be compressed or uncompressed.</span></span> <span data-ttu-id="6ddc6-126">Le lecteur synchrone peut également basculer entre les remises compressées et non compressées lors de la lecture. Cette fonctionnalité est appelée « édition rapide ».</span><span class="sxs-lookup"><span data-stu-id="6ddc6-126">The synchronous reader can also switch between compressed and uncompressed delivery during playback; this feature is known as "fast editing."</span></span> <span data-ttu-id="6ddc6-127">Cette fonctionnalité permet à une application de modification de lire du contenu Windows Media et de la transmettre directement à l’enregistreur jusqu’à ce qu’un frame souhaité soit atteint.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-127">This feature enables an editing application to read Windows Media-based content and pass it directly through to the writer until a desired frame is reached.</span></span> <span data-ttu-id="6ddc6-128">À ce stade, l’application peut indiquer au lecteur de commencer à fournir du contenu non compressé, que l’application peut ensuite modifier et transmettre à l’enregistreur pour la recompression.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-128">At that point the application can tell the reader to start delivering uncompressed content, which the application can then modify and pass to the writer for recompression.</span></span> <span data-ttu-id="6ddc6-129">Lorsque l’application a terminé la modification des frames spécifiés, elle peut demander au lecteur de démarrer à nouveau la diffusion des frames compressés.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-129">When the application has finished modifying the specified frames, it can tell the reader to start delivering compressed frames again.</span></span>

<span data-ttu-id="6ddc6-130">Les fonctionnalités les plus basiques de l’objet lecteur synchrone peuvent être décomposées selon les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-130">The most basic functionality of the synchronous reader object can be broken down into the following steps.</span></span> <span data-ttu-id="6ddc6-131">Dans ces étapes, « l’application » fait référence au programme que vous écrivez à l’aide du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-131">In these steps "the application" refers to the program you write using the Windows Media Format SDK.</span></span>

1.  <span data-ttu-id="6ddc6-132">L’application transmet au lecteur synchrone le nom d’un fichier à lire.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-132">The application passes to the synchronous reader the name of a file to read.</span></span> <span data-ttu-id="6ddc6-133">Lorsque le lecteur synchrone ouvre le fichier, il attribue un numéro de sortie à chaque flux.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-133">When the synchronous reader opens the file, it assigns an output number to each stream.</span></span> <span data-ttu-id="6ddc6-134">Si le fichier utilise l’exclusion mutuelle, le lecteur assigne une seule sortie pour tous les flux qui s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-134">If the file uses mutual exclusion, the reader assigns a single output for all of the mutually exclusive streams.</span></span>
2.  <span data-ttu-id="6ddc6-135">L’application obtient des informations sur la configuration des différentes sorties à partir du lecteur.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-135">The application gets information about the configuration of the various outputs from the reader.</span></span> <span data-ttu-id="6ddc6-136">Les informations collectées permettront à l’application de restituer correctement les exemples de supports.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-136">The information gathered will enable the application to properly render media samples.</span></span>
3.  <span data-ttu-id="6ddc6-137">L’application commence à demander des exemples, l’un après l’autre, à partir du lecteur synchrone.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-137">The application begins requesting samples, one at a time, from the synchronous reader.</span></span> <span data-ttu-id="6ddc6-138">Le lecteur synchrone remet chaque exemple dans un objet buffer pour lequel il remet l’interface [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) .</span><span class="sxs-lookup"><span data-stu-id="6ddc6-138">The synchronous reader delivers each sample in a buffer object for which it delivers the [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) interface.</span></span>
4.  <span data-ttu-id="6ddc6-139">L’application est chargée du rendu des données une fois qu’elles sont fournies par le lecteur.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-139">The application is responsible for rendering data after it is delivered by the reader.</span></span> <span data-ttu-id="6ddc6-140">Le kit de développement logiciel (SDK) Windows Media format ne fournit pas de routines de rendu.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-140">The Windows Media Format SDK does not provide any rendering routines.</span></span> <span data-ttu-id="6ddc6-141">En règle générale, les applications utilisent d’autres kits de développement logiciel (SDK) pour restituer des données, comme le kit de développement logiciel (SDK) Microsoft Direct X ou les fonctions multimédias du kit SDK de plateforme Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-141">Typically, applications will use other SDKs to render data, such as the Microsoft Direct X SDK, or the multimedia functions of the Microsoft Windows Platform SDK.</span></span>

<span data-ttu-id="6ddc6-142">Ces étapes sont illustrées dans l’exemple d’application WMSyncReader.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-142">These steps are illustrated in the WMSyncReader sample application.</span></span> <span data-ttu-id="6ddc6-143">Pour plus d’informations, consultez [exemples d’applications](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="6ddc6-143">For more information, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="6ddc6-144">Le lecteur synchrone prend également en charge des fonctionnalités plus avancées.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-144">The synchronous reader also supports more advanced functionality.</span></span> <span data-ttu-id="6ddc6-145">Le lecteur synchrone vous permet d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="6ddc6-145">The synchronous reader enables you to do the following:</span></span>

-   <span data-ttu-id="6ddc6-146">Spécifiez une plage d’échantillons à récupérer par heure ou par numéro de trame.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-146">Specify a range of samples to retrieve by time or by frame number.</span></span>
-   <span data-ttu-id="6ddc6-147">Contrôle de la sélection de flux pour les flux mutuellement exclusifs.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-147">Control stream selection for mutually exclusive streams.</span></span>
-   <span data-ttu-id="6ddc6-148">Ouvrez un fichier à l’aide de l’interface COM standard, **IStream**.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-148">Open a file using the standard COM interface, **IStream**.</span></span>
-   <span data-ttu-id="6ddc6-149">Lire les données de profil à partir de l’en-tête de fichier.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-149">Read profile data from the file header.</span></span>
-   <span data-ttu-id="6ddc6-150">Lit les métadonnées de l’en-tête de fichier.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-150">Read metadata from the file header.</span></span>
-   <span data-ttu-id="6ddc6-151">Basculer entre les exemples de flux et de sortie pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-151">Switch between stream and output samples during playback.</span></span>
-   <span data-ttu-id="6ddc6-152">Basculer entre les exemples de flux compressés et non compressés pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-152">Switch between compressed and uncompressed stream samples during playback.</span></span>

<span data-ttu-id="6ddc6-153">Les sections suivantes décrivent en détail l’utilisation de l’objet lecteur synchrone.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-153">The following sections describe the use of the synchronous reader object in detail.</span></span>

-   [<span data-ttu-id="6ddc6-154">Pour créer un lecteur synchrone et ouvrir un fichier</span><span class="sxs-lookup"><span data-stu-id="6ddc6-154">To Create a Synchronous Reader and Open a File</span></span>](to-create-a-synchronous-reader-and-open-a-file.md)
-   [<span data-ttu-id="6ddc6-155">Pour rechercher les numéros de flux et les numéros de sortie</span><span class="sxs-lookup"><span data-stu-id="6ddc6-155">To Find Stream Numbers and Output Numbers</span></span>](to-find-stream-numbers-and-output-numbers.md)
-   [<span data-ttu-id="6ddc6-156">Pour récupérer des exemples de médias avec le lecteur synchrone</span><span class="sxs-lookup"><span data-stu-id="6ddc6-156">To Retrieve Media Samples with the Synchronous Reader</span></span>](to-retrieve-media-samples-with-the-synchronous-reader.md)
-   [<span data-ttu-id="6ddc6-157">Pour effectuer une recherche par heure à l’aide du lecteur synchrone</span><span class="sxs-lookup"><span data-stu-id="6ddc6-157">To Seek By Time Using the Synchronous Reader</span></span>](to-seek-by-time-using-the-synchronous-reader.md)
-   [<span data-ttu-id="6ddc6-158">Pour rechercher par numéro de frame à l’aide du lecteur synchrone</span><span class="sxs-lookup"><span data-stu-id="6ddc6-158">To Seek By Frame Number Using the Synchronous Reader</span></span>](to-seek-by-frame-number-using-the-synchronous-reader.md)
-   [<span data-ttu-id="6ddc6-159">Pour effectuer une recherche par code temporel SMPTE à l’aide du lecteur synchrone</span><span class="sxs-lookup"><span data-stu-id="6ddc6-159">To Seek By SMPTE Time Code Using the Synchronous Reader</span></span>](to-seek-by-smpte-time-code-using-the-synchronous-reader.md)
-   [<span data-ttu-id="6ddc6-160">Pour récupérer des exemples de flux avec le lecteur synchrone</span><span class="sxs-lookup"><span data-stu-id="6ddc6-160">To Retrieve Stream Samples with the Synchronous Reader</span></span>](to-retrieve-stream-samples-with-the-synchronous-reader.md)
-   [<span data-ttu-id="6ddc6-161">Pour récupérer des exemples compressés avec le lecteur synchrone</span><span class="sxs-lookup"><span data-stu-id="6ddc6-161">To Retrieve Compressed Samples with the Synchronous Reader</span></span>](to-retrieve-compressed-samples-with-the-synchronous-reader.md)

<span data-ttu-id="6ddc6-162">**Exemple de code**</span><span class="sxs-lookup"><span data-stu-id="6ddc6-162">**Example Code**</span></span>

<span data-ttu-id="6ddc6-163">L’exemple de code suivant montre comment lire des exemples à partir d’un fichier ASF à l’aide du lecteur synchrone.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-163">The following example code shows how to read samples from an ASF file using the synchronous reader.</span></span> <span data-ttu-id="6ddc6-164">Elle spécifie par numéro de trame une plage d’exemples à remettre.</span><span class="sxs-lookup"><span data-stu-id="6ddc6-164">It specifies by frame number a range of samples to deliver.</span></span>


```C++
IWMSyncReader* pSyncReader = NULL;
INSSBuffer*    pMyBuffer   = NULL;

QWORD cnsSampleTime = 0;
QWORD cnsSampleDuration = 0;
DWORD dwFlags = 0;
DWORD dwOutputNumber;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a synchronous reader.
hr = WMCreateSyncReader(NULL, WMT_RIGHT_PLAYBACK, &pSyncReader);

// Open an ASF file.
hr = pSyncReader->Open(L"c:\\somefile.wmv");

// TODO: Identify the properties for each output. This works 
// exactly as it does with the asynchronous reader.

// Specify a playback range from frame number 100 of the video 
// stream to the end of the file. Assume that the video stream 
// is stream number 2.
hr = pSyncReader->SetRangeByFrame(2, 100, 0);

// Loop through all the samples in the specified range.
do
{
   // Get the next sample, regardless of its stream number.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

pSyncReader->Release();
pSyncReader = NULL;

```



## <a name="related-topics"></a><span data-ttu-id="6ddc6-165">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6ddc6-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ddc6-166">**Interface IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="6ddc6-166">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="6ddc6-167">**Lecture des fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="6ddc6-167">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="6ddc6-168">**Lecteur synchrone, objet**</span><span class="sxs-lookup"><span data-stu-id="6ddc6-168">**Synchronous Reader Object**</span></span>](synchronous-reader-object.md)
</dt> </dl>

 

 




