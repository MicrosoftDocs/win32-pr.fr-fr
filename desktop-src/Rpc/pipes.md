---
title: Canaux (RPC)
description: Le constructeur de type pipe est un mécanisme très efficace pour la transmission de grandes quantités de données, ou toute quantité de données qui ne sont pas toutes disponibles en mémoire à un moment donné.
ms.assetid: 913d5e2a-00ad-4060-9274-a6db23fb2817
keywords:
- Appel de procédure distante RPC, décrit, canaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6c670b51dfe634fb5b3318e0a0b8a796cfbf988
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464079"
---
# <a name="pipes-rpc"></a><span data-ttu-id="90d19-104">Canaux (RPC)</span><span class="sxs-lookup"><span data-stu-id="90d19-104">Pipes (RPC)</span></span>

<span data-ttu-id="90d19-105">Le constructeur de type pipe est un mécanisme très efficace pour la transmission de grandes quantités de données, ou toute quantité de données qui ne sont pas toutes disponibles en mémoire à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="90d19-105">The pipe type constructor is a highly efficient mechanism for passing large amounts of data, or any quantity of data that is not all available in memory at one time.</span></span> <span data-ttu-id="90d19-106">À l’aide d’un canal, le temps d’exécution RPC gère le transfert de données réel, éliminant la surcharge associée aux appels de procédure distante répétés.</span><span class="sxs-lookup"><span data-stu-id="90d19-106">By using a pipe, RPC run time handles the actual data transfer, eliminating the overhead associated with repeated remote procedure calls.</span></span>

<span data-ttu-id="90d19-107">Après qu’un client a appelé une procédure distante qui a un paramètre de canal, le client et le serveur entrent des boucles pour transférer des données.</span><span class="sxs-lookup"><span data-stu-id="90d19-107">After a client invokes a remote procedure that has a pipe parameter, the client and server enter loops to transfer data.</span></span> <span data-ttu-id="90d19-108">Les données peuvent être produites sur le client ou sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="90d19-108">The data can be produced on the client or the server.</span></span> <span data-ttu-id="90d19-109">Dans les deux cas, la quantité de données (en octets) n’a pas besoin d’être connue à l’avance.</span><span class="sxs-lookup"><span data-stu-id="90d19-109">Either way, the amount of data (in bytes) does not have to be known in advance.</span></span> <span data-ttu-id="90d19-110">Les données peuvent être produites ou consommées de manière incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="90d19-110">The data can be produced or consumed incrementally.</span></span> <span data-ttu-id="90d19-111">Pendant la boucle de transfert de données, le serveur appelle des routines de stub qui chargent ou déchargent une mémoire tampon de données.</span><span class="sxs-lookup"><span data-stu-id="90d19-111">While in the data-transfer loop, the server calls stub routines that load or unload a buffer of data.</span></span> <span data-ttu-id="90d19-112">Le client appelle des procédures définies par le programmeur pour allouer des tampons, charger des données dans les mémoires tampons et les décharger.</span><span class="sxs-lookup"><span data-stu-id="90d19-112">The client calls programmer-defined procedures to allocate buffers, load data into and unload data from the buffers.</span></span>

<span data-ttu-id="90d19-113">Cette section fournit une vue d’ensemble de l’utilisation de canaux pour les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="90d19-113">This section provides an overview of using pipes for remote procedure calls.</span></span> <span data-ttu-id="90d19-114">Il présente la vue d’ensemble des rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="90d19-114">It presents the overview in the following topics:</span></span>

-   [<span data-ttu-id="90d19-115">Terminologie des canaux essentiels</span><span class="sxs-lookup"><span data-stu-id="90d19-115">Essential Pipe Terminology</span></span>](essential-pipe-terminology.md)
-   [<span data-ttu-id="90d19-116">État du canal</span><span class="sxs-lookup"><span data-stu-id="90d19-116">The Pipe State</span></span>](the-pipe-state.md)
-   [<span data-ttu-id="90d19-117">Définition de canaux dans des fichiers IDL</span><span class="sxs-lookup"><span data-stu-id="90d19-117">Defining Pipes in IDL Files</span></span>](defining-pipes-in-idl-files.md)
-   [<span data-ttu-id="90d19-118">Implémentation de canal côté client</span><span class="sxs-lookup"><span data-stu-id="90d19-118">Client-Side Pipe Implementation</span></span>](client-side-pipe-implementation.md)
-   [<span data-ttu-id="90d19-119">Implémentation de canal côté serveur</span><span class="sxs-lookup"><span data-stu-id="90d19-119">Server-Side Pipe Implementation</span></span>](server-side-pipe-implementation.md)
-   [<span data-ttu-id="90d19-120">Règles pour plusieurs canaux</span><span class="sxs-lookup"><span data-stu-id="90d19-120">Rules for Multiple Pipes</span></span>](rules-for-multiple-pipes.md)
-   [<span data-ttu-id="90d19-121">Combinaison de paramètres de canal et de pas de canal</span><span class="sxs-lookup"><span data-stu-id="90d19-121">Combining Pipe and Nonpipe Parameters</span></span>](combining-pipe-and-nonpipe-parameters.md)

<span data-ttu-id="90d19-122">Pour plus d’informations sur la syntaxe et les restrictions des canaux, consultez [canal](/windows/desktop/Midl/pipe) dans la référence du langage MIDL.</span><span class="sxs-lookup"><span data-stu-id="90d19-122">For more information on pipe syntax and restrictions, see [pipe](/windows/desktop/Midl/pipe) in the MIDL Language Reference.</span></span> <span data-ttu-id="90d19-123">L’exemple de programme PIPES dans le kit de développement logiciel (SDK) samples du kit de développement logiciel (SDK) fournit des exemples d' \\ utilisation **\[ de dans, des canaux out \]** pour transférer des données entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="90d19-123">The PIPES sample program in the Platform Software Development Kit (SDK) samples\\rpc directory demonstrates how to use **\[in,out\]** pipes to transfer data between a client and a server.</span></span>

 

 
