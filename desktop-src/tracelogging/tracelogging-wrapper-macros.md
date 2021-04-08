---
title: Macros Wrapper TraceLogging
description: Répertorie les macros wrapper pour les fournisseurs TraceLogging.
ms.assetid: 806F43F3-D376-4DBD-A4C5-B5F01E5D009D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dc28b3a35074089b1f5c613b041534b8b282423
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675634"
---
# <a name="tracelogging-wrapper-macros"></a><span data-ttu-id="2746d-103">Macros Wrapper TraceLogging</span><span class="sxs-lookup"><span data-stu-id="2746d-103">TraceLogging Wrapper Macros</span></span>

<span data-ttu-id="2746d-104">Répertorie les macros wrapper pour les fournisseurs TraceLogging.</span><span class="sxs-lookup"><span data-stu-id="2746d-104">Lists the wrapper macros for TraceLogging providers.</span></span>

<span data-ttu-id="2746d-105">Pour enregistrer des événements à l’aide des fournisseurs TraceLogging, vous devez utiliser le TraceLogging écrire des macros [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) ou [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity).</span><span class="sxs-lookup"><span data-stu-id="2746d-105">In order to record events using TraceLogging providers, you need to use the TraceLogging write macros [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) or [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity).</span></span> <span data-ttu-id="2746d-106">Ces deux macros vous obligent à encapsuler les données d’événement dans une macro wrapper.</span><span class="sxs-lookup"><span data-stu-id="2746d-106">Both of these macros require you to wrap any event data in a wrapper macro.</span></span> <span data-ttu-id="2746d-107">Il existe plusieurs macros Wrapper différentes pour différents types de données.</span><span class="sxs-lookup"><span data-stu-id="2746d-107">There are several different wrapper macros for different data types.</span></span> <span data-ttu-id="2746d-108">Pour obtenir la liste complète des macros TraceLogging, consultez [macros TraceLogging](trace-logging-macros.md).</span><span class="sxs-lookup"><span data-stu-id="2746d-108">For a complete list of TraceLogging macros, see [TraceLogging Macros](trace-logging-macros.md).</span></span>

<span data-ttu-id="2746d-109">Outre les macros Wrapper ci-dessus, plusieurs macros sont disponibles pour les types de données individuels.</span><span class="sxs-lookup"><span data-stu-id="2746d-109">In addition to the wrapper macros above, several macros are available for individual data types.</span></span> <span data-ttu-id="2746d-110">Toutes ces macros ont le même format que la macro [TraceLoggingValue](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue) .</span><span class="sxs-lookup"><span data-stu-id="2746d-110">All of these macros have the same format as the [TraceLoggingValue](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue) macro.</span></span> <span data-ttu-id="2746d-111">Vous pouvez utiliser la macro TraceLoggingValue pour détecter automatiquement la macro Wrapper appropriée à utiliser, ou utiliser la macro spécifique directement.</span><span class="sxs-lookup"><span data-stu-id="2746d-111">You can use the TraceLoggingValue macro to automatically detect the appropriate wrapper macro to use, or use the specific macro directly.</span></span>

-   [<span data-ttu-id="2746d-112">**TraceLoggingBinary**</span><span class="sxs-lookup"><span data-stu-id="2746d-112">**TraceLoggingBinary**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingbinary)
-   [<span data-ttu-id="2746d-113">**TraceLoggingChannel**</span><span class="sxs-lookup"><span data-stu-id="2746d-113">**TraceLoggingChannel**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingchannel)
-   [<span data-ttu-id="2746d-114">**TraceLoggingCustomAttribute**</span><span class="sxs-lookup"><span data-stu-id="2746d-114">**TraceLoggingCustomAttribute**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingcustomattribute)
-   [<span data-ttu-id="2746d-115">**TraceLoggingDescription**</span><span class="sxs-lookup"><span data-stu-id="2746d-115">**TraceLoggingDescription**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingdescription)
-   [<span data-ttu-id="2746d-116">**TraceLoggingEventTag**</span><span class="sxs-lookup"><span data-stu-id="2746d-116">**TraceLoggingEventTag**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingeventtag)
-   [<span data-ttu-id="2746d-117">**TraceLoggingKeyword**</span><span class="sxs-lookup"><span data-stu-id="2746d-117">**TraceLoggingKeyword**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingkeyword)
-   [<span data-ttu-id="2746d-118">**TraceLoggingLevel**</span><span class="sxs-lookup"><span data-stu-id="2746d-118">**TraceLoggingLevel**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogginglevel)
-   [<span data-ttu-id="2746d-119">**TraceLoggingOpcode**</span><span class="sxs-lookup"><span data-stu-id="2746d-119">**TraceLoggingOpcode**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingopcode)
-   [<span data-ttu-id="2746d-120">**TraceLoggingSocketAddress**</span><span class="sxs-lookup"><span data-stu-id="2746d-120">**TraceLoggingSocketAddress**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingsocketaddress)
-   [<span data-ttu-id="2746d-121">**TraceLoggingStruct**</span><span class="sxs-lookup"><span data-stu-id="2746d-121">**TraceLoggingStruct**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingstruct)
-   [<span data-ttu-id="2746d-122">**TraceLoggingValue**</span><span class="sxs-lookup"><span data-stu-id="2746d-122">**TraceLoggingValue**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue)

