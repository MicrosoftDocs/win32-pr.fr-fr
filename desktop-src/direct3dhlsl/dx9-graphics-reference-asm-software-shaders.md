---
title: Nuanceurs de logiciels
description: Les nuanceurs de logiciels sont mis en œuvre pour permettre le développement de nuanceurs sans prise en charge du matériel sous-jacent. Ils prennent en charge l’ensemble complet des fonctionnalités. Dans la mesure où elles sont implémentées dans le logiciel, elles ne produisent pas les meilleures performances.
ms.assetid: 0153732d-a487-473b-ad77-32ab457979f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df101edd0362321847fb9c0baf7feb3cc865e2da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029882"
---
# <a name="software-shaders"></a><span data-ttu-id="7d80f-105">Nuanceurs de logiciels</span><span class="sxs-lookup"><span data-stu-id="7d80f-105">Software Shaders</span></span>

<span data-ttu-id="7d80f-106">Les nuanceurs de logiciels sont mis en œuvre pour permettre le développement de nuanceurs sans prise en charge du matériel sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="7d80f-106">Software shaders are implemented to allow development of shaders without underlying hardware support.</span></span> <span data-ttu-id="7d80f-107">Ils prennent en charge l’ensemble complet des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="7d80f-107">They support the full feature set.</span></span> <span data-ttu-id="7d80f-108">Dans la mesure où elles sont implémentées dans le logiciel, elles ne produisent pas les meilleures performances.</span><span class="sxs-lookup"><span data-stu-id="7d80f-108">Because they are implemented in software, they will not produce the best performance.</span></span>



| <span data-ttu-id="7d80f-109">Version</span><span class="sxs-lookup"><span data-stu-id="7d80f-109">Version</span></span>   | <span data-ttu-id="7d80f-110">Jeu de fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="7d80f-110">Feature Set</span></span>                  | <span data-ttu-id="7d80f-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7d80f-111">Requirements</span></span>                                                         |
|-----------|------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="7d80f-112">vs \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7d80f-112">vs\_2\_sw</span></span> | <span data-ttu-id="7d80f-113">Toutes les fonctionnalités de vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7d80f-113">All the features of vs\_2\_x</span></span> | <span data-ttu-id="7d80f-114">Pris en charge uniquement par le traitement du vertex logiciel et par un appareil de référence.</span><span class="sxs-lookup"><span data-stu-id="7d80f-114">Only supported by software vertex processing and a reference device.</span></span> |
| <span data-ttu-id="7d80f-115">vs \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7d80f-115">vs\_3\_sw</span></span> | <span data-ttu-id="7d80f-116">Toutes les fonctionnalités de vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7d80f-116">All the features of vs\_3\_0</span></span> | <span data-ttu-id="7d80f-117">Pris en charge uniquement par le traitement du vertex logiciel et par un appareil de référence.</span><span class="sxs-lookup"><span data-stu-id="7d80f-117">Only supported by software vertex processing and a reference device.</span></span> |
| <span data-ttu-id="7d80f-118">\_logiciel PS 2 \_</span><span class="sxs-lookup"><span data-stu-id="7d80f-118">ps\_2\_sw</span></span> | <span data-ttu-id="7d80f-119">Toutes les fonctionnalités de PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7d80f-119">All the features of ps\_2\_x</span></span> | <span data-ttu-id="7d80f-120">Pris en charge uniquement par un appareil de référence.</span><span class="sxs-lookup"><span data-stu-id="7d80f-120">Only supported by a reference device.</span></span>                                |
| <span data-ttu-id="7d80f-121">\_logiciel PS 3 \_</span><span class="sxs-lookup"><span data-stu-id="7d80f-121">ps\_3\_sw</span></span> | <span data-ttu-id="7d80f-122">Toutes les fonctionnalités de PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7d80f-122">All the features of ps\_3\_0</span></span> | <span data-ttu-id="7d80f-123">Pris en charge uniquement par un appareil de référence.</span><span class="sxs-lookup"><span data-stu-id="7d80f-123">Only supported by a reference device.</span></span>                                |



 

<span data-ttu-id="7d80f-124">Certaines validations sont assouplies pour les nuanceurs de logiciels.</span><span class="sxs-lookup"><span data-stu-id="7d80f-124">Some validations are relaxed for software shaders.</span></span> <span data-ttu-id="7d80f-125">Cela est utile à des fins de débogage et de prototypage.</span><span class="sxs-lookup"><span data-stu-id="7d80f-125">This is useful for debugging and prototyping purposes.</span></span> <span data-ttu-id="7d80f-126">Les validations suivantes sont assouplies : (toutes les autres validations restent les mêmes)</span><span class="sxs-lookup"><span data-stu-id="7d80f-126">The following validations are relaxed: (all other validations remain the same)</span></span>



