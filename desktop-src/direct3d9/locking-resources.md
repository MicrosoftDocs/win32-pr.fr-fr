---
description: Le verrouillage d’une ressource signifie accorder l’accès de l’UC à son stockage.
ms.assetid: b17d8262-e514-4b9c-9237-653a4258a14e
title: Verrouillage des ressources (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d66a7a420a33cb908d0974f9d942597019aded
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514721"
---
# <a name="locking-resources-direct3d-9"></a><span data-ttu-id="4ff03-103">Verrouillage des ressources (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4ff03-103">Locking Resources (Direct3D 9)</span></span>

<span data-ttu-id="4ff03-104">Le verrouillage d’une ressource signifie accorder l’accès de l’UC à son stockage.</span><span class="sxs-lookup"><span data-stu-id="4ff03-104">Locking a resource means granting CPU access to its storage.</span></span> <span data-ttu-id="4ff03-105">Les options de verrouillage suivantes sont définies pour les ressources :</span><span class="sxs-lookup"><span data-stu-id="4ff03-105">The following locking options are defined for resources:</span></span>

-   <span data-ttu-id="4ff03-106">D3DLOCK \_ Ignorer</span><span class="sxs-lookup"><span data-stu-id="4ff03-106">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="4ff03-107">D3DLOCK en \_ lecture seule</span><span class="sxs-lookup"><span data-stu-id="4ff03-107">D3DLOCK\_READONLY</span></span>
-   <span data-ttu-id="4ff03-108">D3DLOCK \_ NOOVERWRITE</span><span class="sxs-lookup"><span data-stu-id="4ff03-108">D3DLOCK\_NOOVERWRITE</span></span>
-   <span data-ttu-id="4ff03-109">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="4ff03-109">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="4ff03-110">D3DLOCK \_ aucune \_ \_ mise à jour incorrecte</span><span class="sxs-lookup"><span data-stu-id="4ff03-110">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>

<span data-ttu-id="4ff03-111">Pour plus d’informations sur les indicateurs de verrouillage et sur la façon dont ils sont liés à des ressources spécifiques, consultez les pages de référence sur les méthodes de verrouillage des ressources individuelles.</span><span class="sxs-lookup"><span data-stu-id="4ff03-111">For details on locking flags and how they relate to specific resources, see the reference pages on the individual resource locking methods.</span></span> <span data-ttu-id="4ff03-112">Les développeurs d’applications doivent noter que les \_ indicateurs D3DLOCK Discard, D3DLOCK \_ ReadOnly et D3DLOCK \_ NOOVERWRITE ne sont que des indicateurs.</span><span class="sxs-lookup"><span data-stu-id="4ff03-112">Application developers should note that the D3DLOCK\_DISCARD, D3DLOCK\_READONLY, and D3DLOCK\_NOOVERWRITE flags are only hints.</span></span> <span data-ttu-id="4ff03-113">Le temps d’exécution ne vérifie pas si les applications suivent les fonctionnalités spécifiées par ces indicateurs.</span><span class="sxs-lookup"><span data-stu-id="4ff03-113">The run time does not check that applications are following the functionality specified by these flags.</span></span> <span data-ttu-id="4ff03-114">Une application qui spécifie D3DLOCK \_ ReadOnly, mais qui écrit dans la ressource doit attendre des résultats indéfinis.</span><span class="sxs-lookup"><span data-stu-id="4ff03-114">An application that specifies D3DLOCK\_READONLY but then writes to the resource should expect undefined results.</span></span> <span data-ttu-id="4ff03-115">En général, l’utilisation des indicateurs de verrouillage, y compris les indicateurs d’utilisation de verrouillage, n’est pas garantie dans les versions ultérieures et peut entraîner une baisse significative des performances.</span><span class="sxs-lookup"><span data-stu-id="4ff03-115">In general, working against locking flags, including the locking usage flags, is not guaranteed to work in later releases and may incur a significant performance penalty.</span></span>

<span data-ttu-id="4ff03-116">Une opération de verrouillage est suivie d’une opération de déverrouillage.</span><span class="sxs-lookup"><span data-stu-id="4ff03-116">A lock operation is followed by an unlock operation.</span></span> <span data-ttu-id="4ff03-117">Par exemple, après avoir verrouillé une texture, l’application abandonne par la suite un accès direct aux textures verrouillées en les déverrouillant.</span><span class="sxs-lookup"><span data-stu-id="4ff03-117">For example, after locking a texture, the application subsequently relinquishes direct access to locked textures by unlocking them.</span></span> <span data-ttu-id="4ff03-118">Outre l’octroi de l’accès au processeur, toute autre opération impliquant cette ressource est sérialisée pour la durée d’un verrou.</span><span class="sxs-lookup"><span data-stu-id="4ff03-118">In addition to granting processor access, any other operations involving that resource are serialized for the duration of a lock.</span></span> <span data-ttu-id="4ff03-119">Un seul verrou pour une ressource est autorisé, même pour les régions qui ne se chevauchent pas, et aucune opération d’accélérateur sur une surface ne peut être poursuivie pendant qu’une opération de verrouillage est en suspens sur cette surface.</span><span class="sxs-lookup"><span data-stu-id="4ff03-119">Only a single lock for a resource is allowed, even for non-overlapping regions, and no accelerator operations on a surface can be ongoing while a lock operation is outstanding on that surface.</span></span>

<span data-ttu-id="4ff03-120">Chaque interface de ressource a des méthodes pour verrouiller les mémoires tampons contenues.</span><span class="sxs-lookup"><span data-stu-id="4ff03-120">Each resource interface has methods for locking the contained buffers.</span></span> <span data-ttu-id="4ff03-121">Chaque ressource de texture peut également verrouiller une sous-partie de cette ressource.</span><span class="sxs-lookup"><span data-stu-id="4ff03-121">Each texture resource can also lock a sub-portion of that resource.</span></span> <span data-ttu-id="4ff03-122">les ressources 2D (surfaces) permettent le verrouillage des sous-rectangles, tandis que les ressources de volume permettent de verrouiller des sous-volumes ou des zones.</span><span class="sxs-lookup"><span data-stu-id="4ff03-122">2D resources (surfaces) allow the locking of sub-rectangles, and volume resources allow the locking of sub-volumes or boxes.</span></span> <span data-ttu-id="4ff03-123">Chaque méthode de verrouillage retourne une structure qui contient un pointeur vers le stockage qui stocke la ressource et des valeurs représentant les distances entre les lignes ou les plans de données, selon le type de ressource.</span><span class="sxs-lookup"><span data-stu-id="4ff03-123">Each lock method returns a structure that contains a pointer to the storage backing the resource and values representing the distances between rows or planes of data, depending on the resource type.</span></span> <span data-ttu-id="4ff03-124">Pour plus d’informations, consultez les listes de méthodes pour les interfaces de ressource.</span><span class="sxs-lookup"><span data-stu-id="4ff03-124">For details, see the method lists for the resource interfaces.</span></span> <span data-ttu-id="4ff03-125">Le pointeur retourné pointe toujours vers l’octet supérieur gauche dans les sous-régions verrouillées.</span><span class="sxs-lookup"><span data-stu-id="4ff03-125">The returned pointer always points to the top-left byte in the locked sub-regions.</span></span>

<span data-ttu-id="4ff03-126">Lorsque vous utilisez des mémoires tampons d’index et de vertex, vous pouvez effectuer plusieurs appels de verrouillage. Toutefois, vous devez vous assurer que le nombre d’appels de verrous correspond au nombre d’appels de déverrouillage.</span><span class="sxs-lookup"><span data-stu-id="4ff03-126">When working with index and vertex buffers, you can make multiple lock calls; however, you must ensure that the number of lock calls matches the number of unlock calls.</span></span>

<span data-ttu-id="4ff03-127">Le DXTn stocke les pixels dans des blocs 4x4 encodés et peut uniquement être verrouillé sur des limites de 4 x 4.</span><span class="sxs-lookup"><span data-stu-id="4ff03-127">The DXTn store pixels in encoded 4x4 blocks, and can only be locked on 4x4 boundaries.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ff03-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4ff03-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ff03-129">Ressources Direct3D</span><span class="sxs-lookup"><span data-stu-id="4ff03-129">Direct3D Resources</span></span>](direct3d-resources.md)
</dt> </dl>

 

 



