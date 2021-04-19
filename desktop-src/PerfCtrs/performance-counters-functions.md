---
description: Utilisez les fonctions suivantes pour consommer et fournir des données de performances.
ms.assetid: a2c97b8b-b1b1-4dd8-8f23-edffaa74d028
title: Fonctions des compteurs de performance
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 8ef01ac07ae8507f1005839ab838e2528e76d6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106540863"
---
# <a name="performance-counters-functions"></a><span data-ttu-id="b311c-103">Fonctions des compteurs de performance</span><span class="sxs-lookup"><span data-stu-id="b311c-103">Performance Counters Functions</span></span>

<span data-ttu-id="b311c-104">Utilisez les fonctions suivantes pour consommer et fournir des données de performances.</span><span class="sxs-lookup"><span data-stu-id="b311c-104">Use the following functions to consume and provide performance data.</span></span>

## <a name="consumer-functions"></a><span data-ttu-id="b311c-105">Fonctions de consommateur</span><span class="sxs-lookup"><span data-stu-id="b311c-105">Consumer functions</span></span>

### <a name="performance-data-helper-pdh-functions"></a><span data-ttu-id="b311c-106">Fonctions d’assistance des données de performance (PDH)</span><span class="sxs-lookup"><span data-stu-id="b311c-106">Performance Data Helper (PDH) functions</span></span>

<span data-ttu-id="b311c-107">Utilisez les fonctions d’assistance des données de performance (PDH) pour consommer les données de performances des fournisseurs de données de performances v1 et v2.</span><span class="sxs-lookup"><span data-stu-id="b311c-107">Use the Performance Data Helper (PDH) functions to consume performance data from both V1 and V2 performance data providers.</span></span>

> [!Note]
> <span data-ttu-id="b311c-108">Les applications Windows OneCore ne peuvent pas utiliser les fonctions PDH.</span><span class="sxs-lookup"><span data-stu-id="b311c-108">Windows OneCore apps cannot use the PDH functions.</span></span> <span data-ttu-id="b311c-109">Si vous écrivez des applications OneCore Windows, utilisez les [fonctions de consommateur de Perflib v2](using-the-perflib-functions-to-consume-counter-data.md).</span><span class="sxs-lookup"><span data-stu-id="b311c-109">If you are writing Windows OneCore apps, use [PerfLib V2 Consumer functions](using-the-perflib-functions-to-consume-counter-data.md).</span></span>

