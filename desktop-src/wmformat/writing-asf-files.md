---
title: Écriture de fichiers ASF
description: Écriture de fichiers ASF
ms.assetid: d722b676-bf65-4f91-8118-bb12d3bbb6cb
keywords:
- Windows Media Format SDK, écriture de fichiers ASF
- Windows Media Format SDK, création de fichiers ASF
- Windows Media Format SDK, ASF (Advanced Systems Format)
- ASF (Advanced Systems Format), écriture de fichiers
- ASF (format de systèmes avancés), écriture de fichiers
- ASF (Advanced Systems Format), création de fichiers
- ASF (format des systèmes avancés), création de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c13c1af0d3699c89d26f007e00675ea563639c4e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103841893"
---
# <a name="writing-asf-files"></a><span data-ttu-id="5683d-110">Écriture de fichiers ASF</span><span class="sxs-lookup"><span data-stu-id="5683d-110">Writing ASF Files</span></span>

<span data-ttu-id="5683d-111">Vous pouvez utiliser l’objet Writer du kit de développement logiciel (SDK) Windows Media format pour créer des fichiers ASF à partir de données multimédias numériques.</span><span class="sxs-lookup"><span data-stu-id="5683d-111">You can use the writer object of the Windows Media Format SDK to create ASF files from digital media data.</span></span> <span data-ttu-id="5683d-112">Pour créer une instance de l’objet Writer, appelez la fonction [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) .</span><span class="sxs-lookup"><span data-stu-id="5683d-112">To create an instance of the writer object, call the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function.</span></span> <span data-ttu-id="5683d-113">L’objet Writer coordonne les fonctionnalités d’un certain nombre de composants, y compris les codecs, qui sont externes au kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5683d-113">The writer object coordinates the functionality of a number of components, including codecs, which are external to the Windows Media Format SDK.</span></span>

<span data-ttu-id="5683d-114">Les fonctionnalités de base de l’objet Writer peuvent être décomposées selon les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="5683d-114">The basic functionality of the writer object can be broken down into the following steps.</span></span> <span data-ttu-id="5683d-115">Dans ces étapes, « l’application » fait référence au programme que vous écrivez à l’aide du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5683d-115">In these steps, "the application" refers to the program you write using the Windows Media Format SDK.</span></span>

1.  <span data-ttu-id="5683d-116">L’application fournit à l’enregistreur un profil à utiliser pour créer le fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="5683d-116">The application supplies the writer with a profile to use in creating the ASF file.</span></span> <span data-ttu-id="5683d-117">Lorsque l’enregistreur charge les données de profil, il attribue un numéro d’entrée à chaque connexion du profil.</span><span class="sxs-lookup"><span data-stu-id="5683d-117">When the writer loads the profile data, it assigns an input number to each connection of the profile.</span></span>
2.  <span data-ttu-id="5683d-118">L’application fournit au writer un nom de fichier de sortie pour le fichier à écrire.</span><span class="sxs-lookup"><span data-stu-id="5683d-118">The application supplies the writer with an output file name for the file to be written.</span></span> <span data-ttu-id="5683d-119">L’enregistreur crée un objet récepteur de fichiers de Writer pour gérer la création et l’entrée de fichier.</span><span class="sxs-lookup"><span data-stu-id="5683d-119">The writer creates a writer file sink object to manage the file creation and input.</span></span> <span data-ttu-id="5683d-120">Pour plus d’informations, consultez [objet récepteur de fichiers](writer-file-sink-object.md)de l’enregistreur.</span><span class="sxs-lookup"><span data-stu-id="5683d-120">For more information, see [Writer File Sink Object](writer-file-sink-object.md).</span></span>
3.  <span data-ttu-id="5683d-121">L’enregistreur crée un en-tête pour le nouveau fichier en fonction des informations contenues dans le profil.</span><span class="sxs-lookup"><span data-stu-id="5683d-121">The writer creates a header for the new file based on information in the profile.</span></span>
4.  <span data-ttu-id="5683d-122">L’application transmet des exemples non compressés au writer.</span><span class="sxs-lookup"><span data-stu-id="5683d-122">The application passes uncompressed samples to the writer.</span></span> <span data-ttu-id="5683d-123">Les exemples sont passés un par un dans des mémoires tampons encapsulées dans des objets de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="5683d-123">Samples are passed one at a time in buffers wrapped in buffer objects.</span></span> <span data-ttu-id="5683d-124">L’application doit transmettre simultanément des exemples pour chaque flux afin que le writer reçoive tous les exemples dans l’ordre de la présentation.</span><span class="sxs-lookup"><span data-stu-id="5683d-124">The application should pass samples for each stream concurrently so that the writer receives all samples in presentation-time order.</span></span>
5.  <span data-ttu-id="5683d-125">Le writer passe les exemples au codec approprié pour la compression.</span><span class="sxs-lookup"><span data-stu-id="5683d-125">The writer passes the samples to the appropriate codec for compression.</span></span> <span data-ttu-id="5683d-126">Lorsque l’enregistreur reçoit les exemples compressés, il les entrelace avec des échantillons des autres flux afin que les exemples entrent dans le fichier dans l’ordre chronologique des présentations, quel que soit le flux.</span><span class="sxs-lookup"><span data-stu-id="5683d-126">When the writer receives the compressed samples, it interleaves them with samples from the other streams so that samples go into the file in presentation time order irrespective of stream.</span></span> <span data-ttu-id="5683d-127">Les exemples de données sont ensuite transformés en paquets et écrits dans la section de données du fichier.</span><span class="sxs-lookup"><span data-stu-id="5683d-127">The sample data is then made into packets and written to the data section of the file.</span></span>
6.  <span data-ttu-id="5683d-128">Lorsque tous les échantillons sont traités, le writer peut ajouter un index au fichier pour améliorer les performances de la recherche.</span><span class="sxs-lookup"><span data-stu-id="5683d-128">When all samples are processed, the writer can add an index to the file to enhance seeking performance.</span></span>

