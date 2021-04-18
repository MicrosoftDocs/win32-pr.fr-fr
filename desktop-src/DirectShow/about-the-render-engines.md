---
description: À propos des moteurs de rendu
ms.assetid: 80299b1a-09bf-4660-95d3-41a2b0074745
title: À propos des moteurs de rendu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70fe3a9956bee0d167de9e6618187bfd1f2a6e39
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522236"
---
# <a name="about-the-render-engines"></a><span data-ttu-id="9c726-103">À propos des moteurs de rendu</span><span class="sxs-lookup"><span data-stu-id="9c726-103">About the Render Engines</span></span>

<span data-ttu-id="9c726-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="9c726-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="9c726-105">Cet article décrit comment les [services d’édition DirectShow](directshow-editing-services.md) affichent un projet de montage vidéo.</span><span class="sxs-lookup"><span data-stu-id="9c726-105">This article describes how [DirectShow Editing Services](directshow-editing-services.md) (DES) renders a video editing project.</span></span>

<span data-ttu-id="9c726-106">Dans DES, un projet est représenté sous la forme d’une chronologie.</span><span class="sxs-lookup"><span data-stu-id="9c726-106">In DES, a project is represented as a timeline.</span></span> <span data-ttu-id="9c726-107">La chronologie est utile, car elle simplifie les tâches les plus courantes lors de l’édition vidéo, telles que la réorganisation des éléments sources et l’ajout d’effets vidéo.</span><span class="sxs-lookup"><span data-stu-id="9c726-107">The timeline is useful because it simplifies the most common tasks in video editing, such as rearranging source clips and adding video effects.</span></span> <span data-ttu-id="9c726-108">L’architecture du flux DirectShow, en revanche, nécessite un graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="9c726-108">The DirectShow stream architecture, on the other hand, requires a filter graph.</span></span> <span data-ttu-id="9c726-109">Par conséquent, pour restituer votre projet, vous devez convertir une chronologie en un graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="9c726-109">Thus, to render your project, you must translate a timeline into a filter graph.</span></span> <span data-ttu-id="9c726-110">Le composant qui s’en sert est appelé *moteur de rendu*.</span><span class="sxs-lookup"><span data-stu-id="9c726-110">The component that does this is called a *render engine*.</span></span> <span data-ttu-id="9c726-111">DirectShow fournit deux moteurs de rendu :</span><span class="sxs-lookup"><span data-stu-id="9c726-111">DirectShow provides two render engines:</span></span>

-   <span data-ttu-id="9c726-112">Moteur de rendu de base : crée un graphique de filtre qui fournit une sortie non compressée.</span><span class="sxs-lookup"><span data-stu-id="9c726-112">Basic render engine: Builds a filter graph that delivers uncompressed output.</span></span>
-   <span data-ttu-id="9c726-113">Moteur de rendu intelligent : crée un graphique de filtre qui fournit une sortie compressée.</span><span class="sxs-lookup"><span data-stu-id="9c726-113">Smart render engine: Builds a filter graph that delivers compressed output.</span></span>

<span data-ttu-id="9c726-114">Le moteur de rendu intelligent utilise la recompression intelligente pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="9c726-114">The smart render engine uses smart recompression to improve performance.</span></span> <span data-ttu-id="9c726-115">Avec la recompression intelligente, les fichiers sources sont recompressés uniquement lorsque le format de fichier d’origine est différent du format de sortie final.</span><span class="sxs-lookup"><span data-stu-id="9c726-115">With smart recompression, source files are recompressed only when the original file format differs from the final output format.</span></span> <span data-ttu-id="9c726-116">Si les formats correspondent, la source n’est jamais décompressée.</span><span class="sxs-lookup"><span data-stu-id="9c726-116">If the formats match, the source is never decompressed.</span></span> <span data-ttu-id="9c726-117">La recompression intelligente est prise en charge uniquement pour la compression vidéo, et non pour la compression audio.</span><span class="sxs-lookup"><span data-stu-id="9c726-117">Smart recompression is supported only for video compression, not for audio compression.</span></span>

<span data-ttu-id="9c726-118">Pour la version préliminaire, utilisez le moteur de rendu de base.</span><span class="sxs-lookup"><span data-stu-id="9c726-118">For preview, use the basic render engine.</span></span> <span data-ttu-id="9c726-119">Le moteur de rendu intelligent peut également afficher un aperçu, mais moins efficacement car il doit décompresser le flux compressé.</span><span class="sxs-lookup"><span data-stu-id="9c726-119">The smart render engine can also preview, but less efficiently because it has to decompress the compressed stream.</span></span> <span data-ttu-id="9c726-120">Pour écrire des fichiers, utilisez le moteur de rendu intelligent si vous souhaitez la recompression intelligente.</span><span class="sxs-lookup"><span data-stu-id="9c726-120">For writing files, use the smart render engine if you want smart recompression.</span></span> <span data-ttu-id="9c726-121">Dans le cas contraire, utilisez le moteur de rendu de base.</span><span class="sxs-lookup"><span data-stu-id="9c726-121">Otherwise, use the basic render engine.</span></span> <span data-ttu-id="9c726-122">La recompression intelligente peut réduire de manière considérable le temps nécessaire à l’écriture du fichier.</span><span class="sxs-lookup"><span data-stu-id="9c726-122">Smart recompression can greatly reduce the time it takes to write the file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9c726-123">N’utilisez pas le moteur de rendu intelligent pour lire ou écrire des fichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9c726-123">Do not use the smart render engine to read or write Windows Media files.</span></span>

 

