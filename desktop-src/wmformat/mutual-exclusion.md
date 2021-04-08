---
title: Exclusion mutuelle
description: Exclusion mutuelle
ms.assetid: 3a3f6763-a241-4bbd-a6e8-62041b05622d
keywords:
- Windows Media Format SDK, exclusion mutuelle
- ASF (Advanced Systems Format), exclusion mutuelle
- ASF (format des systèmes avancés), exclusion mutuelle
- Kit de développement logiciel (SDK) Windows Media format, exclusion mutuelle MBR
- ASF (Advanced Systems Format), exclusion mutuelle MBR
- ASF (format des systèmes avancés), exclusion mutuelle MBR
- Windows Media Format SDK, débit binaire multiple (MBR)
- ASF (Advanced Systems Format), à débit binaire multiple (MBR)
- ASF (format de systèmes avancés), débit binaire multiple (MBR)
- exclusion mutuelle, à propos de
- débit binaire multiple (MBR), exclusion mutuelle
- MBR (débit binaire multiple), exclusion mutuelle
- exclusion mutuelle, vitesse de transmission
- exclusion mutuelle, langue
- exclusion mutuelle, présentation
- exclusion mutuelle, inconnue
- exclusion mutuelle, fonctionnalités
- exclusion mutuelle, fonctionnalités avancées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd00bf5bcb544d2541a6bc5465171fe9bacc1b9c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840773"
---
# <a name="mutual-exclusion"></a><span data-ttu-id="338e9-121">Exclusion mutuelle</span><span class="sxs-lookup"><span data-stu-id="338e9-121">Mutual Exclusion</span></span>

<span data-ttu-id="338e9-122">Chaque fichier ASF contient un ou plusieurs flux, chacun contenant des données multimédias numériques.</span><span class="sxs-lookup"><span data-stu-id="338e9-122">Every ASF file contains one or more streams, each containing digital media data.</span></span> <span data-ttu-id="338e9-123">Dans des circonstances normales, chaque flux est associé à une seule sortie.</span><span class="sxs-lookup"><span data-stu-id="338e9-123">Under normal circumstances, each stream is associated with a single output.</span></span> <span data-ttu-id="338e9-124">Lors de la lecture, l’objet lecteur fournit des exemples pour chaque sortie.</span><span class="sxs-lookup"><span data-stu-id="338e9-124">On playback, the reader object delivers samples for each output.</span></span> <span data-ttu-id="338e9-125">Ainsi, par défaut, chaque flux d’un fichier ASF est remis par le lecteur lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="338e9-125">So, as a default, every stream in an ASF file is delivered by the reader on playback.</span></span>

<span data-ttu-id="338e9-126">Dans certains cas, vous ne souhaitez pas que tous les flux soient remis au client.</span><span class="sxs-lookup"><span data-stu-id="338e9-126">There are situations where you do not want every stream delivered to the client.</span></span> <span data-ttu-id="338e9-127">Par exemple, si vous créez un fichier vidéo avec cinq flux audio, un pour chacune des cinq langues, vous n’avez besoin que d’un seul d’entre eux à la fois.</span><span class="sxs-lookup"><span data-stu-id="338e9-127">For example, if you create a video file with five audio streams, one for each of five languages, you want only one of them to be delivered at a time.</span></span> <span data-ttu-id="338e9-128">L’exclusion mutuelle est une fonctionnalité du kit de développement logiciel (SDK) Windows Media format qui vous permet de spécifier un nombre de flux mutuellement exclusifs qui correspondent tous à la même sortie.</span><span class="sxs-lookup"><span data-stu-id="338e9-128">Mutual exclusion is a feature of the Windows Media Format SDK that enables you to specify a number of mutually exclusive streams that all equate to the same output.</span></span>

<span data-ttu-id="338e9-129">L’exclusion mutuelle est définie dans le profil utilisé pour créer un fichier.</span><span class="sxs-lookup"><span data-stu-id="338e9-129">Mutual exclusion is defined in the profile used to create a file.</span></span> <span data-ttu-id="338e9-130">Vous configurez l’exclusion mutuelle dans un profil à l’aide d’objets d’exclusion mutuelle.</span><span class="sxs-lookup"><span data-stu-id="338e9-130">You configure mutual exclusion in a profile by using mutual exclusion objects.</span></span> <span data-ttu-id="338e9-131">Vous ajoutez des flux un à la fois à l’objet exclusion mutuelle, définissez le type et incluez l’objet dans le profil.</span><span class="sxs-lookup"><span data-stu-id="338e9-131">You add streams one at a time to the mutual exclusion object, set the type, and include the object in the profile.</span></span>

