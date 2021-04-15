---
description: FAQ DirectShow
ms.assetid: 198758b9-025a-44af-958c-9ddea8cbb12d
title: FAQ DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7d0959c4abb24509edd9c26d111e80a5af221d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521796"
---
# <a name="directshow-faq"></a><span data-ttu-id="dc5c6-103">FAQ DirectShow</span><span class="sxs-lookup"><span data-stu-id="dc5c6-103">DirectShow FAQ</span></span>

<span data-ttu-id="dc5c6-104">Cet article répond à de nombreuses questions fréquemment posées sur Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-104">This article answers many frequently asked questions about Microsoft DirectShow.</span></span>

<span data-ttu-id="dc5c6-105">**Quels sont les systèmes d’exploitation pris en charge par DirectShow ?**</span><span class="sxs-lookup"><span data-stu-id="dc5c6-105">**What operating systems does DirectShow support?**</span></span>

<span data-ttu-id="dc5c6-106">DirectShow est disponible dans toutes les versions prises en charge de Windows.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-106">DirectShow is available in all supported versions of Windows.</span></span>

<span data-ttu-id="dc5c6-107">**Combien de connaissances COM ai-je besoin pour programmer avec DirectShow ?**</span><span class="sxs-lookup"><span data-stu-id="dc5c6-107">**How much COM knowledge do I need to program with DirectShow?**</span></span>

<span data-ttu-id="dc5c6-108">Pour le développement d’applications, vous devez comprendre les principes de base de l’utilisation des objets COM : comment les instancier, accéder aux interfaces qu’elles exposent et gérer les décomptes de références sur ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-108">For application development, you need to understand the basics of working with COM objects: how to instantiate them, access the interfaces they expose, and manage reference counts on those interfaces.</span></span> <span data-ttu-id="dc5c6-109">Le développement de filtres requiert davantage de connaissances COM.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-109">Filter development requires more COM knowledge.</span></span>

<span data-ttu-id="dc5c6-110">**Quels sont les formats pris en charge par DirectShow ?**</span><span class="sxs-lookup"><span data-stu-id="dc5c6-110">**What formats does DirectShow support?**</span></span>