> [!IMPORTANT]
> <span data-ttu-id="9c726-124">Les deux moteurs de rendu créent une fenêtre invisible qui traite les messages.</span><span class="sxs-lookup"><span data-stu-id="9c726-124">Both render engines create an invisible window that processes messages.</span></span> <span data-ttu-id="9c726-125">Le thread qui crée le moteur de rendu doit avoir une boucle de message pour distribuer les messages.</span><span class="sxs-lookup"><span data-stu-id="9c726-125">The thread that creates the render engine must have a message loop, to dispatch messages.</span></span> <span data-ttu-id="9c726-126">En outre, ce thread ne doit pas quitter tant que le moteur de rendu et le gestionnaire de graphes de filtre ne sont pas libérés.</span><span class="sxs-lookup"><span data-stu-id="9c726-126">Also, that thread must not exit until the Render Engine and the Filter Graph Manager are released.</span></span> <span data-ttu-id="9c726-127">Dans le cas contraire, l’application peut se bloquer.</span><span class="sxs-lookup"><span data-stu-id="9c726-127">Otherwise, the application might deadlock.</span></span>

 

<span data-ttu-id="9c726-128">Construction du graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="9c726-128">Constructing the Filter Graph</span></span>

<span data-ttu-id="9c726-129">Le graphique de filtre est construit en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="9c726-129">The filter graph is built in two stages.</span></span> <span data-ttu-id="9c726-130">Dans la première étape, le moteur de rendu construit un « frontal », qui est un graphique de filtre partiel.</span><span class="sxs-lookup"><span data-stu-id="9c726-130">In the first stage, the render engine constructs a "front end," which is a partial filter graph.</span></span> <span data-ttu-id="9c726-131">Le diagramme suivant illustre un frontal classique :</span><span class="sxs-lookup"><span data-stu-id="9c726-131">The following diagram illustrates a typical front end:</span></span>

![filtrer le graphique frontal](images/rendeng1.png)

<span data-ttu-id="9c726-133">Les sous-systèmes contiennent différents filtres spécialisés, que le moteur de rendu assemble automatiquement.</span><span class="sxs-lookup"><span data-stu-id="9c726-133">The subsystems contain various specialized filters, which the render engine assembles automatically.</span></span> <span data-ttu-id="9c726-134">Le serveur frontal contient une broche de sortie pour chaque groupe dans la chronologie.</span><span class="sxs-lookup"><span data-stu-id="9c726-134">The front end contains one output pin for each group in the timeline.</span></span> <span data-ttu-id="9c726-135">Les broches de sortie fournissent des données non compressées si vous utilisez le moteur de rendu de base, ou des données compressées si vous utilisez le moteur de rendu intelligent.</span><span class="sxs-lookup"><span data-stu-id="9c726-135">The output pins deliver uncompressed data if you use the basic render engine, or compressed data if you use the smart render engine.</span></span>

<span data-ttu-id="9c726-136">Dans la deuxième étape, les broches de sortie sont connectées aux filtres de rendu.</span><span class="sxs-lookup"><span data-stu-id="9c726-136">In the second step, the output pins are connected to rendering filters.</span></span> <span data-ttu-id="9c726-137">Pour la version préliminaire, les filtres de rendu sont des convertisseurs vidéo et audio.</span><span class="sxs-lookup"><span data-stu-id="9c726-137">For preview, the rendering filters are video and audio renderers.</span></span> <span data-ttu-id="9c726-138">Pour l’écriture de fichier, les filtres de rendu sont des filtres multiplexeur (multiplexeur) et des filtres d’écriture de fichier.</span><span class="sxs-lookup"><span data-stu-id="9c726-138">For file writing, the rendering filters are multiplexer (mux) filters and file-writer filters.</span></span>

![remplissage du graphique de filtre](images/rendeng2.png)

## <a name="related-topics"></a><span data-ttu-id="9c726-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9c726-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c726-141">Aperçu d’un projet</span><span class="sxs-lookup"><span data-stu-id="9c726-141">Previewing a Project</span></span>](previewing-a-project.md)
</dt> <dt>

[<span data-ttu-id="9c726-142">Écriture d’un projet dans un fichier</span><span class="sxs-lookup"><span data-stu-id="9c726-142">Writing a Project to a File</span></span>](writing-a-project-to-a-file.md)
</dt> </dl>

 

 



