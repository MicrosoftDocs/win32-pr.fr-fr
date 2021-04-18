---
description: Modèle de chronologie
ms.assetid: 53e782a2-0fab-46b4-b029-20017d9905bd
title: Modèle de chronologie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac01f90e8ca827bde41f2ad36e1ab32b3d429437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104565265"
---
# <a name="the-timeline-model"></a><span data-ttu-id="2697a-103">Modèle de chronologie</span><span class="sxs-lookup"><span data-stu-id="2697a-103">The Timeline Model</span></span>

<span data-ttu-id="2697a-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="2697a-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="2697a-105">Une *chronologie* est un objet utilisé par les [services d’édition DirectShow](directshow-editing-services.md) pour représenter un projet de montage vidéo.</span><span class="sxs-lookup"><span data-stu-id="2697a-105">A *timeline* is an object that [DirectShow Editing Services](directshow-editing-services.md) (DES) uses to represent a video editing project.</span></span> <span data-ttu-id="2697a-106">Un projet d’édition commence sous la forme d’une collection d’éléments sources, issus de fichiers vidéo, de fichiers audio ou de fichiers image toujours.</span><span class="sxs-lookup"><span data-stu-id="2697a-106">An editing project starts as a collection of source clips, taken from video files, sound files, or still image files.</span></span> <span data-ttu-id="2697a-107">Une séquence linéaire d’éléments forme une *piste*. Dans les services de modification DirectShow (DES), l’audio et la vidéo sont placés dans des pistes distinctes.</span><span class="sxs-lookup"><span data-stu-id="2697a-107">A linear sequence of clips forms a *track*. In DirectShow Editing Services (DES), audio and video are placed in separate tracks.</span></span>

<span data-ttu-id="2697a-108">Les pistes peuvent également être superposées.</span><span class="sxs-lookup"><span data-stu-id="2697a-108">Tracks can also be layered.</span></span> <span data-ttu-id="2697a-109">Plusieurs pistes audio sont mélangées et peuvent inclure des effets audio, tels qu’un fondu ou une réverbération.</span><span class="sxs-lookup"><span data-stu-id="2697a-109">Multiple audio tracks are mixed together, and might include audio effects, such as fades or reverb.</span></span> <span data-ttu-id="2697a-110">Plusieurs pistes vidéo sont utilisées pour créer des transitions.</span><span class="sxs-lookup"><span data-stu-id="2697a-110">Multiple video tracks are used to create transitions.</span></span> <span data-ttu-id="2697a-111">Par exemple, vous pouvez créer une réinitialisation d’un élément à un autre.</span><span class="sxs-lookup"><span data-stu-id="2697a-111">For example, you can create a wipe from one clip to another.</span></span> <span data-ttu-id="2697a-112">Un autre exemple est une clé Chroma, dans laquelle l’arrière-plan d’un clip est entré et remplacé par une autre piste. (Les prévisions météorologiques devant une image satelite sont un exemple de masquage Chroma.)</span><span class="sxs-lookup"><span data-stu-id="2697a-112">Another example is a chroma key, in which the background of one clip is keyed out and replaced by a different track. (The weather forecaster in front of a satelite image is an example of chroma keying.)</span></span>

<span data-ttu-id="2697a-113">DES utilise une structure arborescente pour représenter une modification :</span><span class="sxs-lookup"><span data-stu-id="2697a-113">DES uses a tree structure to represent an editing:</span></span>