> [!Note]
>
> <span data-ttu-id="2746d-123">**TraceLoggingOptionGroup** est spécifiquement destiné à être utilisé dans TRACELOGGING \_ définir le \_ fournisseur.</span><span class="sxs-lookup"><span data-stu-id="2746d-123">**TraceLoggingOptionGroup** is specifically for use inside of TRACELOGGING\_DEFINE\_PROVIDER.</span></span>
>
> -   [<span data-ttu-id="2746d-124">**TraceLoggingOptionGroup**</span><span class="sxs-lookup"><span data-stu-id="2746d-124">**TraceLoggingOptionGroup**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup)

 

<span data-ttu-id="2746d-125">Voici les macros Wrapper individuelles.</span><span class="sxs-lookup"><span data-stu-id="2746d-125">Here are the individual wrapper macros.</span></span>

-   <span data-ttu-id="2746d-126">TraceLoggingInt8</span><span class="sxs-lookup"><span data-stu-id="2746d-126">TraceLoggingInt8</span></span>

-   <span data-ttu-id="2746d-127">TraceLoggingUInt8</span><span class="sxs-lookup"><span data-stu-id="2746d-127">TraceLoggingUInt8</span></span>

-   <span data-ttu-id="2746d-128">TraceLoggingInt16</span><span class="sxs-lookup"><span data-stu-id="2746d-128">TraceLoggingInt16</span></span>

-   <span data-ttu-id="2746d-129">TraceLoggingUInt16</span><span class="sxs-lookup"><span data-stu-id="2746d-129">TraceLoggingUInt16</span></span>

-   <span data-ttu-id="2746d-130">TraceLoggingInt32</span><span class="sxs-lookup"><span data-stu-id="2746d-130">TraceLoggingInt32</span></span>

-   <span data-ttu-id="2746d-131">TraceLoggingUInt32</span><span class="sxs-lookup"><span data-stu-id="2746d-131">TraceLoggingUInt32</span></span>

-   <span data-ttu-id="2746d-132">TraceLoggingInt64</span><span class="sxs-lookup"><span data-stu-id="2746d-132">TraceLoggingInt64</span></span>

-   <span data-ttu-id="2746d-133">TraceLoggingUInt64</span><span class="sxs-lookup"><span data-stu-id="2746d-133">TraceLoggingUInt64</span></span>

-   <span data-ttu-id="2746d-134">TraceLoggingFloat32</span><span class="sxs-lookup"><span data-stu-id="2746d-134">TraceLoggingFloat32</span></span>

-   <span data-ttu-id="2746d-135">TraceLoggingFloat64</span><span class="sxs-lookup"><span data-stu-id="2746d-135">TraceLoggingFloat64</span></span>

-   <span data-ttu-id="2746d-136">TraceLoggingBool</span><span class="sxs-lookup"><span data-stu-id="2746d-136">TraceLoggingBool</span></span>

-   <span data-ttu-id="2746d-137">TraceLoggingFileTime</span><span class="sxs-lookup"><span data-stu-id="2746d-137">TraceLoggingFileTime</span></span>

-   <span data-ttu-id="2746d-138">TraceLoggingGuid</span><span class="sxs-lookup"><span data-stu-id="2746d-138">TraceLoggingGuid</span></span>

-   <span data-ttu-id="2746d-139">TraceLoggingPointer</span><span class="sxs-lookup"><span data-stu-id="2746d-139">TraceLoggingPointer</span></span>

