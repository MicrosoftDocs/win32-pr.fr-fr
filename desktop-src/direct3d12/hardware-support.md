---
title: Niveaux matériels
description: Les niveaux de matériel du niveau 1 au niveau 3 ont des ressources accrues disponibles pour le pipeline.
ms.assetid: 5A640BA9-3914-4481-9A0C-E18B52BD8AFE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38773412d135aa4068f0f843c1a6ef64af06a841
ms.sourcegitcommit: 9d7585cb0b840d0d1a2b7fd02135181e69d0dc9d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/15/2020
ms.locfileid: "104548494"
---
# <a name="hardware-tiers"></a><span data-ttu-id="6b801-103">Niveaux matériels</span><span class="sxs-lookup"><span data-stu-id="6b801-103">Hardware Tiers</span></span>

<span data-ttu-id="6b801-104">Les niveaux de matériel du niveau 1 au niveau 3 ont des ressources accrues disponibles pour le pipeline.</span><span class="sxs-lookup"><span data-stu-id="6b801-104">The levels of hardware from Tier 1 to Tier 3 have increasing resources available to the pipeline.</span></span>

-   [<span data-ttu-id="6b801-105">Limites dépend du matériel</span><span class="sxs-lookup"><span data-stu-id="6b801-105">Limits dependant on hardware</span></span>](#limits-dependant-on-hardware)
-   [<span data-ttu-id="6b801-106">Limites invariables</span><span class="sxs-lookup"><span data-stu-id="6b801-106">Invariable limits</span></span>](#invariable-limits)
-   [<span data-ttu-id="6b801-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6b801-107">Related topics</span></span>](#related-topics)

## <a name="limits-dependant-on-hardware"></a><span data-ttu-id="6b801-108">Limites dépend du matériel</span><span class="sxs-lookup"><span data-stu-id="6b801-108">Limits dependant on hardware</span></span>



| <span data-ttu-id="6b801-109">Ressources disponibles pour le pipeline</span><span class="sxs-lookup"><span data-stu-id="6b801-109">Resources Available to the Pipeline</span></span>                                                                                                              | <span data-ttu-id="6b801-110">Niveau 1</span><span class="sxs-lookup"><span data-stu-id="6b801-110">Tier 1</span></span>                                                                   | <span data-ttu-id="6b801-111">Niveau 2</span><span class="sxs-lookup"><span data-stu-id="6b801-111">Tier 2</span></span>        | <span data-ttu-id="6b801-112">Niveau 3</span><span class="sxs-lookup"><span data-stu-id="6b801-112">Tier 3</span></span>        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------|---------------|
| <span data-ttu-id="6b801-113">Niveaux de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="6b801-113">Feature levels</span></span>                                                                                                                                   | <span data-ttu-id="6b801-114">11.0 +</span><span class="sxs-lookup"><span data-stu-id="6b801-114">11.0+</span></span>                                                                    | <span data-ttu-id="6b801-115">11.0 +</span><span class="sxs-lookup"><span data-stu-id="6b801-115">11.0+</span></span>         | <span data-ttu-id="6b801-116">11.1 +</span><span class="sxs-lookup"><span data-stu-id="6b801-116">11.1+</span></span>         |
| <span data-ttu-id="6b801-117">Nombre maximal de descripteurs dans une vue de mémoire tampon constante (CBV), un Affichage des ressources de nuanceur (SRV) ou un tas de vue d’accès non ordonné (UAV) utilisé pour le rendu</span><span class="sxs-lookup"><span data-stu-id="6b801-117">Maximum number of descriptors in a Constant Buffer View (CBV), Shader Resource View (SRV), or Unordered Access View(UAV) heap used for rendering</span></span> | <span data-ttu-id="6b801-118">1 000 000</span><span class="sxs-lookup"><span data-stu-id="6b801-118">1,000,000</span></span>                                                                | <span data-ttu-id="6b801-119">1 000 000</span><span class="sxs-lookup"><span data-stu-id="6b801-119">1,000,000</span></span>     | <span data-ttu-id="6b801-120">1000000 +</span><span class="sxs-lookup"><span data-stu-id="6b801-120">1,000,000+</span></span>    |
| <span data-ttu-id="6b801-121">Nombre maximal de vues de mémoire tampon constante dans toutes les tables de descripteurs par étape de nuanceur</span><span class="sxs-lookup"><span data-stu-id="6b801-121">Maximum number of Constant Buffer Views in all descriptor tables per shader stage</span></span>                                                                | <span data-ttu-id="6b801-122">14</span><span class="sxs-lookup"><span data-stu-id="6b801-122">14</span></span>                                                                       | <span data-ttu-id="6b801-123">14</span><span class="sxs-lookup"><span data-stu-id="6b801-123">14</span></span>            | <span data-ttu-id="6b801-124">**tas complet**</span><span class="sxs-lookup"><span data-stu-id="6b801-124">**full heap**</span></span> |
| <span data-ttu-id="6b801-125">Nombre maximal de vues de ressources de nuanceur dans toutes les tables de descripteurs par étape de nuanceur</span><span class="sxs-lookup"><span data-stu-id="6b801-125">Maximum number of Shader Resource Views in all descriptor tables per shader stage</span></span>                                                                | <span data-ttu-id="6b801-126">128</span><span class="sxs-lookup"><span data-stu-id="6b801-126">128</span></span>                                                                      | <span data-ttu-id="6b801-127">**tas complet**</span><span class="sxs-lookup"><span data-stu-id="6b801-127">**full heap**</span></span> | <span data-ttu-id="6b801-128">tas complet</span><span class="sxs-lookup"><span data-stu-id="6b801-128">full heap</span></span>     |
| <span data-ttu-id="6b801-129">Nombre maximal de vues d’accès non ordonnées dans toutes les tables de descripteurs dans toutes les étapes</span><span class="sxs-lookup"><span data-stu-id="6b801-129">Maximum number of Unordered Access Views in all descriptor tables across all stages</span></span>                                                              | <span data-ttu-id="6b801-130">64 pour les niveaux de fonctionnalité 11.1 +</span><span class="sxs-lookup"><span data-stu-id="6b801-130">64 for feature levels 11.1+</span></span><br/> <span data-ttu-id="6b801-131">8 pour le niveau de fonctionnalité 11</span><span class="sxs-lookup"><span data-stu-id="6b801-131">8 for feature level 11</span></span><br/> | <span data-ttu-id="6b801-132">64</span><span class="sxs-lookup"><span data-stu-id="6b801-132">64</span></span>            | <span data-ttu-id="6b801-133">**tas complet**</span><span class="sxs-lookup"><span data-stu-id="6b801-133">**full heap**</span></span> |
| <span data-ttu-id="6b801-134">Nombre maximal d’échantillonneurs dans toutes les tables de descripteurs par étape de nuanceur</span><span class="sxs-lookup"><span data-stu-id="6b801-134">Maximum number of Samplers in all descriptor tables per shader stage</span></span>                                                                             | <span data-ttu-id="6b801-135">16</span><span class="sxs-lookup"><span data-stu-id="6b801-135">16</span></span>                                                                       | <span data-ttu-id="6b801-136">**2048**</span><span class="sxs-lookup"><span data-stu-id="6b801-136">**2048**</span></span> | <span data-ttu-id="6b801-137">2 048</span><span class="sxs-lookup"><span data-stu-id="6b801-137">2048</span></span>     |



 

<span data-ttu-id="6b801-138">Les entrées en **gras** mettent en évidence des améliorations significatives par rapport au niveau précédent.</span><span class="sxs-lookup"><span data-stu-id="6b801-138">**Bold** entries highlight significant improvements over the previous tier.</span></span>

<span data-ttu-id="6b801-139">Il existe une restriction supplémentaire pour le matériel de niveau 1 qui s’applique à tous les segments de mémoire, et au matériel de niveau 2 qui s’applique aux tas CBV et UAV, que toutes les entrées de tas de descripteurs couvertes par les tables de descripteurs dans la signature racine *doivent* être remplies par les descripteurs au moment de l’exécution du nuanceur, même si le nuanceur</span><span class="sxs-lookup"><span data-stu-id="6b801-139">There is an additional restriction for Tier 1 hardware that applies to all heaps, and to Tier 2 hardware that applies to CBV and UAV heaps, that all descriptor heap entries covered by descriptor tables in the root signature *must* be populated with descriptors by the time the shader executes, even if the shader (perhaps due to branching) does not need the descriptor.</span></span> <span data-ttu-id="6b801-140">Il n’existe aucune restriction de ce type pour le matériel de niveau 3.</span><span class="sxs-lookup"><span data-stu-id="6b801-140">There is no such restriction for Tier 3 hardware.</span></span> <span data-ttu-id="6b801-141">L’une des mesures d’atténuation pour cette restriction est l’utilisation diligente des [descripteurs null](descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="6b801-141">One mitigation for this restriction is the diligent use of [Null descriptors](descriptors.md).</span></span>

## <a name="invariable-limits"></a><span data-ttu-id="6b801-142">Limites invariables</span><span class="sxs-lookup"><span data-stu-id="6b801-142">Invariable limits</span></span>

<span data-ttu-id="6b801-143">Le nombre maximal d’échantillonneurs dans un tas de descripteur visible par le nuanceur est 2048.</span><span class="sxs-lookup"><span data-stu-id="6b801-143">The maximum number of samplers in a shader visible descriptor heap is 2048.</span></span>

<span data-ttu-id="6b801-144">Le nombre maximal d’échantillons statiques uniques dans les signatures racines dynamiques est 2032 (ce qui laisse 16 pour les pilotes qui ont besoin de leurs propres échantillonneurs).</span><span class="sxs-lookup"><span data-stu-id="6b801-144">The maximum number of unique static samplers across live root signatures is 2032 (which leaves 16 for drivers that need their own samplers).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b801-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6b801-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b801-146">Tas de descripteurs</span><span class="sxs-lookup"><span data-stu-id="6b801-146">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> <dt>

[<span data-ttu-id="6b801-147">Niveaux de fonctionnalité matérielle</span><span class="sxs-lookup"><span data-stu-id="6b801-147">Hardware Feature Levels</span></span>](hardware-feature-levels.md)
</dt> </dl>

 

 