-   <span data-ttu-id="2697a-114">Les clips audio et vidéo forment les nœuds terminaux ou les objets *sources* .</span><span class="sxs-lookup"><span data-stu-id="2697a-114">Audio and video clips form the leaf nodes, or *source* objects.</span></span>
-   <span data-ttu-id="2697a-115">Une collection de sources avec un type de média uniforme (audio ou vidéo) est une *piste*.</span><span class="sxs-lookup"><span data-stu-id="2697a-115">A collection of sources with a uniform media type (audio or video) is a *track*.</span></span>
-   <span data-ttu-id="2697a-116">Une collection de pistes est une *composition*.</span><span class="sxs-lookup"><span data-stu-id="2697a-116">A collection of tracks is a *composition*.</span></span> <span data-ttu-id="2697a-117">Une composition est rendue comme composite de toutes les pistes qu’elle contient.</span><span class="sxs-lookup"><span data-stu-id="2697a-117">A composition is rendered as the composite of all the tracks it contains.</span></span> <span data-ttu-id="2697a-118">Les compositions peuvent contenir d’autres compositions, ce qui permet des dispositions complexes des pistes.</span><span class="sxs-lookup"><span data-stu-id="2697a-118">Compositions can contain other compositions, which allows for complex arrangements of tracks.</span></span>
-   <span data-ttu-id="2697a-119">Une collection de niveau supérieur de compositions et de pistes (représentant toutes le même type de média) est un *groupe*.</span><span class="sxs-lookup"><span data-stu-id="2697a-119">A top-level collection of compositions and tracks (all representing the same media type) is a *group*.</span></span>
-   <span data-ttu-id="2697a-120">Un ensemble d’un ou plusieurs groupes forme une *chronologie*.</span><span class="sxs-lookup"><span data-stu-id="2697a-120">A set of one or more groups forms a *timeline*.</span></span> <span data-ttu-id="2697a-121">La chronologie est le nœud racine de l’arborescence.</span><span class="sxs-lookup"><span data-stu-id="2697a-121">The timeline is the root node in the tree.</span></span>

<span data-ttu-id="2697a-122">Une chronologie doit contenir au moins un groupe.</span><span class="sxs-lookup"><span data-stu-id="2697a-122">A timeline must contain at least one group.</span></span> <span data-ttu-id="2697a-123">Chaque groupe représente un seul flux dans la production finale.</span><span class="sxs-lookup"><span data-stu-id="2697a-123">Each group represents a single stream in the final production.</span></span> <span data-ttu-id="2697a-124">Un projet standard comprend un groupe vidéo et un groupe audio.</span><span class="sxs-lookup"><span data-stu-id="2697a-124">A typical project includes one video group and one audio group.</span></span> <span data-ttu-id="2697a-125">Les compositions sont facultatives. ils existent pour fournir davantage de structure si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="2697a-125">Compositions are optional; they exist to provide more structure if needed.</span></span>

<span data-ttu-id="2697a-126">L’illustration suivante montre les relations parent-enfant qui composent une chronologie :</span><span class="sxs-lookup"><span data-stu-id="2697a-126">The following illustration shows the child-parent relations that make up a timeline:</span></span>

![structure de nœud](images/timeline1.png)

<span data-ttu-id="2697a-128">L’exemple suivant montre une chronologie sous la forme d’une séquence temporelle :</span><span class="sxs-lookup"><span data-stu-id="2697a-128">The following shows a timeline as a temporal sequence:</span></span>

![illustration de la chronologie](images/timeline2.png)

<span data-ttu-id="2697a-130">La flèche située en haut représente le sens de la chronologie, à partir de l’heure zéro.</span><span class="sxs-lookup"><span data-stu-id="2697a-130">The arrow at the top represents the direction of the timeline, starting from time zero.</span></span> <span data-ttu-id="2697a-131">Dans le groupe vidéo, Track 1 a une priorité plus élevée que Track 0.</span><span class="sxs-lookup"><span data-stu-id="2697a-131">Within the video group, track 1 has a higher priority than track 0.</span></span> <span data-ttu-id="2697a-132">Les objets sources de Track 1 les masquent dans Track 0.</span><span class="sxs-lookup"><span data-stu-id="2697a-132">The source objects in track 1 obscure those in track 0.</span></span> <span data-ttu-id="2697a-133">Où Track 1 est vide, Track 0» s’affiche.</span><span class="sxs-lookup"><span data-stu-id="2697a-133">Where track 1 is empty, track 0 "shows through."</span></span> <span data-ttu-id="2697a-134">Comme mentionné précédemment, les pistes audio sont simplement mélangées.</span><span class="sxs-lookup"><span data-stu-id="2697a-134">As mentioned earlier, audio tracks are simply mixed together.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2697a-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2697a-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2697a-136">Prise en main avec les services d’édition DirectShow</span><span class="sxs-lookup"><span data-stu-id="2697a-136">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[<span data-ttu-id="2697a-137">Construction d’une chronologie</span><span class="sxs-lookup"><span data-stu-id="2697a-137">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