| <span data-ttu-id="7d80f-127">Type de validation</span><span class="sxs-lookup"><span data-stu-id="7d80f-127">Validation type</span></span>                                 | <span data-ttu-id="7d80f-128">Relax</span><span class="sxs-lookup"><span data-stu-id="7d80f-128">Relaxation</span></span>                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d80f-129">Nombre d’instructions :</span><span class="sxs-lookup"><span data-stu-id="7d80f-129">Instruction Counts:</span></span>                             | <span data-ttu-id="7d80f-130">Cela est assoupli pour vs \_ 2 \_ SW, vs \_ 3 \_ SW et PS \_ 2 \_ SW, PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="7d80f-130">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="7d80f-131">Des instructions illimitées sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="7d80f-131">Unlimited instructions are allowed.</span></span>                                                                                                              |
| <span data-ttu-id="7d80f-132">Nombres de constantes float :</span><span class="sxs-lookup"><span data-stu-id="7d80f-132">Float Constant Counts:</span></span>                          | <span data-ttu-id="7d80f-133">Cela est assoupli pour vs \_ 2 \_ SW, vs \_ 3 \_ SW et PS \_ 2 \_ SW, PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="7d80f-133">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="7d80f-134">Jusqu’à 8192 constantes sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="7d80f-134">Up to 8192 constants are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="7d80f-135">Nombres de constantes entières :</span><span class="sxs-lookup"><span data-stu-id="7d80f-135">Integer Constant Counts:</span></span>                        | <span data-ttu-id="7d80f-136">Cela est assoupli pour vs \_ 2 \_ SW, vs \_ 3 \_ SW et PS \_ 2 \_ SW, PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="7d80f-136">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="7d80f-137">Jusqu’à 2048 constantes sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="7d80f-137">Up to 2048 constants are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="7d80f-138">Nombres de constantes booléennes :</span><span class="sxs-lookup"><span data-stu-id="7d80f-138">Boolean Constant Counts:</span></span>                        | <span data-ttu-id="7d80f-139">Cela est assoupli pour vs \_ 2 \_ SW, vs \_ 3 \_ SW et PS \_ 2 \_ SW, PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="7d80f-139">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="7d80f-140">Jusqu’à 2048 constantes sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="7d80f-140">Up to 2048 constants are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="7d80f-141">Profondeur de lecture dépendante :</span><span class="sxs-lookup"><span data-stu-id="7d80f-141">Dependent-read depth:</span></span>                           | <span data-ttu-id="7d80f-142">Cela est assoupli pour le \_ logiciel PS 2 \_ .</span><span class="sxs-lookup"><span data-stu-id="7d80f-142">This is relaxed for ps\_2\_sw.</span></span> <span data-ttu-id="7d80f-143">Comme dans vs \_ 3 \_ 0 et PS \_ 3 \_ 0, les lectures dépendantes illimitées sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="7d80f-143">Like in vs\_3\_0 and ps\_3\_0, unlimited dependent reads are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="7d80f-144">Nombre d’instructions et d’étiquettes de contrôle de flow :</span><span class="sxs-lookup"><span data-stu-id="7d80f-144">Number of flow control instructions and labels:</span></span> | <span data-ttu-id="7d80f-145">Cela est assoupli pour vs \_ 2 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="7d80f-145">This is relaxed for vs\_2\_sw.</span></span> <span data-ttu-id="7d80f-146">Les instructions de contrôle de Flow illimitées et jusqu’à 2048 étiquettes sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="7d80f-146">Unlimited flow control instructions and upto 2048 labels are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="7d80f-147">Nombre de boucles/Démarrer/Exécuter :</span><span class="sxs-lookup"><span data-stu-id="7d80f-147">Loop count/start/step:</span></span>                          | <span data-ttu-id="7d80f-148">Celles-ci sont assouplies pour vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW et PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="7d80f-148">These are relaxed for vs\_2\_sw, vs\_3\_sw, ps\_2\_sw and ps\_3\_sw.</span></span> <span data-ttu-id="7d80f-149">La taille de l’étape de début et d’itération des itérations pour les instructions REP et Loop sont des intergers signés 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7d80f-149">Iteration start and interation step size for rep and loop instructions are 32-bit signed intergers.</span></span> <span data-ttu-id="7d80f-150">Le nombre d’interconnexions peut atteindre un maximum de \_ int/64.</span><span class="sxs-lookup"><span data-stu-id="7d80f-150">Interation count can be up to MAX\_INT/64.</span></span> |
| <span data-ttu-id="7d80f-151">Limites du port de lecture :</span><span class="sxs-lookup"><span data-stu-id="7d80f-151">Read-port limits:</span></span>                               | <span data-ttu-id="7d80f-152">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW et PS \_ 3 \_ SW n’ont pas de limite de lecture des ports.</span><span class="sxs-lookup"><span data-stu-id="7d80f-152">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw and ps\_3\_sw have no read-port limit.</span></span>                                                                                                                                              |
| <span data-ttu-id="7d80f-153">Nombre d’interpolateurs :</span><span class="sxs-lookup"><span data-stu-id="7d80f-153">Number of interpolators:</span></span>                        | <span data-ttu-id="7d80f-154">Il y a 16 [registres, vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# ) dans vs \_ 3 \_ SW et 10 [PS \_ 3 \_ 0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \# ) pour PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="7d80f-154">There are 16 [Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o\#) in vs\_3\_sw and 10 [ps\_3\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v\#) for ps\_3\_sw.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="7d80f-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7d80f-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d80f-156">Référence du nuanceur asm</span><span class="sxs-lookup"><span data-stu-id="7d80f-156">Asm Shader Reference</span></span>](dx9-graphics-reference-asm.md)
</dt> </dl>

 

 




