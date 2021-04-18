---
description: Architecture des services de modification DirectShow
ms.assetid: ba6cc3f1-9130-4197-8501-c2d0a088e847
title: Architecture des services de modification DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c6059eebe9228e61d3de9677972eedfcb51c62
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106527175"
---
# <a name="directshow-editing-services-architecture"></a><span data-ttu-id="4d6ad-103">Architecture des services de modification DirectShow</span><span class="sxs-lookup"><span data-stu-id="4d6ad-103">DirectShow Editing Services Architecture</span></span>

<span data-ttu-id="4d6ad-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="4d6ad-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="4d6ad-105">L’illustration suivante montre l’architecture des [services de modification DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="4d6ad-105">The following illustration shows the architecture of [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

![architecture des services de modification DirectShow](images/architecture.png)

-   <span data-ttu-id="4d6ad-107">Timeline : représente une production vidéo sous la forme d’une collection d’éléments sources, de transitions et d’effets, organisée en un ensemble de pistes imbriquées.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-107">Timeline: Represents a video production as a collection of source clips, transitions, and effects, organized into a set of nested tracks.</span></span> <span data-ttu-id="4d6ad-108">Pour plus d’informations, consultez [le modèle Timeline](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="4d6ad-108">For more information, see [The Timeline Model](the-timeline-model.md).</span></span>
-   <span data-ttu-id="4d6ad-109">Analyseur XML : analyse la chronologie et génère un fichier de sortie, ou lit un fichier d’entrée et génère une chronologie.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-109">XML Parser: Parses the timeline and generates an output file, or reads an input file and generates a timeline.</span></span> <span data-ttu-id="4d6ad-110">DES prend en charge un format de persistance XML.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-110">DES supports an XML-based persistence format.</span></span>
-   <span data-ttu-id="4d6ad-111">Moteur de rendu : traduit la chronologie en un format qui peut être rendu en tant que média de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-111">Render engine: Translates the timeline into a form that can be rendered as streaming media.</span></span> <span data-ttu-id="4d6ad-112">Par défaut, le moteur de rendu produit un graphique de filtre DirectShow (voir la section suivante).</span><span class="sxs-lookup"><span data-stu-id="4d6ad-112">By default, the render engine produces a DirectShow filter graph (see next section).</span></span>
-   <span data-ttu-id="4d6ad-113">Localisateur de média : conserve un cache d’emplacements d’éléments multimédias.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-113">Media locator: Maintains a cache of locations of media elements.</span></span> <span data-ttu-id="4d6ad-114">En cas d’échec d’une tentative d’ouverture d’un élément multimédia, les utilisent le cache pour localiser l’élément, en fonction de l’historique des ouvertures réussies.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-114">When an attempt to open a media element fails, DES uses the cache to locate the element, based on a history of successful opens.</span></span>

<span data-ttu-id="4d6ad-115">La chronologie est une description abstraite d’un projet de montage vidéo.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-115">The timeline is an abstract description of a video editing project.</span></span> <span data-ttu-id="4d6ad-116">Il spécifie les éléments sources utilisés dans le projet, les heures de démarrage et d’arrêt, les effets et les transitions, etc.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-116">It specifies the source clips used in the project, start and stop times, effects and transitions, and so forth.</span></span> <span data-ttu-id="4d6ad-117">Toutefois, la chronologie ne rend pas les flux vidéo et audio.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-117">The timeline does not render the video and audio streams, however.</span></span> <span data-ttu-id="4d6ad-118">Au lieu de cela, le moteur de rendu traduit la chronologie en un graphique de filtre, pour la sortie de l’aperçu ou du fichier.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-118">Instead, the render engine translates the timeline into a filter graph, for either preview or file output.</span></span> <span data-ttu-id="4d6ad-119">Une application manipule la chronologie plutôt que de manipuler directement le graphique de filtre, ce qui serait fastidieux et sujet aux erreurs.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-119">An application manipulates the timeline rather than directly manipulating the filter graph, which would be cumbersome and error prone.</span></span>

<span data-ttu-id="4d6ad-120">Le tableau suivant répertorie les principales tâches qu’une application de modification vidéo classique effectue, ainsi que les interfaces qui prennent en charge chaque tâche.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-120">The following table lists the main tasks that a typical video editing application performs, along with the interfaces that support each task.</span></span> <span data-ttu-id="4d6ad-121">Les sections suivantes décrivent ces tâches et les interfaces plus en détail.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-121">Later sections describe these tasks and the interfaces in more detail.</span></span>



| <span data-ttu-id="4d6ad-122">Tâche</span><span class="sxs-lookup"><span data-stu-id="4d6ad-122">Task</span></span>                                     | <span data-ttu-id="4d6ad-123">Interface (s)</span><span class="sxs-lookup"><span data-stu-id="4d6ad-123">Interface(s)</span></span>                                                                             |
|------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d6ad-124">Construisez ou modifiez une chronologie.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-124">Construct or modify a timeline.</span></span>          | <span data-ttu-id="4d6ad-125">[**IAMTimeline**](iamtimeline.md) et les autres interfaces **IAMTimelineXXXX**</span><span class="sxs-lookup"><span data-stu-id="4d6ad-125">[**IAMTimeline**](iamtimeline.md) and the other **IAMTimelineXXXX** interfaces</span></span>          |
| <span data-ttu-id="4d6ad-126">Enregistrez et chargez les fichiers projet.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-126">Save and load project files.</span></span>             | [<span data-ttu-id="4d6ad-127">**IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="4d6ad-127">**IXml2Dex**</span></span>](ixml2dex.md)                                                             |
| <span data-ttu-id="4d6ad-128">Affichez l’aperçu d’un projet ou écrivez-le dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-128">Preview a project or write it to a file.</span></span> | <span data-ttu-id="4d6ad-129">[**IRenderEngine**](irenderengine.md), [ **ISmartRenderEngine**](ismartrenderengine.md)</span><span class="sxs-lookup"><span data-stu-id="4d6ad-129">[**IRenderEngine**](irenderengine.md), [**ISmartRenderEngine**](ismartrenderengine.md)</span></span> |



 

<span data-ttu-id="4d6ad-130">En outre, une application peut effectuer une partie ou l’ensemble des tâches secondaires suivantes.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-130">In addition, an application might perform some or all of the following secondary tasks.</span></span>



| <span data-ttu-id="4d6ad-131">Tâche</span><span class="sxs-lookup"><span data-stu-id="4d6ad-131">Task</span></span>                                                                                           | <span data-ttu-id="4d6ad-132">Interface (s)</span><span class="sxs-lookup"><span data-stu-id="4d6ad-132">Interface(s)</span></span>                                                                 |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="4d6ad-133">Obtenir des informations sur les fichiers multimédias.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-133">Obtain information about media files.</span></span> <span data-ttu-id="4d6ad-134">(Nombre de flux, format et durée de chaque flux.)</span><span class="sxs-lookup"><span data-stu-id="4d6ad-134">(Number of streams; format and duration of each stream.)</span></span> | [<span data-ttu-id="4d6ad-135">**IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="4d6ad-135">**IMediaDet**</span></span>](imediadet.md)                                               |
| <span data-ttu-id="4d6ad-136">Définissez les propriétés des transitions et des effets.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-136">Set properties on transitions and effects.</span></span>                                                     | [<span data-ttu-id="4d6ad-137">**IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="4d6ad-137">**IPropertySetter**</span></span>](ipropertysetter.md)                                   |
| <span data-ttu-id="4d6ad-138">Recevoir une notification lorsque des erreurs se produisent pendant le rendu.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-138">Receive notification when errors occur during rendering.</span></span>                                       | <span data-ttu-id="4d6ad-139">[**IAMSetErrorLog**](iamseterrorlog.md), [ **IAMErrorLog**](iamerrorlog.md)</span><span class="sxs-lookup"><span data-stu-id="4d6ad-139">[**IAMSetErrorLog**](iamseterrorlog.md), [**IAMErrorLog**](iamerrorlog.md)</span></span> |
| <span data-ttu-id="4d6ad-140">Récupérez les images de poster.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-140">Retrieve poster frames.</span></span>                                                                        | <span data-ttu-id="4d6ad-141">[**IMediaDet**](imediadet.md), [ **ISampleGrabber**](isamplegrabber.md)</span><span class="sxs-lookup"><span data-stu-id="4d6ad-141">[**IMediaDet**](imediadet.md), [**ISampleGrabber**](isamplegrabber.md)</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="4d6ad-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4d6ad-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d6ad-143">Prise en main avec les services d’édition DirectShow</span><span class="sxs-lookup"><span data-stu-id="4d6ad-143">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



