---
title: Délégation et emprunt d’identité
description: Dans les scénarios client/serveur, il est courant pour un serveur d’appeler un autre serveur pour accomplir une tâche au nom d’un client. La situation dans laquelle un serveur est autorisé à agir au nom d’un client est appelée délégation.
ms.assetid: 245bff1a-31d3-49ce-847e-c37d0c96f9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356708008274bdeb2aa80631bec777fbd02fd38d
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2021
ms.locfileid: "104550301"
---
# <a name="delegation-and-impersonation"></a><span data-ttu-id="2da71-104">Délégation et emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="2da71-104">Delegation and Impersonation</span></span>

<span data-ttu-id="2da71-105">Dans les scénarios client/serveur, il est courant pour un serveur d’appeler un autre serveur pour accomplir une tâche au nom d’un client.</span><span class="sxs-lookup"><span data-stu-id="2da71-105">In client/server scenarios, it is common for one server to call another server to accomplish some task on a client's behalf.</span></span> <span data-ttu-id="2da71-106">La situation dans laquelle un serveur est autorisé à agir au nom d’un client est appelée *délégation*.</span><span class="sxs-lookup"><span data-stu-id="2da71-106">The situation where a server is given the authority to act on a client's behalf is called *delegation*.</span></span>

<span data-ttu-id="2da71-107">Du point de vue de la sécurité, deux problèmes se posent concernant la délégation :</span><span class="sxs-lookup"><span data-stu-id="2da71-107">From a security standpoint, two issues arise regarding delegation:</span></span>

-   <span data-ttu-id="2da71-108">Que doit être autorisé le serveur lorsqu’il agit au nom du client ?</span><span class="sxs-lookup"><span data-stu-id="2da71-108">What should the server be allowed to do when acting on the client's behalf?</span></span>
-   <span data-ttu-id="2da71-109">Quelle identité est présentée par le serveur lorsqu’il appelle d’autres serveurs pour le compte d’un client ?</span><span class="sxs-lookup"><span data-stu-id="2da71-109">What identity is presented by the server when it calls other servers on behalf of a client?</span></span>

<span data-ttu-id="2da71-110">Pour traiter ces problèmes, COM fournit les fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="2da71-110">To deal with these issues, COM provides the following functionality.</span></span> <span data-ttu-id="2da71-111">Le client peut définir un *niveau d’emprunt d’identité* qui détermine dans quelle mesure le serveur pourra agir en tant que client.</span><span class="sxs-lookup"><span data-stu-id="2da71-111">The client can set an *impersonation level* that determines to what extent the server will be able to act as the client.</span></span> <span data-ttu-id="2da71-112">Si le client accorde une autorité suffisante au serveur, le serveur peut *emprunter l’identité* du client (prétend être).</span><span class="sxs-lookup"><span data-stu-id="2da71-112">If the client grants enough authority to the server, the server can *impersonate* (pretend to be) the client.</span></span> <span data-ttu-id="2da71-113">Lorsque vous empruntez l’identité du client, le serveur est autorisé à accéder uniquement aux objets ou aux ressources que le client est autorisé à utiliser.</span><span class="sxs-lookup"><span data-stu-id="2da71-113">When impersonating the client, the server is given access to only those objects or resources that the client has permission to use.</span></span> <span data-ttu-id="2da71-114">Le serveur, agissant comme un client, peut également activer le *masquage* pour masquer sa propre identité et projeter l’identité du client dans les appels à d’autres composants com.</span><span class="sxs-lookup"><span data-stu-id="2da71-114">The server, acting as a client, can also enable *cloaking* to mask its own identity and project the client's identity in calls to other COM components.</span></span>

![Diagramme qui montre comment le serveur agissant en tant que client peut activer le masquage.](images/172e04f7-568d-450b-9785-2c1a2b40e549.png)

<span data-ttu-id="2da71-116">Prenons le scénario illustré dans la figure précédente, où A et B sont des processus sur un ordinateur différent de C. le processus A appelle B et B appelle C. le client A définit le niveau d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="2da71-116">Consider the scenario illustrated by the preceding figure, where A and B are processes on a different machine from C. Process A calls B, and B calls C. Client A sets the impersonation level.</span></span> <span data-ttu-id="2da71-117">B définit la fonctionnalité de voilage.</span><span class="sxs-lookup"><span data-stu-id="2da71-117">B sets the cloaking capability.</span></span> <span data-ttu-id="2da71-118">Si un définit un niveau d’emprunt d’identité qui autorise l’emprunt d’identité, B peut emprunter l’identité d’un lors de l’appel de C en son nom.</span><span class="sxs-lookup"><span data-stu-id="2da71-118">If A sets an impersonation level that permits impersonation, B can impersonate A when calling C on A's behalf.</span></span> <span data-ttu-id="2da71-119">L’identité présentée au processus C sera l’identité de l’identité de l’une ou de l’identité de B, selon que le masquage a été activé ou non par B. Si le masquage est activé, l’identité présentée au processus C correspond à celle d’un. Si le masquage n’est pas activé, l’identité de B est présentée à C.</span><span class="sxs-lookup"><span data-stu-id="2da71-119">The identity that is presented to process C will be either A's identity or B's identity, depending on whether cloaking was enabled by B. If cloaking is enabled, the identity presented to process C will be that of A. If cloaking is not enabled, B's identity will be presented to C.</span></span>

<span data-ttu-id="2da71-120">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="2da71-120">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="2da71-121">Emprunt d'identité</span><span class="sxs-lookup"><span data-stu-id="2da71-121">Impersonation</span></span>](impersonation.md)
-   [<span data-ttu-id="2da71-122">Niveaux d’emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="2da71-122">Impersonation Levels</span></span>](impersonation-levels.md)
-   [<span data-ttu-id="2da71-123">Masquer</span><span class="sxs-lookup"><span data-stu-id="2da71-123">Cloaking</span></span>](cloaking.md)

 

 