<span data-ttu-id="dc5c6-111">Consultez [formats pris en charge dans DirectShow](supported-formats-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="dc5c6-111">See [Supported Formats in DirectShow](supported-formats-in-directshow.md).</span></span>

<span data-ttu-id="dc5c6-112">**Existe-t-il une liste de compatibilité matérielle (HCL) DirectShow ?**</span><span class="sxs-lookup"><span data-stu-id="dc5c6-112">**Is there a DirectShow Hardware Compatibility List (HCL)?**</span></span>

<span data-ttu-id="dc5c6-113">Non.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-113">No.</span></span> <span data-ttu-id="dc5c6-114">DirectShow utilise les fonctionnalités matérielles Microsoft DirectDraw et Microsoft DirectSound s’ils sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-114">DirectShow uses Microsoft DirectDraw and Microsoft DirectSound hardware capabilities if they are available.</span></span> <span data-ttu-id="dc5c6-115">Quand aucun matériel spécial n’est disponible, DirectShow utilise GDI pour dessiner une vidéo  et les \* API multimédias WaveOut pour la lecture audio.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-115">When no special hardware is available, DirectShow uses GDI to draw video and the **waveOut** \* multimedia APIs to play audio.</span></span>

<span data-ttu-id="dc5c6-116">**Quelles langues puis-je utiliser pour écrire une application DirectShow ?**</span><span class="sxs-lookup"><span data-stu-id="dc5c6-116">**What languages can I use to write a DirectShow application?**</span></span>

<span data-ttu-id="dc5c6-117">DirectShow est conçu principalement pour le développement C++.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-117">DirectShow is designed primarily for C++ development.</span></span> <span data-ttu-id="dc5c6-118">Un petit sous-ensemble de l’API DirectShow est exposé via Visual Basic 6,0 ; Toutefois, cette fonctionnalité est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-118">A small sub-set of the DirectShow API is exposed through Visual Basic 6.0; however, this feature is deprecated.</span></span>

<span data-ttu-id="dc5c6-119">**DirectShow sera-t-il jamais accessible via du code géré ?**</span><span class="sxs-lookup"><span data-stu-id="dc5c6-119">**Will DirectShow ever be accessible through managed code?**</span></span>

<span data-ttu-id="dc5c6-120">Microsoft n’a pas de plan actuel pour implémenter une API DirectShow gérée.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-120">Microsoft has no current plans to implement a managed DirectShow API.</span></span>

<span data-ttu-id="dc5c6-121">**Quel compilateur ai-je besoin pour le développement DirectShow ?**</span><span class="sxs-lookup"><span data-stu-id="dc5c6-121">**What compiler do I need for DirectShow development?**</span></span>

<span data-ttu-id="dc5c6-122">Tout compilateur qui peut générer des objets COM (Component Object Model) doit fonctionner une fois que l’environnement du compilateur a été configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-122">Any compiler capable of generating Component Object Model (COM) objects should work once the compiler's environment has been configured correctly.</span></span>

<span data-ttu-id="dc5c6-123">**Comment DirectShow est-il lié à Microsoft DirectX ?**</span><span class="sxs-lookup"><span data-stu-id="dc5c6-123">**How does DirectShow relate to Microsoft DirectX?**</span></span>

<span data-ttu-id="dc5c6-124">En interne, DirectShow utilise DirectSound et DirectDraw lorsque le matériel le prend en charge.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-124">Internally, DirectShow uses DirectSound and DirectDraw when the hardware supports it.</span></span> <span data-ttu-id="dc5c6-125">Les filtres de mélangeur vidéo et de mixage de superposition utilisent des surfaces DirectDraw 3 et DirectDraw 5.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-125">The Video Renderer and Overlay Mixer filters use DirectDraw 3 and DirectDraw 5 surfaces.</span></span> <span data-ttu-id="dc5c6-126">Le convertisseur de mixage vidéo 7 (Windows XP uniquement) utilise des surfaces DirectDraw 7.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-126">The Video Mixing Renderer 7 (Windows XP only) uses DirectDraw 7 surfaces.</span></span> <span data-ttu-id="dc5c6-127">Le convertisseur de mixage vidéo 9 et le convertisseur vidéo amélioré utilisent les API Microsoft Direct3D les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-127">The Video Mixing Renderer 9 and the Enhanced Video Renderer use the latest Microsoft Direct3D APIs.</span></span> <span data-ttu-id="dc5c6-128">Vous n’avez pas besoin d’utiliser les autres API DirectX pour écrire une application DirectShow, bien qu’il soit possible de les combiner.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-128">You do not need to use the other DirectX APIs to write a DirectShow application, although it is possible to combine them.</span></span>

<span data-ttu-id="dc5c6-129">**Comment DirectShow est-il lié à Microsoft ActiveMovie ?**</span><span class="sxs-lookup"><span data-stu-id="dc5c6-129">**How does DirectShow relate to Microsoft ActiveMovie?**</span></span>

<span data-ttu-id="dc5c6-130">ActiveMovie était le nom d’origine de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-130">ActiveMovie was the original name for DirectShow.</span></span> <span data-ttu-id="dc5c6-131">Le terme ActiveMovie n’est plus utilisé.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-131">The term ActiveMovie is no longer used.</span></span>

<span data-ttu-id="dc5c6-132">**Le code source de l’utilitaire GraphEdit est-il disponible ? GraphEdit peut-il être redistribué ?**</span><span class="sxs-lookup"><span data-stu-id="dc5c6-132">**Is the source code to the GraphEdit utility available? Can GraphEdit be redistributed?**</span></span>

<span data-ttu-id="dc5c6-133">Non, la source n’est pas disponible et Graphedt.exe n’est pas redistribuable.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-133">No, the source is not available, and Graphedt.exe is not redistributable.</span></span>

<span data-ttu-id="dc5c6-134">**DMOs remplacer les filtres DirectShow ?**</span><span class="sxs-lookup"><span data-stu-id="dc5c6-134">**Do DMOs replace DirectShow filters?**</span></span>

<span data-ttu-id="dc5c6-135">Microsoft DirectX Media Objects (DMOs) peut être utilisé dans une application DirectShow.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-135">Microsoft DirectX Media Objects (DMOs) can be used in a DirectShow application.</span></span> <span data-ttu-id="dc5c6-136">Pour les encodeurs, les décodeurs et les effets, il est recommandé d’écrire un DMO au lieu d’un filtre DirectShow.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-136">For encoders, decoders, and effects, you are encouraged to write a DMO instead of a DirectShow filter.</span></span> <span data-ttu-id="dc5c6-137">(Remarque : Si vous souhaitez utiliser l’accélération vidéo DirectX dans votre décodeur, vous devez l’implémenter en tant que filtre.) À d’autres fins, un filtre DirectShow peut être plus approprié.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-137">(Note: If you want to use DirectX Video Acceleration in your decoder, you must implement it as a filter.) For other purposes, a DirectShow filter might be more appropriate.</span></span> <span data-ttu-id="dc5c6-138">Pour plus d’informations sur DMOs, consultez [objets multimédia DirectX](directx-media-objects.md).</span><span class="sxs-lookup"><span data-stu-id="dc5c6-138">For more information about DMOs, see [DirectX Media Objects](directx-media-objects.md).</span></span>

<span data-ttu-id="dc5c6-139">**Je lit un fichier de format AVI avec le lecteur Windows Media. Je peux entendre le son, mais il semble qu’il n’y ait pas de vidéo. à la place, je ne vois que le noir. Qu'est-ce qui ne va pas?**</span><span class="sxs-lookup"><span data-stu-id="dc5c6-139">**I'm playing an AVI format file with Windows Media Player. I can hear the audio, but there doesn't seem to be any video-instead, I just see black. What's wrong?**</span></span>

<span data-ttu-id="dc5c6-140">Probablement, le fichier a été encodé avec un codec qui n’est pas présent sur votre système.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-140">Probably the file was encoded with a codec that is not present on your system.</span></span> <span data-ttu-id="dc5c6-141">Bien que le format de fichier AVI soit courant, il est possible de créer des fichiers AVI avec de nombreux formats de compression (codecs).</span><span class="sxs-lookup"><span data-stu-id="dc5c6-141">Although the AVI file format is common, AVI files can be created with many different compression formats (codecs).</span></span> <span data-ttu-id="dc5c6-142">Si vous tentez de lire un fichier AVI qui utilise un codec non pris en charge, vous pouvez entendre le composant audio, mais la vidéo s’affichera sous la forme d’un écran noir ou le contenu de l’écran restera inchangé.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-142">If you try to play an AVI file that uses an unsupported codec, you might hear the audio component, but the video will display as a black screen or the screen contents will remain unchanged.</span></span>

> [!Note]  
> <span data-ttu-id="dc5c6-143">Le lecteur Windows Media tente souvent de télécharger et d’installer un codec s’il n’est pas présent sur votre système.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-143">Windows Media Player often attempts to download and install a codec if it is not present on your system.</span></span>

 

<span data-ttu-id="dc5c6-144">**Comment faire générer mon application ? De quelles bibliothèques et fichiers d’en-tête ai-je besoin ?**</span><span class="sxs-lookup"><span data-stu-id="dc5c6-144">**How do I build my application? What libraries and header files do I need?**</span></span>

<span data-ttu-id="dc5c6-145">Consultez [configuration de l’environnement de génération](setting-up-the-build-environment.md).</span><span class="sxs-lookup"><span data-stu-id="dc5c6-145">See [Setting Up the Build Environment](setting-up-the-build-environment.md).</span></span>

<span data-ttu-id="dc5c6-146">**GraphEdit affiche un grand nombre de filtres qui ne sont pas documentés. Qu’est-ce que ces filtres ?**</span><span class="sxs-lookup"><span data-stu-id="dc5c6-146">**GraphEdit displays a lot of filters that aren't documented. What are these filters?**</span></span>

<span data-ttu-id="dc5c6-147">GraphEdit énumère tous les filtres inscrits sur votre système dans une catégorie de filtre.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-147">GraphEdit enumerates all of the filters that are registered on your system in a filter category.</span></span> <span data-ttu-id="dc5c6-148">Il peut s’agir de filtres installés par des applications tierces ou installés par d’autres technologies Microsoft, telles que Windows Media ou NetMeeting.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-148">This might include filters installed by third-party applications, or installed by other Microsoft technologies, such as Windows Media or NetMeeting.</span></span> <span data-ttu-id="dc5c6-149">En outre, certains filtres DirectShow jouent le rôle de wrappers pour les codecs ou les périphériques matériels, chaque codec ou périphérique étant considéré comme un filtre distinct.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-149">Also, some DirectShow filters act as wrappers for codecs or hardware devices, with each codec or device appearing as a distinct filter.</span></span> <span data-ttu-id="dc5c6-150">Le codec vidéo Microsoft H. 263 est utilisé par NetMeeting et n’est plus pris en charge dans DirectShow.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-150">The Microsoft H.263 Video Codec is used by NetMeeting and is no longer supported in DirectShow.</span></span> <span data-ttu-id="dc5c6-151">Pour plus d’informations, consultez [énumération des appareils et des filtres](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="dc5c6-151">For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>

<span data-ttu-id="dc5c6-152">**Je ne parviens pas à créer mon graphique personnalisé par programmation.**</span><span class="sxs-lookup"><span data-stu-id="dc5c6-152">**I'm having trouble building my custom graph programmatically.**</span></span>

<span data-ttu-id="dc5c6-153">Essayez d’abord de créer le graphique de filtre avec GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-153">First try building the filter graph with GraphEdit.</span></span> <span data-ttu-id="dc5c6-154">Cet outil vous permet de simuler un grand nombre de possibilités rapidement.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-154">This tool enables you to simulate lots of possibilities quickly.</span></span> <span data-ttu-id="dc5c6-155">GraphEdit est toujours l’emplacement idéal pour tester le graphique avant de tenter de le générer avec le code source.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-155">GraphEdit is always a great place to test out the graph before attempting to build it with source code.</span></span>

<span data-ttu-id="dc5c6-156">Pour plus d’informations sur la création de graphiques, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="dc5c6-156">For more information about graph building, see the following articles:</span></span>

-   [<span data-ttu-id="dc5c6-157">Génération du graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="dc5c6-157">Building the Filter Graph</span></span>](building-the-filter-graph.md)
-   [<span data-ttu-id="dc5c6-158">Énumération d’objets dans un graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="dc5c6-158">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)

<span data-ttu-id="dc5c6-159">**Comment puis-je détecter si DirectShow est installé sur un ordinateur donné ?**</span><span class="sxs-lookup"><span data-stu-id="dc5c6-159">**How can I detect whether DirectShow is installed on a given machine?**</span></span>

<span data-ttu-id="dc5c6-160">Appelez **CoCreateInstance** pour créer une instance du gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-160">Call **CoCreateInstance** to create an instance of the Filter Graph Manager.</span></span> <span data-ttu-id="dc5c6-161">Si cet appel se déroule correctement, DirectShow est installé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-161">If this call succeeds, DirectShow is installed on the machine.</span></span> <span data-ttu-id="dc5c6-162">Le code suivant illustre comment procéder :</span><span class="sxs-lookup"><span data-stu-id="dc5c6-162">The following code shows how to do this:</span></span>


```C++
IGraphBuilder *pGraph;

HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void **) &pGraph);
```



<span data-ttu-id="dc5c6-163">**Comment faire modifier les paramètres d’un filtre sans afficher la page de propriétés ?**</span><span class="sxs-lookup"><span data-stu-id="dc5c6-163">**How do I change a filter's settings without displaying the property page?**</span></span>

<span data-ttu-id="dc5c6-164">La plupart des filtres exposent une ou plusieurs interfaces pour définir des propriétés sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-164">Most filters expose one or more interfaces for setting properties on the filter.</span></span> <span data-ttu-id="dc5c6-165">Consultez la page de référence du filtre en question.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-165">Consult the reference page for the filter in question.</span></span> <span data-ttu-id="dc5c6-166">(Voir [filtres DirectShow](directshow-filters.md).)</span><span class="sxs-lookup"><span data-stu-id="dc5c6-166">(See [DirectShow Filters](directshow-filters.md).)</span></span>

<span data-ttu-id="dc5c6-167">**Puis-je tester le filtre avec GraphEdit ?**</span><span class="sxs-lookup"><span data-stu-id="dc5c6-167">**Can I test my filter with GraphEdit?**</span></span>

<span data-ttu-id="dc5c6-168">Lorsque vous développez un filtre, GraphEdit peut vous aider à visualiser les connexions entre les filtres.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-168">While you are developing a filter, GraphEdit can help you to visualize the connections between filters.</span></span> <span data-ttu-id="dc5c6-169">Il peut également fournir un test rapide des fonctionnalités d’un filtre.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-169">It can also provide a quick test of a filter's functionality.</span></span> <span data-ttu-id="dc5c6-170">Toutefois, il n’est pas conçu comme une plateforme de test robuste.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-170">However, it is not meant as a robust test platform.</span></span>

<span data-ttu-id="dc5c6-171">**À quel moment les filtres de l’anneau des privilèges sont-ils exécutés ?**</span><span class="sxs-lookup"><span data-stu-id="dc5c6-171">**At what privilege ring do filters run?**</span></span>

<span data-ttu-id="dc5c6-172">Les filtres s’exécutent à l’anneau 3, bien que certains filtres contrôlent les périphériques de diffusion en continu qui s’exécutent à l’anneau 0.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-172">Filters run at ring 3, although some filters control streaming devices that run at ring 0.</span></span> <span data-ttu-id="dc5c6-173">Pour plus d’informations, voir [Comment les périphériques matériels participent au graphique de filtre](how-hardware-devices-participate-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="dc5c6-173">For more information, see [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).</span></span>

<span data-ttu-id="dc5c6-174">**Ai-je besoin d’utiliser un débogueur de noyau ?**</span><span class="sxs-lookup"><span data-stu-id="dc5c6-174">**Do I need to use a kernel debugger?**</span></span>

<span data-ttu-id="dc5c6-175">Cela dépend de votre projet spécifique.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-175">That depends on your specific project.</span></span> <span data-ttu-id="dc5c6-176">L’installation des bibliothèques Runtime de débogage DirectX signifie que vous installez des pilotes de débogage et d’autres composants en mode noyau, et que si votre application provoque une assertion de débogage dans l’un de ces composants, votre ordinateur redémarre automatiquement, sauf si un débogueur de noyau est attaché à votre processus.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-176">Installing the DirectX debug runtime libraries means that you are installing debug drivers and other kernel mode components, and that if your application causes a debug assert in one of these components, your machine will automatically reboot unless you have a kernel debugger attached to your process.</span></span>

<span data-ttu-id="dc5c6-177">**Lorsque j’exécute mon application dans le débogueur, elle se bloque.**</span><span class="sxs-lookup"><span data-stu-id="dc5c6-177">**When I run my application in the debugger, it crashes.**</span></span>

<span data-ttu-id="dc5c6-178">Certains décodeurs sont conçus pour ne pas fonctionner pendant que l’application est attachée au débogueur.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-178">Some decoders are designed not to work while the application is attached to the debugger.</span></span> <span data-ttu-id="dc5c6-179">Essayez d’exécuter l’application en dehors du débogueur.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-179">Try running the application outside the debugger.</span></span>

<span data-ttu-id="dc5c6-180">**Comment \_ fonctionne la macro GUID de définition ?**</span><span class="sxs-lookup"><span data-stu-id="dc5c6-180">**How does the DEFINE\_GUID macro work?**</span></span>

<span data-ttu-id="dc5c6-181">La macro **définir le \_ GUID** résout le problème de la déclaration de `extern` références aux valeurs GUID dans votre code source.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-181">The **DEFINE\_GUID** macro solves the problem of declaring `extern` references to GUID values in your source code.</span></span> <span data-ttu-id="dc5c6-182">Supposons, par exemple, que votre projet comporte trois fichiers sources, src1. cpp, src2. cpp et Src3. cpp, et que les trois fichiers utilisent une certaine valeur GUID que vous avez définie.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-182">For example, suppose that your project has three source files, Src1.cpp, Src2.cpp, and Src3.cpp, and all three files use a certain GUID value that you have defined.</span></span> <span data-ttu-id="dc5c6-183">La valeur GUID doit être définie exactement une fois dans votre projet, et les autres fichiers sources doivent déclarer des `extern` références à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-183">The GUID value must be defined exactly once in your project, and the other source files must declare `extern` references to it.</span></span> <span data-ttu-id="dc5c6-184">Avec la macro **définir le \_ GUID** , vous pouvez utiliser le même fichier d’en-tête dans les deux cas.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-184">With the **DEFINE\_GUID** macro, you can use the same header file for both purposes.</span></span> <span data-ttu-id="dc5c6-185">Dans votre fichier d’en-tête, déclarez le GUID comme suit :</span><span class="sxs-lookup"><span data-stu-id="dc5c6-185">In your header file, declare the GUID as follows:</span></span>


```C++
DEFINE_GUID(CLSID_MyObject, 
0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



<span data-ttu-id="dc5c6-186">(Où cet exemple a des zéros, placez les valeurs GUID réelles.) Vous pouvez utiliser l’utilitaire Guidgen.exe pour créer un nouveau GUID et le coller dans le fichier d’en-tête au format **\_ GUID** .</span><span class="sxs-lookup"><span data-stu-id="dc5c6-186">(Where this example has zeroes, put the actual GUID values.) You can use the Guidgen.exe utility to create a new GUID and paste it into the header file in the **DEFINE\_GUID** format.</span></span> <span data-ttu-id="dc5c6-187">Incluez ce fichier d’en-tête dans chaque fichier source qui référence le GUID.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-187">Include this header file in every source file that references the GUID.</span></span> <span data-ttu-id="dc5c6-188">Dans exactement l’un des fichiers source, incluez le fichier d’en-tête Initguid. h avant votre fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-188">In exactly one of the source files, include the header file Initguid.h before your header file.</span></span> <span data-ttu-id="dc5c6-189">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="dc5c6-189">For example:</span></span>


```C++
// Src1.cpp
#include <initguid.h>
#include "MyGuids.h"

// Src2.cpp
#include "MyGuids.h"

// Src3.cpp
#include "MyGuids.h"
```



<span data-ttu-id="dc5c6-190">Partout où le fichier d’en-tête Initguid. h n’est pas inclus, la macro **définir le \_ GUID** crée une `extern` référence à la valeur Guid.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-190">Wherever the Initguid.h header file is not included, the **DEFINE\_GUID** macro creates an `extern` reference to the GUID value.</span></span> <span data-ttu-id="dc5c6-191">Lorsque le fichier d’en-tête Initguid. h est inclus, il redéfinit la macro **définir le \_ GUID** afin que **définir le \_ GUID** crée une déclaration de définition du GUID.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-191">When the Initguid.h header file is included, it redefines the **DEFINE\_GUID** macro so that **DEFINE\_GUID** creates a defining declaration of the GUID.</span></span>

<span data-ttu-id="dc5c6-192">Si vous n’incluez pas Initguid. h dans aucun des fichiers sources, vous obtiendrez une erreur de lien « symbole externe non résolu ».</span><span class="sxs-lookup"><span data-stu-id="dc5c6-192">If you do not include Initguid.h in any of the source files, you will get a link error "unresolved external symbol."</span></span> <span data-ttu-id="dc5c6-193">Si vous incluez Initguid. h deux fois pour le même GUID, vous obtiendrez une erreur de compilation «redéfinition ; initialisation multiple.»</span><span class="sxs-lookup"><span data-stu-id="dc5c6-193">If you include Initguid.h twice for the same GUID, you will get a compile error "redefinition; multiple initialization."</span></span> <span data-ttu-id="dc5c6-194">Pour résoudre ces erreurs, assurez-vous que Initguid. h est inclus une seule fois.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-194">To resolve these errors, make sure that Initguid.h is included exactly once.</span></span> <span data-ttu-id="dc5c6-195">En outre, n’incluez pas Initguid. h dans un fichier d’en-tête précompilé, car en effet, l’en-tête précompilé est inclus dans chaque fichier source.</span><span class="sxs-lookup"><span data-stu-id="dc5c6-195">Also, do not include Initguid.h inside a precompiled header file, because in effect the precompiled header is included in every source file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc5c6-196">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dc5c6-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc5c6-197">Présentation de DirectShow</span><span class="sxs-lookup"><span data-stu-id="dc5c6-197">Introduction to DirectShow</span></span>](introduction-to-directshow.md)
</dt> </dl>

 

 