<span data-ttu-id="338e9-132">Le kit de développement logiciel (SDK) Windows Media format reconnaît quatre types d’exclusion mutuelle :</span><span class="sxs-lookup"><span data-stu-id="338e9-132">The Windows Media Format SDK recognizes four types of mutual exclusion:</span></span>

-   <span data-ttu-id="338e9-133">Vitesse de transmission</span><span class="sxs-lookup"><span data-stu-id="338e9-133">Bit rate</span></span>
-   <span data-ttu-id="338e9-134">Language</span><span class="sxs-lookup"><span data-stu-id="338e9-134">Language</span></span>
-   <span data-ttu-id="338e9-135">Présentation</span><span class="sxs-lookup"><span data-stu-id="338e9-135">Presentation</span></span>
-   <span data-ttu-id="338e9-136">Unknown</span><span class="sxs-lookup"><span data-stu-id="338e9-136">Unknown</span></span>

## <a name="mutual-exclusion-by-bit-rate"></a><span data-ttu-id="338e9-137">Exclusion mutuelle par vitesse de transmission</span><span class="sxs-lookup"><span data-stu-id="338e9-137">Mutual Exclusion by Bit Rate</span></span>

<span data-ttu-id="338e9-138">L’exclusion mutuelle de la vitesse de transmission est un type spécial d’exclusion mutuelle qui est plus communément appelée exclusion mutuelle de la vitesse de transmission multiple (MBR).</span><span class="sxs-lookup"><span data-stu-id="338e9-138">Bit rate mutual exclusion is a special type of mutual exclusion and is more commonly referred to as multiple bit rate (MBR) mutual exclusion.</span></span> <span data-ttu-id="338e9-139">Une exclusion mutuelle MBR contient un certain nombre de flux qui proviennent de la même entrée, mais qui sont encodés à des vitesses de transmission différentes.</span><span class="sxs-lookup"><span data-stu-id="338e9-139">An MBR mutual exclusion contains a number of streams that all originate from the same input, but are encoded at different bit rates.</span></span> <span data-ttu-id="338e9-140">Lors de la lecture d’un fichier avec MBR, le lecteur détermine le meilleur flux à utiliser en fonction de la bande passante disponible.</span><span class="sxs-lookup"><span data-stu-id="338e9-140">When playing a file with MBR, the reader determines the best stream to use based on the available bandwidth.</span></span>

<span data-ttu-id="338e9-141">Le kit de développement logiciel (SDK) Windows Media format prend en charge MBR pour les flux audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="338e9-141">The Windows Media Format SDK supports MBR for audio and video streams.</span></span> <span data-ttu-id="338e9-142">Le kit de développement logiciel (SDK) prend également en charge un type spécial de vidéo MBR appelée plusieurs MBR de taille vidéo.</span><span class="sxs-lookup"><span data-stu-id="338e9-142">The SDK also supports a special type of MBR video called multiple video size MBR.</span></span> <span data-ttu-id="338e9-143">C’est comme une vidéo MBR normale, à la différence que les flux individuels peuvent avoir des tailles de frame différentes.</span><span class="sxs-lookup"><span data-stu-id="338e9-143">This is like normal MBR video except that the individual streams can have different frame sizes.</span></span> <span data-ttu-id="338e9-144">Par exemple, vous pouvez avoir des flux à la taille vidéo 320 x 240 par défaut et d’autres avec des taux de bits plus élevés et une taille vidéo de 640 x 480.</span><span class="sxs-lookup"><span data-stu-id="338e9-144">For example, you might have some streams at the default 320 x 240 video size and some others with higher bit rates and 640 x 480 video size.</span></span>

## <a name="mutual-exclusion-by-language"></a><span data-ttu-id="338e9-145">Exclusion mutuelle par langue</span><span class="sxs-lookup"><span data-stu-id="338e9-145">Mutual Exclusion by Language</span></span>

<span data-ttu-id="338e9-146">L’exclusion mutuelle basée sur le langage est conçue pour être utilisée avec du contenu (généralement audio) enregistré dans plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="338e9-146">Language-based mutual exclusion is designed for use with content (usually audio) recorded in several languages.</span></span> <span data-ttu-id="338e9-147">Une exclusion mutuelle basée sur le langage comprend plusieurs flux provenant d’entrées uniques.</span><span class="sxs-lookup"><span data-stu-id="338e9-147">A language-based mutual exclusion includes several streams that originate from unique inputs.</span></span> <span data-ttu-id="338e9-148">Chaque entrée est du même contenu, mais dans une langue différente.</span><span class="sxs-lookup"><span data-stu-id="338e9-148">Each input is the same content, but in a different language.</span></span>

