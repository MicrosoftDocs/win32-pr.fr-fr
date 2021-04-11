---
title: Types de données NAP (NapTypes. h)
description: 'Remarque : la plateforme de protection d’accès réseau n’est pas disponible à partir de Windows 10. les types de données pour l’API de protection d’accès réseau (NAP) sont les suivants.'
ms.assetid: 54f2866b-4333-4fc8-bb25-b7d4ae72b7dc
keywords:
- ProbationTime
- ProtocolMaxSize
- NapComponentId
- SystemHealthEntityId
- EnforcementEntityId
- SystemHealthEntityCount
- EnforcementEntityCount
- StringCorrelationId
- ConnectionId
- Pourcentage
- MessageId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5780d73701354a12b244c5e5ea6167c2cfba70d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942626"
---
# <a name="nap-datatypes"></a><span data-ttu-id="53931-114">Types de données NAP</span><span class="sxs-lookup"><span data-stu-id="53931-114">NAP Datatypes</span></span>

> [!Note]  
> <span data-ttu-id="53931-115">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="53931-115">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="53931-116">Les types de données de l’API de protection d’accès réseau (NAP) sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="53931-116">The datatypes for the Network Access Protection (NAP) API are as follows.</span></span>


```C++
typedef FILETIME ProbationTime;
typedef UINT32 ProtocolMaxSize;
typedef UINT32 NapComponentId;
typedef NapComponentId SystemHealthEntityId;
typedef NapComponentId EnforcementEntityId;
typedef UINT16 SystemHealthEntityCount;
typedef UINT16 EnforcementEntityCount;
typedef CountedString StringCorrelationId;
typedef GUID ConnectionId;
typedef UINT8 Percentage;
typedef UINT32 MessageId;
```



<dl> <dt>

<span data-ttu-id="53931-117">**ProbationTime**</span><span class="sxs-lookup"><span data-stu-id="53931-117">**ProbationTime**</span></span>
</dt> <dd>