-   <span data-ttu-id="2746d-140">TraceLoggingSystemTime</span><span class="sxs-lookup"><span data-stu-id="2746d-140">TraceLoggingSystemTime</span></span>

-   <span data-ttu-id="2746d-141">TraceLoggingHexInt8</span><span class="sxs-lookup"><span data-stu-id="2746d-141">TraceLoggingHexInt8</span></span>

-   <span data-ttu-id="2746d-142">TraceLoggingHexUInt8</span><span class="sxs-lookup"><span data-stu-id="2746d-142">TraceLoggingHexUInt8</span></span>

-   <span data-ttu-id="2746d-143">TraceLoggingHexInt32</span><span class="sxs-lookup"><span data-stu-id="2746d-143">TraceLoggingHexInt32</span></span>

-   <span data-ttu-id="2746d-144">TraceLoggingHexUInt32</span><span class="sxs-lookup"><span data-stu-id="2746d-144">TraceLoggingHexUInt32</span></span>

-   <span data-ttu-id="2746d-145">TraceLoggingHexInt64</span><span class="sxs-lookup"><span data-stu-id="2746d-145">TraceLoggingHexInt64</span></span>

-   <span data-ttu-id="2746d-146">TraceLoggingHexUInt64</span><span class="sxs-lookup"><span data-stu-id="2746d-146">TraceLoggingHexUInt64</span></span>

-   <span data-ttu-id="2746d-147">TraceLoggingWchar</span><span class="sxs-lookup"><span data-stu-id="2746d-147">TraceLoggingWchar</span></span>

-   <span data-ttu-id="2746d-148">TraceLoggingChar</span><span class="sxs-lookup"><span data-stu-id="2746d-148">TraceLoggingChar</span></span>

-   <span data-ttu-id="2746d-149">TraceLoggingIntPtr</span><span class="sxs-lookup"><span data-stu-id="2746d-149">TraceLoggingIntPtr</span></span>

-   <span data-ttu-id="2746d-150">TraceLoggingUIntPtr</span><span class="sxs-lookup"><span data-stu-id="2746d-150">TraceLoggingUIntPtr</span></span>

-   <span data-ttu-id="2746d-151">TraceLoggingBoolean</span><span class="sxs-lookup"><span data-stu-id="2746d-151">TraceLoggingBoolean</span></span>

-   <span data-ttu-id="2746d-152">TraceLoggingHexInt16</span><span class="sxs-lookup"><span data-stu-id="2746d-152">TraceLoggingHexInt16</span></span>

-   <span data-ttu-id="2746d-153">TraceLoggingHexUInt16</span><span class="sxs-lookup"><span data-stu-id="2746d-153">TraceLoggingHexUInt16</span></span>

-   <span data-ttu-id="2746d-154">TraceLoggingPid</span><span class="sxs-lookup"><span data-stu-id="2746d-154">TraceLoggingPid</span></span>

-   <span data-ttu-id="2746d-155">TraceLoggingTid</span><span class="sxs-lookup"><span data-stu-id="2746d-155">TraceLoggingTid</span></span>

-   <span data-ttu-id="2746d-156">TraceLoggingPort</span><span class="sxs-lookup"><span data-stu-id="2746d-156">TraceLoggingPort</span></span>

-   <span data-ttu-id="2746d-157">TraceLoggingWinError</span><span class="sxs-lookup"><span data-stu-id="2746d-157">TraceLoggingWinError</span></span>

-   <span data-ttu-id="2746d-158">TraceLoggingNTStatus</span><span class="sxs-lookup"><span data-stu-id="2746d-158">TraceLoggingNTStatus</span></span>

-   <span data-ttu-id="2746d-159">TraceLoggingHResult</span><span class="sxs-lookup"><span data-stu-id="2746d-159">TraceLoggingHResult</span></span>

-   <span data-ttu-id="2746d-160">TraceLoggingSocketAddress</span><span class="sxs-lookup"><span data-stu-id="2746d-160">TraceLoggingSocketAddress</span></span>

-   <span data-ttu-id="2746d-161">TraceLoggingSid</span><span class="sxs-lookup"><span data-stu-id="2746d-161">TraceLoggingSid</span></span>

-   <span data-ttu-id="2746d-162">TraceLoggingString</span><span class="sxs-lookup"><span data-stu-id="2746d-162">TraceLoggingString</span></span>

-   <span data-ttu-id="2746d-163">TraceLoggingWideString</span><span class="sxs-lookup"><span data-stu-id="2746d-163">TraceLoggingWideString</span></span>

