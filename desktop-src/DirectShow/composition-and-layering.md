---
description: Composition et structuration en couches
ms.assetid: c1aefd92-b47f-4af1-8299-9ba401ad5fe8
title: Composition et structuration en couches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7dce1e1df87b5ffc5c65e9090c6fb7266b972d3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514303"
---
# <a name="composition-and-layering"></a><span data-ttu-id="fdb63-103">Composition et structuration en couches</span><span class="sxs-lookup"><span data-stu-id="fdb63-103">Composition and Layering</span></span>

<span data-ttu-id="fdb63-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="fdb63-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="fdb63-105">Dans une collection de suivis, la première piste a la priorité la plus faible (priorité 0) et chaque piste suivante a une priorité d’un niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="fdb63-105">In a collection of tracks, the first track has the lowest priority (priority 0) and each subsequent track has a priority one level higher.</span></span> <span data-ttu-id="fdb63-106">À chaque niveau de priorité, les éléments sources de cette piste masquent les éléments sources dans les pistes situées en dessous, sauf si cette couche contient également une transition.</span><span class="sxs-lookup"><span data-stu-id="fdb63-106">At each priority level, the source clips in that track hide the source clips in the tracks below it, unless that layer also contains a transition.</span></span> <span data-ttu-id="fdb63-107">Ainsi, vous pouvez imaginer plusieurs passages lors du rendu.</span><span class="sxs-lookup"><span data-stu-id="fdb63-107">Thus you can imagine DES making several passes when it renders.</span></span>

<span data-ttu-id="fdb63-108">Tout d’abord, elle affiche la piste 0.</span><span class="sxs-lookup"><span data-stu-id="fdb63-108">First, it renders track 0.</span></span> <span data-ttu-id="fdb63-109">Il n’y a rien « sous «Track 0 », donc les régions vides sont rendues sous la forme d’une image noire unie.</span><span class="sxs-lookup"><span data-stu-id="fdb63-109">There is nothing "under" Track 0, so empty regions are rendered as a solid black image.</span></span> <span data-ttu-id="fdb63-110">Les transitions dans cette couche se produisent entre l’image noire et la piste 0, ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="fdb63-110">Transitions in this layer occur between the black image and track 0 or vice versa.</span></span> <span data-ttu-id="fdb63-111">DES présente le suivi 1 en plus de la piste 0, générant des transitions entre les deux pistes.</span><span class="sxs-lookup"><span data-stu-id="fdb63-111">DES lays track 1 on top of track 0, generating any transitions between the two tracks.</span></span> <span data-ttu-id="fdb63-112">Le résultat est le composite des deux pistes.</span><span class="sxs-lookup"><span data-stu-id="fdb63-112">The result is the composite of the two tracks.</span></span> <span data-ttu-id="fdb63-113">Ensuite, il place la piste 2 sur ce composite.</span><span class="sxs-lookup"><span data-stu-id="fdb63-113">Next, it places track 2 onto this composite.</span></span> <span data-ttu-id="fdb63-114">Les transitions à cette couche se produisent entre le composite et le rail 2.</span><span class="sxs-lookup"><span data-stu-id="fdb63-114">Transitions at this layer occur between the composite and track 2.</span></span> <span data-ttu-id="fdb63-115">Le processus se poursuit jusqu’à ce que la dernière piste (priorité la plus élevée) soit déplacée.</span><span class="sxs-lookup"><span data-stu-id="fdb63-115">The process continues until the last (highest-priority) track is put down.</span></span>

<span data-ttu-id="fdb63-116">Lorsque plusieurs pistes sont composites ensemble, elles se comportent comme une seule piste (appelée une piste virtuelle).</span><span class="sxs-lookup"><span data-stu-id="fdb63-116">When several tracks are composited together, they behave like a single track (called a virtual track).</span></span> <span data-ttu-id="fdb63-117">L’objet composition encapsule ce comportement, ce qui rend possible des transitions complexes.</span><span class="sxs-lookup"><span data-stu-id="fdb63-117">The composition object encapsulates this behavior, making complex transitions possible.</span></span> <span data-ttu-id="fdb63-118">Par exemple, un clip vidéo peut être réinitialisé jusqu’à un deuxième élément, tandis que le composite (les deux clips et la réinitialisation) apparaît en fondu sur un troisième élément.</span><span class="sxs-lookup"><span data-stu-id="fdb63-118">For example, one video clip can wipe to a second clip, while the composite (both clips plus the wipe) fades to a third clip.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fdb63-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fdb63-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdb63-120">Prise en main avec les services d’édition DirectShow</span><span class="sxs-lookup"><span data-stu-id="fdb63-120">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