<span data-ttu-id="53931-118">Structure [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime) qui contient une heure relative à la période d’essai d’une machine cliente.</span><span class="sxs-lookup"><span data-stu-id="53931-118">A [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that contains a time related to a client machine's probation.</span></span>

</dd> <dt>

<span data-ttu-id="53931-119">**ProtocolMaxSize**</span><span class="sxs-lookup"><span data-stu-id="53931-119">**ProtocolMaxSize**</span></span>
</dt> <dd>

<span data-ttu-id="53931-120">Valeur qui spécifie la plage de valeurs possibles pour la taille maximale, en octets, d’un paquet [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) tel que défini par Range ([**minProtocolMaxSize, maxProtocolMaxSize**](nap-type-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="53931-120">A value that specifies the range of possible values for the maximum size, in bytes, of an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet as defined by range([**minProtocolMaxSize, maxProtocolMaxSize**](nap-type-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="53931-121">**NapComponentId**</span><span class="sxs-lookup"><span data-stu-id="53931-121">**NapComponentId**</span></span>
</dt> <dd>

<span data-ttu-id="53931-122">Identificateur à 4 octets unique utilisé par les clients de l’SHA, des validateurs d’intégrité du système et de l’application pour s’identifier eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="53931-122">A unique 4-byte identifier used by SHAs, SHVs and enforcement clients to identify themselves.</span></span> <span data-ttu-id="53931-123">Les trois premiers octets sont le code SMI affecté par l’IETF du fournisseur et le dernier octet identifie le composant lui-même.</span><span class="sxs-lookup"><span data-stu-id="53931-123">The first three bytes are the IETF-assigned SMI code of the vendor, and the last byte identifies the component itself.</span></span>

</dd> <dt>

<span data-ttu-id="53931-124">**SystemHealthEntityId**</span><span class="sxs-lookup"><span data-stu-id="53931-124">**SystemHealthEntityId**</span></span>
</dt> <dd>

<span data-ttu-id="53931-125">Valeur **NapComponentId** utilisée pour identifier les paires SHA/SHV.</span><span class="sxs-lookup"><span data-stu-id="53931-125">A **NapComponentId** value used to identify SHA/SHV pairs.</span></span>

</dd> <dt>

<span data-ttu-id="53931-126">**EnforcementEntityId**</span><span class="sxs-lookup"><span data-stu-id="53931-126">**EnforcementEntityId**</span></span>
</dt> <dd>

<span data-ttu-id="53931-127">Valeur **NapComponentId** utilisée pour identifier les clients de contrainte.</span><span class="sxs-lookup"><span data-stu-id="53931-127">A **NapComponentId** value used to identify enforcement clients.</span></span>

</dd> <dt>

<span data-ttu-id="53931-128">**SystemHealthEntityCount**</span><span class="sxs-lookup"><span data-stu-id="53931-128">**SystemHealthEntityCount**</span></span>
</dt> <dd>

<span data-ttu-id="53931-129">Valeur qui spécifie le nombre de Sha inscrits dans le système NAP dans la plage 0 (zéro) à [**maxSystemHealthEntityCount**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="53931-129">A value that specifies the number of registered SHAs in the NAP system in the range 0 (zero) to [**maxSystemHealthEntityCount**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="53931-130">**EnforcementEntityCount**</span><span class="sxs-lookup"><span data-stu-id="53931-130">**EnforcementEntityCount**</span></span>
</dt> <dd>

<span data-ttu-id="53931-131">Valeur qui spécifie le nombre de clients de mise en œuvre dans le système NAP dans la plage 0 (zéro) à [**maxEnforcerCount**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="53931-131">A value that specifies the number of enforcement clients in the NAP system in the range 0 (zero) to [**maxEnforcerCount**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="53931-132">**StringCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="53931-132">**StringCorrelationId**</span></span>
</dt> <dd>

<span data-ttu-id="53931-133">Version [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) d’une structure [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) utilisée pour coupler [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) à **SoHResponses**.</span><span class="sxs-lookup"><span data-stu-id="53931-133">The [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) version of a [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) structure used to pair [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) to **SoHResponses**.</span></span>

</dd> <dt>

<span data-ttu-id="53931-134">**ID**</span><span class="sxs-lookup"><span data-stu-id="53931-134">**ConnectionId**</span></span>
</dt> <dd>

<span data-ttu-id="53931-135">Identificateur global unique (GUID) unique utilisé pour identifier les connexions NAP gérées par les clients de contrainte.</span><span class="sxs-lookup"><span data-stu-id="53931-135">A unique Globally Unique Identifier (GUID) used to identify a NAP connections maintained by enforcement clients.</span></span>

</dd> <dt>

<span data-ttu-id="53931-136">**Percentage**</span><span class="sxs-lookup"><span data-stu-id="53931-136">**Percentage**</span></span>
</dt> <dd>

<span data-ttu-id="53931-137">Valeur qui contient le pourcentage compris entre 0 (zéro) et 100 de correction terminée.</span><span class="sxs-lookup"><span data-stu-id="53931-137">A value that contains the percentage between 0 (zero) and 100 of remediation that is complete</span></span>

</dd> <dt>

<span data-ttu-id="53931-138">**MessageId**</span><span class="sxs-lookup"><span data-stu-id="53931-138">**MessageId**</span></span>
</dt> <dd>

<span data-ttu-id="53931-139">Valeur unique utilisée pour identifier les messages du système NAP.</span><span class="sxs-lookup"><span data-stu-id="53931-139">A unique value used to identify NAP system messages.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="53931-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53931-140">Requirements</span></span>



| <span data-ttu-id="53931-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53931-141">Requirement</span></span> | <span data-ttu-id="53931-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="53931-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53931-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53931-143">Minimum supported client</span></span><br/> | <span data-ttu-id="53931-144">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53931-144">Windows Vista \[desktop apps only\]</span></span><br/>                                                                                                                      |
| <span data-ttu-id="53931-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53931-145">Minimum supported server</span></span><br/> | <span data-ttu-id="53931-146">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53931-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                |
| <span data-ttu-id="53931-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="53931-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="53931-148"><dt>NapTypes. h ; </dt> <dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="53931-148"><dt>NapTypes.h; </dt> <dt>NapEnforcementClient.h</dt></span></span> </dl> |



 

