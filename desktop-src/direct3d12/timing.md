---
title: Minutage (Direct3D 12 Graphics)
description: Cette section traite de l’interrogation des horodateurs et de l’étalonnage des compteurs GPU et horodateur de l’UC.
ms.assetid: CC1E5BAB-4363-43FF-BF5B-6C9AEBECD6CA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 979c51b3c88be184cb23afaa2008e90eaec1f9c5
ms.sourcegitcommit: a1f58e231315e95bbf9178994f8c52303fc0d4a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/21/2020
ms.locfileid: "104548609"
---
# <a name="timing-direct3d-12-graphics"></a><span data-ttu-id="ef97d-103">Minutage (Direct3D 12 Graphics)</span><span class="sxs-lookup"><span data-stu-id="ef97d-103">Timing (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="ef97d-104">Cette section traite de l’interrogation des horodateurs et de l’étalonnage des compteurs GPU et horodateur de l’UC.</span><span class="sxs-lookup"><span data-stu-id="ef97d-104">This section covers querying timestamps, and calibrating the GPU and CPU timestamp counters.</span></span>

## <a name="timestamp-frequency"></a><span data-ttu-id="ef97d-105">Fréquence d’horodatage</span><span class="sxs-lookup"><span data-stu-id="ef97d-105">Timestamp frequency</span></span>

<span data-ttu-id="ef97d-106">Votre application peut interroger la fréquence d’horodatage du GPU en fonction de la file d’attente par commande (reportez-vous à la méthode [**ID3D12CommandQueue :: GetTimestampFrequency**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency) ).</span><span class="sxs-lookup"><span data-stu-id="ef97d-106">Your application can query the GPU timestamp frequency on a per-command queue basis (refer to the [**ID3D12CommandQueue::GetTimestampFrequency**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency) method).</span></span>

<span data-ttu-id="ef97d-107">La fréquence retournée est mesurée en Hz (cycles/s).</span><span class="sxs-lookup"><span data-stu-id="ef97d-107">The returned frequency is measured in Hz (ticks/sec).</span></span> <span data-ttu-id="ef97d-108">Si la file d’attente de commandes spécifiée ne prend pas en charge les horodateurs (voir le tableau dans la section [requêtes](queries.md) ), cette API échoue (et retourne **E_FAIL**).</span><span class="sxs-lookup"><span data-stu-id="ef97d-108">If the specified command queue doesn't support timestamps (see the table in the [Queries](queries.md) section), then this API fails (and returns **E_FAIL**).</span></span> <span data-ttu-id="ef97d-109">[**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) et [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) prennent toujours en charge les horodateurs.</span><span class="sxs-lookup"><span data-stu-id="ef97d-109">[**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) and [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) always support timestamps.</span></span> <span data-ttu-id="ef97d-110">[**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) prend éventuellement en charge les horodatages si le membre [**D3D12_FEATURE_DATA_D3D12_OPTIONS3 :: CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="ef97d-110">[**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) optionally supports timestamps if the [**D3D12_FEATURE_DATA_D3D12_OPTIONS3::CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) member is **TRUE**.</span></span>

## <a name="timestamp-calibration"></a><span data-ttu-id="ef97d-111">Étalonnage de l’horodateur</span><span class="sxs-lookup"><span data-stu-id="ef97d-111">Timestamp calibration</span></span>

<span data-ttu-id="ef97d-112">D3D12 permet aux applications de mettre en corrélation les résultats obtenus à partir des requêtes d’horodatage avec les résultats obtenus lors de l’appel de `QueryPerformanceCounter` .</span><span class="sxs-lookup"><span data-stu-id="ef97d-112">D3D12 enables applications to correlate results obtained from timestamp queries with results obtained from calling `QueryPerformanceCounter`.</span></span> <span data-ttu-id="ef97d-113">Cette option est activée par l’appel de [**ID3D12CommandQueue :: GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration).</span><span class="sxs-lookup"><span data-stu-id="ef97d-113">This is enabled by the call [**ID3D12CommandQueue::GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration).</span></span>

<span data-ttu-id="ef97d-114">[**GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration) échantillonne le compteur d’horodatage GPU pour une file d’attente de commandes donnée et échantillonne le compteur UC `QueryPerformanceCounter` à presque en même temps.</span><span class="sxs-lookup"><span data-stu-id="ef97d-114">[**GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration) samples the GPU timestamp counter for a given command queue and samples the CPU counter via `QueryPerformanceCounter` at nearly the same time.</span></span> <span data-ttu-id="ef97d-115">Là encore, cette API échoue (en renvoyant E \_ Fail) si la file d’attente de commandes spécifiée ne prend pas en charge les horodateurs (voir le tableau dans la rubrique [requêtes](queries.md) ).</span><span class="sxs-lookup"><span data-stu-id="ef97d-115">Again this API fails (returning E\_FAIL) if the specified command queue does not support timestamps (see the table in the [Queries](queries.md) topic).</span></span>

<span data-ttu-id="ef97d-116">Notez que les compteurs du GPU et de l’horodateur de l’UC ne sont pas nécessairement directement liés à la fréquence d’horloge de ces processeurs, mais qu’ils fonctionnent à la place des graduations d’horodatage.</span><span class="sxs-lookup"><span data-stu-id="ef97d-116">Note that GPU and CPU timestamp counters are not necessarily directly related to the clock speed of these processors, but instead work from timestamp ticks.</span></span>

