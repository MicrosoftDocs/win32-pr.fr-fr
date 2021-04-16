---
description: Construction d’une chronologie
ms.assetid: 4909f797-d296-4c9f-83fb-543e48bbe75d
title: Construction d’une chronologie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c16b1134eb92b3e3ac5a0f1919d7c4a2736b206
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392723"
---
# <a name="constructing-a-timeline"></a><span data-ttu-id="55abb-103">Construction d’une chronologie</span><span class="sxs-lookup"><span data-stu-id="55abb-103">Constructing a Timeline</span></span>

<span data-ttu-id="55abb-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="55abb-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="55abb-105">Cet article explique comment construire une chronologie dans les [services de modification DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="55abb-105">This article describes how to construct a timeline in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="55abb-106">Il présente un exemple d’application console qui crée une chronologie et l’affiche.</span><span class="sxs-lookup"><span data-stu-id="55abb-106">It presents an example console application that creates a timeline and renders it.</span></span> <span data-ttu-id="55abb-107">La chronologie est minimale, composée d’un seul groupe vidéo avec un seul clip source, mais elle présente la plupart des concepts nécessaires pour créer des chronologies plus complexes.</span><span class="sxs-lookup"><span data-stu-id="55abb-107">The timeline is minimal, consisting of a single video group with one source clip, but it demonstrates most of the concepts needed to create more complex timelines.</span></span>

<span data-ttu-id="55abb-108">Cet article contient les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="55abb-108">This article contains the following topics.</span></span>

-   [<span data-ttu-id="55abb-109">Création d’objets Timeline</span><span class="sxs-lookup"><span data-stu-id="55abb-109">Creating Timeline Objects</span></span>](creating-timeline-objects.md)
-   [<span data-ttu-id="55abb-110">Création de groupes, de compositions et de suivis</span><span class="sxs-lookup"><span data-stu-id="55abb-110">Creating Groups, Compositions, and Tracks</span></span>](creating-groups-compositions-and-tracks.md)
-   [<span data-ttu-id="55abb-111">Définition du type de support de groupe</span><span class="sxs-lookup"><span data-stu-id="55abb-111">Setting the Group Media Type</span></span>](setting-the-group-media-type.md)
-   [<span data-ttu-id="55abb-112">Ajout d’une source</span><span class="sxs-lookup"><span data-stu-id="55abb-112">Adding a Source</span></span>](adding-a-source.md)
-   [<span data-ttu-id="55abb-113">Création d’une chronologie : exemple de code</span><span class="sxs-lookup"><span data-stu-id="55abb-113">Creating a Timeline: Example Code</span></span>](creating-a-timeline--example-code.md)

## <a name="related-topics"></a><span data-ttu-id="55abb-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="55abb-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55abb-115">Utilisation des services de modification DirectShow</span><span class="sxs-lookup"><span data-stu-id="55abb-115">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



