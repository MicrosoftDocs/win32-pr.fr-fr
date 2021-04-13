---
title: Fonctionnalités de lecture de fichier
description: Fonctionnalités de lecture de fichier
ms.assetid: ba6dd328-2250-4867-94e0-f66c70ac1bac
keywords:
- Windows Media Format SDK, fonctionnalités de lecture de fichiers
- Windows Media Format SDK, lecture asynchrone des fichiers
- Windows Media Format SDK, lecture synchrone de fichiers
- ASF (Advanced Systems Format), fonctionnalités de lecture de fichiers
- ASF (format des systèmes avancés), fonctionnalités de lecture de fichiers
- ASF (Advanced Systems Format), lecture asynchrone des fichiers
- ASF (format de systèmes avancés), lecture de fichier asynchrone
- ASF (Advanced Systems Format), lecture synchrone des fichiers
- ASF (format avancé des systèmes), lecture synchrone des fichiers
- lecture asynchrone de fichiers
- lecture synchrone de fichiers
- lecteurs synchrones, fonctionnalités de lecture de fichiers
- lecture du fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83d3ce112d0d9e47626b4f7850f760da5c6583e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311269"
---
# <a name="file-reading-features"></a><span data-ttu-id="617e3-116">Fonctionnalités de lecture de fichier</span><span class="sxs-lookup"><span data-stu-id="617e3-116">File Reading Features</span></span>

<span data-ttu-id="617e3-117">La lecture des fichiers ASF est l’une des principales fonctionnalités du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="617e3-117">Reading ASF files is one of the primary features of the Windows Media Format SDK.</span></span> <span data-ttu-id="617e3-118">Deux types de lecture sont pris en charge : asynchrone et synchrone.</span><span class="sxs-lookup"><span data-stu-id="617e3-118">Two types of reading are supported: asynchronous and synchronous.</span></span> <span data-ttu-id="617e3-119">La lecture asynchrone des fichiers est gérée par l’objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="617e3-119">Asynchronous file reading is handled by the reader object.</span></span> <span data-ttu-id="617e3-120">L’objet lecteur synchrone est utilisé pour lire les fichiers de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="617e3-120">The synchronous reader object is used to read files synchronously.</span></span> <span data-ttu-id="617e3-121">Pour plus d’informations sur les différents objets de lecture, consultez [objet lecteur](reader-object.md) et [objet lecteur synchrone](synchronous-reader-object.md).</span><span class="sxs-lookup"><span data-stu-id="617e3-121">For more information about the different reading objects, see [Reader Object](reader-object.md) and [Synchronous Reader Object](synchronous-reader-object.md).</span></span>

<span data-ttu-id="617e3-122">Dans le scénario de lecture de fichier asynchrone le plus basique, vous devez implémenter une méthode de rappel que l’objet lecteur appellera quand les exemples sont prêts.</span><span class="sxs-lookup"><span data-stu-id="617e3-122">In the most basic asynchronous file reading scenario, you must implement a callback method that the reader object will call when samples are ready.</span></span> <span data-ttu-id="617e3-123">Une fois que vous avez commencé à lire un fichier, votre application attend que les exemples soient remis à votre méthode de rappel.</span><span class="sxs-lookup"><span data-stu-id="617e3-123">After you begin reading a file, your application waits for the samples to be delivered to your callback method.</span></span> <span data-ttu-id="617e3-124">La lecture asynchrone est utile pour les applications de lecteur et prend en charge les fonctionnalités non disponibles avec la lecture synchrone.</span><span class="sxs-lookup"><span data-stu-id="617e3-124">Asynchronous reading is useful for player applications, and supports features not available with synchronous reading.</span></span> <span data-ttu-id="617e3-125">Si votre application a besoin de lire des fichiers à partir d’un emplacement réseau ou d’interagir avec un serveur exécutant Windows Media Services, vous devez utiliser l’objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="617e3-125">If your application needs to read files from a network location, or interact with a server running Windows Media Services, you must use the reader object.</span></span> <span data-ttu-id="617e3-126">L’inconvénient de l’objet lecteur est qu’un thread distinct est utilisé pour chaque sortie fournie.</span><span class="sxs-lookup"><span data-stu-id="617e3-126">The disadvantage of the reader object is that a separate thread is used for each output delivered.</span></span> <span data-ttu-id="617e3-127">En outre, l’objet lecteur n’est pas aussi flexible que le lecteur synchrone dans la manière dont il peut fournir des exemples.</span><span class="sxs-lookup"><span data-stu-id="617e3-127">Additionally, the reader object is not as flexible as the synchronous reader in how it can deliver samples.</span></span>

