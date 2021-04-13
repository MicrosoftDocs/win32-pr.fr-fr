---
description: Le pipeline graphique Direct3D 10 représente une modification d’architecture fondamentale, reconstruite à partir de la base du matériel et des logiciels pour alimenter la prochaine génération de jeux et d’applications multimédias 3D.
ms.assetid: 2e24de6c-4f73-4844-b87f-3487ef069db6
title: Fonctionnalités de l’API (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab12285509441bb429c78d995e68ed1753ceb5bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200924"
---
# <a name="api-features-direct3d-10"></a><span data-ttu-id="44096-103">Fonctionnalités de l’API (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="44096-103">API Features (Direct3D 10)</span></span>

<span data-ttu-id="44096-104">Le pipeline graphique Direct3D 10 représente une modification d’architecture fondamentale, reconstruite à partir de la base du matériel et des logiciels pour alimenter la prochaine génération de jeux et d’applications multimédias 3D.</span><span class="sxs-lookup"><span data-stu-id="44096-104">The Direct3D 10 graphics pipeline represents a fundamental architecture change, rebuilt from the ground-up in hardware and software to power the next-generation of games and 3D multimedia applications.</span></span> <span data-ttu-id="44096-105">Il utilise le modèle WDDM (Windows Display Driver Model), qui permet des améliorations des performances et du comportement, telles que la mémoire du GPU virtuel.</span><span class="sxs-lookup"><span data-stu-id="44096-105">It uses the Windows Display Driver Model (WDDM), which enables performance and behavioral enhancements such as virtual GPU memory.</span></span>

<span data-ttu-id="44096-106">Les développeurs familiarisés avec Direct3D 9 découvriront une série d’améliorations fonctionnelles et des améliorations des performances dans Direct3D 10, notamment :</span><span class="sxs-lookup"><span data-stu-id="44096-106">Developers familiar with Direct3D 9 will discover a series of functional enhancements and performance improvements in Direct3D 10, including:</span></span>

-   <span data-ttu-id="44096-107">Capacité de traiter des primitives entières dans la nouvelle [étape Geometry-Shader](/previous-versions//bb205146(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="44096-107">The ability to process entire primitives in the new [geometry-shader stage](/previous-versions//bb205146(v=vs.85)).</span></span>
-   <span data-ttu-id="44096-108">Possibilité de produire des données de vertex générées par le pipeline dans la mémoire à l’aide de l' [étape de flux de sortie](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md).</span><span class="sxs-lookup"><span data-stu-id="44096-108">The ability to output pipeline-generated vertex data to memory using the [stream-output stage](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md).</span></span>
-   <span data-ttu-id="44096-109">Organisation de l’état du pipeline en 5 [objets d’État](d3d10-graphics-programming-guide-api-features-state-objects.md)immuables, permettant une configuration rapide du pipeline.</span><span class="sxs-lookup"><span data-stu-id="44096-109">Organization of pipeline state into 5 immutable [state objects](d3d10-graphics-programming-guide-api-features-state-objects.md), enabling fast configuration of the pipeline.</span></span>
-   <span data-ttu-id="44096-110">Organisation des constantes de nuanceur dans des [mémoires tampons constantes](d3d10-graphics-programming-guide-resources-types.md), minimisant la surcharge de bande passante pour fournir des données de nuanceur constantes.</span><span class="sxs-lookup"><span data-stu-id="44096-110">Organization of shader constants into [constant buffers](d3d10-graphics-programming-guide-resources-types.md), minimizing bandwidth overhead for supplying shader-constant data.</span></span>
-   <span data-ttu-id="44096-111">La possibilité d’effectuer un échange de matériel par primitive et une configuration à l’aide d’un nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="44096-111">The ability to perform per-primitive material swapping and setup using a geometry shader.</span></span>
-   <span data-ttu-id="44096-112">Nouveaux [types de ressources](d3d10-graphics-programming-guide-resources-types.md) (y compris des tableaux de textures qui peuvent être indexés à partir de nuanceurs) et des formats de ressources.</span><span class="sxs-lookup"><span data-stu-id="44096-112">New [resource types](d3d10-graphics-programming-guide-resources-types.md) (including texture arrays that can be indexed from shaders) and resource formats.</span></span>
-   <span data-ttu-id="44096-113">Plus grande généralisation de l’accès aux ressources à l’aide d’une [vue](d3d10-graphics-programming-guide-resources-access-views.md).</span><span class="sxs-lookup"><span data-stu-id="44096-113">Increased generalization of resource access using a [view](d3d10-graphics-programming-guide-resources-access-views.md).</span></span>
-   <span data-ttu-id="44096-114">Les bits des fonctionnalités matérielles héritées ont été supprimés en faveur d’un ensemble complet de fonctionnalités garanties, qui ciblent le matériel de classe Direct3D 10 (minimum).</span><span class="sxs-lookup"><span data-stu-id="44096-114">Legacy hardware capability bits (caps) have been removed in favor of a rich set of guaranteed functionality, which targets Direct3D 10-class hardware (minimum).</span></span>
-   <span data-ttu-id="44096-115">[Runtime à couches](d3d10-graphics-programming-guide-api-features-layers.md) : l’API Direct3D 10 est construite avec des couches, en commençant par les fonctionnalités de base au cœur et en créant des fonctionnalités facultatives et d’assistance aux développeurs (débogage, etc.) dans les couches externes.</span><span class="sxs-lookup"><span data-stu-id="44096-115">[Layered Runtime](d3d10-graphics-programming-guide-api-features-layers.md) - The Direct3D 10 API is constructed with layers, starting with the basic functionality at the core and building optional and developer-assist functionality (debug, etc.) in outer layers.</span></span>
-   <span data-ttu-id="44096-116">Intégration HLSL complète : tous les nuanceurs Direct3D 10 sont écrits en HLSL et implémentés avec le [Common-Shader Core](../direct3dhlsl/dx-graphics-hlsl-common-core.md).</span><span class="sxs-lookup"><span data-stu-id="44096-116">Full HLSL integration - All Direct3D 10 shaders are written in HLSL and implemented with the [common-shader core](../direct3dhlsl/dx-graphics-hlsl-common-core.md).</span></span>
-   <span data-ttu-id="44096-117">Augmentation du nombre de cibles de rendu, de textures et d’échantillonneurs.</span><span class="sxs-lookup"><span data-stu-id="44096-117">An increase in the number of render targets, textures, and samplers.</span></span> <span data-ttu-id="44096-118">Il n’existe pas non plus de limite de longueur de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="44096-118">There is also no shader length limit.</span></span>
-   <span data-ttu-id="44096-119">Opérations sur les entiers et les nuanceurs au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="44096-119">Integer and bitwise shader operations.</span></span>
-   <span data-ttu-id="44096-120">Readback d’une surface de profondeur/stencil ou d’une ressource à échantillonnage unique, une fois qu’elle n’est plus liée en tant que cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="44096-120">Readback of a depth/stencil surface or a multisampled resource, once it is no longer bound as a render target.</span></span>
-   <span data-ttu-id="44096-121">Prise en charge de l’alpha-à-couverture à l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="44096-121">Multisampled alpha-to-coverage support.</span></span>

<span data-ttu-id="44096-122">Des différences de comportement supplémentaires doivent également être prises en charge par les développeurs Direct3D 9 (voir [considérations relatives à Direct3D 9 vers Direct3D 10](d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations.md)).</span><span class="sxs-lookup"><span data-stu-id="44096-122">There are additional behavioral differences that Direct3D 9 developers should also be aware of (see [Direct3D 9 to Direct3D 10 Considerations](d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations.md)).</span></span>

<span data-ttu-id="44096-123">Voici une liste de fonctionnalités Direct3D 9 qui ne sont plus prises en charge ou qui ont été révisées dans Direct3D 10 (voir [fonctionnalités déconseillées](d3d10-graphics-programming-guide-api-features-deprecated.md)).</span><span class="sxs-lookup"><span data-stu-id="44096-123">Here is a list of Direct3D 9 features that either are no longer supported, or have been revised in Direct3D 10 (see [Deprecated Features](d3d10-graphics-programming-guide-api-features-deprecated.md)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="44096-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="44096-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44096-125">Guide de programmation pour Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="44096-125">Programming Guide for Direct3D 10</span></span>](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
