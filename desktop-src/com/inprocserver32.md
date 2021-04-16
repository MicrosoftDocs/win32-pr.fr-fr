---
title: InprocServer32
description: Inscrit un serveur in-process 32 bits et spécifie le modèle de thread du cloisonnement sur lequel le serveur peut s’exécuter.
ms.assetid: 4edbbd9d-7ea1-4476-aee7-eaf30e54db8d
keywords:
- Clé de Registre InprocServer32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0daae9d495ad588e0dc710b63fe7d7ae9f48c11d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507363"
---
# <a name="inprocserver32"></a><span data-ttu-id="1d0a5-104">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="1d0a5-104">InprocServer32</span></span>

<span data-ttu-id="1d0a5-105">Inscrit un serveur in-process 32 bits et spécifie le modèle de thread du cloisonnement sur lequel le serveur peut s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="1d0a5-105">Registers a 32-bit in-process server and specifies the threading model of the apartment the server can run in.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="1d0a5-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="1d0a5-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         (Default) = path
         ThreadingModel = value
```

## <a name="remarks"></a><span data-ttu-id="1d0a5-107">Notes</span><span class="sxs-lookup"><span data-stu-id="1d0a5-107">Remarks</span></span>

<span data-ttu-id="1d0a5-108">**ThreadingModel** est une valeur de **reg \_ SZ** qui spécifie le modèle de thread.</span><span class="sxs-lookup"><span data-stu-id="1d0a5-108">**ThreadingModel** is a **REG\_SZ** value the specifies the threading model.</span></span> <span data-ttu-id="1d0a5-109">Les valeurs possibles sont indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1d0a5-109">The possible values are shown in the following table.</span></span>



| <span data-ttu-id="1d0a5-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d0a5-110">Value</span></span>     | <span data-ttu-id="1d0a5-111">Description</span><span class="sxs-lookup"><span data-stu-id="1d0a5-111">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="1d0a5-112">STA</span><span class="sxs-lookup"><span data-stu-id="1d0a5-112">Apartment</span></span> | <span data-ttu-id="1d0a5-113">Cloisonnement à thread unique</span><span class="sxs-lookup"><span data-stu-id="1d0a5-113">Single-threaded apartment</span></span>                  |
| <span data-ttu-id="1d0a5-114">Les deux</span><span class="sxs-lookup"><span data-stu-id="1d0a5-114">Both</span></span>      | <span data-ttu-id="1d0a5-115">Cloisonnement monothread ou multithread</span><span class="sxs-lookup"><span data-stu-id="1d0a5-115">Single-threaded or multithreaded apartment</span></span> |
| <span data-ttu-id="1d0a5-116">Gratuit</span><span class="sxs-lookup"><span data-stu-id="1d0a5-116">Free</span></span>      | <span data-ttu-id="1d0a5-117">Multithread cloisonné</span><span class="sxs-lookup"><span data-stu-id="1d0a5-117">Multithreaded apartment</span></span>                    |
| <span data-ttu-id="1d0a5-118">Neutre</span><span class="sxs-lookup"><span data-stu-id="1d0a5-118">Neutral</span></span>   | <span data-ttu-id="1d0a5-119">Cloisonnement neutre</span><span class="sxs-lookup"><span data-stu-id="1d0a5-119">Neutral apartment</span></span>                          |



 

<span data-ttu-id="1d0a5-120">Vous devez utiliser la même valeur pour chaque objet fourni par le serveur in-process.</span><span class="sxs-lookup"><span data-stu-id="1d0a5-120">You must use the same value for every object provided by the in-process server.</span></span>

<span data-ttu-id="1d0a5-121">Si **ThreadingModel** n’est pas présent ou n’est pas défini sur une valeur, le serveur est chargé dans le premier cloisonnement qui a été initialisé dans le processus.</span><span class="sxs-lookup"><span data-stu-id="1d0a5-121">If **ThreadingModel** is not present or is not set to a value, the server is loaded into the first apartment that was initialized in the process.</span></span> <span data-ttu-id="1d0a5-122">Ce cloisonnement est parfois appelé STA (Single-Threaded Apartment).</span><span class="sxs-lookup"><span data-stu-id="1d0a5-122">This apartment is sometimes referred to as the main single-threaded apartment (STA).</span></span> <span data-ttu-id="1d0a5-123">Si le premier STA d’un processus est initialisé par COM, plutôt que par un appel explicite à [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), il est appelé STA de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="1d0a5-123">If the first STA in a process is initialized by COM, rather than by an explicit call to [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), it is called the host STA.</span></span> <span data-ttu-id="1d0a5-124">Par exemple, COM crée un STA hôte si un serveur in-process à charger requiert un STA, mais qu’il n’existe actuellement aucun STA dans le processus.</span><span class="sxs-lookup"><span data-stu-id="1d0a5-124">For example, COM creates a host STA if an in-process server to be loaded requires an STA but there is currently no STA in the process.</span></span>

<span data-ttu-id="1d0a5-125">Dans la mesure du possible, le serveur in-process est chargé dans le même cloisonnement que le client qui le charge.</span><span class="sxs-lookup"><span data-stu-id="1d0a5-125">Whenever possible, the in-process server is loaded in the same apartment as the client that loads it.</span></span> <span data-ttu-id="1d0a5-126">Si le modèle de thread de l’Apartment client n’est pas compatible avec le modèle spécifié, le serveur est chargé comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1d0a5-126">If the threading model of the client apartment is not compatible with the model specified, the server is loaded as indicated in the following table.</span></span>



| <span data-ttu-id="1d0a5-127">Modèle de thread du serveur</span><span class="sxs-lookup"><span data-stu-id="1d0a5-127">Threading model of server</span></span> | <span data-ttu-id="1d0a5-128">Serveur cloisonné en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="1d0a5-128">Apartment server is run in</span></span> |
|---------------------------|----------------------------|
| <not specified>     | <span data-ttu-id="1d0a5-129">STA principal</span><span class="sxs-lookup"><span data-stu-id="1d0a5-129">Main STA</span></span>                   |
| <span data-ttu-id="1d0a5-130">Les deux</span><span class="sxs-lookup"><span data-stu-id="1d0a5-130">Both</span></span>                      | <span data-ttu-id="1d0a5-131">Même cloisonnement que le client</span><span class="sxs-lookup"><span data-stu-id="1d0a5-131">Same apartment as client</span></span>   |
| <span data-ttu-id="1d0a5-132">Gratuit</span><span class="sxs-lookup"><span data-stu-id="1d0a5-132">Free</span></span>                      | <span data-ttu-id="1d0a5-133">Multithread cloisonné</span><span class="sxs-lookup"><span data-stu-id="1d0a5-133">Multithreaded apartment</span></span>    |
| <span data-ttu-id="1d0a5-134">Neutre</span><span class="sxs-lookup"><span data-stu-id="1d0a5-134">Neutral</span></span>                   | <span data-ttu-id="1d0a5-135">Cloisonnement neutre</span><span class="sxs-lookup"><span data-stu-id="1d0a5-135">Neutral apartment</span></span>          |



 

<span data-ttu-id="1d0a5-136">Si le modèle de thread du serveur est cloisonné, le cloisonnement dans lequel le serveur est chargé dépend de l’appartement dans lequel le client s’exécute, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1d0a5-136">If the threading model of the server is Apartment, the apartment the server is loaded in depends on the apartment the client is running in, as indicated in the following table.</span></span>



| <span data-ttu-id="1d0a5-137">Le client Apartment est exécuté dans</span><span class="sxs-lookup"><span data-stu-id="1d0a5-137">Apartment client is run in</span></span> | <span data-ttu-id="1d0a5-138">Serveur cloisonné en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="1d0a5-138">Apartment server is run in</span></span> |
|----------------------------|----------------------------|
| <span data-ttu-id="1d0a5-139">Multithread</span><span class="sxs-lookup"><span data-stu-id="1d0a5-139">Multithreaded</span></span>              | <span data-ttu-id="1d0a5-140">STA hôte</span><span class="sxs-lookup"><span data-stu-id="1d0a5-140">Host STA</span></span>                   |
| <span data-ttu-id="1d0a5-141">Neutral (sur thread STA)</span><span class="sxs-lookup"><span data-stu-id="1d0a5-141">Neutral (on STA thread)</span></span>    | <span data-ttu-id="1d0a5-142">Même cloisonnement que le client</span><span class="sxs-lookup"><span data-stu-id="1d0a5-142">Same apartment as client</span></span>   |
| <span data-ttu-id="1d0a5-143">Neutral (sur thread MTA)</span><span class="sxs-lookup"><span data-stu-id="1d0a5-143">Neutral (on MTA thread)</span></span>    | <span data-ttu-id="1d0a5-144">STA hôte</span><span class="sxs-lookup"><span data-stu-id="1d0a5-144">Host STA</span></span>                   |



 

<span data-ttu-id="1d0a5-145">COM peut également créer un hôte multithread cloisonné (MTA).</span><span class="sxs-lookup"><span data-stu-id="1d0a5-145">COM can also create a host multithreaded apartment (MTA).</span></span> <span data-ttu-id="1d0a5-146">Si un client d’un cloisonnement à thread unique demande un serveur in-process dont le modèle de thread est libre en l’absence de MTA dans le processus, COM crée un MTA hôte et y charge le serveur.</span><span class="sxs-lookup"><span data-stu-id="1d0a5-146">If a client in a single-threaded apartment requests an in-process server whose threading model is Free when there is no MTA in the process, COM creates a host MTA and loads the server into it.</span></span>

<span data-ttu-id="1d0a5-147">Pour un serveur in-process 32 bits, les clés [**InprocHandler32**](inprochandler32.md), [**InprocServer**](inprocserver.md), **InprocServer32** et [**Insertable**](insertable.md) doivent être inscrites.</span><span class="sxs-lookup"><span data-stu-id="1d0a5-147">For a 32-bit in-process server, the [**InprocHandler32**](inprochandler32.md), [**InprocServer**](inprocserver.md), **InprocServer32**, and [**Insertable**](insertable.md) keys must be registered.</span></span> <span data-ttu-id="1d0a5-148">L’entrée **InprocServer** est nécessaire uniquement pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="1d0a5-148">The **InprocServer** entry is needed only for backward compatibility.</span></span> <span data-ttu-id="1d0a5-149">Si elle est manquante, la classe fonctionne toujours, mais elle ne peut pas être chargée dans des applications 16 bits.</span><span class="sxs-lookup"><span data-stu-id="1d0a5-149">If it is missing, the class still works but it cannot be loaded in 16-bit applications.</span></span>

<span data-ttu-id="1d0a5-150">Si un conteneur recherche un serveur in-process dans le registre, la version 16 bits a la priorité sur un conteneur de 16 bits et la version 32 bits a la priorité sur un conteneur 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1d0a5-150">If a container is searching the registry for an in-process server, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d0a5-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1d0a5-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d0a5-152">**InprocServer**</span><span class="sxs-lookup"><span data-stu-id="1d0a5-152">**InprocServer**</span></span>](inprocserver.md)
</dt> </dl>

 

 




