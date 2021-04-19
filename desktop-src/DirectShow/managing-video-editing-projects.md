---
description: Gestion des projets de montage vidéo
ms.assetid: f8d74807-562f-429b-93a1-e65d0f15163b
title: Gestion des projets de montage vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491cfcb9a6e94874d2cae43567b61666bbd43cd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516543"
---
# <a name="managing-video-editing-projects"></a><span data-ttu-id="3fbbd-103">Gestion des projets de montage vidéo</span><span class="sxs-lookup"><span data-stu-id="3fbbd-103">Managing Video Editing Projects</span></span>

<span data-ttu-id="3fbbd-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="3fbbd-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="3fbbd-105">Les conseils suivants vous aideront à gérer les projets dans les [services de modification DirectShow](directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="3fbbd-105">The following tips will help you to manage projects in [DirectShow Editing Services](directshow-editing-services.md).</span></span>

<span data-ttu-id="3fbbd-106">Modifications apportées à la chronologie</span><span class="sxs-lookup"><span data-stu-id="3fbbd-106">Changes to the Timeline</span></span>

-   <span data-ttu-id="3fbbd-107">Si vous modifiez la chronologie après avoir généré le graphique de filtre, appelez [**IRenderEngine :: ConnectFrontEnd**](irenderengine-connectfrontend.md) à nouveau pour reconstruire le serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-107">If you change the timeline after you build the filter graph, call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) again to rebuild the front end.</span></span> <span data-ttu-id="3fbbd-108">En règle générale, cela n’affecte pas le reste du graphique.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-108">Usually, this does not affect the rest of the graph.</span></span> <span data-ttu-id="3fbbd-109">Toutefois, le moteur de rendu doit parfois supprimer l’intégralité du graphique avant de regénérer le serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-109">Occasionally, however, the render engine needs to delete the entire graph before it rebuilds the front end.</span></span> <span data-ttu-id="3fbbd-110">(Cela se produit, par exemple, si vous ajoutez ou supprimez un groupe.) La méthode **ConnectFrontEnd** retourne S \_ WARN \_ OUTPUTRESET pour signaler qu’il a supprimé le graphique.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-110">(For example, this happens if you add or remove a group.) The **ConnectFrontEnd** method returns S\_WARN\_OUTPUTRESET to signal that it deleted the graph.</span></span> <span data-ttu-id="3fbbd-111">Dans ce cas, votre application doit reconstruire la section de rendu du graphique.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-111">If this happens, your application must rebuild the rendering section of the graph.</span></span>
-   <span data-ttu-id="3fbbd-112">Pour supprimer complètement tous les objets de la chronologie, appelez la méthode [**IAMTimeline :: ClearAllGroups**](iamtimeline-clearallgroups.md) .</span><span class="sxs-lookup"><span data-stu-id="3fbbd-112">To remove all objects completely from the timeline, call the [**IAMTimeline::ClearAllGroups**](iamtimeline-clearallgroups.md) method.</span></span>

<span data-ttu-id="3fbbd-113">**Nettoyage**</span><span class="sxs-lookup"><span data-stu-id="3fbbd-113">**Cleanup**</span></span>

-   <span data-ttu-id="3fbbd-114">Lorsque vous avez terminé d’utiliser un moteur de rendu, appelez la méthode [**IRenderEngine :: ScrapIt**](irenderengine-scrapit.md) .</span><span class="sxs-lookup"><span data-stu-id="3fbbd-114">When you are finished using a render engine, call the [**IRenderEngine::ScrapIt**](irenderengine-scrapit.md) method.</span></span> <span data-ttu-id="3fbbd-115">Comme pour tout objet COM, veillez à libérer chaque pointeur d’interface lorsque vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-115">As with any COM object, be sure to release every interface pointer when you are finished using it.</span></span>
-   <span data-ttu-id="3fbbd-116">Le moteur de rendu ne conserve pas un décompte de références sur la chronologie.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-116">The render engine does not keep a reference count on the timeline.</span></span> <span data-ttu-id="3fbbd-117">Ne libérez pas la chronologie avant de l’utiliser, et appelez toujours **ScrapIt** sur le moteur de rendu en premier.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-117">Do not release the timeline before you are done using it, and always call **ScrapIt** on the render engine first.</span></span>
-   <span data-ttu-id="3fbbd-118">Si vous publiez toutes les références à une chronologie, n’utilisez pas les objets de cette chronologie, même si vous y avez des décomptes de références.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-118">If you release all references to a timeline, do not use any of the objects in that timeline, even if you are holding reference counts on them.</span></span>

<span data-ttu-id="3fbbd-119">**Plusieurs instances de chronologie**</span><span class="sxs-lookup"><span data-stu-id="3fbbd-119">**Multiple Timeline Instances**</span></span>

-   <span data-ttu-id="3fbbd-120">Ne déplacez pas les objets Timeline entre les chronologies.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-120">Do not move timeline objects between timelines.</span></span> <span data-ttu-id="3fbbd-121">Chaque objet d’une chronologie doit être créé par cette chronologie.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-121">Every object in a timeline must be created by that timeline.</span></span> <span data-ttu-id="3fbbd-122">La chronologie contient un cache interne avec des informations sur les objets qu’il crée ; le déplacement d’objets de chronologie peut perturber le cache.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-122">The timeline holds an internal cache with information about the objects that it creates; moving timeline objects can disrupt the cache.</span></span>
-   <span data-ttu-id="3fbbd-123">N’utilisez jamais la même instance d’un moteur de rendu avec plusieurs chronologies.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-123">Never use the same instance of a render engine with more than one timeline.</span></span> <span data-ttu-id="3fbbd-124">Le moteur de rendu contient un cache contenant des informations sur la chronologie.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-124">The render engine holds a cache with information about the timeline.</span></span> <span data-ttu-id="3fbbd-125">Plusieurs chronologies interrompent le cache et entraînent des résultats imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-125">Multiple timelines will disrupt the cache and cause unpredictable results.</span></span> <span data-ttu-id="3fbbd-126">Si vous avez besoin de deux chronologies actives, créez des instances distinctes des moteurs de rendu pour chaque chronologie.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-126">If you need two active timelines, make separate instances of render engines for each timeline.</span></span>
-   <span data-ttu-id="3fbbd-127">Une chronologie peut utiliser plusieurs moteurs de rendu, mais pas en même temps.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-127">A timeline can use more than one render engine, but not at the same time.</span></span> <span data-ttu-id="3fbbd-128">Supprimez l’ancien moteur de rendu avant d’utiliser un autre moteur de rendu.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-128">Delete the old render engine before using another render engine.</span></span> <span data-ttu-id="3fbbd-129">(C’est généralement le cas lorsque vous passez de l’utilisation du moteur de rendu de base à la version préliminaire au moteur de rendu intelligent pour l’écriture de fichiers.)</span><span class="sxs-lookup"><span data-stu-id="3fbbd-129">(You would typically do this when you switch from using the basic render engine for preview to the smart render engine for file writing.)</span></span>

<span data-ttu-id="3fbbd-130">**Persistance**</span><span class="sxs-lookup"><span data-stu-id="3fbbd-130">**Persistence**</span></span>

-   <span data-ttu-id="3fbbd-131">Le graphique de filtre n’est pas persistant lorsque vous enregistrez le projet dans un fichier XML.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-131">The filter graph is not persistent when you save the project to an XML file.</span></span> <span data-ttu-id="3fbbd-132">Par conséquent, vous perdez toutes les informations relatives à la recompression intelligente, au format de compression ou aux paramètres de compression.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-132">Therefore, you lose any information relating to smart recompression, compression format, or compression parameters.</span></span> <span data-ttu-id="3fbbd-133">Il revient à l’application de restaurer ces paramètres après le chargement d’un projet.</span><span class="sxs-lookup"><span data-stu-id="3fbbd-133">It is up to the application to restore these parameters after it loads a project.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fbbd-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3fbbd-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fbbd-135">Utilisation des services de modification DirectShow</span><span class="sxs-lookup"><span data-stu-id="3fbbd-135">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