-   <span data-ttu-id="2746d-164">TraceLoggingCountedString</span><span class="sxs-lookup"><span data-stu-id="2746d-164">TraceLoggingCountedString</span></span>

-   <span data-ttu-id="2746d-165">TraceLoggingCountedWideString</span><span class="sxs-lookup"><span data-stu-id="2746d-165">TraceLoggingCountedWideString</span></span>

-   <span data-ttu-id="2746d-166">TraceLoggingAnsiString</span><span class="sxs-lookup"><span data-stu-id="2746d-166">TraceLoggingAnsiString</span></span>

-   <span data-ttu-id="2746d-167">TraceLoggingUnicodeString</span><span class="sxs-lookup"><span data-stu-id="2746d-167">TraceLoggingUnicodeString</span></span>

-   <span data-ttu-id="2746d-168">TraceLoggingBinary (void \* Data, taille des données en octets, \[ facultatif \] Name) les paramètres de cette macro diffèrent de ceux ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="2746d-168">TraceLoggingBinary(void \*data, size of the data in bytes, \[optional\] name ) The parameters to this macro differ from those above.</span></span> <span data-ttu-id="2746d-169">Si le paramètre *Name* est spécifié, il doit s’agir d’un littéral de chaîne (et non d’une variable) et ne peut pas contenir de caractères null incorporés.</span><span class="sxs-lookup"><span data-stu-id="2746d-169">If the *name* parameter is specified, it must be a string literal (not a variable) and may not contain any embedded null characters.</span></span> <span data-ttu-id="2746d-170">Si le paramètre *Name* n’est pas fourni, un nom est généré automatiquement.</span><span class="sxs-lookup"><span data-stu-id="2746d-170">If the *name* parameter is not provided, a name is generated automatically.</span></span>

<span data-ttu-id="2746d-171">L’API TraceLogging rend également plusieurs macros disponibles pour les tableaux.</span><span class="sxs-lookup"><span data-stu-id="2746d-171">The TraceLogging API also makes several macros available for arrays.</span></span> <span data-ttu-id="2746d-172">Ces tableaux peuvent avoir une longueur fixe ou être d’une longueur variable, en fonction de la macro wrapper que vous choisissez d’utiliser.</span><span class="sxs-lookup"><span data-stu-id="2746d-172">These arrays can either have a fixed length or be of a variable length, depending on the wrapper macro you choose to use.</span></span> <span data-ttu-id="2746d-173">Toutes ces macros Wrapper suivent ce format.</span><span class="sxs-lookup"><span data-stu-id="2746d-173">All of these wrapper macros follow this format.</span></span>

`TraceLoggingBooleanArray(pVals, cVals, name, desc, tags)`

<span data-ttu-id="2746d-174">Le paramètre *pVals* pointe vers le tableau de données et *cVals* indique le nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="2746d-174">The parameter *pVals* points to the array of data and *cVals* indicates the number of elements in the array.</span></span> <span data-ttu-id="2746d-175">*cVals* doit être une constante et ne peut pas être une variable.</span><span class="sxs-lookup"><span data-stu-id="2746d-175">*cVals* must be a constant and cannot be a variable.</span></span> <span data-ttu-id="2746d-176">Comme avec les macros wrapper à valeur unique, *Name*, **desc** et *Tags* sont des paramètres facultatifs et doivent respecter les mêmes restrictions que celles expliquées avec la macro **TraceLoggingValue** .</span><span class="sxs-lookup"><span data-stu-id="2746d-176">As with the single value wrapper macros, *name*, **desc**, and *tags* are optional parameters and must follow the same restrictions as explained with the **TraceLoggingValue** macro.</span></span>

-   <span data-ttu-id="2746d-177">TraceLoggingInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-177">TraceLoggingInt8FixedArray</span></span>

-   <span data-ttu-id="2746d-178">TraceLoggingUInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-178">TraceLoggingUInt8FixedArray</span></span>

-   <span data-ttu-id="2746d-179">TraceLoggingInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-179">TraceLoggingInt16FixedArray</span></span>

-   <span data-ttu-id="2746d-180">TraceLoggingUInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-180">TraceLoggingUInt16FixedArray</span></span>

-   <span data-ttu-id="2746d-181">TraceLoggingInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-181">TraceLoggingInt32FixedArray</span></span>

