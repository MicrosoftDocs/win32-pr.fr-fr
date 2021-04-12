---
description: Considérations relatives aux performances (Direct3D 10)
ms.assetid: 9f029be5-4ce0-46ca-909b-adaa980398e7
title: Considérations relatives aux performances (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba2dbe00475efebdb6ff5d772b3eccd6cd4263a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033631"
---
# <a name="performance-considerations-direct3d-10"></a><span data-ttu-id="a195a-103">Considérations relatives aux performances (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="a195a-103">Performance Considerations (Direct3D 10)</span></span>

## <a name="using-effect-pools"></a><span data-ttu-id="a195a-104">Utilisation des pools d’effets</span><span class="sxs-lookup"><span data-stu-id="a195a-104">Using Effect Pools</span></span>

<span data-ttu-id="a195a-105">Il est courant que les pipelines de rendu utilisent de nombreux nuanceurs pour afficher différents types d’objets et effets spéciaux.</span><span class="sxs-lookup"><span data-stu-id="a195a-105">It is common for rendering pipelines to use many shaders to render different object types and special effects.</span></span> <span data-ttu-id="a195a-106">Le nuanceur est un mélange d’États qui sont communs à tous les nuanceurs tels qu’une matrice universelle ou une position légère, et d’autres États spécifiques à chaque nuanceur, tels que la couleur diffuse d’un objet ou le calcul de surbrillance spéculaire.</span><span class="sxs-lookup"><span data-stu-id="a195a-106">The shader are a mixture of states that a common among all the shaders such as a world matrix or a light position, and other state that is specific to each shader such as an object's diffuse color, or specular highlight calculation.</span></span> <span data-ttu-id="a195a-107">Un pool d’effets est un emplacement en mémoire où stocker l’État utilisé dans de nombreux nuanceurs, ainsi que des objets d’appareil courants tels que les nuanceurs, les objets d’état de rendu et les mémoires tampons constantes.</span><span class="sxs-lookup"><span data-stu-id="a195a-107">An effect pool is a place in memory to store state that is used across many shaders, as well as common device objects such as shaders, render state objects and constant buffers.</span></span> <span data-ttu-id="a195a-108">L’amélioration des performances résulte de la mise à jour de l’État commun une seule fois pour tous les nuanceurs qui ont besoin de cet État.</span><span class="sxs-lookup"><span data-stu-id="a195a-108">The performance improvement results from updating the common state once for all the shaders that need that state.</span></span>

<span data-ttu-id="a195a-109">Un pool d’effets est un emplacement de mémoire partagée pour l’état de l’effet.</span><span class="sxs-lookup"><span data-stu-id="a195a-109">An effect pool is a shared memory location for effect state.</span></span> <span data-ttu-id="a195a-110">Un pool est créé de la même façon qu’un effet ; Il peut être créé à partir de la mémoire (ou d’un fichier ou d’une ressource).</span><span class="sxs-lookup"><span data-stu-id="a195a-110">A pool is created similarly to an effect; it can be created from memory (or a file or a resource).</span></span> <span data-ttu-id="a195a-111">Cela entraîne deux types différents d’effets : un effet global qui ne dépend pas de l’état d’un autre effet par rapport à un effet enfant qui dépend de l’état d’un autre effet.</span><span class="sxs-lookup"><span data-stu-id="a195a-111">This leads to two different types of effects: a global effect that does not depend on state in other effect versus a child effect which depends on state in another effect.</span></span>

<span data-ttu-id="a195a-112">Vous spécifiez si un effet est un effet global (cas par défaut) ou un effet enfant (en fournissant l’effet D3D10 l’indicateur de compilation d’effet [ \_ \_ \_ enfant \_ ](d3d10-effect.md) ) lors de la création de l’effet.</span><span class="sxs-lookup"><span data-stu-id="a195a-112">You specify whether an effect is a global effect (the default case) or a child effect (by supplying the [D3D10\_EFFECT\_COMPILE\_CHILD\_EFFECT](d3d10-effect.md) flag) when the effect is created.</span></span> <span data-ttu-id="a195a-113">Un effet global peut servir de pool d’effets ; un effet enfant ne peut pas être un pool d’effets.</span><span class="sxs-lookup"><span data-stu-id="a195a-113">A global effect can serve as an effect pool; a child effect cannot be an effect pool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a195a-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a195a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a195a-115">Rendu d’un effet</span><span class="sxs-lookup"><span data-stu-id="a195a-115">Rendering an Effect</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> <dt>

[<span data-ttu-id="a195a-116">Effets (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="a195a-116">Effects (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