<span data-ttu-id="5683d-129">Ces étapes sont illustrées dans l’exemple d’application WMStats, entre autres.</span><span class="sxs-lookup"><span data-stu-id="5683d-129">These steps are illustrated in the WMStats sample application, among others.</span></span> <span data-ttu-id="5683d-130">Pour plus d’informations, consultez [exemples d’applications](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="5683d-130">For more information, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="5683d-131">L’enregistreur prend également en charge des fonctionnalités plus avancées, ce qui vous permet d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="5683d-131">The writer also supports more advanced functionality, enabling you to do the following:</span></span>

-   <span data-ttu-id="5683d-132">Modifiez les métadonnées dans l’en-tête du fichier.</span><span class="sxs-lookup"><span data-stu-id="5683d-132">Edit metadata in the header of the file.</span></span>
-   <span data-ttu-id="5683d-133">Écrire des exemples précompressés.</span><span class="sxs-lookup"><span data-stu-id="5683d-133">Write precompressed samples.</span></span>
-   <span data-ttu-id="5683d-134">Écrire dans les récepteurs réseau pour la diffusion en continu des données actives.</span><span class="sxs-lookup"><span data-stu-id="5683d-134">Write to network sinks for streaming live data.</span></span>
-   <span data-ttu-id="5683d-135">Écrire dans les récepteurs de fichiers pour les options de contrôle de fichier avancées.</span><span class="sxs-lookup"><span data-stu-id="5683d-135">Write to file sinks for advanced file control options.</span></span>
-   <span data-ttu-id="5683d-136">Écrire dans des récepteurs de notifications push pour la distribution aux serveurs qui fourniront du contenu aux utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="5683d-136">Write to push sinks for distribution to servers that will deliver content to end users.</span></span>
-   <span data-ttu-id="5683d-137">Fournissez des exemples postview pour la vérification de la sortie.</span><span class="sxs-lookup"><span data-stu-id="5683d-137">Deliver postview samples for verification of output.</span></span>
-   <span data-ttu-id="5683d-138">Fournir l’enregistreur-statistiques de performances.</span><span class="sxs-lookup"><span data-stu-id="5683d-138">Deliver writer-performance statistics.</span></span>

<span data-ttu-id="5683d-139">Les sections suivantes décrivent en détail l’utilisation de l’objet Writer.</span><span class="sxs-lookup"><span data-stu-id="5683d-139">The following sections describe the use of the writer object in detail.</span></span>



| <span data-ttu-id="5683d-140">Section</span><span class="sxs-lookup"><span data-stu-id="5683d-140">Section</span></span>                                                                    | <span data-ttu-id="5683d-141">Description</span><span class="sxs-lookup"><span data-stu-id="5683d-141">Description</span></span>                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5683d-142">Pour utiliser des profils avec l’auteur</span><span class="sxs-lookup"><span data-stu-id="5683d-142">To Use Profiles with the Writer</span></span>](to-use-profiles-with-the-writer.md)     | <span data-ttu-id="5683d-143">Décrit comment spécifier un profil à utiliser avec le writer.</span><span class="sxs-lookup"><span data-stu-id="5683d-143">Describes how to specify a profile to use with the writer.</span></span>                                             |
| [<span data-ttu-id="5683d-144">Utilisation des entrées</span><span class="sxs-lookup"><span data-stu-id="5683d-144">Working with Inputs</span></span>](working-with-inputs.md)                             | <span data-ttu-id="5683d-145">Décrit comment identifier et configurer les paramètres d’entrée dans le writer.</span><span class="sxs-lookup"><span data-stu-id="5683d-145">Describes how to identify and configure the input settings in the writer.</span></span>                              |
| [<span data-ttu-id="5683d-146">Pour modifier des métadonnées avec le writer</span><span class="sxs-lookup"><span data-stu-id="5683d-146">To Edit Metadata with the Writer</span></span>](to-edit-metadata-with-the-writer.md)   | <span data-ttu-id="5683d-147">Décrit comment utiliser le writer pour modifier les métadonnées d’un nouveau fichier.</span><span class="sxs-lookup"><span data-stu-id="5683d-147">Describes how to use the writer to edit metadata for a new file.</span></span>                                       |
| [<span data-ttu-id="5683d-148">Pour écrire des exemples</span><span class="sxs-lookup"><span data-stu-id="5683d-148">To Write Samples</span></span>](to-write-samples.md)                                   | <span data-ttu-id="5683d-149">Décrit comment passer des exemples au writer.</span><span class="sxs-lookup"><span data-stu-id="5683d-149">Describes how to pass samples to the writer.</span></span>                                                           |
| [<span data-ttu-id="5683d-150">Définition des extensions d’unité de données</span><span class="sxs-lookup"><span data-stu-id="5683d-150">Setting Data Unit Extensions</span></span>](setting-data-unit-extensions.md)           | <span data-ttu-id="5683d-151">Décrit comment ajouter des données étendues à des exemples.</span><span class="sxs-lookup"><span data-stu-id="5683d-151">Describes how to add extended data to samples.</span></span>                                                         |
| [<span data-ttu-id="5683d-152">Écriture d’exemples compressés</span><span class="sxs-lookup"><span data-stu-id="5683d-152">Writing Compressed Samples</span></span>](writing-compressed-samples.md)               | <span data-ttu-id="5683d-153">Décrit comment passer des échantillons précompressés au writer.</span><span class="sxs-lookup"><span data-stu-id="5683d-153">Describes how to pass pre-compressed samples to the writer.</span></span>                                            |
| [<span data-ttu-id="5683d-154">Écriture de flux d’images</span><span class="sxs-lookup"><span data-stu-id="5683d-154">Writing Image Streams</span></span>](writing-image-streams.md)                         | <span data-ttu-id="5683d-155">Décrit comment configurer une entrée pour un flux d’image.</span><span class="sxs-lookup"><span data-stu-id="5683d-155">Describes how to configure an input for an image stream.</span></span>                                               |
| [<span data-ttu-id="5683d-156">Écriture d’exemples d’images vidéo</span><span class="sxs-lookup"><span data-stu-id="5683d-156">Writing Video Image Samples</span></span>](writing-video-image-samples.md)             | <span data-ttu-id="5683d-157">Décrit comment configurer des exemples d’images vidéo.</span><span class="sxs-lookup"><span data-stu-id="5683d-157">Describes how to configure Video Image samples.</span></span>                                                        |
| [<span data-ttu-id="5683d-158">Écriture de flux de vitesse binaire variable</span><span class="sxs-lookup"><span data-stu-id="5683d-158">Writing Variable Bit Rate Streams</span></span>](writing-variable-bit-rate-streams.md) | <span data-ttu-id="5683d-159">Décrit comment écrire des flux à débit binaire variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="5683d-159">Describes how to write variable bit rate (VBR) streams.</span></span>                                                |
| [<span data-ttu-id="5683d-160">Utilisation de l’encodage Two-Pass</span><span class="sxs-lookup"><span data-stu-id="5683d-160">Using Two-Pass Encoding</span></span>](using-two-pass-encoding.md)                     | <span data-ttu-id="5683d-161">Décrit comment faire en sorte que le codec effectue une étape préliminaire avant d’écrire le fichier.</span><span class="sxs-lookup"><span data-stu-id="5683d-161">Describes how to have the codec perform a preliminary pass before writing the file.</span></span>                    |
| [<span data-ttu-id="5683d-162">Pour forcer l’insertion d' Key-Frame</span><span class="sxs-lookup"><span data-stu-id="5683d-162">To Force Key-Frame Insertion</span></span>](to-force-key-frame-insertion.md)           | <span data-ttu-id="5683d-163">Décrit comment forcer manuellement le codec à encoder un exemple en tant qu’image clé.</span><span class="sxs-lookup"><span data-stu-id="5683d-163">Describes how to manually force the codec to encode a sample as a key frame.</span></span>                           |
| [<span data-ttu-id="5683d-164">Pour gérer la latence de l’enregistreur</span><span class="sxs-lookup"><span data-stu-id="5683d-164">To Manage Writer Latency</span></span>](to-manage-writer-latency.md)                   | <span data-ttu-id="5683d-165">Décrit comment réduire le temps nécessaire au Writer pour traiter des exemples dans un fichier ou un récepteur de sortie.</span><span class="sxs-lookup"><span data-stu-id="5683d-165">Describes how to minimize the time it takes the writer to process samples into an output file or sink.</span></span> |
| [<span data-ttu-id="5683d-166">Utilisation des récepteurs d’écriture</span><span class="sxs-lookup"><span data-stu-id="5683d-166">Working with Writer Sinks</span></span>](working-with-writer-sinks.md)                 | <span data-ttu-id="5683d-167">Décrit comment utiliser des récepteurs d’enregistreur pour distribuer votre contenu à des fichiers ou à des emplacements réseau.</span><span class="sxs-lookup"><span data-stu-id="5683d-167">Describes how to use writer sinks to deliver your content to files or network locations.</span></span>               |
| [<span data-ttu-id="5683d-168">Pour connaître les statistiques de l’enregistreur</span><span class="sxs-lookup"><span data-stu-id="5683d-168">To Get Writer Statistics</span></span>](to-get-writer-statistics.md)                   | <span data-ttu-id="5683d-169">Décrit comment obtenir des statistiques pour l’enregistreur.</span><span class="sxs-lookup"><span data-stu-id="5683d-169">Describes how to get statistics for the writer.</span></span>                                                        |
| [<span data-ttu-id="5683d-170">Pour utiliser l’enregistreur Postview</span><span class="sxs-lookup"><span data-stu-id="5683d-170">To Use Writer Postview</span></span>](to-use-writer-postview.md)                       | <span data-ttu-id="5683d-171">Décrit comment obtenir des exemples non compressés quand vous écrivez un fichier à des fins de vérification.</span><span class="sxs-lookup"><span data-stu-id="5683d-171">Describes how to get uncompressed samples as you write a file for verification.</span></span>                        |



 

## <a name="related-topics"></a><span data-ttu-id="5683d-172">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5683d-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5683d-173">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="5683d-173">**Programming Guide**</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="5683d-174">**Récepteur de fichiers d’auteur, objet**</span><span class="sxs-lookup"><span data-stu-id="5683d-174">**Writer File Sink Object**</span></span>](writer-file-sink-object.md)
</dt> <dt>

[<span data-ttu-id="5683d-175">**Objet récepteur réseau de l’enregistreur**</span><span class="sxs-lookup"><span data-stu-id="5683d-175">**Writer Network Sink Object**</span></span>](writer-network-sink-object.md)
</dt> <dt>

[<span data-ttu-id="5683d-176">**Auteur, objet**</span><span class="sxs-lookup"><span data-stu-id="5683d-176">**Writer Object**</span></span>](writer-object.md)
</dt> </dl>

 

 




