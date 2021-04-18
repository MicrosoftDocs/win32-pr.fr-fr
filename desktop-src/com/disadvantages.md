---
title: Inconvénients
description: Inconvénients
ms.assetid: ce6885d9-7056-42bc-85d1-27ce32b1be5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a22e409414a1df60e2dd9dff3adbfc6000b953a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507394"
---
# <a name="disadvantages"></a><span data-ttu-id="67ef2-103">Inconvénients</span><span class="sxs-lookup"><span data-stu-id="67ef2-103">Disadvantages</span></span>

<span data-ttu-id="67ef2-104">Les serveurs in-process fournissent l’avantage de vitesse et de taille d’un gestionnaire d’objets avec la fonction de modification d’un serveur local.</span><span class="sxs-lookup"><span data-stu-id="67ef2-104">In-process servers provide the speed and size advantage of an object handler with the editing capability of a local server.</span></span> <span data-ttu-id="67ef2-105">Pourquoi choisir d’implémenter votre application OLE en tant que serveur local plutôt qu’en tant que serveur in-process ?</span><span class="sxs-lookup"><span data-stu-id="67ef2-105">So why would you ever choose to implement your OLE application as a local server rather than an in-process server?</span></span> <span data-ttu-id="67ef2-106">Il existe plusieurs raisons à cela :</span><span class="sxs-lookup"><span data-stu-id="67ef2-106">There are several reasons:</span></span>

-   <span data-ttu-id="67ef2-107">Sécurité.</span><span class="sxs-lookup"><span data-stu-id="67ef2-107">Security.</span></span> <span data-ttu-id="67ef2-108">Seul un serveur local a son espace d’adressage isolé de celui du client.</span><span class="sxs-lookup"><span data-stu-id="67ef2-108">Only a local server has its address space isolated from that of the client.</span></span> <span data-ttu-id="67ef2-109">Un serveur in-process partage l’espace d’adressage et le contexte de processus du client et peut donc être moins fiable face aux erreurs ou à la programmation malveillante.</span><span class="sxs-lookup"><span data-stu-id="67ef2-109">An in-process server shares the address space and process context of the client and can therefore be less robust in the face of faults or malicious programming.</span></span>
-   <span data-ttu-id="67ef2-110">Granularité.</span><span class="sxs-lookup"><span data-stu-id="67ef2-110">Granularity.</span></span> <span data-ttu-id="67ef2-111">Un serveur local peut héberger plusieurs instances de son objet sur de nombreux clients différents, en partageant l’état du serveur entre des objets de plusieurs clients de manière difficile ou impossible à implémenter en tant que serveur in-process, qui est simplement une DLL chargée dans chaque client.</span><span class="sxs-lookup"><span data-stu-id="67ef2-111">A local server can host multiple instances of its object across many different clients, sharing server state between objects in multiple clients in ways that would be difficult or impossible if implemented as an in-process server, which is simply a DLL loaded into each client.</span></span>
-   <span data-ttu-id="67ef2-112">Compatibilité.</span><span class="sxs-lookup"><span data-stu-id="67ef2-112">Compatibility.</span></span> <span data-ttu-id="67ef2-113">Si vous choisissez d’implémenter un serveur in-process, vous abandonnez la compatibilité avec OLE 1, qui ne prend pas en charge ces serveurs.</span><span class="sxs-lookup"><span data-stu-id="67ef2-113">If you choose to implement an in-process server, you relinquish compatibility with OLE 1, which does not support such servers.</span></span> <span data-ttu-id="67ef2-114">Ce n’est pas une considération pour de nombreux développeurs, mais si c’est le cas, il s’agit d’un problème critique.</span><span class="sxs-lookup"><span data-stu-id="67ef2-114">This will not be a consideration for many developers, but if it is, then it is of critical concern.</span></span>
-   <span data-ttu-id="67ef2-115">Impossible de prendre en charge les liens.</span><span class="sxs-lookup"><span data-stu-id="67ef2-115">Inability to support links.</span></span> <span data-ttu-id="67ef2-116">Un serveur in-process ne peut pas servir de source de liaison.</span><span class="sxs-lookup"><span data-stu-id="67ef2-116">An in-process server cannot serve as a link source.</span></span> <span data-ttu-id="67ef2-117">Étant donné qu’une DLL ne peut pas s’exécuter elle-même, elle ne peut pas créer d’objet de fichier à lier.</span><span class="sxs-lookup"><span data-stu-id="67ef2-117">Since a DLL cannot run by itself, it cannot create a file object to be linked to.</span></span>

<span data-ttu-id="67ef2-118">Malgré ces inconvénients, un serveur in-process peut être un excellent choix pour sa vitesse et sa taille, s’il répond à toutes vos exigences.</span><span class="sxs-lookup"><span data-stu-id="67ef2-118">Despite these disadvantages, an in-process server can be an excellent choice for its speed and size — if it fits all your other requirements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67ef2-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="67ef2-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67ef2-120">Avantages</span><span class="sxs-lookup"><span data-stu-id="67ef2-120">Advantages</span></span>](advantages.md)
</dt> <dt>

[<span data-ttu-id="67ef2-121">Serveurs in-process</span><span class="sxs-lookup"><span data-stu-id="67ef2-121">In-Process Servers</span></span>](in-process-servers.md)
</dt> </dl>

 

 




