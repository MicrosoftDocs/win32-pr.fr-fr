---
title: Implémentation du canal Client-Side
description: Implémentation du canal côté client dans l’appel de procédure distante (RPC).
ms.assetid: d790f859-47a9-4b6c-a218-8cbe05db21b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5666656f1f7296c252395255c17902a91cb32a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840569"
---
# <a name="client-side-pipe-implementation"></a><span data-ttu-id="a19d2-103">Implémentation du canal Client-Side</span><span class="sxs-lookup"><span data-stu-id="a19d2-103">Client-Side Pipe Implementation</span></span>

<span data-ttu-id="a19d2-104">L’application cliente doit implémenter les procédures suivantes, que le stub client appellera pendant le transfert de données :</span><span class="sxs-lookup"><span data-stu-id="a19d2-104">The client application must implement the following procedures, which the client stub will call during data transfer:</span></span>

-   <span data-ttu-id="a19d2-105">Une procédure Pull (pour un canal d’entrée)</span><span class="sxs-lookup"><span data-stu-id="a19d2-105">A pull procedure (for an input pipe)</span></span>
-   <span data-ttu-id="a19d2-106">Procédure push (pour un canal de sortie)</span><span class="sxs-lookup"><span data-stu-id="a19d2-106">A push procedure (for an output pipe)</span></span>
-   <span data-ttu-id="a19d2-107">Une procédure Alloc pour allouer une mémoire tampon pour les données de transfert</span><span class="sxs-lookup"><span data-stu-id="a19d2-107">An alloc procedure to allocate a buffer for the transfer data</span></span>

<span data-ttu-id="a19d2-108">Toutes ces procédures doivent utiliser les arguments spécifiés par le fichier d’en-tête généré par MIDL.</span><span class="sxs-lookup"><span data-stu-id="a19d2-108">All of these procedures must use the arguments specified by the MIDL-generated header file.</span></span> <span data-ttu-id="a19d2-109">En outre, l’application cliente doit avoir une variable d’État pour identifier où localiser ou placer les données.</span><span class="sxs-lookup"><span data-stu-id="a19d2-109">In addition, the client application must have a state variable to identify where to locate or place data.</span></span>

<span data-ttu-id="a19d2-110">La procédure Alloc peut également être aussi simple ou complexe que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a19d2-110">The alloc procedure can also be as simple or as complex as needed.</span></span> <span data-ttu-id="a19d2-111">Par exemple, il peut retourner un pointeur vers la même mémoire tampon chaque fois que le stub appelle la fonction, ou il peut allouer une quantité de mémoire différente à chaque fois.</span><span class="sxs-lookup"><span data-stu-id="a19d2-111">For example, it can return a pointer to the same buffer every time the stub calls the function, or it can allocate a different amount of memory each time.</span></span> <span data-ttu-id="a19d2-112">Si vos données sont déjà au format approprié (un tableau d’éléments de canal, par exemple), vous pouvez coordonner la procédure Alloc avec la procédure pull pour allouer une mémoire tampon qui contient déjà les données.</span><span class="sxs-lookup"><span data-stu-id="a19d2-112">If your data is already in the proper form (an array of pipe elements, for example) you can coordinate the alloc procedure with the pull procedure to allocate a buffer that already contains the data.</span></span> <span data-ttu-id="a19d2-113">Dans ce cas, votre procédure pull peut être une routine vide.</span><span class="sxs-lookup"><span data-stu-id="a19d2-113">In that case, your pull procedure could be an empty routine.</span></span>

<span data-ttu-id="a19d2-114">L’allocation de mémoire tampon doit être en octets.</span><span class="sxs-lookup"><span data-stu-id="a19d2-114">The buffer allocation must be in bytes.</span></span> <span data-ttu-id="a19d2-115">Les procédures push et pull, en revanche, manipulent les éléments dont la taille en octets dépend de la façon dont ils ont été définis.</span><span class="sxs-lookup"><span data-stu-id="a19d2-115">The push and pull procedures, on the other hand, manipulate elements, whose size in bytes depends on how they were defined.</span></span>

<span data-ttu-id="a19d2-116">Cette section décrit l’implémentation cliente des canaux d’entrée et de sortie dans les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="a19d2-116">This section discusses the client implementation of input and output pipes in the following sections:</span></span>

-   [<span data-ttu-id="a19d2-117">Implémentation de canaux d’entrée sur le client</span><span class="sxs-lookup"><span data-stu-id="a19d2-117">Implementing Input Pipes on the Client</span></span>](implementing-input-pipes-on-the-client.md)
-   [<span data-ttu-id="a19d2-118">Implémentation de canaux de sortie sur le client</span><span class="sxs-lookup"><span data-stu-id="a19d2-118">Implementing Output Pipes on the Client</span></span>](implementing-output-pipes-on-the-client.md)

 

 




