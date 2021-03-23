---
title: Limites de signature racine
description: La signature racine est un grand patrimoine et il existe des limites et des coûts stricts à prendre en compte.
ms.assetid: 01121D3A-1926-4246-9C20-5E11F2E0B092
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25986da72cfcad7b714031e063341e1832d6ae68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104136"
---
# <a name="root-signature-limits"></a><span data-ttu-id="e4410-103">Limites de signature racine</span><span class="sxs-lookup"><span data-stu-id="e4410-103">Root Signature Limits</span></span>

<span data-ttu-id="e4410-104">La signature racine est un grand patrimoine et il existe des limites et des coûts stricts à prendre en compte.</span><span class="sxs-lookup"><span data-stu-id="e4410-104">The root signature is prime real estate, and there are strict limits and costs to consider.</span></span>

-   [<span data-ttu-id="e4410-105">Limites et coûts de la mémoire</span><span class="sxs-lookup"><span data-stu-id="e4410-105">Memory limits and costs</span></span>](#memory-limits-and-costs)
-   [<span data-ttu-id="e4410-106">Coûts de performances</span><span class="sxs-lookup"><span data-stu-id="e4410-106">Performance costs</span></span>](#performance-costs)
-   [<span data-ttu-id="e4410-107">Échantillonneurs statiques</span><span class="sxs-lookup"><span data-stu-id="e4410-107">Static samplers</span></span>](#static-samplers)
-   [<span data-ttu-id="e4410-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e4410-108">Related topics</span></span>](#related-topics)

## <a name="memory-limits-and-costs"></a><span data-ttu-id="e4410-109">Limites et coûts de la mémoire</span><span class="sxs-lookup"><span data-stu-id="e4410-109">Memory limits and costs</span></span>

<span data-ttu-id="e4410-110">La taille maximale d’une signature racine est de 64 DWORDs.</span><span class="sxs-lookup"><span data-stu-id="e4410-110">The maximum size of a root signature is 64 DWORDs.</span></span>

<span data-ttu-id="e4410-111">Cette taille maximale est choisie pour empêcher un abus de la signature racine comme un moyen de stocker des données en bloc.</span><span class="sxs-lookup"><span data-stu-id="e4410-111">This maximum size is chosen to prevent abuse of the root signature as a way of storing bulk data.</span></span> <span data-ttu-id="e4410-112">Chaque entrée dans la signature racine a un coût pour cette limite DWORD de 64 :</span><span class="sxs-lookup"><span data-stu-id="e4410-112">Each entry in the root signature has a cost towards this 64 DWORD limit:</span></span>

-   <span data-ttu-id="e4410-113">Tables de descripteur coût 1 DWORD chacune.</span><span class="sxs-lookup"><span data-stu-id="e4410-113">Descriptor tables cost 1 DWORD each.</span></span>
-   <span data-ttu-id="e4410-114">Les constantes racine cost 1 DWORD sont chacune, car il s’agit de valeurs 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e4410-114">Root constants cost 1 DWORD each, since they are 32-bit values.</span></span>
-   <span data-ttu-id="e4410-115">Les descripteurs racine (adresses virtuelles du GPU 64 bits) coûtent 2 DWORD.</span><span class="sxs-lookup"><span data-stu-id="e4410-115">Root descriptors (64-bit GPU virtual addresses) cost 2 DWORDs each.</span></span>

<span data-ttu-id="e4410-116">Les échantillonneurs statiques n’ont aucun coût dans la taille de la signature racine.</span><span class="sxs-lookup"><span data-stu-id="e4410-116">Static samplers do not have any cost in the size of the root signature.</span></span>

## <a name="performance-costs"></a><span data-ttu-id="e4410-117">Coûts de performances</span><span class="sxs-lookup"><span data-stu-id="e4410-117">Performance costs</span></span>

<span data-ttu-id="e4410-118">Le coût des performances (en termes de niveaux d’indirection) est égal à zéro pour une constante racine, 1 à un descripteur racine et 2 pour une table de descripteurs.</span><span class="sxs-lookup"><span data-stu-id="e4410-118">The performance cost (in terms of levels of indirection) are zero for a root constant, 1 for a root descriptor, and 2 for a descriptor table.</span></span> <span data-ttu-id="e4410-119">Si une signature racine est volumineuse et déborde de la mémoire la plus rapide dans une mémoire légèrement plus lente (qui peut se produire sur du matériel), ajoutez 1 au coût des performances pour les éléments de dépassement à la fin de la signature racine.</span><span class="sxs-lookup"><span data-stu-id="e4410-119">If a root signature is large and overflows out of the fastest memory into slightly slower memory (which can happen on some hardware), then add 1 to the performance cost for the overflowing items at the end of the root signature.</span></span>

<span data-ttu-id="e4410-120">Un dépassement de capacité peut se produire sur du matériel qui peut avoir, par exemple, une taille fixe de 16 DWORDs pour l’espace d’argument racine.</span><span class="sxs-lookup"><span data-stu-id="e4410-120">An overflow can occur on hardware that might have, for example, a fixed size of 16 DWORDs for root argument space.</span></span> <span data-ttu-id="e4410-121">Cette limite peut être plus réduite d’une unité si l’assembleur d’entrée est utilisé.</span><span class="sxs-lookup"><span data-stu-id="e4410-121">This limit might be further reduced by one if the Input Assembler is used.</span></span> <span data-ttu-id="e4410-122">Dans ce cas, la mémoire est légèrement plus lente si la signature racine est trop grande pour la mémoire native de 15 ou 16 DWORD.</span><span class="sxs-lookup"><span data-stu-id="e4410-122">In this case there is overflow into slightly slower memory if the root signature is too large for the 15 or 16 DWORD native memory.</span></span> <span data-ttu-id="e4410-123">Dans un autre matériel, il n’existe pas de mémoire d’arguments racine Native fixe (la situation de dépassement de capacité ne se produit donc jamais).</span><span class="sxs-lookup"><span data-stu-id="e4410-123">In other hardware there is no fixed native root argument memory (so the overflow situation never occurs).</span></span>

<span data-ttu-id="e4410-124">Pour tout le matériel, si un argument racine change, le pilote doit conserver une version de tous les arguments racine (contrairement à d’autres stockages, tels que les tas de descripteurs et les ressources de mémoire tampon, qui ne sont pas gérées par le pilote).</span><span class="sxs-lookup"><span data-stu-id="e4410-124">For all hardware, if any root argument changes, the driver must maintain a version of all the root arguments (unlike other storage such as descriptor heaps and buffer resources, which are not versioned by the driver).</span></span> <span data-ttu-id="e4410-125">Dans le matériel qu’une situation de dépassement de capacité se produit, seule la version native ou de dépassement de capacité doit être gérée, selon l’endroit où la modification s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e4410-125">In hardware that an overflow situation occurs, only the native or overflow area needs to be versioned, depending on where the change occurred.</span></span> <span data-ttu-id="e4410-126">La quantité de contrôle de version doit évidemment être conservée au minimum nécessaire.</span><span class="sxs-lookup"><span data-stu-id="e4410-126">The amount of versioning should obviously be kept to the necessary minimum.</span></span>

<span data-ttu-id="e4410-127">En règle générale, tenez compte des recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e4410-127">Generally, consider the following guidelines:</span></span>

-   <span data-ttu-id="e4410-128">Utilisez une petite signature racine en fonction des besoins, bien que l’équilibre avec la flexibilité d’une signature racine plus grande.</span><span class="sxs-lookup"><span data-stu-id="e4410-128">Use a small a root signature as necessary, though balance this with the flexibility of a larger root signature.</span></span>
-   <span data-ttu-id="e4410-129">Réorganisez les paramètres dans une grande signature racine afin que les paramètres les plus susceptibles d’être modifiés souvent, ou si une faible latence d’accès pour un paramètre donné soit importante, se produisent en premier.</span><span class="sxs-lookup"><span data-stu-id="e4410-129">Arrange parameters in a large root signature so that the parameters most likely to change often, or if low access latency for a given parameter is important, occur first.</span></span>
-   <span data-ttu-id="e4410-130">Si vous le faites, utilisez des constantes racine ou des vues de mémoire tampon constantes racine pour placer des vues de mémoire tampon constantes dans un tas de descripteur.</span><span class="sxs-lookup"><span data-stu-id="e4410-130">If convenient, use root constants or root constant buffer views over putting constant buffer views in a descriptor heap.</span></span>

## <a name="static-samplers"></a><span data-ttu-id="e4410-131">Échantillonneurs statiques</span><span class="sxs-lookup"><span data-stu-id="e4410-131">Static samplers</span></span>

<span data-ttu-id="e4410-132">Les échantillonneurs statiques (exemples dans lesquels l’État est entièrement défini et immuable) font partie des signatures racines, mais ne sont pas pris en compte dans la limite DWORD de 64.</span><span class="sxs-lookup"><span data-stu-id="e4410-132">Static samplers (samplers where the state is fully defined and immutable) are part of root signatures, but do not count towards the 64 DWORD limit.</span></span> <span data-ttu-id="e4410-133">Si un échantillonneur peut être défini comme static, il n’est pas nécessaire que l’échantillonneur fasse partie d’un tas de descripteur.</span><span class="sxs-lookup"><span data-stu-id="e4410-133">If a sampler can be defined as static, there is no need for the sampler to be part of a descriptor heap.</span></span>

<span data-ttu-id="e4410-134">Il n’y a aucun coût de performance pour l’utilisation d’échantillonneurs statiques, et une signature racine peut contenir une combinaison d’échantillonneurs statiques (stockés dans la signature racine ou dans un espace réservé sur un matériel) et d’échantillonneurs dynamiques (stockés dans un tas de descripteur d’échantillonneur).</span><span class="sxs-lookup"><span data-stu-id="e4410-134">There is no performance cost to using static samplers, and a root signature can contain a mix of static samplers (stored in the root signature, or in reserved space on some hardware) and dynamic samplers (stored in a sampler descriptor heap).</span></span> <span data-ttu-id="e4410-135">Les échantillonneurs d’un tas de descripteur peuvent être attribués et indexés dynamiquement, ce qui ne peut pas être le signe d’échantillonneurs statiques.</span><span class="sxs-lookup"><span data-stu-id="e4410-135">Samplers in a descriptor heap can be dynamically assigned and indexed, which static samplers cannot.</span></span>

<span data-ttu-id="e4410-136">Les échantillonneurs statiques peuvent être écrits dans le cadre de la signature racine dans les nuanceurs HLSL (reportez-vous à [spécification des signatures racines en HLSL](specifying-root-signatures-in-hlsl.md)).</span><span class="sxs-lookup"><span data-stu-id="e4410-136">Static samplers can be written as part of the root signature in HLSL shaders (refer to [Specifying Root Signatures in HLSL](specifying-root-signatures-in-hlsl.md)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4410-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e4410-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4410-138">Signatures racines</span><span class="sxs-lookup"><span data-stu-id="e4410-138">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 