- [<span data-ttu-id="b311c-110">*CounterPathCallBack*</span><span class="sxs-lookup"><span data-stu-id="b311c-110">*CounterPathCallBack*</span></span>](/windows/desktop/api/Pdh/nc-pdh-counterpathcallback)
- [<span data-ttu-id="b311c-111">**PdhAddCounter**</span><span class="sxs-lookup"><span data-stu-id="b311c-111">**PdhAddCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera)
- [<span data-ttu-id="b311c-112">**PdhAddEnglishCounter**</span><span class="sxs-lookup"><span data-stu-id="b311c-112">**PdhAddEnglishCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhaddenglishcountera)
- [<span data-ttu-id="b311c-113">**PdhBindInputDataSource**</span><span class="sxs-lookup"><span data-stu-id="b311c-113">**PdhBindInputDataSource**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea)
- [<span data-ttu-id="b311c-114">**PdhBrowseCounters**</span><span class="sxs-lookup"><span data-stu-id="b311c-114">**PdhBrowseCounters**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa)
- [<span data-ttu-id="b311c-115">**PdhBrowseCountersH**</span><span class="sxs-lookup"><span data-stu-id="b311c-115">**PdhBrowseCountersH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersha)
- [<span data-ttu-id="b311c-116">**PdhCalculateCounterFromRawValue**</span><span class="sxs-lookup"><span data-stu-id="b311c-116">**PdhCalculateCounterFromRawValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcalculatecounterfromrawvalue)
- [<span data-ttu-id="b311c-117">**PdhCloseLog**</span><span class="sxs-lookup"><span data-stu-id="b311c-117">**PdhCloseLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcloselog)
- [<span data-ttu-id="b311c-118">**PdhCloseQuery**</span><span class="sxs-lookup"><span data-stu-id="b311c-118">**PdhCloseQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [<span data-ttu-id="b311c-119">**PdhCollectQueryData**</span><span class="sxs-lookup"><span data-stu-id="b311c-119">**PdhCollectQueryData**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [<span data-ttu-id="b311c-120">**PdhCollectQueryDataEx**</span><span class="sxs-lookup"><span data-stu-id="b311c-120">**PdhCollectQueryDataEx**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydataex)
- [<span data-ttu-id="b311c-121">**PdhCollectQueryDataWithTime**</span><span class="sxs-lookup"><span data-stu-id="b311c-121">**PdhCollectQueryDataWithTime**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydatawithtime)
- [<span data-ttu-id="b311c-122">**PdhComputeCounterStatistics**</span><span class="sxs-lookup"><span data-stu-id="b311c-122">**PdhComputeCounterStatistics**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics)
- [<span data-ttu-id="b311c-123">**PdhConnectMachine**</span><span class="sxs-lookup"><span data-stu-id="b311c-123">**PdhConnectMachine**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhconnectmachinea)
- [<span data-ttu-id="b311c-124">**PdhEnumLogSetNames**</span><span class="sxs-lookup"><span data-stu-id="b311c-124">**PdhEnumLogSetNames**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumlogsetnamesa)
- [<span data-ttu-id="b311c-125">**PdhEnumMachines**</span><span class="sxs-lookup"><span data-stu-id="b311c-125">**PdhEnumMachines**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenummachinesa)
- [<span data-ttu-id="b311c-126">**PdhEnumMachinesH**</span><span class="sxs-lookup"><span data-stu-id="b311c-126">**PdhEnumMachinesH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenummachinesha)
- [<span data-ttu-id="b311c-127">**PdhEnumObjectItems**</span><span class="sxs-lookup"><span data-stu-id="b311c-127">**PdhEnumObjectItems**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa)
- [<span data-ttu-id="b311c-128">**PdhEnumObjectItemsH**</span><span class="sxs-lookup"><span data-stu-id="b311c-128">**PdhEnumObjectItemsH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsha)
- [<span data-ttu-id="b311c-129">**PdhEnumObjects**</span><span class="sxs-lookup"><span data-stu-id="b311c-129">**PdhEnumObjects**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa)
- [<span data-ttu-id="b311c-130">**PdhEnumObjectsH**</span><span class="sxs-lookup"><span data-stu-id="b311c-130">**PdhEnumObjectsH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsha)
- [<span data-ttu-id="b311c-131">**PdhExpandCounterPath**</span><span class="sxs-lookup"><span data-stu-id="b311c-131">**PdhExpandCounterPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhexpandcounterpatha)
- [<span data-ttu-id="b311c-132">**PdhExpandWildCardPath**</span><span class="sxs-lookup"><span data-stu-id="b311c-132">**PdhExpandWildCardPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha)
- [<span data-ttu-id="b311c-133">**PdhExpandWildCardPathH**</span><span class="sxs-lookup"><span data-stu-id="b311c-133">**PdhExpandWildCardPathH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpathha)
- [<span data-ttu-id="b311c-134">**PdhFormatFromRawValue**</span><span class="sxs-lookup"><span data-stu-id="b311c-134">**PdhFormatFromRawValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhformatfromrawvalue)
- [<span data-ttu-id="b311c-135">**PdhGetCounterInfo**</span><span class="sxs-lookup"><span data-stu-id="b311c-135">**PdhGetCounterInfo**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetcounterinfoa)
- [<span data-ttu-id="b311c-136">**PdhGetCounterTimeBase**</span><span class="sxs-lookup"><span data-stu-id="b311c-136">**PdhGetCounterTimeBase**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetcountertimebase)
- [<span data-ttu-id="b311c-137">**PdhGetDataSourceTimeRange**</span><span class="sxs-lookup"><span data-stu-id="b311c-137">**PdhGetDataSourceTimeRange**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea)
- [<span data-ttu-id="b311c-138">**PdhGetDataSourceTimeRangeH**</span><span class="sxs-lookup"><span data-stu-id="b311c-138">**PdhGetDataSourceTimeRangeH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangeh)
- [<span data-ttu-id="b311c-139">**PdhGetDefaultPerfCounter**</span><span class="sxs-lookup"><span data-stu-id="b311c-139">**PdhGetDefaultPerfCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfcountera)
- [<span data-ttu-id="b311c-140">**PdhGetDefaultPerfCounterH**</span><span class="sxs-lookup"><span data-stu-id="b311c-140">**PdhGetDefaultPerfCounterH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfcounterha)
- [<span data-ttu-id="b311c-141">**PdhGetDefaultPerfObject**</span><span class="sxs-lookup"><span data-stu-id="b311c-141">**PdhGetDefaultPerfObject**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfobjecta)
- [<span data-ttu-id="b311c-142">**PdhGetDefaultPerfObjectH**</span><span class="sxs-lookup"><span data-stu-id="b311c-142">**PdhGetDefaultPerfObjectH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfobjectha)
- [<span data-ttu-id="b311c-143">**PdhGetDllVersion**</span><span class="sxs-lookup"><span data-stu-id="b311c-143">**PdhGetDllVersion**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdllversion)
- [<span data-ttu-id="b311c-144">**PdhGetFormattedCounterArray**</span><span class="sxs-lookup"><span data-stu-id="b311c-144">**PdhGetFormattedCounterArray**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcounterarraya)
- [<span data-ttu-id="b311c-145">**PdhGetFormattedCounterValue**</span><span class="sxs-lookup"><span data-stu-id="b311c-145">**PdhGetFormattedCounterValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue)
- [<span data-ttu-id="b311c-146">**PdhGetLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="b311c-146">**PdhGetLogFileSize**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
- [<span data-ttu-id="b311c-147">**PdhGetRawCounterArray**</span><span class="sxs-lookup"><span data-stu-id="b311c-147">**PdhGetRawCounterArray**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcounterarraya)
- [<span data-ttu-id="b311c-148">**PdhGetRawCounterValue**</span><span class="sxs-lookup"><span data-stu-id="b311c-148">**PdhGetRawCounterValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue)
- [<span data-ttu-id="b311c-149">**PdhIsRealTimeQuery**</span><span class="sxs-lookup"><span data-stu-id="b311c-149">**PdhIsRealTimeQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhisrealtimequery)
- [<span data-ttu-id="b311c-150">**PdhLookupPerfIndexByName**</span><span class="sxs-lookup"><span data-stu-id="b311c-150">**PdhLookupPerfIndexByName**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhlookupperfindexbynamea)
- [<span data-ttu-id="b311c-151">**PdhLookupPerfNameByIndex**</span><span class="sxs-lookup"><span data-stu-id="b311c-151">**PdhLookupPerfNameByIndex**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhlookupperfnamebyindexa)
- [<span data-ttu-id="b311c-152">**PdhMakeCounterPath**</span><span class="sxs-lookup"><span data-stu-id="b311c-152">**PdhMakeCounterPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhmakecounterpatha)
- [<span data-ttu-id="b311c-153">**PdhOpenLog**</span><span class="sxs-lookup"><span data-stu-id="b311c-153">**PdhOpenLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
- [<span data-ttu-id="b311c-154">**PdhOpenQuery**</span><span class="sxs-lookup"><span data-stu-id="b311c-154">**PdhOpenQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya)
- [<span data-ttu-id="b311c-155">**PdhOpenQueryH**</span><span class="sxs-lookup"><span data-stu-id="b311c-155">**PdhOpenQueryH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenqueryh)
- [<span data-ttu-id="b311c-156">**PdhParseCounterPath**</span><span class="sxs-lookup"><span data-stu-id="b311c-156">**PdhParseCounterPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha)
- [<span data-ttu-id="b311c-157">**PdhParseInstanceName**</span><span class="sxs-lookup"><span data-stu-id="b311c-157">**PdhParseInstanceName**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea)
- [<span data-ttu-id="b311c-158">**PdhReadRawLogRecord**</span><span class="sxs-lookup"><span data-stu-id="b311c-158">**PdhReadRawLogRecord**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhreadrawlogrecord)
- [<span data-ttu-id="b311c-159">**PdhRemoveCounter**</span><span class="sxs-lookup"><span data-stu-id="b311c-159">**PdhRemoveCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [<span data-ttu-id="b311c-160">**PdhSelectDataSource**</span><span class="sxs-lookup"><span data-stu-id="b311c-160">**PdhSelectDataSource**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhselectdatasourcea)
- [<span data-ttu-id="b311c-161">**PdhSetCounterScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="b311c-161">**PdhSetCounterScaleFactor**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhsetcounterscalefactor)
- [<span data-ttu-id="b311c-162">**PdhSetDefaultRealTimeDataSource**</span><span class="sxs-lookup"><span data-stu-id="b311c-162">**PdhSetDefaultRealTimeDataSource**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhsetdefaultrealtimedatasource)
- [<span data-ttu-id="b311c-163">**PdhSetQueryTimeRange**</span><span class="sxs-lookup"><span data-stu-id="b311c-163">**PdhSetQueryTimeRange**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange)
- [<span data-ttu-id="b311c-164">**PdhUpdateLog**</span><span class="sxs-lookup"><span data-stu-id="b311c-164">**PdhUpdateLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
- [<span data-ttu-id="b311c-165">**PdhUpdateLogFileCatalog**</span><span class="sxs-lookup"><span data-stu-id="b311c-165">**PdhUpdateLogFileCatalog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhupdatelogfilecatalog)
- [<span data-ttu-id="b311c-166">**PdhValidatePath**</span><span class="sxs-lookup"><span data-stu-id="b311c-166">**PdhValidatePath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha)
- [<span data-ttu-id="b311c-167">**PdhValidatePathEx**</span><span class="sxs-lookup"><span data-stu-id="b311c-167">**PdhValidatePathEx**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepathexa)

### <a name="perflib-v2-consumer-functions"></a><span data-ttu-id="b311c-168">Fonctions de consommateur de PerfLib v2</span><span class="sxs-lookup"><span data-stu-id="b311c-168">PerfLib V2 Consumer functions</span></span>

<span data-ttu-id="b311c-169">Utilisez les fonctions de consommateur de PerfLib v2 pour consommer les données de performances des fournisseurs de données de performances v2 si vous ne pouvez pas utiliser les fonctions d’assistance des données de performance (PDH).</span><span class="sxs-lookup"><span data-stu-id="b311c-169">Use the PerfLib V2 Consumer functions to consume performance data from V2 performance data providers if you cannot use the Performance Data Helper (PDH) functions.</span></span> <span data-ttu-id="b311c-170">Ces fonctions peuvent être utilisées lors de l’écriture d’applications OneCore pour collecter des countersets v2 ou lorsque vous devez collecter des countersets v2 spécifiques avec des dépendances et une surcharge minimales.</span><span class="sxs-lookup"><span data-stu-id="b311c-170">These functions might be used when writing OneCore applications to collect V2 countersets or when you need to collect specific V2 countersets with minimal dependencies and overhead.</span></span>

> [!TIP]
> <span data-ttu-id="b311c-171">Les fonctions de consommateur de PerfLib v2 sont plus difficiles à utiliser que les fonctions de performance Data Helper (PDH) et ne prennent en charge que la collecte de données à partir de fournisseurs v2.</span><span class="sxs-lookup"><span data-stu-id="b311c-171">The PerfLib V2 Consumer functions are harder to use than the Performance Data Helper (PDH) functions and only support collecting data from V2 providers.</span></span> <span data-ttu-id="b311c-172">Les fonctions PDH doivent être préférées pour la plupart des applications.</span><span class="sxs-lookup"><span data-stu-id="b311c-172">The PDH functions should be preferred for most applications.</span></span>

- [<span data-ttu-id="b311c-173">**PerfAddCounters**</span><span class="sxs-lookup"><span data-stu-id="b311c-173">**PerfAddCounters**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfaddcounters)
- [<span data-ttu-id="b311c-174">**PerfCloseQueryHandle**</span><span class="sxs-lookup"><span data-stu-id="b311c-174">**PerfCloseQueryHandle**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfclosequeryhandle)
- [<span data-ttu-id="b311c-175">**PerfDeleteCounters**</span><span class="sxs-lookup"><span data-stu-id="b311c-175">**PerfDeleteCounters**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdeletecounters)
- [<span data-ttu-id="b311c-176">**PerfEnumerateCounterSet**</span><span class="sxs-lookup"><span data-stu-id="b311c-176">**PerfEnumerateCounterSet**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecounterset)
- [<span data-ttu-id="b311c-177">**PerfEnumerateCounterSetInstances**</span><span class="sxs-lookup"><span data-stu-id="b311c-177">**PerfEnumerateCounterSetInstances**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecountersetinstances)
- [<span data-ttu-id="b311c-178">**PerfOpenQueryHandle**</span><span class="sxs-lookup"><span data-stu-id="b311c-178">**PerfOpenQueryHandle**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfopenqueryhandle)
- [<span data-ttu-id="b311c-179">**PerfQueryCounterData**</span><span class="sxs-lookup"><span data-stu-id="b311c-179">**PerfQueryCounterData**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterdata)
- [<span data-ttu-id="b311c-180">**PerfQueryCounterInfo**</span><span class="sxs-lookup"><span data-stu-id="b311c-180">**PerfQueryCounterInfo**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterinfo)
- [<span data-ttu-id="b311c-181">**PerfQueryCounterSetRegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="b311c-181">**PerfQueryCounterSetRegistrationInfo**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfquerycountersetregistrationinfo)

## <a name="provider-functions"></a><span data-ttu-id="b311c-182">Fonctions du fournisseur</span><span class="sxs-lookup"><span data-stu-id="b311c-182">Provider functions</span></span>

### <a name="perflib-v2-provider-functions"></a><span data-ttu-id="b311c-183">Fonctions du fournisseur PerfLib v2</span><span class="sxs-lookup"><span data-stu-id="b311c-183">PerfLib V2 Provider functions</span></span>

<span data-ttu-id="b311c-184">Les [fournisseurs de données de performances v2](providing-counter-data-using-version-2-0.md) utilisent les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="b311c-184">[V2 performance data providers](providing-counter-data-using-version-2-0.md) use the following functions:</span></span>

- [<span data-ttu-id="b311c-185">*AllocateMemory*</span><span class="sxs-lookup"><span data-stu-id="b311c-185">*AllocateMemory*</span></span>](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)
- [<span data-ttu-id="b311c-186">*ControlCallback*</span><span class="sxs-lookup"><span data-stu-id="b311c-186">*ControlCallback*</span></span>](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [<span data-ttu-id="b311c-187">**CounterCleanup**</span><span class="sxs-lookup"><span data-stu-id="b311c-187">**CounterCleanup**</span></span>](countercleanup.md)
- [<span data-ttu-id="b311c-188">**CounterInitialize**</span><span class="sxs-lookup"><span data-stu-id="b311c-188">**CounterInitialize**</span></span>](counterinitialize.md)
- [<span data-ttu-id="b311c-189">*FreeMemory*</span><span class="sxs-lookup"><span data-stu-id="b311c-189">*FreeMemory*</span></span>](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free)
- [<span data-ttu-id="b311c-190">**PerfCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="b311c-190">**PerfCreateInstance**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [<span data-ttu-id="b311c-191">**PerfDecrementULongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="b311c-191">**PerfDecrementULongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulongcountervalue)
- [<span data-ttu-id="b311c-192">**PerfDecrementULongLongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="b311c-192">**PerfDecrementULongLongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulonglongcountervalue)
- [<span data-ttu-id="b311c-193">**PerfDeleteInstance**</span><span class="sxs-lookup"><span data-stu-id="b311c-193">**PerfDeleteInstance**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [<span data-ttu-id="b311c-194">**PerfIncrementULongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="b311c-194">**PerfIncrementULongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue)
- [<span data-ttu-id="b311c-195">**PerfIncrementULongLongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="b311c-195">**PerfIncrementULongLongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfincrementulonglongcountervalue)
- [<span data-ttu-id="b311c-196">**PerfQueryInstance**</span><span class="sxs-lookup"><span data-stu-id="b311c-196">**PerfQueryInstance**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [<span data-ttu-id="b311c-197">**PerfSetCounterSetInfo**</span><span class="sxs-lookup"><span data-stu-id="b311c-197">**PerfSetCounterSetInfo**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [<span data-ttu-id="b311c-198">**PerfSetULongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="b311c-198">**PerfSetULongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [<span data-ttu-id="b311c-199">**PerfSetULongLongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="b311c-199">**PerfSetULongLongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [<span data-ttu-id="b311c-200">**PerfSetCounterRefValue**</span><span class="sxs-lookup"><span data-stu-id="b311c-200">**PerfSetCounterRefValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [<span data-ttu-id="b311c-201">**PerfStartProvider**</span><span class="sxs-lookup"><span data-stu-id="b311c-201">**PerfStartProvider**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [<span data-ttu-id="b311c-202">**PerfStartProviderEx**</span><span class="sxs-lookup"><span data-stu-id="b311c-202">**PerfStartProviderEx**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstartproviderex)
- [<span data-ttu-id="b311c-203">**PerfStopProvider**</span><span class="sxs-lookup"><span data-stu-id="b311c-203">**PerfStopProvider**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

> [!Note]
> <span data-ttu-id="b311c-204">Pour installer et désinstaller des fournisseurs v2, utilisez les outils **lodctr** et **unlodctr** .</span><span class="sxs-lookup"><span data-stu-id="b311c-204">To install and uninstall V2 providers, use the **lodctr** and **unlodctr** tools.</span></span> <span data-ttu-id="b311c-205">Les fonctions **LoadPerfCounterTextStrings** et **UnloadPerfCounterTextStrings** ne peuvent pas être utilisées pour installer et désinstaller des fournisseurs v2.</span><span class="sxs-lookup"><span data-stu-id="b311c-205">The **LoadPerfCounterTextStrings** and **UnloadPerfCounterTextStrings** functions cannot be used to install and uninstall V2 providers.</span></span>

### <a name="performance-dll-functions"></a><span data-ttu-id="b311c-206">Fonctions de la DLL de performance</span><span class="sxs-lookup"><span data-stu-id="b311c-206">Performance DLL functions</span></span>

<span data-ttu-id="b311c-207">Les [fournisseurs de données de performance v1](providing-counter-data-using-a-performance-dll.md) implémentent une dll qui fournit les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="b311c-207">[V1 performance data providers](providing-counter-data-using-a-performance-dll.md) implement a DLL that provides the following functions:</span></span>

- [<span data-ttu-id="b311c-208">*ClosePerformanceData*</span><span class="sxs-lookup"><span data-stu-id="b311c-208">*ClosePerformanceData*</span></span>](/windows/win32/api/winperf/nc-winperf-pm_close_proc)
- [<span data-ttu-id="b311c-209">*CollectPerformanceData*</span><span class="sxs-lookup"><span data-stu-id="b311c-209">*CollectPerformanceData*</span></span>](/windows/win32/api/winperf/nc-winperf-pm_collect_proc)
- <span data-ttu-id="b311c-210">[*OpenPerformanceData*](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b311c-210">[*OpenPerformanceData*](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))</span></span>

> [!Note]
> <span data-ttu-id="b311c-211">En raison de problèmes de performances et de fiabilité importants, les fournisseurs de données de performances v1 sont déconseillés.</span><span class="sxs-lookup"><span data-stu-id="b311c-211">Due to significant performance and reliability issues, V1 performance data providers are deprecated.</span></span> <span data-ttu-id="b311c-212">Bien que vous puissiez toujours utiliser une DLL d’extension de performance pour fournir des données de compteur, il est recommandé de [créer un fournisseur v2 à la](providing-counter-data-using-version-2-0.md) place.</span><span class="sxs-lookup"><span data-stu-id="b311c-212">Although you still can use a performance extension DLL to provide counter data, you are encouraged to [create a V2 provider](providing-counter-data-using-version-2-0.md) instead.</span></span> <span data-ttu-id="b311c-213">Il est également recommandé de remplacer les fournisseurs v1 existants par des fournisseurs v2.</span><span class="sxs-lookup"><span data-stu-id="b311c-213">You also are encouraged to replace existing V1 providers with V2 providers.</span></span>

<span data-ttu-id="b311c-214">Les fournisseurs v1 peuvent être installés et désinstallés à l’aide des outils **lodctr** et **unlodctr** ou en appelant les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="b311c-214">V1 providers can be installed and uninstalled using the **lodctr** and **unlodctr** tools or by calling the following functions:</span></span>

- [<span data-ttu-id="b311c-215">**LoadPerfCounterTextStrings**</span><span class="sxs-lookup"><span data-stu-id="b311c-215">**LoadPerfCounterTextStrings**</span></span>](/windows/desktop/api/Loadperf/nf-loadperf-loadperfcountertextstringsa)
- [<span data-ttu-id="b311c-216">**UnloadPerfCounterTextStrings**</span><span class="sxs-lookup"><span data-stu-id="b311c-216">**UnloadPerfCounterTextStrings**</span></span>](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa)
