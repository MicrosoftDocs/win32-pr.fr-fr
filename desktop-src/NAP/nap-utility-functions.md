---
title: Fonctions de l’utilitaire NAP
description: Les fonctions utilitaires suivantes prennent en charge l’API NAP.
ms.assetid: 0819067c-cca5-4140-8b4d-f3b996826152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260c423909011c81f52ea89ce8d3137b35c55167
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672733"
---
# <a name="nap-utility-functions"></a><span data-ttu-id="95543-103">Fonctions de l’utilitaire NAP</span><span class="sxs-lookup"><span data-stu-id="95543-103">NAP Utility Functions</span></span>

> [!Note]  
> <span data-ttu-id="95543-104">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="95543-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="95543-105">Les fonctions utilitaires suivantes prennent en charge l’API NAP.</span><span class="sxs-lookup"><span data-stu-id="95543-105">The following utility functions support the NAP API.</span></span>

<span data-ttu-id="95543-106">Toutes les interfaces COM prises en charge par le système NAP utilisent des règles de gestion de mémoire COM standard et l’allocateur de mémoire COM (CoTaskMemAlloc et CoTaskMemFree).</span><span class="sxs-lookup"><span data-stu-id="95543-106">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocator (CoTaskMemAlloc and CoTaskMemFree).</span></span>

-   <span data-ttu-id="95543-107">DANS les paramètres, alloué et libéré par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="95543-107">IN parameters — allocated and freed by caller.</span></span>
-   <span data-ttu-id="95543-108">Paramètres OUT — alloués par l’appelé, libérés par l’appelant à l’aide de CoTaskMem \* ()</span><span class="sxs-lookup"><span data-stu-id="95543-108">OUT parameters — allocated by callee, freed by caller using CoTaskMem\*()</span></span>
-   <span data-ttu-id="95543-109">Paramètres IN/OUT — alloués par l’appelant, libérés et réalloués par l’appelé, libérés en fin de terme par l’appelant, à l’aide de CoTaskMem \* ()</span><span class="sxs-lookup"><span data-stu-id="95543-109">IN/OUT parameters — allocated by caller, freed and reallocated by callee, ultimately freed by caller, using CoTaskMem\*()</span></span>

<span data-ttu-id="95543-110">Dans les fonctions FreeXxx (), tous les pointeurs incorporés sont également libérés.</span><span class="sxs-lookup"><span data-stu-id="95543-110">In the FreeXxx() functions, all embedded pointers will also be freed.</span></span>

-   [<span data-ttu-id="95543-111">**AllocConnections**</span><span class="sxs-lookup"><span data-stu-id="95543-111">**AllocConnections**</span></span>](allocconnections-func.md)
-   [<span data-ttu-id="95543-112">**AllocCountedString**</span><span class="sxs-lookup"><span data-stu-id="95543-112">**AllocCountedString**</span></span>](alloccountedstring-func.md)
-   [<span data-ttu-id="95543-113">**AllocFixupInfo**</span><span class="sxs-lookup"><span data-stu-id="95543-113">**AllocFixupInfo**</span></span>](allocfixupinfo-func.md)
-   [<span data-ttu-id="95543-114">**FreeConnections**</span><span class="sxs-lookup"><span data-stu-id="95543-114">**FreeConnections**</span></span>](freeconnections-func.md)
-   [<span data-ttu-id="95543-115">**FreeCountedString**</span><span class="sxs-lookup"><span data-stu-id="95543-115">**FreeCountedString**</span></span>](freecountedstring-func.md)
-   [<span data-ttu-id="95543-116">**FreeFixupInfo**</span><span class="sxs-lookup"><span data-stu-id="95543-116">**FreeFixupInfo**</span></span>](freefixupinfo-func.md)
-   [<span data-ttu-id="95543-117">**FreeIsolationInfo**</span><span class="sxs-lookup"><span data-stu-id="95543-117">**FreeIsolationInfo**</span></span>](freeisolationinfo-func.md)
-   [<span data-ttu-id="95543-118">**FreeIsolationInfoEx**</span><span class="sxs-lookup"><span data-stu-id="95543-118">**FreeIsolationInfoEx**</span></span>](freeisolationinfoex.md)
-   [<span data-ttu-id="95543-119">**FreeNapComponentRegistrationInfoArray**</span><span class="sxs-lookup"><span data-stu-id="95543-119">**FreeNapComponentRegistrationInfoArray**</span></span>](freenapcomponentregistrationinfoarray-func.md)
-   [<span data-ttu-id="95543-120">**FreeNetworkSoH**</span><span class="sxs-lookup"><span data-stu-id="95543-120">**FreeNetworkSoH**</span></span>](freenetworksoh-func.md)
-   [<span data-ttu-id="95543-121">**FreePrivateData**</span><span class="sxs-lookup"><span data-stu-id="95543-121">**FreePrivateData**</span></span>](freeprivatedata-func.md)
-   [<span data-ttu-id="95543-122">**FreeSoH**</span><span class="sxs-lookup"><span data-stu-id="95543-122">**FreeSoH**</span></span>](freesoh-func.md)
-   [<span data-ttu-id="95543-123">**FreeSoHAttributeValue**</span><span class="sxs-lookup"><span data-stu-id="95543-123">**FreeSoHAttributeValue**</span></span>](freesohattributevalue-func.md)
-   [<span data-ttu-id="95543-124">**FreeSystemHealthAgentState**</span><span class="sxs-lookup"><span data-stu-id="95543-124">**FreeSystemHealthAgentState**</span></span>](freesystemhealthagentstate-func.md)
-   [<span data-ttu-id="95543-125">**InitializeNapAgentNotifier**</span><span class="sxs-lookup"><span data-stu-id="95543-125">**InitializeNapAgentNotifier**</span></span>](initializenapagentnotifier.md)
-   [<span data-ttu-id="95543-126">**UninitializeNapAgentNotifier**</span><span class="sxs-lookup"><span data-stu-id="95543-126">**UninitializeNapAgentNotifier**</span></span>](uninitializenapagentnotifier.md)

 

 