## <a name="timestamp-queries"></a><span data-ttu-id="ef97d-117">Requêtes d’horodatage</span><span class="sxs-lookup"><span data-stu-id="ef97d-117">Timestamp queries</span></span>

<span data-ttu-id="ef97d-118">Vous pouvez obtenir des horodateurs dans le cadre d’une liste de commandes (au lieu d’un appel côté processeur sur une file d’attente de commandes) via des requêtes d’horodatage.</span><span class="sxs-lookup"><span data-stu-id="ef97d-118">You can obtain timestamps as part of a command list (rather than a CPU-side call on a command queue) via timestamp queries.</span></span> <span data-ttu-id="ef97d-119">(Pour plus d’informations sur les requêtes, consultez [requêtes](queries.md) en général).</span><span class="sxs-lookup"><span data-stu-id="ef97d-119">(See [Queries](queries.md) for more information about queries in general).</span></span> 

<span data-ttu-id="ef97d-120">Toutes les requêtes d’horodatage utilisent le type [**D3D12_QUERY_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type) pour la requête réelle.</span><span class="sxs-lookup"><span data-stu-id="ef97d-120">All timestamp queries use the type [**D3D12_QUERY_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type) for the actual query.</span></span> <span data-ttu-id="ef97d-121">Toutefois, en raison des limitations matérielles, [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) et [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) utiliser un [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type) différent de celui utilisé par [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) .</span><span class="sxs-lookup"><span data-stu-id="ef97d-121">However, due to hardware limitations, [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) and [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) use a different [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type) from the one that [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) uses.</span></span>

<span data-ttu-id="ef97d-122">Les files d’attente de calcul et direct utilisent [**D3D12_QUERY_HEAP_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span><span class="sxs-lookup"><span data-stu-id="ef97d-122">Direct and compute queues use [**D3D12_QUERY_HEAP_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span></span>

<span data-ttu-id="ef97d-123">Les files d’attente de copie utilisent [**D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span><span class="sxs-lookup"><span data-stu-id="ef97d-123">Copy queues use [**D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span></span>

<span data-ttu-id="ef97d-124">Les requêtes de file d’attente de copie sont prises en charge uniquement si le membre [**D3D12_FEATURE_DATA_D3D12_OPTIONS3 :: CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="ef97d-124">Copy queue queries are supported only if the [**D3D12_FEATURE_DATA_D3D12_OPTIONS3::CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) member is **TRUE**.</span></span>

<span data-ttu-id="ef97d-125">Les requêtes d’horodatage, une fois résolues via [**ID3D12GraphicsCommandList :: ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), sont des **uint64s** qui représentent des graduations, telles qu’elles sont retournées par [**ID3D12CommandQueue :: GetClockCalibration**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)et, par conséquent, elles doivent être divisées par la fréquence de la file d’attente pour obtenir la longueur en secondes.</span><span class="sxs-lookup"><span data-stu-id="ef97d-125">Timestamp queries, once resolved via [**ID3D12GraphicsCommandList::ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), are a **UINT64** that represents ticks, as is returned by [**ID3D12CommandQueue::GetClockCalibration**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration), and as such it must be divided by the queue frequency to get the length in seconds.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ef97d-126">Pour plus de précision, utilisez l’arithmétique à virgule flottante lors du calcul des intervalles de seconde ou de milliseconde des horodateurs.</span><span class="sxs-lookup"><span data-stu-id="ef97d-126">For accuracy, use floating-point arithmetic when calculating second or millisecond intervals of timestamps.</span></span> <span data-ttu-id="ef97d-127">Par exemple, utilisez `queriedTicks / (double)Frequency` au lieu de `queriedTicks / Frequency`.</span><span class="sxs-lookup"><span data-stu-id="ef97d-127">For example, use `queriedTicks / (double)Frequency` instead of `queriedTicks / Frequency`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef97d-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ef97d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef97d-129">Compteurs et requêtes</span><span class="sxs-lookup"><span data-stu-id="ef97d-129">Counters and Queries</span></span>](counters-and-queries.md)
</dt> <dt>

[<span data-ttu-id="ef97d-130">**ID3D12Device::SetStablePowerState**</span><span class="sxs-lookup"><span data-stu-id="ef97d-130">**ID3D12Device::SetStablePowerState**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
</dt> <dt>

[<span data-ttu-id="ef97d-131">**ID3D12Object :: SetName**</span><span class="sxs-lookup"><span data-stu-id="ef97d-131">**ID3D12Object::SetName**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname)
</dt> <dt>

[<span data-ttu-id="ef97d-132">**ID3DUserDefinedAnnotation**</span><span class="sxs-lookup"><span data-stu-id="ef97d-132">**ID3DUserDefinedAnnotation**</span></span>](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation)
</dt> <dt>

[<span data-ttu-id="ef97d-133">Mesure des performances</span><span class="sxs-lookup"><span data-stu-id="ef97d-133">Performance Measurement</span></span>](performance-measurement.md)
</dt> </dl>
