---
title: Accès aux interfaces à travers les Apartments
description: Accès aux interfaces à travers les Apartments
ms.assetid: 4e0467b9-bbf1-410c-8aab-40450a7f963a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626707daf721aee3b440bb79ba2d1e084d154a98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672373"
---
# <a name="accessing-interfaces-across-apartments"></a><span data-ttu-id="5be16-103">Accès aux interfaces à travers les Apartments</span><span class="sxs-lookup"><span data-stu-id="5be16-103">Accessing Interfaces Across Apartments</span></span>

<span data-ttu-id="5be16-104">COM permet à n’importe quel cloisonnement d’un processus d’obtenir l’accès à une interface implémentée sur un objet dans n’importe quel autre cloisonnement du processus.</span><span class="sxs-lookup"><span data-stu-id="5be16-104">COM provides a way for any apartment in a process to get access to an interface implemented on an object in any other apartment in the process.</span></span> <span data-ttu-id="5be16-105">Cette opération s’effectue par le biais de l’interface [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) .</span><span class="sxs-lookup"><span data-stu-id="5be16-105">This is done through the [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface.</span></span> <span data-ttu-id="5be16-106">Cette interface a trois méthodes, qui vous permettent d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="5be16-106">This interface has three methods, which allow you to do the following:</span></span>

-   <span data-ttu-id="5be16-107">Inscrire une interface en tant qu’interface *globale* (échelle).</span><span class="sxs-lookup"><span data-stu-id="5be16-107">Register an interface as a *global* (processwide) interface.</span></span>
-   <span data-ttu-id="5be16-108">Obtient un pointeur vers cette interface à partir de tout autre cloisonnement via un cookie.</span><span class="sxs-lookup"><span data-stu-id="5be16-108">Get a pointer to that interface from any other apartment through a cookie.</span></span>
-   <span data-ttu-id="5be16-109">Révoque l’inscription globale d’une interface.</span><span class="sxs-lookup"><span data-stu-id="5be16-109">Revoke the global registration of an interface.</span></span>

<span data-ttu-id="5be16-110">L’interface [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) est un moyen efficace pour un processus de stocker un pointeur d’interface dans un emplacement de mémoire accessible à partir de plusieurs cloisonnements au sein du processus, tels que des variables à l’ensemble du processus et des objets *agile* (objets marshalés en thread) qui contiennent des pointeurs d’interface vers d’autres objets.</span><span class="sxs-lookup"><span data-stu-id="5be16-110">The [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface is an efficient way for a process to store an interface pointer in a memory location that can be accessed from multiple apartments within the process, such as process-wide variables and *agile* objects (free-threaded, marshaled objects) containing interface pointers to other objects.</span></span>

<span data-ttu-id="5be16-111">Un objet agile ne tient pas compte de l’infrastructure COM sous-jacente dans laquelle il s’exécute ; en d’autres termes, le cloisonnement, le contexte et le thread sur lequel il s’exécute.</span><span class="sxs-lookup"><span data-stu-id="5be16-111">An agile object is unaware of the underlying COM infrastructure in which it runs; in other words, what apartment, context, and thread it is executing on.</span></span> <span data-ttu-id="5be16-112">L’objet peut contenir des interfaces spécifiques à un cloisonnement ou à un contexte.</span><span class="sxs-lookup"><span data-stu-id="5be16-112">The object may be holding on to interfaces that are specific to an apartment or context.</span></span> <span data-ttu-id="5be16-113">Pour cette raison, l’appel de ces interfaces à partir de partout où le composant agile s’exécute peut ne pas toujours fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="5be16-113">For this reason, calling these interfaces from wherever the agile component is executing might not always work properly.</span></span> <span data-ttu-id="5be16-114">La table d’interface globale évite ce problème en garantissant qu’un proxy (ou pointeur direct) valide pour l’objet est utilisé, en fonction de l’endroit où l’objet agile s’exécute.</span><span class="sxs-lookup"><span data-stu-id="5be16-114">The global interface table avoids this problem by guaranteeing that a valid proxy (or direct pointer) to the object is used, based on where the agile object is executing.</span></span>

> [!Note]  
> <span data-ttu-id="5be16-115">La table d’interface globale n’étant pas portable au-delà des limites des processus ou des ordinateurs, elle ne peut pas être utilisée à la place du mécanisme de passage de paramètres normal.</span><span class="sxs-lookup"><span data-stu-id="5be16-115">The global interface table is not portable across process or machine boundaries, so it cannot be used in place of the normal parameter-passing mechanism.</span></span>

 

<span data-ttu-id="5be16-116">Pour plus d’informations sur la création et l’utilisation d’une table d’interface globale, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="5be16-116">For information about creating and using a global interface table, see the following topics:</span></span>

-   [<span data-ttu-id="5be16-117">Création de la table d’interface globale</span><span class="sxs-lookup"><span data-stu-id="5be16-117">Creating the Global Interface Table</span></span>](creating-the-global-interface-table.md)
-   [<span data-ttu-id="5be16-118">Quand utiliser la table d’interface globale</span><span class="sxs-lookup"><span data-stu-id="5be16-118">When to Use the Global Interface Table</span></span>](when-to-use-the-global-interface-table.md)

## <a name="related-topics"></a><span data-ttu-id="5be16-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5be16-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5be16-120">Choix du modèle de thread</span><span class="sxs-lookup"><span data-stu-id="5be16-120">Choosing the Threading Model</span></span>](choosing-the-threading-model.md)
</dt> <dt>

[<span data-ttu-id="5be16-121">Apartments (cloisonnés) multithread</span><span class="sxs-lookup"><span data-stu-id="5be16-121">Multithreaded Apartments</span></span>](multithreaded-apartments.md)
</dt> <dt>

[<span data-ttu-id="5be16-122">Problèmes liés aux threads du serveur in-process</span><span class="sxs-lookup"><span data-stu-id="5be16-122">In-Process Server Threading Issues</span></span>](in-process-server-threading-issues.md)
</dt> <dt>

[<span data-ttu-id="5be16-123">Processus, threads et Apartments</span><span class="sxs-lookup"><span data-stu-id="5be16-123">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> <dt>

[<span data-ttu-id="5be16-124">Communication monothread et multithread</span><span class="sxs-lookup"><span data-stu-id="5be16-124">Single-Threaded and Multithreaded Communication</span></span>](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[<span data-ttu-id="5be16-125">Apartments (cloisonnés) à thread unique</span><span class="sxs-lookup"><span data-stu-id="5be16-125">Single-Threaded Apartments</span></span>](single-threaded-apartments.md)
</dt> </dl>

 

 