-   <span data-ttu-id="2746d-182">TraceLoggingUInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-182">TraceLoggingUInt32FixedArray</span></span>

-   <span data-ttu-id="2746d-183">TraceLoggingInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-183">TraceLoggingInt64FixedArray</span></span>

-   <span data-ttu-id="2746d-184">TraceLoggingUInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-184">TraceLoggingUInt64FixedArray</span></span>

-   <span data-ttu-id="2746d-185">TraceLoggingFloat32FixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-185">TraceLoggingFloat32FixedArray</span></span>

-   <span data-ttu-id="2746d-186">TraceLoggingFloat64FixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-186">TraceLoggingFloat64FixedArray</span></span>

-   <span data-ttu-id="2746d-187">TraceLoggingBoolFixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-187">TraceLoggingBoolFixedArray</span></span>

-   <span data-ttu-id="2746d-188">TraceLoggingGuidFixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-188">TraceLoggingGuidFixedArray</span></span>

-   <span data-ttu-id="2746d-189">TraceLoggingPointerFixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-189">TraceLoggingPointerFixedArray</span></span>

-   <span data-ttu-id="2746d-190">TraceLoggingFileTimeFixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-190">TraceLoggingFileTimeFixedArray</span></span>

-   <span data-ttu-id="2746d-191">TraceLoggingSystemTimeFixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-191">TraceLoggingSystemTimeFixedArray</span></span>

-   <span data-ttu-id="2746d-192">TraceLoggingHexInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-192">TraceLoggingHexInt8FixedArray</span></span>

-   <span data-ttu-id="2746d-193">TraceLoggingHexUInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-193">TraceLoggingHexUInt8FixedArray</span></span>

-   <span data-ttu-id="2746d-194">TraceLoggingHexInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-194">TraceLoggingHexInt32FixedArray</span></span>

-   <span data-ttu-id="2746d-195">TraceLoggingHexUInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-195">TraceLoggingHexUInt32FixedArray</span></span>

-   <span data-ttu-id="2746d-196">TraceLoggingHexInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-196">TraceLoggingHexInt64FixedArray</span></span>

-   <span data-ttu-id="2746d-197">TraceLoggingHexUInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-197">TraceLoggingHexUInt64FixedArray</span></span>

-   <span data-ttu-id="2746d-198">TraceLoggingWcharFixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-198">TraceLoggingWcharFixedArray</span></span>

-   <span data-ttu-id="2746d-199">TraceLoggingCharFixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-199">TraceLoggingCharFixedArray</span></span>

-   <span data-ttu-id="2746d-200">TraceLoggingIntPtrFixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-200">TraceLoggingIntPtrFixedArray</span></span>

-   <span data-ttu-id="2746d-201">TraceLoggingUIntPtrFixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-201">TraceLoggingUIntPtrFixedArray</span></span>

-   <span data-ttu-id="2746d-202">TraceLoggingBooleanFixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-202">TraceLoggingBooleanFixedArray</span></span>

-   <span data-ttu-id="2746d-203">TraceLoggingHexInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-203">TraceLoggingHexInt16FixedArray</span></span>

-   <span data-ttu-id="2746d-204">TraceLoggingHexUInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="2746d-204">TraceLoggingHexUInt16FixedArray</span></span>

-   <span data-ttu-id="2746d-205">TraceLoggingInt8Array</span><span class="sxs-lookup"><span data-stu-id="2746d-205">TraceLoggingInt8Array</span></span>

-   <span data-ttu-id="2746d-206">TraceLoggingUInt8Array</span><span class="sxs-lookup"><span data-stu-id="2746d-206">TraceLoggingUInt8Array</span></span>

-   <span data-ttu-id="2746d-207">TraceLoggingInt16Array</span><span class="sxs-lookup"><span data-stu-id="2746d-207">TraceLoggingInt16Array</span></span>

-   <span data-ttu-id="2746d-208">TraceLoggingUInt16Array</span><span class="sxs-lookup"><span data-stu-id="2746d-208">TraceLoggingUInt16Array</span></span>

-   <span data-ttu-id="2746d-209">TraceLoggingInt32Array</span><span class="sxs-lookup"><span data-stu-id="2746d-209">TraceLoggingInt32Array</span></span>

-   <span data-ttu-id="2746d-210">TraceLoggingUInt32Array</span><span class="sxs-lookup"><span data-stu-id="2746d-210">TraceLoggingUInt32Array</span></span>