<span data-ttu-id="338e9-149">Pour que l’exclusion mutuelle par langue fonctionne, l’application de lecture doit inclure une logique pour sélectionner la langue appropriée.</span><span class="sxs-lookup"><span data-stu-id="338e9-149">For mutual exclusion by language to work, the reading application must include logic to select the appropriate language.</span></span> <span data-ttu-id="338e9-150">Si vous écrivez une application pour lire des fichiers ASF et que vous souhaitez prendre en charge des fichiers avec l’exclusion mutuelle basée sur la langue, vous devez sélectionner le flux approprié avant de commencer la lecture.</span><span class="sxs-lookup"><span data-stu-id="338e9-150">If you write an application to play ASF files, and you want to support files with language-based mutual exclusion, you should select the appropriate stream before beginning playback.</span></span>

## <a name="mutual-exclusion-by-presentation"></a><span data-ttu-id="338e9-151">Exclusion mutuelle par présentation</span><span class="sxs-lookup"><span data-stu-id="338e9-151">Mutual Exclusion by Presentation</span></span>

<span data-ttu-id="338e9-152">L’exclusion mutuelle basée sur la présentation est fournie pour prendre en charge les flux vidéo qui contiennent le même contenu encodé avec des proportions différentes.</span><span class="sxs-lookup"><span data-stu-id="338e9-152">Presentation-based mutual exclusion is provided to support video streams that contain the same content encoded with different aspect ratios.</span></span> <span data-ttu-id="338e9-153">En règle générale, cette fonction est utilisée pour fournir une vidéo dans une version de bandes (proportions 16:9), ainsi qu’une mise en forme pour les écrans de télévision (proportions 4:3).</span><span class="sxs-lookup"><span data-stu-id="338e9-153">Typically, this is used when providing video in a letterbox version (aspect ratio 16:9) as well as formatted for television screens (aspect ratio 4:3).</span></span>

<span data-ttu-id="338e9-154">La sélection d’une présentation pour la lecture est généralement déterminée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="338e9-154">The selection of a presentation for playback is most often determined by the user.</span></span> <span data-ttu-id="338e9-155">Si vous écrivez une application pour lire des fichiers ASF et souhaitez prendre en charge des fichiers avec l’exclusion mutuelle basée sur une présentation, vous devez présenter à l’utilisateur la possibilité de sélectionner un type de présentation à afficher.</span><span class="sxs-lookup"><span data-stu-id="338e9-155">If you write an application to play ASF files and want to support files with presentation based mutual exclusion, you should present the user with the option of selecting a presentation type for viewing.</span></span>

## <a name="unknown-mutual-exclusion"></a><span data-ttu-id="338e9-156">Exclusion mutuelle inconnue</span><span class="sxs-lookup"><span data-stu-id="338e9-156">Unknown Mutual Exclusion</span></span>

<span data-ttu-id="338e9-157">Vous pouvez créer une exclusion mutuelle en fonction des critères de votre choix.</span><span class="sxs-lookup"><span data-stu-id="338e9-157">You can create mutual exclusion based on any criteria you like.</span></span> <span data-ttu-id="338e9-158">Tous les types d’exclusion mutuelle personnalisés doivent être créés à l’aide du type inconnu.</span><span class="sxs-lookup"><span data-stu-id="338e9-158">All custom mutual exclusion types should be created using the unknown type.</span></span>

## <a name="advanced-mutual-exclusion-features"></a><span data-ttu-id="338e9-159">Fonctionnalités avancées d’exclusion mutuelle</span><span class="sxs-lookup"><span data-stu-id="338e9-159">Advanced Mutual Exclusion Features</span></span>

<span data-ttu-id="338e9-160">Vous pouvez également utiliser l’exclusion mutuelle pour affecter des flux à des groupes qui s’excluent mutuellement les uns des autres.</span><span class="sxs-lookup"><span data-stu-id="338e9-160">You can also use mutual exclusion to assign streams to groups that are mutually exclusive of one another.</span></span> <span data-ttu-id="338e9-161">Par exemple, vous souhaiterez peut-être avoir des flux audio dans plusieurs langues et affecter un flux de vidéo différent à chacun d’entre eux.</span><span class="sxs-lookup"><span data-stu-id="338e9-161">For example, you might want to have audio streams in multiple languages and assign a different video stream to each.</span></span> <span data-ttu-id="338e9-162">Vous utilisez l’exclusion mutuelle pour regrouper chaque flux audio avec son flux vidéo correspondant et rendre tous les groupes mutuellement exclusifs.</span><span class="sxs-lookup"><span data-stu-id="338e9-162">You use mutual exclusion to group each audio stream with its corresponding video stream and make all groups mutually exclusive.</span></span>

