---
description: Chronologie
ms.assetid: a3b8bff2-8593-483c-af49-a975ab2dc330
title: Chronologie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6ac73b84409629f63ad4be469edf6b943f9e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535700"
---
# <a name="the-timeline"></a><span data-ttu-id="01cf1-103">Chronologie</span><span class="sxs-lookup"><span data-stu-id="01cf1-103">The Timeline</span></span>

<span data-ttu-id="01cf1-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="01cf1-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="01cf1-105">La chronologie expose l’interface [**IAMTimeline**](iamtimeline.md) .</span><span class="sxs-lookup"><span data-stu-id="01cf1-105">The timeline exposes the [**IAMTimeline**](iamtimeline.md) interface.</span></span> <span data-ttu-id="01cf1-106">Cette interface contient des méthodes pour définir des propriétés sur la chronologie ; pour ajouter des groupes à la chronologie ; et pour créer des objets Timeline, tels que des groupes, des pistes et des sources.</span><span class="sxs-lookup"><span data-stu-id="01cf1-106">This interface contains methods for setting properties on the timeline; for adding groups to the timeline; and for creating timeline objects, such as groups, tracks, and sources.</span></span> <span data-ttu-id="01cf1-107">Pour créer une nouvelle chronologie, appelez la fonction **CoCreateInstance** standard comme suit :</span><span class="sxs-lookup"><span data-stu-id="01cf1-107">To create a new timeline, call the standard **CoCreateInstance** function as follows:</span></span>


```C++
IAMTimeline *pTL = NULL;
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
        IID_IAMTimeline, (void**)&pTL);
```



<span data-ttu-id="01cf1-108">La Nouvelle chronologie est vide.</span><span class="sxs-lookup"><span data-stu-id="01cf1-108">The new timeline is empty.</span></span> <span data-ttu-id="01cf1-109">À ce stade, vous pouvez charger un fichier projet existant (voir [chargement et aperçu d’un projet](loading-and-previewing-a-project.md)), ou générer la chronologie en créant et en insérant de nouveaux objets (consultez [construction d’une chronologie](constructing-a-timeline.md)).</span><span class="sxs-lookup"><span data-stu-id="01cf1-109">At this point you can either load an existing project file (see [Loading and Previewing a Project](loading-and-previewing-a-project.md)), or build up the timeline by creating and inserting new objects (see [Constructing a Timeline](constructing-a-timeline.md)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="01cf1-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="01cf1-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01cf1-111">Vue d’ensemble des composants de la chronologie</span><span class="sxs-lookup"><span data-stu-id="01cf1-111">Overview of the Timeline Components</span></span>](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