<span data-ttu-id="617e3-128">Avec le lecteur synchrone, vous n’avez pas besoin d’utiliser de méthodes de rappel.</span><span class="sxs-lookup"><span data-stu-id="617e3-128">With the synchronous reader you do not need to use any callback methods.</span></span> <span data-ttu-id="617e3-129">Au lieu de cela, vous sélectionnez une partie du fichier pour lire et récupérer les exemples un par un avec les appels de méthode.</span><span class="sxs-lookup"><span data-stu-id="617e3-129">Instead, you select a portion of the file to read and retrieve the samples one at a time with method calls.</span></span> <span data-ttu-id="617e3-130">Le lecteur synchrone est bien adapté aux besoins des applications de modification de contenu, où l’accès rapide à des exemples spécifiques est essentiel.</span><span class="sxs-lookup"><span data-stu-id="617e3-130">The synchronous reader is well suited to the needs of content-editing applications, where quick access to specific samples is essential.</span></span> <span data-ttu-id="617e3-131">Étant donné qu’aucune méthode de rappel n’est utilisée par le lecteur synchrone, vous pouvez créer des applications pour lire les fichiers ASF avec un minimum de surcharge de codage.</span><span class="sxs-lookup"><span data-stu-id="617e3-131">Because no callback methods are used by the synchronous reader, you can create applications to read ASF files with a minimum of coding overhead.</span></span> <span data-ttu-id="617e3-132">Toutefois, le lecteur synchrone ne peut pas ouvrir un fichier à partir d’un emplacement réseau ou interagir avec un serveur exécutant Windows Media Services ou lire des fichiers protégés par [*DRM*](wmformat-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="617e3-132">However, the synchronous reader cannot open a file from a network location, or interact with a server running Windows Media Services, or read files protected with [*DRM*](wmformat-glossary.md).</span></span>

<span data-ttu-id="617e3-133">Les rubriques suivantes décrivent les fonctionnalités du lecteur et du lecteur synchrone.</span><span class="sxs-lookup"><span data-stu-id="617e3-133">The following topics discuss the features of the reader and the synchronous reader.</span></span>



| <span data-ttu-id="617e3-134">Rubrique</span><span class="sxs-lookup"><span data-stu-id="617e3-134">Topic</span></span>                                                              | <span data-ttu-id="617e3-135">Description</span><span class="sxs-lookup"><span data-stu-id="617e3-135">Description</span></span>                                                                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="617e3-136">Prise en charge de l’exemple alloué par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="617e3-136">User Allocated Sample Support</span></span>](user-allocated-sample-support.md) | <span data-ttu-id="617e3-137">Décrit l’allocation de mémoire tampon dans le lecteur et le lecteur synchrone, et comment l’allocation des utilisateurs peut améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="617e3-137">Discusses buffer allocation in the reader and synchronous reader, and how user allocation can improve performance.</span></span> |
| [<span data-ttu-id="617e3-138">Énumération de format de sortie</span><span class="sxs-lookup"><span data-stu-id="617e3-138">Output Format Enumeration</span></span>](output-format-enumeration.md)         | <span data-ttu-id="617e3-139">Présente l’énumération de format de sortie.</span><span class="sxs-lookup"><span data-stu-id="617e3-139">Discusses output format enumeration.</span></span>                                                                               |



 

<span data-ttu-id="617e3-140">En outre, les rubriques suivantes de la section écriture des fonctionnalités s’appliquent également à la lecture de fichiers :</span><span class="sxs-lookup"><span data-stu-id="617e3-140">In addition, the following topics from the writing features section also apply to file reading:</span></span>

-   [<span data-ttu-id="617e3-141">Redimensionnement vidéo</span><span class="sxs-lookup"><span data-stu-id="617e3-141">Video Resizing</span></span>](video-resizing.md)
-   [<span data-ttu-id="617e3-142">Conversion de l’espace colorimétrique</span><span class="sxs-lookup"><span data-stu-id="617e3-142">Color Space Conversion</span></span>](color-space-conversion.md)
-   [<span data-ttu-id="617e3-143">Rééchantillonnage audio</span><span class="sxs-lookup"><span data-stu-id="617e3-143">Audio Resampling</span></span>](audio-resampling.md)

## <a name="related-topics"></a><span data-ttu-id="617e3-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="617e3-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="617e3-145">**Fonctionnalités**</span><span class="sxs-lookup"><span data-stu-id="617e3-145">**Features**</span></span>](features.md)
</dt> <dt>

[<span data-ttu-id="617e3-146">**Lecture des fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="617e3-146">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




