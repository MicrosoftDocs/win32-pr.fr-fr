---
description: Un effet (qui est souvent stocké dans un fichier avec une extension de fichier. FX) déclare l’état du pipeline défini par un effet.
ms.assetid: 75b76d65-be97-41c2-8c45-4369fcfd69ce
title: Format d’effet (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5671750d7b4146ae5da8b0ba61ceae390b60a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393220"
---
# <a name="effect-format-direct3d-10"></a><span data-ttu-id="eb830-103">Format d’effet (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="eb830-103">Effect Format (Direct3D 10)</span></span>

<span data-ttu-id="eb830-104">Un effet (qui est souvent stocké dans un fichier avec une extension de fichier. FX) déclare l’état du pipeline défini par un effet.</span><span class="sxs-lookup"><span data-stu-id="eb830-104">An effect (which is often stored in a file with a .fx file extension) declares the pipeline state set by an effect.</span></span> <span data-ttu-id="eb830-105">L’état de l’effet peut être divisé en trois catégories :</span><span class="sxs-lookup"><span data-stu-id="eb830-105">Effect state can be roughly broken down into three categories:</span></span>

-   <span data-ttu-id="eb830-106">[Variables](d3d10-effect-variable-syntax.md), qui sont généralement déclarées en haut d’un effet.</span><span class="sxs-lookup"><span data-stu-id="eb830-106">[Variables](d3d10-effect-variable-syntax.md), which are usually declared at the top of an effect.</span></span>
-   <span data-ttu-id="eb830-107">Les [fonctions](d3d10-effect-function-syntax.md), qui implémentent le code du nuanceur, ou sont utilisées comme fonctions d’assistance par d’autres fonctions.</span><span class="sxs-lookup"><span data-stu-id="eb830-107">[Functions](d3d10-effect-function-syntax.md), which implement shader code, or are used as helper functions by other functions.</span></span>
-   <span data-ttu-id="eb830-108">[Technique](d3d10-effect-technique-syntax.md), qui implémente des séquences de rendu à l’aide d’une ou de plusieurs passes d’effet.</span><span class="sxs-lookup"><span data-stu-id="eb830-108">[A technique](d3d10-effect-technique-syntax.md), which implements rendering sequences using one or more effect passes.</span></span> <span data-ttu-id="eb830-109">Chaque passe définit un ou plusieurs [groupes d’États](d3d10-effect-states.md) et appelle des fonctions de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="eb830-109">Each pass sets one or more [state groups](d3d10-effect-states.md) and calls shader functions.</span></span>

![diagramme des catégories d’état d’effet](images/d3d10-effect-intro.png)

<span data-ttu-id="eb830-111">Le diagramme précédent montre les catégories d’état d’effet.</span><span class="sxs-lookup"><span data-stu-id="eb830-111">The preceding diagram shows the categories of effect state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb830-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eb830-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb830-113">Référence d’effet</span><span class="sxs-lookup"><span data-stu-id="eb830-113">Effect Reference</span></span>](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 



