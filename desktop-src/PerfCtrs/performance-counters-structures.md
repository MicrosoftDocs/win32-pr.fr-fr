---
description: Vous utilisez les structures suivantes lorsque vous travaillez avec des données de performances.
ms.assetid: 97118b64-3a2f-49c0-92e7-324df08bdb12
title: Structures des compteurs de performance
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 0629aa1763f08dfce9e2cc646bd1b5744d6591cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951997"
---
# <a name="performance-counters-structures"></a><span data-ttu-id="35a54-103">Structures des compteurs de performance</span><span class="sxs-lookup"><span data-stu-id="35a54-103">Performance Counters Structures</span></span>

<span data-ttu-id="35a54-104">Vous utilisez les structures suivantes lorsque vous travaillez avec des données de performances.</span><span class="sxs-lookup"><span data-stu-id="35a54-104">You use the following structures when working with performance data.</span></span>

<span data-ttu-id="35a54-105">Pour plus d’informations sur les fonctions qui sont disponibles pour l’utilisation des compteurs de performance, consultez [fonctions des compteurs de performances](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="35a54-105">For information about the functions that are available for working with performance counters, see [Performance Counters Functions](performance-counters-functions.md).</span></span>

## <a name="performance-data-helper-pdh-structures"></a><span data-ttu-id="35a54-106">Structures d’assistance des données de performance (PDH)</span><span class="sxs-lookup"><span data-stu-id="35a54-106">Performance Data Helper (PDH) structures</span></span>

<span data-ttu-id="35a54-107">Les consommateurs qui utilisent les fonctions [d’assistance des données de performance (PDH)](using-the-pdh-functions-to-consume-counter-data.md) utilisent les structures suivantes :</span><span class="sxs-lookup"><span data-stu-id="35a54-107">Consumers that use the [Performance Data Helper (PDH)](using-the-pdh-functions-to-consume-counter-data.md) functions use the following structures:</span></span>

- [<span data-ttu-id="35a54-108">**PDH \_ Parcourir \_ DLG \_ config**</span><span class="sxs-lookup"><span data-stu-id="35a54-108">**PDH\_BROWSE\_DLG\_CONFIG**</span></span>](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a)
- [<span data-ttu-id="35a54-109">**PDH \_ Parcourir \_ DLG \_ config \_ H**</span><span class="sxs-lookup"><span data-stu-id="35a54-109">**PDH\_BROWSE\_DLG\_CONFIG\_H**</span></span>](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_ha)
- [<span data-ttu-id="35a54-110">**\_informations sur le compteur PDH \_**</span><span class="sxs-lookup"><span data-stu-id="35a54-110">**PDH\_COUNTER\_INFO**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_info_a)
- [<span data-ttu-id="35a54-111">**\_éléments du \_ chemin d’accès au compteur PDH \_**</span><span class="sxs-lookup"><span data-stu-id="35a54-111">**PDH\_COUNTER\_PATH\_ELEMENTS**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a)
- [<span data-ttu-id="35a54-112">**\_éléments du \_ \_ chemin d' \_ accès de l’élément de données PDH**</span><span class="sxs-lookup"><span data-stu-id="35a54-112">**PDH\_DATA\_ITEM\_PATH\_ELEMENTS**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_data_item_path_elements_a)
- [<span data-ttu-id="35a54-113">**PDH \_ fmt \_ COUNTERVALUE**</span><span class="sxs-lookup"><span data-stu-id="35a54-113">**PDH\_FMT\_COUNTERVALUE**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue)
- [<span data-ttu-id="35a54-114">**\_ \_ élément COUNTERVALUE de la fmt PDH \_**</span><span class="sxs-lookup"><span data-stu-id="35a54-114">**PDH\_FMT\_COUNTERVALUE\_ITEM**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue_item_a)
- [<span data-ttu-id="35a54-115">**\_compteur brut \_ PDH**</span><span class="sxs-lookup"><span data-stu-id="35a54-115">**PDH\_RAW\_COUNTER**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)
- [<span data-ttu-id="35a54-116">**\_élément de \_ compteur \_ brut PDH**</span><span class="sxs-lookup"><span data-stu-id="35a54-116">**PDH\_RAW\_COUNTER\_ITEM**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter_item_a)
- [<span data-ttu-id="35a54-117">**\_enregistrement de \_ journal \_ brut PDH**</span><span class="sxs-lookup"><span data-stu-id="35a54-117">**PDH\_RAW\_LOG\_RECORD**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_log_record)
- [<span data-ttu-id="35a54-118">**\_statistiques PDH**</span><span class="sxs-lookup"><span data-stu-id="35a54-118">**PDH\_STATISTICS**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_statistics)
- [<span data-ttu-id="35a54-119">**\_informations de temps PDH \_**</span><span class="sxs-lookup"><span data-stu-id="35a54-119">**PDH\_TIME\_INFO**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info)

## <a name="perflib-v2-consumer-structures"></a><span data-ttu-id="35a54-120">Structures de consommateur PerfLib v2</span><span class="sxs-lookup"><span data-stu-id="35a54-120">PerfLib V2 Consumer structures</span></span>

<span data-ttu-id="35a54-121">Les consommateurs qui utilisent les fonctions de [consommateur de Perflib v2](using-the-perflib-functions-to-consume-counter-data.md) utilisent les structures suivantes :</span><span class="sxs-lookup"><span data-stu-id="35a54-121">Consumers that use the [PerfLib V2 Consumer](using-the-perflib-functions-to-consume-counter-data.md) functions use the following structures:</span></span>

- [<span data-ttu-id="35a54-122">**\_données du compteur de performances \_**</span><span class="sxs-lookup"><span data-stu-id="35a54-122">**PERF\_COUNTER\_DATA**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_data)
- [<span data-ttu-id="35a54-123">**\_ \_ en-tête de compteur de performances**</span><span class="sxs-lookup"><span data-stu-id="35a54-123">**PERF\_COUNTER\_HEADER**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_header)
- [<span data-ttu-id="35a54-124">**\_identificateur du compteur de performances \_**</span><span class="sxs-lookup"><span data-stu-id="35a54-124">**PERF\_COUNTER\_IDENTIFIER**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identifier)
- [<span data-ttu-id="35a54-125">**\_informations de \_ Registre du compteur de performances \_**</span><span class="sxs-lookup"><span data-stu-id="35a54-125">**PERF\_COUNTER\_REG\_INFO**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_reg_info)
- [<span data-ttu-id="35a54-126">**\_ \_ informations sur le registre de performance COUNTERSET \_**</span><span class="sxs-lookup"><span data-stu-id="35a54-126">**PERF\_COUNTERSET\_REG\_INFO**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_reg_info)
- [<span data-ttu-id="35a54-127">**\_ \_ en-tête de données perf**</span><span class="sxs-lookup"><span data-stu-id="35a54-127">**PERF\_DATA\_HEADER**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_data_header)
- [<span data-ttu-id="35a54-128">**\_ \_ en-tête d’instance perf**</span><span class="sxs-lookup"><span data-stu-id="35a54-128">**PERF\_INSTANCE\_HEADER**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_instance_header)
- [<span data-ttu-id="35a54-129">**\_compteurs multiples de performances \_**</span><span class="sxs-lookup"><span data-stu-id="35a54-129">**PERF\_MULTI\_COUNTERS**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_multi_counters)
- [<span data-ttu-id="35a54-130">**\_instances multiples \_ perf**</span><span class="sxs-lookup"><span data-stu-id="35a54-130">**PERF\_MULTI\_INSTANCES**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_multi_instances)
- [<span data-ttu-id="35a54-131">**\_ \_ en-tête de mémoire tampon de chaîne perf \_**</span><span class="sxs-lookup"><span data-stu-id="35a54-131">**PERF\_STRING\_BUFFER\_HEADER**</span></span>](/windows/win32/api/perflib/ns-perflib-perf_string_buffer_header)
- [<span data-ttu-id="35a54-132">**\_ \_ en-tête de compteur de chaîne perf \_**</span><span class="sxs-lookup"><span data-stu-id="35a54-132">**PERF\_STRING\_COUNTER\_HEADER**</span></span>](/windows/win32/api/perflib/ns-perflib-perf_string_counter_header)

## <a name="perflib-v2-provider-structures"></a><span data-ttu-id="35a54-133">Structures du fournisseur PerfLib v2</span><span class="sxs-lookup"><span data-stu-id="35a54-133">PerfLib V2 Provider structures</span></span>

<span data-ttu-id="35a54-134">Les [fournisseurs de données de performances v2](providing-counter-data-using-version-2-0.md) utilisent les structures suivantes :</span><span class="sxs-lookup"><span data-stu-id="35a54-134">[V2 performance data providers](providing-counter-data-using-version-2-0.md) use the following structures:</span></span>

- [<span data-ttu-id="35a54-135">**\_identité du compteur de performances \_**</span><span class="sxs-lookup"><span data-stu-id="35a54-135">**PERF\_COUNTER\_IDENTITY**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [<span data-ttu-id="35a54-136">**\_informations sur le compteur de performances \_**</span><span class="sxs-lookup"><span data-stu-id="35a54-136">**PERF\_COUNTER\_INFO**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [<span data-ttu-id="35a54-137">**\_informations du COUNTERSET de performance \_**</span><span class="sxs-lookup"><span data-stu-id="35a54-137">**PERF\_COUNTERSET\_INFO**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [<span data-ttu-id="35a54-138">**\_instance du COUNTERSET de performance \_**</span><span class="sxs-lookup"><span data-stu-id="35a54-138">**PERF\_COUNTERSET\_INSTANCE**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)
- [<span data-ttu-id="35a54-139">**\_contexte du fournisseur de performances \_**</span><span class="sxs-lookup"><span data-stu-id="35a54-139">**PERF\_PROVIDER\_CONTEXT**</span></span>](/windows/win32/api/perflib/ns-perflib-perf_provider_context)

## <a name="performance-dll-structures"></a><span data-ttu-id="35a54-140">Structures de DLL de performance</span><span class="sxs-lookup"><span data-stu-id="35a54-140">Performance DLL structures</span></span>

<span data-ttu-id="35a54-141">Les [fournisseurs de DLL d’extension de performance](providing-counter-data-using-a-performance-dll.md) et les [consommateurs qui utilisent les fonctions de Registre pour consommer des données de compteur](using-the-registry-functions-to-consume-counter-data.md) utilisent les structures suivantes :</span><span class="sxs-lookup"><span data-stu-id="35a54-141">[Performance extension DLL providers](providing-counter-data-using-a-performance-dll.md) and [consumers that use the registry functions to consume counter data](using-the-registry-functions-to-consume-counter-data.md) use the following structures:</span></span>

- [<span data-ttu-id="35a54-142">**\_bloc de compteur de performances \_**</span><span class="sxs-lookup"><span data-stu-id="35a54-142">**PERF\_COUNTER\_BLOCK**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block)
- [<span data-ttu-id="35a54-143">**\_définition du compteur de performances \_**</span><span class="sxs-lookup"><span data-stu-id="35a54-143">**PERF\_COUNTER\_DEFINITION**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition)
- [<span data-ttu-id="35a54-144">**\_bloc de données perf \_**</span><span class="sxs-lookup"><span data-stu-id="35a54-144">**PERF\_DATA\_BLOCK**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_data_block)
- [<span data-ttu-id="35a54-145">**définition de l' \_ instance perf \_**</span><span class="sxs-lookup"><span data-stu-id="35a54-145">**PERF\_INSTANCE\_DEFINITION**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition)
- [<span data-ttu-id="35a54-146">**\_type d’objet perf \_**</span><span class="sxs-lookup"><span data-stu-id="35a54-146">**PERF\_OBJECT\_TYPE**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_object_type)
