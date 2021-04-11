---
title: Présentation du gestionnaire de téléchargement
description: Présentation du gestionnaire de téléchargement
ms.assetid: a13435ac-3784-4d4c-ba49-a51e373a2874
keywords:
- Windows Media Player Online stores, gestionnaire de téléchargement
- magasins en ligne, gestionnaire de téléchargement
- tapez 2 magasins en ligne, gestionnaire de téléchargement
- Windows Media Player Online stores, téléchargement en temps réel
- magasins en ligne, téléchargement en temps réel
- tapez 2 magasins en ligne, téléchargement en temps réel
- Windows Media Player Online stores, téléchargement en arrière-plan
- magasins en ligne, téléchargement en arrière-plan
- tapez 2 magasins en ligne, téléchargement en arrière-plan
- Lecteur Windows Media, gestionnaire de téléchargement
- Gestionnaire de téléchargement du lecteur Windows Media
- Gestionnaire de téléchargement
- Téléchargement en temps réel
- Téléchargement en arrière-plan
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b709df13e239b0fbd7f5c5403998b8c996c228d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029755"
---
# <a name="download-manager-overview"></a><span data-ttu-id="ffd86-117">Présentation du gestionnaire de téléchargement</span><span class="sxs-lookup"><span data-stu-id="ffd86-117">Download Manager Overview</span></span>

<span data-ttu-id="ffd86-118">Le lecteur Microsoft Windows Media fournit des volets des tâches de la boutique en ligne qui contiennent une fenêtre de navigateur hébergée.</span><span class="sxs-lookup"><span data-stu-id="ffd86-118">Microsoft Windows Media Player provides online store task panes that contain a hosted browser window.</span></span> <span data-ttu-id="ffd86-119">Grâce aux magasins en ligne, les utilisateurs peuvent interagir avec les pages Web du magasin en ligne sur Internet.</span><span class="sxs-lookup"><span data-stu-id="ffd86-119">Through the online stores, users can interact with online store webpages across the Internet.</span></span>

