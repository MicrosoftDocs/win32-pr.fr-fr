---
title: Segment de mémoire (heap)
description: Un segment de mémoire effectue le suivi d’un groupe d’allocations libérées en tant qu’unité.
ms.assetid: 3a25284a-8f15-42d4-a292-ece28a08fb69
keywords:
- Services Web du tas pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e1651f90b8ad1afca8f85f9dd2e6f10fc7f5c3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383348"
---
# <a name="heap"></a><span data-ttu-id="617a2-106">Segment de mémoire (heap)</span><span class="sxs-lookup"><span data-stu-id="617a2-106">Heap</span></span>

<span data-ttu-id="617a2-107">Un segment de mémoire effectue le suivi d’un groupe d’allocations libérées en tant qu’unité.</span><span class="sxs-lookup"><span data-stu-id="617a2-107">A heap tracks a group of allocations that are freed as a unit.</span></span>

<span data-ttu-id="617a2-108">Cela vous permet d’éviter des modèles complexes d’allocation et de libération de mémoire lorsque vous utilisez WWSAPI.</span><span class="sxs-lookup"><span data-stu-id="617a2-108">This allows you to avoid complex patterns of allocating and deallocating memory when you use the WWSAPI.</span></span>


<span data-ttu-id="617a2-109">Un segment de mémoire est associé à chaque message.</span><span class="sxs-lookup"><span data-stu-id="617a2-109">There is a heap associated with every message.</span></span> <span data-ttu-id="617a2-110">Lorsqu’un message est envoyé ou qu’un message est reçu, le segment de mémoire du message est utilisé pour toutes les allocations associées à ce message particulier.</span><span class="sxs-lookup"><span data-stu-id="617a2-110">As a message is being sent, or as a message is being received, the heap of the message is used for any allocations relating to that particular message.</span></span> <span data-ttu-id="617a2-111">Après l’envoi ou la réception d’un message, le segment de mémoire est réinitialisé (ce qui nettoie toutes les allocations associées au message en question).</span><span class="sxs-lookup"><span data-stu-id="617a2-111">After a message is sent or received, the heap is reset (which cleans up any allocations related to the particular message).</span></span>

<span data-ttu-id="617a2-112">Les segments de mémoire peuvent également être utilisés pour stocker des données de message indépendamment de la durée de vie d’un message.</span><span class="sxs-lookup"><span data-stu-id="617a2-112">Heaps can also be used to store message data separately from the lifetime of a message.</span></span> <span data-ttu-id="617a2-113">La plupart des spécifications allow de l’API du tas à utiliser lors de la lecture des données donnent un contrôle explicite sur la durée de vie des données lues.</span><span class="sxs-lookup"><span data-stu-id="617a2-113">Many of the API's allow specification of the heap to use when reading data give explicit control over the lifetime of any data read.</span></span>

<span data-ttu-id="617a2-114">L’alignement des allocations d’un segment de mémoire sur au moins une limite de 8 octets est garanti.</span><span class="sxs-lookup"><span data-stu-id="617a2-114">Allocations from a heap are guaranteed to be aligned on at least an 8 byte boundary.</span></span>

<span data-ttu-id="617a2-115">Les allocations de zéro octet retournent un pointeur non NULL.</span><span class="sxs-lookup"><span data-stu-id="617a2-115">Zero byte allocations will return a non-NULL pointer.</span></span>

<span data-ttu-id="617a2-116">Dans Windows 7, si PageHeap est activé, un segment de mémoire retourné par HeapCreate est utilisé pour gérer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="617a2-116">In Windows 7, if PageHeap is enabled, a heap returned from HeapCreate is used to manage the memory.</span></span> <span data-ttu-id="617a2-117">Dans ce cas, [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) est directement mappé à HeapAlloc et [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) est mappé à HeapDestroy.</span><span class="sxs-lookup"><span data-stu-id="617a2-117">In this case, [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) maps directly to HeapAlloc and [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) maps to HeapDestroy.</span></span>

<span data-ttu-id="617a2-118">L’énumération suivante est utilisée avec le tas :</span><span class="sxs-lookup"><span data-stu-id="617a2-118">The following enumeration is used with the heap:</span></span>

-   [<span data-ttu-id="617a2-119">**\_ID de \_ propriété du tas WS \_**</span><span class="sxs-lookup"><span data-stu-id="617a2-119">**WS\_HEAP\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_heap_property_id)

<span data-ttu-id="617a2-120">Les fonctions suivantes sont utilisées avec le tas :</span><span class="sxs-lookup"><span data-stu-id="617a2-120">The following functions are used with the heap:</span></span>

-   [<span data-ttu-id="617a2-121">**WsAlloc**</span><span class="sxs-lookup"><span data-stu-id="617a2-121">**WsAlloc**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsalloc)
-   [<span data-ttu-id="617a2-122">**WsCreateHeap**</span><span class="sxs-lookup"><span data-stu-id="617a2-122">**WsCreateHeap**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreateheap)
-   [<span data-ttu-id="617a2-123">**WsFreeHeap**</span><span class="sxs-lookup"><span data-stu-id="617a2-123">**WsFreeHeap**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreeheap)
-   [<span data-ttu-id="617a2-124">**WsGetHeapProperty**</span><span class="sxs-lookup"><span data-stu-id="617a2-124">**WsGetHeapProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetheapproperty)
-   [<span data-ttu-id="617a2-125">**WsResetHeap**</span><span class="sxs-lookup"><span data-stu-id="617a2-125">**WsResetHeap**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetheap)

<span data-ttu-id="617a2-126">Le handle suivant est utilisé avec le tas :</span><span class="sxs-lookup"><span data-stu-id="617a2-126">The following handle is used with the heap:</span></span>

-   [<span data-ttu-id="617a2-127">\_tas WS</span><span class="sxs-lookup"><span data-stu-id="617a2-127">WS\_HEAP</span></span>](ws-heap.md)

<span data-ttu-id="617a2-128">Les structures suivantes sont utilisées avec le tas :</span><span class="sxs-lookup"><span data-stu-id="617a2-128">The following structures are used with the heap:</span></span>

-   [<span data-ttu-id="617a2-129">**\_Propriétés du tas WS \_**</span><span class="sxs-lookup"><span data-stu-id="617a2-129">**WS\_HEAP\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_heap_properties)
-   [<span data-ttu-id="617a2-130">**\_propriété du tas WS \_**</span><span class="sxs-lookup"><span data-stu-id="617a2-130">**WS\_HEAP\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_heap_property)

 

 




