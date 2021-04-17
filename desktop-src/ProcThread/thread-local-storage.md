---
description: Avec le stockage local des threads (TLS), vous pouvez fournir des données uniques pour chaque thread auquel le processus peut accéder à l’aide d’un index global. Un thread alloue l’index, qui peut être utilisé par les autres threads pour récupérer les données uniques associées à l’index.
ms.assetid: 40df7410-64d6-4edd-8009-d9c3d2aca920
title: stockage local des threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17d2ff7a1ff253ce5a20b3921cc9605bf2989f6
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2021
ms.locfileid: "104566307"
---
# <a name="thread-local-storage"></a><span data-ttu-id="a4192-104">stockage local des threads</span><span class="sxs-lookup"><span data-stu-id="a4192-104">Thread Local Storage</span></span>

<span data-ttu-id="a4192-105">Tous les threads d’un processus partagent son espace d’adressage virtuel.</span><span class="sxs-lookup"><span data-stu-id="a4192-105">All threads of a process share its virtual address space.</span></span> <span data-ttu-id="a4192-106">Les variables locales d’une fonction sont uniques à chaque thread qui exécute la fonction.</span><span class="sxs-lookup"><span data-stu-id="a4192-106">The local variables of a function are unique to each thread that runs the function.</span></span> <span data-ttu-id="a4192-107">Toutefois, les variables statiques et globales sont partagées par tous les threads dans le processus.</span><span class="sxs-lookup"><span data-stu-id="a4192-107">However, the static and global variables are shared by all threads in the process.</span></span> <span data-ttu-id="a4192-108">Avec le *stockage local des threads* (TLS), vous pouvez fournir des données uniques pour chaque thread auquel le processus peut accéder à l’aide d’un index global.</span><span class="sxs-lookup"><span data-stu-id="a4192-108">With *thread local storage* (TLS), you can provide unique data for each thread that the process can access using a global index.</span></span> <span data-ttu-id="a4192-109">Un thread alloue l’index, qui peut être utilisé par les autres threads pour récupérer les données uniques associées à l’index.</span><span class="sxs-lookup"><span data-stu-id="a4192-109">One thread allocates the index, which can be used by the other threads to retrieve the unique data associated with the index.</span></span>

<span data-ttu-id="a4192-110">La constante TLS \_ minimale \_ disponible définit le nombre minimal d’index TLS disponibles dans chaque processus.</span><span class="sxs-lookup"><span data-stu-id="a4192-110">The constant TLS\_MINIMUM\_AVAILABLE defines the minimum number of TLS indexes available in each process.</span></span> <span data-ttu-id="a4192-111">Cette valeur minimale est d’au moins 64 pour tous les systèmes.</span><span class="sxs-lookup"><span data-stu-id="a4192-111">This minimum is guaranteed to be at least 64 for all systems.</span></span> <span data-ttu-id="a4192-112">Le nombre maximal d’index par processus est de 1 088.</span><span class="sxs-lookup"><span data-stu-id="a4192-112">The maximum number of indexes per process is 1,088.</span></span>

<span data-ttu-id="a4192-113">Lorsque les threads sont créés, le système alloue un tableau de valeurs **LPVOID** pour TLS, qui sont initialisées à la valeur null.</span><span class="sxs-lookup"><span data-stu-id="a4192-113">When the threads are created, the system allocates an array of **LPVOID** values for TLS, which are initialized to NULL.</span></span> <span data-ttu-id="a4192-114">Pour qu’un index puisse être utilisé, il doit être alloué par l’un des threads.</span><span class="sxs-lookup"><span data-stu-id="a4192-114">Before an index can be used, it must be allocated by one of the threads.</span></span> <span data-ttu-id="a4192-115">Chaque thread stocke ses données pour un index TLS dans un *emplacement TLS* dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="a4192-115">Each thread stores its data for a TLS index in a *TLS slot* in the array.</span></span> <span data-ttu-id="a4192-116">Si les données associées à un index tiennent dans une valeur **LPVOID** , vous pouvez stocker les données directement dans l’emplacement TLS.</span><span class="sxs-lookup"><span data-stu-id="a4192-116">If the data associated with an index will fit in an **LPVOID** value, you can store the data directly in the TLS slot.</span></span> <span data-ttu-id="a4192-117">Toutefois, si vous utilisez un grand nombre d’index de cette manière, il est préférable d’allouer un stockage distinct, de consolider les données et de réduire le nombre d’emplacements TLS en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="a4192-117">However, if you are using a large number of indexes in this way, it is better to allocate separate storage, consolidate the data, and minimize the number of TLS slots in use.</span></span>

