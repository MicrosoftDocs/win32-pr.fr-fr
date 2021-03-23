---
title: Pipelines et nuanceurs avec Direct3D 12
description: Le pipeline programmable Direct3D 12 augmente considérablement les performances de rendu par rapport aux interfaces de programmation graphique de génération précédente.
ms.assetid: 329882F5-D2A9-4D6D-AC3B-29F370D22C97
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2c392b3915443da2f287a5511f3959cbb7179f
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104548527"
---
# <a name="pipelines-and-shaders-with-direct3d-12"></a><span data-ttu-id="907f9-103">Pipelines et nuanceurs avec Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="907f9-103">Pipelines and Shaders with Direct3D 12</span></span>

<span data-ttu-id="907f9-104">Le pipeline programmable Direct3D 12 augmente considérablement les performances de rendu par rapport aux interfaces de programmation graphique de génération précédente.</span><span class="sxs-lookup"><span data-stu-id="907f9-104">The Direct3D 12 programmable pipeline significantly increases rendering performance compared to previous generation graphics programming interfaces.</span></span>

-   [<span data-ttu-id="907f9-105">Pipeline graphique Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="907f9-105">Direct3D 12 graphics pipeline</span></span>](#direct3d-12-graphics-pipeline)
-   [<span data-ttu-id="907f9-106">Objets d’état de pipeline</span><span class="sxs-lookup"><span data-stu-id="907f9-106">Pipeline state objects</span></span>](#pipeline-state-objects)
-   [<span data-ttu-id="907f9-107">Pipeline de calcul Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="907f9-107">Direct3D 12 compute pipeline</span></span>](#direct3d-12-compute-pipeline)
-   [<span data-ttu-id="907f9-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="907f9-108">Related topics</span></span>](#related-topics)

## <a name="direct3d-12-graphics-pipeline"></a><span data-ttu-id="907f9-109">Pipeline graphique Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="907f9-109">Direct3D 12 graphics pipeline</span></span>

<span data-ttu-id="907f9-110">Le diagramme suivant illustre l’État et le pipeline de graphiques Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="907f9-110">The following diagram illustrates the Direct3D 12 graphics pipeline and state.</span></span>

![Diagramme illustrant l’État et le pipeline Direct3D 12](images/pipeline.png)

<span data-ttu-id="907f9-112">Un pipeline Graphics est le workflow séquentiel des entrées et sorties de données à mesure que le GPU restitue des frames.</span><span class="sxs-lookup"><span data-stu-id="907f9-112">A graphics pipeline is the sequential flow of data inputs and outputs as the GPU renders frames.</span></span> <span data-ttu-id="907f9-113">Étant donné l’état du pipeline et les entrées, le GPU effectue une série d’opérations pour créer les images résultantes.</span><span class="sxs-lookup"><span data-stu-id="907f9-113">Given the pipeline state and inputs, the GPU performs a series of operations to create the resulting images.</span></span> <span data-ttu-id="907f9-114">Un pipeline graphique contient des nuanceurs qui effectuent des calculs et des effets de rendu programmables, ainsi que des opérations de fonction fixes.</span><span class="sxs-lookup"><span data-stu-id="907f9-114">A graphics pipeline contains shaders, which perform programmable rendering effects and calculations, and fixed function operations.</span></span>

<span data-ttu-id="907f9-115">Notez les points suivants lorsque vous faites référence au diagramme d’État du pipeline :</span><span class="sxs-lookup"><span data-stu-id="907f9-115">Note the following when referring to the pipeline state diagram:</span></span>

-   <span data-ttu-id="907f9-116">Les tables de descripteurs et les tas peuvent être disposés arbitrairement : SRVs, CBVs et UAVs peuvent être référencés et alloués dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="907f9-116">The descriptor tables and heaps can be arbitrarily arranged: SRVs, CBVs and UAVs can be referenced and allocated in any order.</span></span>
-   <span data-ttu-id="907f9-117">Certaines opérations du pipeline sont configurables.</span><span class="sxs-lookup"><span data-stu-id="907f9-117">Some operations of the pipeline are configurable.</span></span> <span data-ttu-id="907f9-118">Par exemple, la fusion de sortie fonctionne généralement sur une base de lecture-modification-écriture avec les vues de la cible de rendu et du stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="907f9-118">For example, the output merger typically operates on a read-modify-write basis with the render target and depth stencil views.</span></span> <span data-ttu-id="907f9-119">Toutefois, le pipeline peut être configuré de sorte que l’un de ces affichages soit en lecture seule ou en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="907f9-119">However the pipeline can be configured so that either of these views are read-only or write-only.</span></span>
-   <span data-ttu-id="907f9-120">Les échantillonneurs statiques ne font pas partie des arguments racine, car ils sont statiques.</span><span class="sxs-lookup"><span data-stu-id="907f9-120">Static samplers are not part of the root arguments since they are static.</span></span>

## <a name="pipeline-state-objects"></a><span data-ttu-id="907f9-121">Objets d’état de pipeline</span><span class="sxs-lookup"><span data-stu-id="907f9-121">Pipeline state objects</span></span>

<span data-ttu-id="907f9-122">Direct3D 12 introduit l’objet d’État du pipeline (PSO).</span><span class="sxs-lookup"><span data-stu-id="907f9-122">Direct3D 12 introduces the pipeline state object (PSO).</span></span> <span data-ttu-id="907f9-123">Au lieu de stocker et de représenter l’état du pipeline sur un grand nombre d’objets de niveau supérieur, les États des composants de pipeline tels que l’assembleur d’entrée, le rastériseur, le nuanceur de pixels et la fusion de sortie sont stockés dans un objet PSO.</span><span class="sxs-lookup"><span data-stu-id="907f9-123">Rather than storing and representing pipeline state across a large number of high-level objects, the states of pipeline components like the input assembler, rasterizer, pixel shader, and output merger are stored in a PSO.</span></span> <span data-ttu-id="907f9-124">Un objet PSO est un objet d’état de pipeline unifié qui est immuable après la création.</span><span class="sxs-lookup"><span data-stu-id="907f9-124">A PSO is a unified pipeline state object that is immutable after creation.</span></span> <span data-ttu-id="907f9-125">L’PSO actuellement sélectionné peut être modifié rapidement et de façon dynamique, et le matériel et les pilotes peuvent convertir directement un PSO en instructions et États matériels natifs, en préservant le GPU pour le traitement des graphiques.</span><span class="sxs-lookup"><span data-stu-id="907f9-125">The currently selected PSO can be changed quickly and dynamically, and the hardware and drivers can directly convert a PSO into native hardware instructions and state, readying the GPU for graphics processing.</span></span> <span data-ttu-id="907f9-126">Pour appliquer un PSO, le matériel copie une quantité minimale d’État précalculé directement dans les registres matériels.</span><span class="sxs-lookup"><span data-stu-id="907f9-126">To apply a PSO, the hardware copies a minimal amount of pre-computed state directly to the hardware registers.</span></span> <span data-ttu-id="907f9-127">Cela supprime la surcharge causée par le pilote Graphics qui recalcule continuellement l’état du matériel en fonction de tous les paramètres de pipeline et de rendu actuellement applicables.</span><span class="sxs-lookup"><span data-stu-id="907f9-127">This removes the overhead caused by the graphics driver continually recomputing hardware state based on all currently applicable rendering and pipeline settings.</span></span> <span data-ttu-id="907f9-128">Le résultat est considérablement réduit la surcharge des appels de dessin, des performances accrues et d’autres appels de dessin par trame.</span><span class="sxs-lookup"><span data-stu-id="907f9-128">The result is significantly reduced draw call overhead, increased performance, and more draw calls per frame.</span></span>

<span data-ttu-id="907f9-129">L’PSO actuellement appliqué définit et connecte tous les nuanceurs utilisés dans le pipeline de rendu.</span><span class="sxs-lookup"><span data-stu-id="907f9-129">The currently applied PSO defines and connects all of the shaders being used in the rendering pipeline.</span></span> <span data-ttu-id="907f9-130">Le [langage HLSL (High Level Shader Language) de Microsoft](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) est précompilé en objets nuanceur, qui sont ensuite utilisés au moment de l’exécution en tant qu’entrée pour les objets d’état de pipeline.</span><span class="sxs-lookup"><span data-stu-id="907f9-130">[Microsoft High Level Shader Language (HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) is pre-compiled into shader objects, which are then used at run time as input for pipeline state objects.</span></span> <span data-ttu-id="907f9-131">Pour plus d’informations sur le fonctionnement des fonctions PSO dans le pipeline Graphics, consultez [gestion de l’état des pipelines graphiques dans Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="907f9-131">For more information about how the PSO functions within the graphics pipeline, see [Managing graphics pipeline state in Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).</span></span>

## <a name="direct3d-12-compute-pipeline"></a><span data-ttu-id="907f9-132">Pipeline de calcul Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="907f9-132">Direct3D 12 compute pipeline</span></span>

<span data-ttu-id="907f9-133">Le diagramme suivant illustre l’État et le pipeline de calcul Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="907f9-133">The following diagram illustrates the Direct3D 12 compute pipeline and state.</span></span>

![Diagramme qui montre le pipeline de calcul Direct3D 12.](images/compute-pipeline.png)

<span data-ttu-id="907f9-135">Il n’y a pas d’unités de fonction fixe dans ce pipeline, mais les tas de descripteurs, les tas d’échantillonneur et les échantillonneurs statiques sont toujours disponibles dans Compute.</span><span class="sxs-lookup"><span data-stu-id="907f9-135">There are no fixed function units in this pipeline, however descriptor heaps, sampler heaps and static samplers are still available in compute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="907f9-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="907f9-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="907f9-137">Envoi de travail dans Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="907f9-137">Work Submission in Direct3D 12</span></span>](command-queues-and-command-lists.md)
</dt> </dl>

 

 