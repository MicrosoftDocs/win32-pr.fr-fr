---
title: Récepteurs
description: Récepteurs
ms.assetid: 6781a326-a30a-4d4d-96db-332d0f681a31
keywords:
- Windows Media Format SDK, récepteurs
- Windows Media Format SDK, récepteurs de fichiers
- ASF (Advanced Systems Format), récepteurs
- ASF (format des systèmes avancés), récepteurs
- ASF (Advanced Systems Format), récepteurs de fichiers
- ASF (format des systèmes avancés), récepteurs de fichiers
- Windows Media Format SDK, récepteurs réseau
- Windows Media Format SDK, récepteurs Push
- ASF (Advanced Systems Format), récepteurs réseau
- ASF (format des systèmes avancés), récepteurs réseau
- ASF (Advanced Systems Format), récepteurs Push
- ASF (format avancé des systèmes), récepteurs Push
- récepteurs, à propos de
- récepteurs de fichiers, à propos de
- récepteurs réseau
- récepteurs Push
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a62548f159172f58d4f52b0289c5adbfef02f55
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030828"
---
# <a name="sinks"></a><span data-ttu-id="99fff-119">Récepteurs</span><span class="sxs-lookup"><span data-stu-id="99fff-119">Sinks</span></span>

<span data-ttu-id="99fff-120">L’objet Writer du kit de développement logiciel (SDK) du format Windows Media fournit le contenu traité aux récepteurs.</span><span class="sxs-lookup"><span data-stu-id="99fff-120">The writer object of the Windows Media Format SDK delivers processed content to sinks.</span></span> <span data-ttu-id="99fff-121">Chaque récepteur est un objet qui fournit des données.</span><span class="sxs-lookup"><span data-stu-id="99fff-121">Each sink is an object that delivers data.</span></span> <span data-ttu-id="99fff-122">Le point de remise dépend du type de récepteur.</span><span class="sxs-lookup"><span data-stu-id="99fff-122">The point of delivery depends upon the type of sink.</span></span> <span data-ttu-id="99fff-123">Il existe trois types de récepteurs : les récepteurs de fichiers, les récepteurs réseau et les récepteurs de notifications push.</span><span class="sxs-lookup"><span data-stu-id="99fff-123">There are three types of sinks: file sinks, network sinks, and push sinks.</span></span>

## <a name="file-sinks"></a><span data-ttu-id="99fff-124">Récepteurs de fichiers</span><span class="sxs-lookup"><span data-stu-id="99fff-124">File Sinks</span></span>

<span data-ttu-id="99fff-125">Les récepteurs de fichiers écrivent du contenu ASF dans un fichier sur un lecteur local ou réseau.</span><span class="sxs-lookup"><span data-stu-id="99fff-125">File sinks write ASF content to a file on a local or network drive.</span></span> <span data-ttu-id="99fff-126">Lorsque vous utilisez l’objet Writer pour écrire un fichier sans ajouter explicitement un récepteur de fichiers, le writer en crée un pour vous en utilisant le nom que vous transmettez à [**IWMWriter :: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename).</span><span class="sxs-lookup"><span data-stu-id="99fff-126">When you use the writer object to write a file without explicitly adding a file sink, the writer will create one for you using the name you pass to [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename).</span></span> <span data-ttu-id="99fff-127">Vous pouvez assigner plusieurs récepteurs de fichiers à un objet Writer pour écrire le contenu dans plusieurs fichiers à la fois.</span><span class="sxs-lookup"><span data-stu-id="99fff-127">You can assign multiple file sinks to a writer object to write the content in several files at once.</span></span>

<span data-ttu-id="99fff-128">À l’aide d’un récepteur de fichiers, vous pouvez contrôler de nombreux aspects du fichier.</span><span class="sxs-lookup"><span data-stu-id="99fff-128">By using a file sink, you can control many aspects of the file.</span></span> <span data-ttu-id="99fff-129">Les fonctionnalités suivantes sont disponibles via un récepteur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="99fff-129">The following features are available through a file sink.</span></span>

-   <span data-ttu-id="99fff-130">Analyse des statistiques de fichiers.</span><span class="sxs-lookup"><span data-stu-id="99fff-130">File statistics monitoring.</span></span> <span data-ttu-id="99fff-131">Vous pouvez surveiller la taille et la durée des fichiers au fur et à mesure de leur création.</span><span class="sxs-lookup"><span data-stu-id="99fff-131">You can monitor the file size and duration as it is being created.</span></span>
-   <span data-ttu-id="99fff-132">Création partielle du fichier de contenu.</span><span class="sxs-lookup"><span data-stu-id="99fff-132">Partial content file creation.</span></span> <span data-ttu-id="99fff-133">Les récepteurs de fichiers peuvent être configurés pour commencer à écrire du contenu à un moment donné et pour terminer l’écriture à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="99fff-133">File sinks can be configured to begin writing content at a specific time and to end writing at a specific time.</span></span> <span data-ttu-id="99fff-134">Cela vous permet de créer plusieurs fichiers contenant différentes sections du même contenu dans le même test d’écriture.</span><span class="sxs-lookup"><span data-stu-id="99fff-134">This enables you to create multiple files containing different sections of the same content in the same writing pass.</span></span>

## <a name="network-sinks"></a><span data-ttu-id="99fff-135">Récepteurs réseau</span><span class="sxs-lookup"><span data-stu-id="99fff-135">Network Sinks</span></span>

<span data-ttu-id="99fff-136">Les récepteurs réseau diffusent du contenu vers une adresse réseau.</span><span class="sxs-lookup"><span data-stu-id="99fff-136">Network sinks broadcast content to a network address.</span></span> <span data-ttu-id="99fff-137">La lecture des clients peut se connecter à l’adresse pour recevoir la diffusion.</span><span class="sxs-lookup"><span data-stu-id="99fff-137">Reading clients can connect to the address to receive the broadcast.</span></span>

## <a name="push-sinks"></a><span data-ttu-id="99fff-138">Récepteurs Push</span><span class="sxs-lookup"><span data-stu-id="99fff-138">Push Sinks</span></span>

<span data-ttu-id="99fff-139">Les récepteurs de notifications push délivrent le contenu du writer à un serveur exécutant Windows Media Services.</span><span class="sxs-lookup"><span data-stu-id="99fff-139">Push sinks deliver content from the writer to a server running Windows Media Services.</span></span> <span data-ttu-id="99fff-140">Les récepteurs de notifications push sont généralement utilisés dans les scénarios où un ordinateur encode le contenu dynamique et le remet à un ou plusieurs serveurs pour une distribution étendue.</span><span class="sxs-lookup"><span data-stu-id="99fff-140">Push sinks are typically used in scenarios where one computer encodes live content and delivers it to one or more servers for wide distribution.</span></span> <span data-ttu-id="99fff-141">L’utilisation d’un récepteur de notifications Push vous permet de dédier des ordinateurs à des tâches spécifiques, économisant ainsi la bande passante et la puissance de traitement sur chaque serveur.</span><span class="sxs-lookup"><span data-stu-id="99fff-141">Using a push sink enables you to dedicate computers to specific tasks, saving bandwidth and processing power on each server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99fff-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="99fff-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99fff-143">**Fonctionnalités d’écriture de fichier**</span><span class="sxs-lookup"><span data-stu-id="99fff-143">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="99fff-144">**Utilisation des récepteurs d’écriture**</span><span class="sxs-lookup"><span data-stu-id="99fff-144">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