<span data-ttu-id="a4192-118">Le diagramme suivant illustre le fonctionnement du protocole TLS.</span><span class="sxs-lookup"><span data-stu-id="a4192-118">The following diagram illustrates how TLS works.</span></span> <span data-ttu-id="a4192-119">Pour obtenir un exemple de code illustrant l’utilisation du stockage local des threads, consultez [utilisation du stockage local des threads](using-thread-local-storage.md).</span><span class="sxs-lookup"><span data-stu-id="a4192-119">For a code example illustrating the use of thread local storage, see [Using Thread Local Storage](using-thread-local-storage.md).</span></span>

![Diagramme illustrant le fonctionnement du processus T L S.](images/tls.png)

<span data-ttu-id="a4192-121">Le processus a deux threads, thread 1 et thread 2.</span><span class="sxs-lookup"><span data-stu-id="a4192-121">The process has two threads, Thread 1 and Thread 2.</span></span> <span data-ttu-id="a4192-122">Il alloue deux index pour une utilisation avec TLS, gdwTlsIndex1 et gdwTlsIndex2.</span><span class="sxs-lookup"><span data-stu-id="a4192-122">It allocates two indexes for use with TLS, gdwTlsIndex1 and gdwTlsIndex2.</span></span> <span data-ttu-id="a4192-123">Chaque thread alloue deux blocs de mémoire (un pour chaque index) dans lequel stocker les données et stocke les pointeurs vers ces blocs de mémoire dans les emplacements TLS correspondants.</span><span class="sxs-lookup"><span data-stu-id="a4192-123">Each thread allocates two memory blocks (one for each index) in which to store the data, and stores the pointers to these memory blocks in the corresponding TLS slots.</span></span> <span data-ttu-id="a4192-124">Pour accéder aux données associées à un index, le thread récupère le pointeur vers le bloc de mémoire à partir de l’emplacement TLS et le stocke dans la variable locale lpvData.</span><span class="sxs-lookup"><span data-stu-id="a4192-124">To access the data associated with an index, the thread retrieves the pointer to the memory block from the TLS slot and stores it in the lpvData local variable.</span></span>

<span data-ttu-id="a4192-125">Il est idéal d’utiliser TLS dans une bibliothèque de liens dynamiques (DLL).</span><span class="sxs-lookup"><span data-stu-id="a4192-125">It is ideal to use TLS in a dynamic-link library (DLL).</span></span> <span data-ttu-id="a4192-126">Pour obtenir un exemple, consultez [utilisation du stockage local des threads dans une bibliothèque de liens dynamiques](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md).</span><span class="sxs-lookup"><span data-stu-id="a4192-126">For an example, see [Using Thread Local Storage in a Dynamic Link Library](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4192-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a4192-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4192-128">Stockage local des threads (Visual C++)</span><span class="sxs-lookup"><span data-stu-id="a4192-128">Thread Local Storage (Visual C++)</span></span>](/cpp/parallel/thread-local-storage-tls?view=vs-2019)
</dt> <dt>

[<span data-ttu-id="a4192-129">Utilisation de TLS (Thread Local Storage)</span><span class="sxs-lookup"><span data-stu-id="a4192-129">Using Thread Local Storage</span></span>](using-thread-local-storage.md)
</dt> <dt>

[<span data-ttu-id="a4192-130">Utilisation du stockage local des threads dans une bibliothèque de liens dynamiques</span><span class="sxs-lookup"><span data-stu-id="a4192-130">Using Thread Local Storage in a Dynamic Link Library</span></span>](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 
