---
description: Les modèles de thread COM+ sont conçus autour d’une collection d’objets appelée cloisonnement. Un cloisonnement est une collection de contextes contenus dans un processus.
ms.assetid: c73fb4c5-20ae-4873-afd2-4f40eb47bade
title: Modèles de thread COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f07b065861c042e68add633368a9c8b8ba41b2
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "103761114"
---
# <a name="com-threading-models"></a><span data-ttu-id="1f062-104">Modèles de thread COM+</span><span class="sxs-lookup"><span data-stu-id="1f062-104">COM+ Threading Models</span></span>

<span data-ttu-id="1f062-105">Les modèles de thread COM+ sont conçus autour d’une collection d’objets appelée cloisonnement.</span><span class="sxs-lookup"><span data-stu-id="1f062-105">COM+ threading models are designed around an object collection called an apartment.</span></span> <span data-ttu-id="1f062-106">Un cloisonnement est une collection de contextes contenus dans un processus, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="1f062-106">An apartment is a collection of contexts contained in a process, as shown in the following illustration.</span></span>

![Diagramme qui montre une collection de contextes dans une activité, au sein d’un cloisonnement, au sein d’un processus.](images/6b86fe3b-262a-483a-a418-67d60f9a5d68.png)

<span data-ttu-id="1f062-108">Les appels au sein d’un cloisonnement sont directs, tandis que les appels entre les Apartments (out-of-process) sont indirects et requièrent du code proxy et stub.</span><span class="sxs-lookup"><span data-stu-id="1f062-108">Calls within an apartment are direct, while calls across apartments (out-of-process) are indirect and require proxy and stub code.</span></span> <span data-ttu-id="1f062-109">Les Apartments autorisent les objets avec des propriétés de synchronisation et de réentrance différentes et ont deux catégories : à thread unique et multithread.</span><span class="sxs-lookup"><span data-stu-id="1f062-109">Apartments allow for objects with different synchronization and reentrancy properties and have two categories: single-threaded and multithreaded.</span></span> <span data-ttu-id="1f062-110">Les objets dans un thread cloisonné (STA) s’exécutent sur le thread particulier dans lequel ils ont été créés.</span><span class="sxs-lookup"><span data-stu-id="1f062-110">Objects in a single-threaded apartment (STA) execute on the particular thread in which they were created.</span></span> <span data-ttu-id="1f062-111">Les STA autorisent l’exécution d’une seule méthode à la fois.</span><span class="sxs-lookup"><span data-stu-id="1f062-111">STAs allow only one method to execute at a time.</span></span> <span data-ttu-id="1f062-112">Ils sont conçus pour les interfaces utilisateur et s’appuient sur la file d’attente de messages Microsoft Windows pour traiter les appels entrants.</span><span class="sxs-lookup"><span data-stu-id="1f062-112">They are designed for user interfaces and rely on the Microsoft Windows message queue to process incoming calls.</span></span>

<span data-ttu-id="1f062-113">Les objets d’un cloisonnement multithread (MTA) s’exécutent sur n’importe quel thread et permettent à un nombre quelconque de méthodes de se produire simultanément.</span><span class="sxs-lookup"><span data-stu-id="1f062-113">Objects in a multithreaded apartment (MTA) execute on any thread and allow any number of methods to occur simultaneously.</span></span> <span data-ttu-id="1f062-114">Les MTA prennent en charge la réentrance implicitement.</span><span class="sxs-lookup"><span data-stu-id="1f062-114">MTAs support reentrance implicitly.</span></span>

<span data-ttu-id="1f062-115">Les classes COM+ sont marquées avec une propriété **ThreadingModel** qui permet à com+ de créer l’objet dans le cloisonnement approprié.</span><span class="sxs-lookup"><span data-stu-id="1f062-115">COM+ classes are marked with a **ThreadingModel** property that allows COM+ to create the object in the proper apartment.</span></span> <span data-ttu-id="1f062-116">Pour déterminer le cloisonnement dans lequel un objet est créé, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) utilise la propriété **ThreadingModel** .</span><span class="sxs-lookup"><span data-stu-id="1f062-116">To determine which apartment an object is created in, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) uses the **ThreadingModel** property.</span></span>

<span data-ttu-id="1f062-117">Les threads doivent appeler [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) pour pouvoir utiliser com+.</span><span class="sxs-lookup"><span data-stu-id="1f062-117">Threads must call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) before they can use COM+.</span></span> <span data-ttu-id="1f062-118">Cela les crée à l’intérieur du cloisonnement et du contexte appropriés.</span><span class="sxs-lookup"><span data-stu-id="1f062-118">This creates them inside the correct apartment and context.</span></span> <span data-ttu-id="1f062-119">Le thread cloisonné principal est déterminé comme étant le premier STA appelé par **CoInitializeEx**.</span><span class="sxs-lookup"><span data-stu-id="1f062-119">The main thread apartment is determined to be the first STA called by **CoInitializeEx**.</span></span> <span data-ttu-id="1f062-120">Cela est généralement associé au thread principal d’un processus.</span><span class="sxs-lookup"><span data-stu-id="1f062-120">This is usually associated with the main thread of a process.</span></span> <span data-ttu-id="1f062-121">**CoInitializeEx** indique le type de cloisonnement requis par le thread en définissant les indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="1f062-121">**CoInitializeEx** indicates the type of apartment required by the thread by setting the following flags:</span></span>

-   <span data-ttu-id="1f062-122">**COinit \_ MULTITHREAD**: localise le thread dans le seul cloisonnement multithread.</span><span class="sxs-lookup"><span data-stu-id="1f062-122">**COINIT\_MULTITHREADED**—Locates the thread in the single multithreaded apartment.</span></span>
-   <span data-ttu-id="1f062-123">**COinit \_ APARTMENTTHREADED**: place le thread dans un nouveau STA.</span><span class="sxs-lookup"><span data-stu-id="1f062-123">**COINIT\_APARTMENTTHREADED**—Places the thread into a new STA.</span></span>

<span data-ttu-id="1f062-124">Les rubriques suivantes de cette section fournissent des informations supplémentaires sur l’utilisation des modèles de thread et des cloisonnements dans COM+ :</span><span class="sxs-lookup"><span data-stu-id="1f062-124">The following topics in this section provide more information about using threading models and apartments in COM+:</span></span>

-   [<span data-ttu-id="1f062-125">Attribut de modèle de thread</span><span class="sxs-lookup"><span data-stu-id="1f062-125">Threading Model Attribute</span></span>](threading-model-attribute.md)
-   [<span data-ttu-id="1f062-126">Cloisonnements neutres</span><span class="sxs-lookup"><span data-stu-id="1f062-126">Neutral Apartments</span></span>](neutral-apartments.md)

## <a name="related-topics"></a><span data-ttu-id="1f062-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1f062-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f062-128">Processus, threads et Apartments</span><span class="sxs-lookup"><span data-stu-id="1f062-128">Processes, Threads, and Apartments</span></span>](/windows/desktop/com/processes--threads--and-apartments)
</dt> <dt>

[<span data-ttu-id="1f062-129">**ThreadingModel**</span><span class="sxs-lookup"><span data-stu-id="1f062-129">**ThreadingModel**</span></span>](components.md)
</dt> </dl>

 

 