<span data-ttu-id="ffd86-120">Le gestionnaire de téléchargement du lecteur Windows Media fournit un modèle d’objet que vous pouvez utiliser pour gérer les tâches associées au téléchargement de contenu sur l’ordinateur de l’utilisateur à partir de Microsoft Internet Information Services (IIS) à l’aide du protocole HTTP (Hypertext Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="ffd86-120">The Windows Media Player Download Manager provides an object model that you can use to handle the tasks associated with downloading content to the user's computer from Microsoft Internet Information Services (IIS) using Hypertext Transfer Protocol (HTTP).</span></span> <span data-ttu-id="ffd86-121">Avec le gestionnaire de téléchargement, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="ffd86-121">With the Download Manager, you can:</span></span>

-   <span data-ttu-id="ffd86-122">Gérer plusieurs téléchargements simultanément en tant que collection.</span><span class="sxs-lookup"><span data-stu-id="ffd86-122">Manage multiple downloads simultaneously as a collection.</span></span>
-   <span data-ttu-id="ffd86-123">Spécifiez une URL pour un fichier et démarrez le téléchargement à l’aide de HTTP.</span><span class="sxs-lookup"><span data-stu-id="ffd86-123">Specify a URL for a file and start it downloading using HTTP.</span></span>
-   <span data-ttu-id="ffd86-124">Recherchez l’État et la progression du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="ffd86-124">Query for the download state and progress.</span></span>
-   <span data-ttu-id="ffd86-125">Suspendre, reprendre ou annuler un téléchargement.</span><span class="sxs-lookup"><span data-stu-id="ffd86-125">Pause, resume, or cancel a download.</span></span>
-   <span data-ttu-id="ffd86-126">Spécifiez si un téléchargement est effectué en arrière-plan ou en temps réel.</span><span class="sxs-lookup"><span data-stu-id="ffd86-126">Specify whether a download occurs in the background or in real time.</span></span> <span data-ttu-id="ffd86-127">(Le téléchargement en arrière-plan est uniquement disponible sur le système d’exploitation Microsoft Windows XP.) Consultez [à propos du téléchargement en temps réel et en arrière-plan](#about-background-and-real-time-downloading).</span><span class="sxs-lookup"><span data-stu-id="ffd86-127">(Background downloading is only available on the Microsoft Windows XP operating system.) See [About Background and Real-time Downloading](#about-background-and-real-time-downloading).</span></span>
-   <span data-ttu-id="ffd86-128">Spécifiez le mode d’affichage du contenu dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="ffd86-128">Specify how content is displayed in the library.</span></span> <span data-ttu-id="ffd86-129">Consultez [à propos de l’intégration de la bibliothèque](#about-library-integration).</span><span class="sxs-lookup"><span data-stu-id="ffd86-129">See [About Library Integration](#about-library-integration).</span></span>

<span data-ttu-id="ffd86-130">Le gestionnaire de téléchargement est la solution permettant de télécharger du contenu à partir de code de script dans des pages hébergées sur des pages Web.</span><span class="sxs-lookup"><span data-stu-id="ffd86-130">The Download Manager is the solution for downloading content from script code in hosted webpages.</span></span> <span data-ttu-id="ffd86-131">Pour télécharger du contenu à l’aide de code C++, utilisez le Service de transfert intelligent en arrière-plan Windows XP (BITS).</span><span class="sxs-lookup"><span data-stu-id="ffd86-131">To download content using C++ code, use the Windows XP Background Intelligent Transfer Service (BITS).</span></span> <span data-ttu-id="ffd86-132">Pour plus d’informations, consultez [bits](bits.md).</span><span class="sxs-lookup"><span data-stu-id="ffd86-132">For more information, see [BITS](bits.md).</span></span>

## <a name="about-background-and-real-time-downloading"></a><span data-ttu-id="ffd86-133">À propos du téléchargement en temps réel et en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="ffd86-133">About Background and Real-time Downloading</span></span>

<span data-ttu-id="ffd86-134">Le gestionnaire de téléchargement offre deux types de téléchargements : arrière-plan et en temps réel.</span><span class="sxs-lookup"><span data-stu-id="ffd86-134">The Download Manager offers two types of downloading: background and real-time.</span></span> <span data-ttu-id="ffd86-135">Le type que vous utilisez dépend de vous, et il est possible de permettre à l’utilisateur de sélectionner également le type de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="ffd86-135">Which type you use is up to you, and it is possible to allow the user to select the download type as well.</span></span> <span data-ttu-id="ffd86-136">Si vous choisissez d’autoriser l’utilisateur à sélectionner le type de téléchargement, veillez à expliquer les différences entre les deux types disponibles.</span><span class="sxs-lookup"><span data-stu-id="ffd86-136">If you choose to allow the user to select the download type, be sure to explain the differences between the two available types.</span></span>

<span data-ttu-id="ffd86-137">Le téléchargement en temps réel a lieu en même temps.</span><span class="sxs-lookup"><span data-stu-id="ffd86-137">Real-time downloading occurs all at once.</span></span> <span data-ttu-id="ffd86-138">Lorsque l’utilisateur démarre un téléchargement de fichier, le fichier entier est transféré à l’ordinateur de l’utilisateur dans un seul flux continu.</span><span class="sxs-lookup"><span data-stu-id="ffd86-138">When the user starts a file download, the entire file is transferred to the user's computer in a single, continuous stream.</span></span> <span data-ttu-id="ffd86-139">L’utilisateur ne peut pas suspendre ou interrompre le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="ffd86-139">The user cannot pause or otherwise interrupt the download.</span></span> <span data-ttu-id="ffd86-140">Si l’utilisateur choisit de fermer le lecteur Windows Media avant la fin du téléchargement, il perd tous les fichiers incomplets et doit les télécharger depuis le début pour obtenir le contenu.</span><span class="sxs-lookup"><span data-stu-id="ffd86-140">If the user chooses to close Windows Media Player before the download is finished, he or she loses any incomplete files and must download them from the beginning to acquire the content.</span></span>

<span data-ttu-id="ffd86-141">Le principal avantage du téléchargement en temps réel est qu’il permet à l’utilisateur d’acquérir le contenu plus rapidement que le téléchargement en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="ffd86-141">The main advantage of real-time downloading is that it allows the user to acquire the content faster than background downloading.</span></span> <span data-ttu-id="ffd86-142">Le téléchargement en temps réel est disponible pour les utilisateurs de Windows XP, mais il s’agit du seul type de téléchargement disponible sur les versions du système d’exploitation Windows antérieures à Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ffd86-142">Real-time downloading is available to users of Windows XP, but it is the only type of downloading available on versions of the Windows operating system prior to Windows XP.</span></span>

<span data-ttu-id="ffd86-143">Le téléchargement en arrière-plan s’effectue de manière fragmentaire.</span><span class="sxs-lookup"><span data-stu-id="ffd86-143">Background downloading happens in a piecemeal fashion.</span></span> <span data-ttu-id="ffd86-144">Lorsque l’utilisateur démarre un téléchargement en arrière-plan, certaines parties du fichier sont transférées sur l’ordinateur de l’utilisateur lorsque le temps processeur est disponible.</span><span class="sxs-lookup"><span data-stu-id="ffd86-144">When the user starts a background download, parts of the file are transferred to the user's computer when processor time is available.</span></span> <span data-ttu-id="ffd86-145">Il est possible de suspendre et de reprendre un téléchargement en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="ffd86-145">It is possible to pause and resume a background download.</span></span> <span data-ttu-id="ffd86-146">Si l’utilisateur choisit de fermer le lecteur Windows Media avant la fin du téléchargement en arrière-plan, la condition de tous les fichiers incomplets est enregistrée et le téléchargement peut continuer en arrière-plan, même après le redémarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ffd86-146">If the user chooses to close Windows Media Player before background downloading is finished, the condition of any incomplete files is saved and the downloading can continue in the background, even after restarting the computer.</span></span>

<span data-ttu-id="ffd86-147">Le téléchargement en arrière-plan peut prendre plus de temps que le téléchargement en temps réel, car le processus de téléchargement ne se produit que lorsque le processeur n’effectue pas d’autres tâches.</span><span class="sxs-lookup"><span data-stu-id="ffd86-147">Background downloading can take longer than real-time downloading because the download process only happens when the processor is not performing other tasks.</span></span>

<span data-ttu-id="ffd86-148">Le téléchargement en arrière-plan est disponible uniquement lors de l’utilisation de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ffd86-148">Background downloading is only available when using Windows XP.</span></span>

## <a name="about-library-integration"></a><span data-ttu-id="ffd86-149">À propos de l’intégration de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ffd86-149">About Library Integration</span></span>

<span data-ttu-id="ffd86-150">Le lecteur Windows Media peut automatiquement organiser le contenu de la boutique en ligne dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="ffd86-150">Windows Media Player can automatically organize online store content in the library.</span></span> <span data-ttu-id="ffd86-151">Pour ce faire, vous devez spécifier une valeur pour l’attribut **WM/ContentDistributor** pour chaque fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="ffd86-151">To enable this, you must specify a value for the **WM/ContentDistributor** attribute for each digital media file.</span></span> <span data-ttu-id="ffd86-152">Lorsqu’un fichier multimédia numérique est ajouté à la bibliothèque, ce qui se produit automatiquement lors de l’utilisation du gestionnaire de téléchargement, le fichier est automatiquement listé dans le nœud **musique achetée** ou **vidéos achetées** .</span><span class="sxs-lookup"><span data-stu-id="ffd86-152">When a digital media file is added to the library, which happens automatically when using the Download Manager, the file is listed in the **Purchased Music** or **Purchased Videos** node automatically.</span></span> <span data-ttu-id="ffd86-153">Par exemple, si la valeur de **WM/ContentDistributor** est « Proseware » et que le fichier multimédia numérique contient musique, le contenu apparaît dans la bibliothèque à l’emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="ffd86-153">For example, if the value for **WM/ContentDistributor** is "Proseware" and the digital media file contains music, the content would appear in the library in the following location:</span></span>

<span data-ttu-id="ffd86-154">Toute la musique/musique achetée/Proseware</span><span class="sxs-lookup"><span data-stu-id="ffd86-154">All Music/Purchased Music/Proseware</span></span>

## <a name="related-topics"></a><span data-ttu-id="ffd86-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ffd86-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffd86-156">**Gestionnaire de téléchargement**</span><span class="sxs-lookup"><span data-stu-id="ffd86-156">**Download Manager**</span></span>](download-manager.md)
</dt> <dt>

[<span data-ttu-id="ffd86-157">**DownloadCollection.startDownload**</span><span class="sxs-lookup"><span data-stu-id="ffd86-157">**DownloadCollection.startDownload**</span></span>](downloadcollection-startdownload.md)
</dt> </dl>

 

 




