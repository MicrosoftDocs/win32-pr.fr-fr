---
title: Utilisation de récepteurs de fichiers
description: Utilisation de récepteurs de fichiers
ms.assetid: 0cc4320a-c975-452d-bd1c-394d43bd4585
keywords:
- ASF (Advanced Systems Format), récepteurs de fichiers
- ASF (format des systèmes avancés), récepteurs de fichiers
- ASF (Advanced Systems Format), récepteurs
- ASF (format des systèmes avancés), récepteurs
- récepteurs, récepteurs de fichiers
- récepteurs de fichiers, à propos de
- récepteurs de fichiers, création
- récepteurs de fichiers, arrêt
- récepteurs de fichiers, démarrage
- récepteurs de fichiers, fermeture
- récepteurs, statistiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7a7f09a08788128719ea80a2a06d339f6398e6
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104101344"
---
# <a name="using-file-sinks"></a><span data-ttu-id="fb07a-114">Utilisation de récepteurs de fichiers</span><span class="sxs-lookup"><span data-stu-id="fb07a-114">Using File Sinks</span></span>

<span data-ttu-id="fb07a-115">Dans des circonstances normales, vous pouvez simplement transmettre à l’enregistreur un nom de fichier de sortie à l’aide de la méthode [**IWMWriter :: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) , et l’objet enregistreur écrira automatiquement le fichier sur le disque.</span><span class="sxs-lookup"><span data-stu-id="fb07a-115">Under normal circumstances, you can simply pass the writer an output file name using the [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) method, and the writer object will write the file to disk automatically.</span></span> <span data-ttu-id="fb07a-116">Dans ce cas, l’enregistreur crée et contrôle un objet récepteur de fichiers de writer qui gère l’écriture du fichier sur le disque.</span><span class="sxs-lookup"><span data-stu-id="fb07a-116">In this case, the writer is actually creating and controlling a writer file sink object that handles writing the file to disk.</span></span> <span data-ttu-id="fb07a-117">Un objet récepteur de fichiers du writer contrôle le déroulement des données de l’objet Writer dans un fichier unique.</span><span class="sxs-lookup"><span data-stu-id="fb07a-117">A writer file sink object controls the flow of data from the writer object to a single file.</span></span>

<span data-ttu-id="fb07a-118">Vous pouvez créer vos propres récepteurs de fichiers pour mieux contrôler la façon dont le récepteur écrit le fichier.</span><span class="sxs-lookup"><span data-stu-id="fb07a-118">You can create your own file sinks to get more control over how the sink writes the file.</span></span> <span data-ttu-id="fb07a-119">Vous pouvez également accéder au récepteur de fichiers du writer par défaut créé par le writer en réponse à un appel à **SetOutputFilename**.</span><span class="sxs-lookup"><span data-stu-id="fb07a-119">You can also access the default writer file sink created by the writer in response to a call to **SetOutputFilename**.</span></span>

## <a name="creating-file-sinks"></a><span data-ttu-id="fb07a-120">Création de récepteurs de fichiers</span><span class="sxs-lookup"><span data-stu-id="fb07a-120">Creating File Sinks</span></span>

<span data-ttu-id="fb07a-121">Pour créer un récepteur de fichiers et l’ajouter au writer, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="fb07a-121">To create a file sink and add it to the writer, perform the following steps.</span></span>

1.  <span data-ttu-id="fb07a-122">Créez un récepteur en appelant la fonction [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink) .</span><span class="sxs-lookup"><span data-stu-id="fb07a-122">Create a new sink by calling the [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink) function.</span></span>
2.  <span data-ttu-id="fb07a-123">Fournissez un nom de fichier pour le récepteur en appelant [**IWMWriterFileSink :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open).</span><span class="sxs-lookup"><span data-stu-id="fb07a-123">Supply a file name for the sink by calling [**IWMWriterFileSink::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open).</span></span>
3.  <span data-ttu-id="fb07a-124">Ajoutez le récepteur de fichiers au writer en appelant [**IWMWriterAdvanced :: AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink).</span><span class="sxs-lookup"><span data-stu-id="fb07a-124">Add the file sink to the writer by calling [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink).</span></span>
4.  <span data-ttu-id="fb07a-125">Effectuez l’écriture de la manière habituelle.</span><span class="sxs-lookup"><span data-stu-id="fb07a-125">Perform writing in the usual way.</span></span>
5.  <span data-ttu-id="fb07a-126">Une fois l’écriture terminée, le récepteur ferme automatiquement le fichier.</span><span class="sxs-lookup"><span data-stu-id="fb07a-126">After writing is completed, the sink will close the file automatically.</span></span>

## <a name="stopping-and-starting-file-sinks"></a><span data-ttu-id="fb07a-127">Arrêt et démarrage des récepteurs de fichiers</span><span class="sxs-lookup"><span data-stu-id="fb07a-127">Stopping and Starting File Sinks</span></span>