-   <span data-ttu-id="2746d-211">TraceLoggingInt64Array</span><span class="sxs-lookup"><span data-stu-id="2746d-211">TraceLoggingInt64Array</span></span>

-   <span data-ttu-id="2746d-212">TraceLoggingUInt64Array</span><span class="sxs-lookup"><span data-stu-id="2746d-212">TraceLoggingUInt64Array</span></span>

-   <span data-ttu-id="2746d-213">TraceLoggingFloat32Array</span><span class="sxs-lookup"><span data-stu-id="2746d-213">TraceLoggingFloat32Array</span></span>

-   <span data-ttu-id="2746d-214">TraceLoggingFloat64Array</span><span class="sxs-lookup"><span data-stu-id="2746d-214">TraceLoggingFloat64Array</span></span>

-   <span data-ttu-id="2746d-215">TraceLoggingBoolArray</span><span class="sxs-lookup"><span data-stu-id="2746d-215">TraceLoggingBoolArray</span></span>

-   <span data-ttu-id="2746d-216">TraceLoggingGuidArray</span><span class="sxs-lookup"><span data-stu-id="2746d-216">TraceLoggingGuidArray</span></span>

-   <span data-ttu-id="2746d-217">TraceLoggingPointerArray</span><span class="sxs-lookup"><span data-stu-id="2746d-217">TraceLoggingPointerArray</span></span>

-   <span data-ttu-id="2746d-218">TraceLoggingFileTimeArray</span><span class="sxs-lookup"><span data-stu-id="2746d-218">TraceLoggingFileTimeArray</span></span>

-   <span data-ttu-id="2746d-219">TraceLoggingSystemTimeArray</span><span class="sxs-lookup"><span data-stu-id="2746d-219">TraceLoggingSystemTimeArray</span></span>

-   <span data-ttu-id="2746d-220">TraceLoggingHexInt8Array</span><span class="sxs-lookup"><span data-stu-id="2746d-220">TraceLoggingHexInt8Array</span></span>

-   <span data-ttu-id="2746d-221">TraceLoggingHexUInt8Array</span><span class="sxs-lookup"><span data-stu-id="2746d-221">TraceLoggingHexUInt8Array</span></span>

-   <span data-ttu-id="2746d-222">TraceLoggingHexInt32Array</span><span class="sxs-lookup"><span data-stu-id="2746d-222">TraceLoggingHexInt32Array</span></span>

-   <span data-ttu-id="2746d-223">TraceLoggingHexUInt32Array</span><span class="sxs-lookup"><span data-stu-id="2746d-223">TraceLoggingHexUInt32Array</span></span>

-   <span data-ttu-id="2746d-224">TraceLoggingHexInt64Array</span><span class="sxs-lookup"><span data-stu-id="2746d-224">TraceLoggingHexInt64Array</span></span>

-   <span data-ttu-id="2746d-225">TraceLoggingHexUInt64Array</span><span class="sxs-lookup"><span data-stu-id="2746d-225">TraceLoggingHexUInt64Array</span></span>

-   <span data-ttu-id="2746d-226">TraceLoggingWcharArray</span><span class="sxs-lookup"><span data-stu-id="2746d-226">TraceLoggingWcharArray</span></span>

-   <span data-ttu-id="2746d-227">TraceLoggingCharArray</span><span class="sxs-lookup"><span data-stu-id="2746d-227">TraceLoggingCharArray</span></span>

-   <span data-ttu-id="2746d-228">TraceLoggingIntPtrArray</span><span class="sxs-lookup"><span data-stu-id="2746d-228">TraceLoggingIntPtrArray</span></span>

-   <span data-ttu-id="2746d-229">TraceLoggingUIntPtrArray</span><span class="sxs-lookup"><span data-stu-id="2746d-229">TraceLoggingUIntPtrArray</span></span>

-   <span data-ttu-id="2746d-230">TraceLoggingBooleanArray</span><span class="sxs-lookup"><span data-stu-id="2746d-230">TraceLoggingBooleanArray</span></span>

-   <span data-ttu-id="2746d-231">TraceLoggingHexInt16Array</span><span class="sxs-lookup"><span data-stu-id="2746d-231">TraceLoggingHexInt16Array</span></span>

-   <span data-ttu-id="2746d-232">TraceLoggingHexUInt16Array</span><span class="sxs-lookup"><span data-stu-id="2746d-232">TraceLoggingHexUInt16Array</span></span>

 

 




