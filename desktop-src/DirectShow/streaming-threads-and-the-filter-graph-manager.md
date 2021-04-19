---
description: Streaming threads et le gestionnaire de graphique de filtre
ms.assetid: b490b72a-ab34-46e6-8dc6-a7bb07cfc7b1
title: Streaming threads et le gestionnaire de graphique de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a8c5b8fa972a8118563ae8f9e73d480ac15e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520625"
---
# <a name="streaming-threads-and-the-filter-graph-manager"></a><span data-ttu-id="83aa1-103">Streaming threads et le gestionnaire de graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="83aa1-103">Streaming Threads and the Filter Graph Manager</span></span>

<span data-ttu-id="83aa1-104">Lorsque le gestionnaire de graphes de filtres arrête le graphique, il attend que tous les threads de diffusion en continu s’arrêtent.</span><span class="sxs-lookup"><span data-stu-id="83aa1-104">When the Filter Graph Manager stops the graph, it waits for all streaming threads to shut down.</span></span> <span data-ttu-id="83aa1-105">Cela a les conséquences suivantes pour les filtres :</span><span class="sxs-lookup"><span data-stu-id="83aa1-105">This has the following implications for filters:</span></span>

-   <span data-ttu-id="83aa1-106">Un filtre ne doit jamais appeler de méthodes sur le gestionnaire de graphique de filtre à partir d’un thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="83aa1-106">A filter must never call methods on the Filter Graph Manager from a streaming thread.</span></span>

    <span data-ttu-id="83aa1-107">Le gestionnaire de graphique de filtre utilise une section critique pour synchroniser ses propres opérations.</span><span class="sxs-lookup"><span data-stu-id="83aa1-107">The Filter Graph Manager uses a critical section to synchronize its own operations.</span></span> <span data-ttu-id="83aa1-108">Si un thread de streaming tente de conserver cette section critique, il peut provoquer un blocage.</span><span class="sxs-lookup"><span data-stu-id="83aa1-108">If a streaming thread tries to hold this critical section, it can cause a deadlock.</span></span> <span data-ttu-id="83aa1-109">Par exemple : Supposons qu’un autre thread arrête le graphique.</span><span class="sxs-lookup"><span data-stu-id="83aa1-109">For example: Suppose that another thread stops the graph.</span></span> <span data-ttu-id="83aa1-110">Ce thread prend le verrou du graphique de filtre et attend que votre filtre cesse de transmettre des données.</span><span class="sxs-lookup"><span data-stu-id="83aa1-110">That thread takes the filter graph lock and waits for your filter to stop delivering data.</span></span> <span data-ttu-id="83aa1-111">Si votre filtre attend le verrou, il ne s’arrêtera jamais, provoquant ainsi un blocage.</span><span class="sxs-lookup"><span data-stu-id="83aa1-111">If your filter is waiting for the lock, it will never stop, causing a deadlock.</span></span>

-   <span data-ttu-id="83aa1-112">Un filtre ne doit jamais **AddRef** ou **QueryInterface** du gestionnaire de graphique de filtre à partir d’un thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="83aa1-112">A filter must never **AddRef** or **QueryInterface** the Filter Graph Manager from a streaming thread.</span></span>

    <span data-ttu-id="83aa1-113">Si le filtre contient un décompte de références sur le gestionnaire de graphes de filtre (par le biais de **AddRef** ou **QueryInterface**), il peut devenir le dernier objet à contenir un décompte de références.</span><span class="sxs-lookup"><span data-stu-id="83aa1-113">If the filter holds a reference count on the Filter Graph Manager (through **AddRef** or **QueryInterface**), it might become the last object to hold a reference count.</span></span> <span data-ttu-id="83aa1-114">Lorsque le filtre appelle **Release**, le gestionnaire de graphique de filtre détruit lui-même.</span><span class="sxs-lookup"><span data-stu-id="83aa1-114">When the filter calls **Release**, the Filter Graph Manager destroys itself.</span></span> <span data-ttu-id="83aa1-115">Au sein de sa routine de nettoyage, le gestionnaire de graphes de filtre tente d’arrêter le graphique, provoquant l’attente de la fermeture du thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="83aa1-115">Inside its cleanup routine, the Filter Graph Manager attempts to stop the graph, causing it to wait for the streaming thread to exit.</span></span> <span data-ttu-id="83aa1-116">Toutefois, il attend dans le thread de diffusion en continu, donc le thread de streaming ne peut pas quitter.</span><span class="sxs-lookup"><span data-stu-id="83aa1-116">However, it is waiting inside the streaming thread, so the streaming thread cannot exit.</span></span> <span data-ttu-id="83aa1-117">Le résultat est un interblocage.</span><span class="sxs-lookup"><span data-stu-id="83aa1-117">The result is a deadlock.</span></span>

 

 