<span data-ttu-id="fb07a-128">Une fois les opérations d’écriture commencées, vous pouvez arrêter l’écriture dans un récepteur de fichiers en appelant [**IWMWriterFileSink2 :: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop).</span><span class="sxs-lookup"><span data-stu-id="fb07a-128">After writing operations begin, you can stop writing to a file sink by calling [**IWMWriterFileSink2::Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop).</span></span>

<span data-ttu-id="fb07a-129">Il existe de nombreuses raisons possibles pour lesquelles vous souhaiteriez arrêter l’écriture dans un récepteur.</span><span class="sxs-lookup"><span data-stu-id="fb07a-129">There are many potential reasons why you would want to stop writing to a sink.</span></span> <span data-ttu-id="fb07a-130">Par exemple, si vous enregistrez à partir d’une source active, vous pouvez être intéressé uniquement par une partie du contenu.</span><span class="sxs-lookup"><span data-stu-id="fb07a-130">For example, if you are recording from a live source, you may only be interested in some of the content.</span></span>

<span data-ttu-id="fb07a-131">Vous pouvez reprendre l’écriture dans un récepteur de fichiers en appelant [**IWMWriterFileSink2 :: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start).</span><span class="sxs-lookup"><span data-stu-id="fb07a-131">You can resume writing to a file sink by calling [**IWMWriterFileSink2::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start).</span></span> <span data-ttu-id="fb07a-132">Les deux options **arrêter** et **Démarrer** utilisent des durées de présentation pour contrôler approximativement le moment où la commande est exécutée.</span><span class="sxs-lookup"><span data-stu-id="fb07a-132">Both **Stop** and **Start** use presentation times to control approximately when the command is executed.</span></span> <span data-ttu-id="fb07a-133">Vous pouvez utiliser les méthodes [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3) pour mieux contrôler les heures de démarrage et d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="fb07a-133">You can use the [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3) methods to gain more control over start and stop times.</span></span>

## <a name="closing-file-sinks"></a><span data-ttu-id="fb07a-134">Fermeture des récepteurs de fichiers</span><span class="sxs-lookup"><span data-stu-id="fb07a-134">Closing File Sinks</span></span>

<span data-ttu-id="fb07a-135">Normalement, un récepteur de fichiers est fermé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="fb07a-135">Normally, a file sink is closed automatically.</span></span> <span data-ttu-id="fb07a-136">Si vous avez terminé l’écriture dans un récepteur, mais que l’écriture d’opérations sur d’autres récepteurs se poursuit, vous devez fermer explicitement le récepteur pour conserver les ressources.</span><span class="sxs-lookup"><span data-stu-id="fb07a-136">If you are finished writing to a sink, but writing operations to other sinks are continuing, you should explicitly close the sink to conserve resources.</span></span> <span data-ttu-id="fb07a-137">Pour fermer un récepteur de fichiers, appelez [**IWMWriterFileSink2 :: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close).</span><span class="sxs-lookup"><span data-stu-id="fb07a-137">To close a file sink, call [**IWMWriterFileSink2::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close).</span></span>

## <a name="getting-sink-statistics"></a><span data-ttu-id="fb07a-138">Obtention des statistiques du récepteur</span><span class="sxs-lookup"><span data-stu-id="fb07a-138">Getting Sink Statistics</span></span>

<span data-ttu-id="fb07a-139">Vous pouvez obtenir la taille de fichier et la durée d’un récepteur ouvert en appelant [**IWMWriterFileSink2 :: GetFileSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfilesize) et [**IWMWriterFileSink2 :: GetFileDuration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfileduration) respectivement.</span><span class="sxs-lookup"><span data-stu-id="fb07a-139">You can get the file size and duration for an open sink by calling [**IWMWriterFileSink2::GetFileSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfilesize) and [**IWMWriterFileSink2::GetFileDuration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfileduration) respectively.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb07a-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fb07a-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb07a-141">**Interface IWMWriterFileSink**</span><span class="sxs-lookup"><span data-stu-id="fb07a-141">**IWMWriterFileSink Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)
</dt> <dt>

[<span data-ttu-id="fb07a-142">**Interface IWMWriterFileSink2**</span><span class="sxs-lookup"><span data-stu-id="fb07a-142">**IWMWriterFileSink2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)
</dt> <dt>

[<span data-ttu-id="fb07a-143">**Interface IWMWriterFileSink3**</span><span class="sxs-lookup"><span data-stu-id="fb07a-143">**IWMWriterFileSink3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)
</dt> <dt>

[<span data-ttu-id="fb07a-144">**Récepteur de fichiers d’auteur, objet**</span><span class="sxs-lookup"><span data-stu-id="fb07a-144">**Writer File Sink Object**</span></span>](writer-file-sink-object.md)
</dt> <dt>

[<span data-ttu-id="fb07a-145">**Écriture de fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="fb07a-145">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