<span data-ttu-id="338e9-163">Le lecteur sélectionne automatiquement les flux pour toutes les exclusions mutuelles.</span><span class="sxs-lookup"><span data-stu-id="338e9-163">The reader automatically selects streams for all mutual exclusions.</span></span> <span data-ttu-id="338e9-164">Pour tous les types d’exclusion mutuelle, à l’exception de MBR et de l’exclusion mutuelle basée sur le langage, le lecteur sélectionne toujours le flux par défaut, qui est le premier flux ajouté à l’objet d’exclusion mutuelle dans le profil.</span><span class="sxs-lookup"><span data-stu-id="338e9-164">For all types of mutual exclusion except MBR and language-based mutual exclusion, the reader always selects the default stream, which is the first stream added to the mutual exclusion object in the profile.</span></span> <span data-ttu-id="338e9-165">Pour MBR, le lecteur sélectionne le flux qui correspond le mieux à la bande passante disponible au moment de la lecture.</span><span class="sxs-lookup"><span data-stu-id="338e9-165">For MBR, the reader selects the stream that best suits the available bandwidth at the time of playback.</span></span> <span data-ttu-id="338e9-166">Si vous ne souhaitez pas utiliser le flux par défaut, vous pouvez définir la sélection de flux sur manuel avant de commencer à lire un fichier.</span><span class="sxs-lookup"><span data-stu-id="338e9-166">If you do not want to use the default stream, you can set stream selection to manual before starting to read a file.</span></span>

<span data-ttu-id="338e9-167">La sélection manuelle de flux s’applique à l’ensemble du fichier.</span><span class="sxs-lookup"><span data-stu-id="338e9-167">Manual stream selection applies to the entire file.</span></span> <span data-ttu-id="338e9-168">Des problèmes peuvent survenir lorsque vous avez des exclusions mutuelles de types différents dans le même fichier.</span><span class="sxs-lookup"><span data-stu-id="338e9-168">Difficulties can arise when you have mutual exclusions of different types in the same file.</span></span> <span data-ttu-id="338e9-169">Par exemple, un fichier peut contenir à la fois une exclusion mutuelle basée sur une vitesse de transmission et une exclusion mutuelle personnalisée.</span><span class="sxs-lookup"><span data-stu-id="338e9-169">For example, a file can contain both bit-rate-based mutual exclusion and custom mutual exclusion.</span></span> <span data-ttu-id="338e9-170">Pour sélectionner un flux autre que celui par défaut dans l’exclusion mutuelle personnalisée, vous devez utiliser la sélection manuelle des flux.</span><span class="sxs-lookup"><span data-stu-id="338e9-170">To select a stream other than the default in the custom mutual exclusion, you must use manual stream selection.</span></span> <span data-ttu-id="338e9-171">Toutefois, si vous utilisez la sélection manuelle de flux, le lecteur ne sélectionne pas automatiquement le flux à plusieurs vitesses de transmission.</span><span class="sxs-lookup"><span data-stu-id="338e9-171">If you use manual stream selection, however, the reader will not automatically select the multiple bit rate stream.</span></span> <span data-ttu-id="338e9-172">Vous devez planifier cette éventualité dans votre application si vous envisagez de prendre en charge plusieurs types d’exclusion mutuelle dans un seul fichier.</span><span class="sxs-lookup"><span data-stu-id="338e9-172">You must plan for this eventuality in your application if you plan to support multiple types of mutual exclusion in a single file.</span></span> <span data-ttu-id="338e9-173">En général, cela implique la création de vos propres routines de sélection de flux pour les types automatiques automatiques d’exclusion mutuelle.</span><span class="sxs-lookup"><span data-stu-id="338e9-173">Typically this means creating your own stream selection routines for normally automatic types of mutual exclusion.</span></span>

## <a name="related-topics"></a><span data-ttu-id="338e9-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="338e9-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="338e9-175">**Fonctionnalités des fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="338e9-175">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="338e9-176">**Utilisation de l’exclusion mutuelle**</span><span class="sxs-lookup"><span data-stu-id="338e9-176">**Using Mutual Exclusion**</span></span>](using-mutual-exclusion.md)
</dt> </dl>

 

 




