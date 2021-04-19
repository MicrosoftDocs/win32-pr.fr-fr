---
title: Constantes de type NAP (NapTypes. h)
description: Les constantes NAP suivantes sont définies.
ms.assetid: 2727487c-8c6a-4cd9-b6d8-253191a7d7f6
topic_type:
- apiref
api_name:
- maxSoHAttributeCount
- maxSoHAttributeSize
- minNetworkSoHSize
- maxNetworkSoHSize
- maxDwordCountPerSoHAttribute
- maxIpv4CountPerSoHAttribute
- maxIpv6CountPerSoHAttribute
- maxStringLength
- maxStringLengthInBytes
- maxSystemHealthEntityCount
- SystemHealthEntityCount
- maxEnforcerCount
- EnforcementEntityCount
- maxPrivateDataSize
- maxConnectionCountPerEnforcer
- maxCachedSoHCount
- freshSoHRequest
- shaFixup
- failureCategoryCount
- ComponentTypeEnforcementClientSoH
- ComponentTypeEnforcementClientRp
- defaultProtocolMaxSize
- maxProtocolMaxSize
- minProtocolMaxSize
- ProtocolMaxSize
api_location:
- NapTypes.h
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85692a7ccc9cbb602a34da714a5eeb488ea5c4a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513626"
---
# <a name="nap-type-constants"></a><span data-ttu-id="5db3e-103">Constantes de type NAP</span><span class="sxs-lookup"><span data-stu-id="5db3e-103">NAP Type Constants</span></span>

> [!Note]  
> <span data-ttu-id="5db3e-104">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="5db3e-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5db3e-105">Les constantes NAP suivantes sont définies.</span><span class="sxs-lookup"><span data-stu-id="5db3e-105">The following NAP constants are defined.</span></span>

<span data-ttu-id="5db3e-106">Les constantes NAP suivantes sont définies dans NapTypes. h :</span><span class="sxs-lookup"><span data-stu-id="5db3e-106">The following NAP constants are defined in NapTypes.h:</span></span>

<dl> <dt>

<span data-ttu-id="5db3e-107"><span id="maxSoHAttributeCount"></span><span id="maxsohattributecount"></span><span id="MAXSOHATTRIBUTECOUNT"></span>**maxSoHAttributeCount**</span><span class="sxs-lookup"><span data-stu-id="5db3e-107"><span id="maxSoHAttributeCount"></span><span id="maxsohattributecount"></span><span id="MAXSOHATTRIBUTECOUNT"></span>**maxSoHAttributeCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db3e-108">0x64</span><span class="sxs-lookup"><span data-stu-id="5db3e-108">0x64</span></span>
</dt> <dt>



<span data-ttu-id="5db3e-109">Nombre maximal d’objets [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) type-length-value (TLV) associés à un paquet [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="5db3e-109">The maximum number of [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) type-length-value (TLV) objects associated with an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5db3e-110"><span id="maxSoHAttributeSize"></span><span id="maxsohattributesize"></span><span id="MAXSOHATTRIBUTESIZE"></span>**maxSoHAttributeSize**</span><span class="sxs-lookup"><span data-stu-id="5db3e-110"><span id="maxSoHAttributeSize"></span><span id="maxsohattributesize"></span><span id="MAXSOHATTRIBUTESIZE"></span>**maxSoHAttributeSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db3e-111">0xFA0</span><span class="sxs-lookup"><span data-stu-id="5db3e-111">0xFA0</span></span>
</dt> <dt>



<span data-ttu-id="5db3e-112">Taille maximale, en octets, d’un objet [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) associé à un paquet de déclaration d’intégrité ([**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh)).</span><span class="sxs-lookup"><span data-stu-id="5db3e-112">The maximum size, in bytes, of a [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) object associated with a statement of health ([**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5db3e-113"><span id="minNetworkSoHSize"></span><span id="minnetworksohsize"></span><span id="MINNETWORKSOHSIZE"></span>**minNetworkSoHSize**</span><span class="sxs-lookup"><span data-stu-id="5db3e-113"><span id="minNetworkSoHSize"></span><span id="minnetworksohsize"></span><span id="MINNETWORKSOHSIZE"></span>**minNetworkSoHSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db3e-114">0xC</span><span class="sxs-lookup"><span data-stu-id="5db3e-114">0xC</span></span>
</dt> <dt>



<span data-ttu-id="5db3e-115">Taille minimale, en octets, d’un paquet [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="5db3e-115">The minimum size, in bytes, of an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5db3e-116"><span id="maxNetworkSoHSize"></span><span id="maxnetworksohsize"></span><span id="MAXNETWORKSOHSIZE"></span>**maxNetworkSoHSize**</span><span class="sxs-lookup"><span data-stu-id="5db3e-116"><span id="maxNetworkSoHSize"></span><span id="maxnetworksohsize"></span><span id="MAXNETWORKSOHSIZE"></span>**maxNetworkSoHSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db3e-117">0xFA0</span><span class="sxs-lookup"><span data-stu-id="5db3e-117">0xFA0</span></span>
</dt> <dt>



<span data-ttu-id="5db3e-118">Taille maximale, en octets, d’un paquet [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="5db3e-118">The maximum size, in bytes, of an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5db3e-119"><span id="maxDwordCountPerSoHAttribute"></span><span id="maxdwordcountpersohattribute"></span><span id="MAXDWORDCOUNTPERSOHATTRIBUTE"></span>**maxDwordCountPerSoHAttribute**</span><span class="sxs-lookup"><span data-stu-id="5db3e-119"><span id="maxDwordCountPerSoHAttribute"></span><span id="maxdwordcountpersohattribute"></span><span id="MAXDWORDCOUNTPERSOHATTRIBUTE"></span>**maxDwordCountPerSoHAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db3e-120">maxSoHAttributeSize/sizeof (DWORD)</span><span class="sxs-lookup"><span data-stu-id="5db3e-120">maxSoHAttributeSize / sizeof(DWORD)</span></span>
</dt> <dt>



<span data-ttu-id="5db3e-121">Nombre maximal de valeurs DWORD associées à un [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span><span class="sxs-lookup"><span data-stu-id="5db3e-121">The maximum number of DWORD values associated with an [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5db3e-122"><span id="maxIpv4CountPerSoHAttribute"></span><span id="maxipv4countpersohattribute"></span><span id="MAXIPV4COUNTPERSOHATTRIBUTE"></span>**maxIpv4CountPerSoHAttribute**</span><span class="sxs-lookup"><span data-stu-id="5db3e-122"><span id="maxIpv4CountPerSoHAttribute"></span><span id="maxipv4countpersohattribute"></span><span id="MAXIPV4COUNTPERSOHATTRIBUTE"></span>**maxIpv4CountPerSoHAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db3e-123">maxSoHAttributeSize/0x4</span><span class="sxs-lookup"><span data-stu-id="5db3e-123">maxSoHAttributeSize / 0x4</span></span>
</dt> <dt>



<span data-ttu-id="5db3e-124">Nombre maximal d’adresses IPv4 associées à un [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span><span class="sxs-lookup"><span data-stu-id="5db3e-124">The maximum number of IPv4 addresses associated with an [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5db3e-125"><span id="maxIpv6CountPerSoHAttribute"></span><span id="maxipv6countpersohattribute"></span><span id="MAXIPV6COUNTPERSOHATTRIBUTE"></span>**maxIpv6CountPerSoHAttribute**</span><span class="sxs-lookup"><span data-stu-id="5db3e-125"><span id="maxIpv6CountPerSoHAttribute"></span><span id="maxipv6countpersohattribute"></span><span id="MAXIPV6COUNTPERSOHATTRIBUTE"></span>**maxIpv6CountPerSoHAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db3e-126">maxSoHAttributeSize/0x10</span><span class="sxs-lookup"><span data-stu-id="5db3e-126">maxSoHAttributeSize / 0x10</span></span>
</dt> <dt>



<span data-ttu-id="5db3e-127">Nombre maximal d’adresses IPv6 associées à un [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span><span class="sxs-lookup"><span data-stu-id="5db3e-127">The maximum number of IPv6 addresses associated with an [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5db3e-128"><span id="maxStringLength"></span><span id="maxstringlength"></span><span id="MAXSTRINGLENGTH"></span>**maxStringLength**</span><span class="sxs-lookup"><span data-stu-id="5db3e-128"><span id="maxStringLength"></span><span id="maxstringlength"></span><span id="MAXSTRINGLENGTH"></span>**maxStringLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db3e-129">0x400</span><span class="sxs-lookup"><span data-stu-id="5db3e-129">0x400</span></span>
</dt> <dt>



<span data-ttu-id="5db3e-130">Longueur maximale d’une chaîne spécifiée par la structure [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .</span><span class="sxs-lookup"><span data-stu-id="5db3e-130">The maximum length of a string specified by the [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5db3e-131"><span id="maxStringLengthInBytes"></span><span id="maxstringlengthinbytes"></span><span id="MAXSTRINGLENGTHINBYTES"></span>**maxStringLengthInBytes**</span><span class="sxs-lookup"><span data-stu-id="5db3e-131"><span id="maxStringLengthInBytes"></span><span id="maxstringlengthinbytes"></span><span id="MAXSTRINGLENGTHINBYTES"></span>**maxStringLengthInBytes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db3e-132">(maxStringLength + 1) \* sizeof (WCHAR)</span><span class="sxs-lookup"><span data-stu-id="5db3e-132">(maxStringLength + 1) \* sizeof(WCHAR)</span></span>
</dt> <dt>



<span data-ttu-id="5db3e-133">Longueur maximale, en octets, d’une chaîne spécifiée par la structure [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .</span><span class="sxs-lookup"><span data-stu-id="5db3e-133">The maximum length, in bytes, of a string specified by the [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5db3e-134"><span id="maxSystemHealthEntityCount"></span><span id="maxsystemhealthentitycount"></span><span id="MAXSYSTEMHEALTHENTITYCOUNT"></span>**maxSystemHealthEntityCount**</span><span class="sxs-lookup"><span data-stu-id="5db3e-134"><span id="maxSystemHealthEntityCount"></span><span id="maxsystemhealthentitycount"></span><span id="MAXSYSTEMHEALTHENTITYCOUNT"></span>**maxSystemHealthEntityCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db3e-135">0x14</span><span class="sxs-lookup"><span data-stu-id="5db3e-135">0x14</span></span>
</dt> <dt>



<span data-ttu-id="5db3e-136">Nombre maximal d’entités d’intégrité système, telles que les validateurs d’intégrité et les Sha.</span><span class="sxs-lookup"><span data-stu-id="5db3e-136">The maximum number of system health entities, such as SHVs and SHAs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5db3e-137"><span id="SystemHealthEntityCount"></span><span id="systemhealthentitycount"></span><span id="SYSTEMHEALTHENTITYCOUNT"></span>**SystemHealthEntityCount**</span><span class="sxs-lookup"><span data-stu-id="5db3e-137"><span id="SystemHealthEntityCount"></span><span id="systemhealthentitycount"></span><span id="SYSTEMHEALTHENTITYCOUNT"></span>**SystemHealthEntityCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db3e-138">\[Plage (0, maxSystemHealthEntityCount)\]</span><span class="sxs-lookup"><span data-stu-id="5db3e-138">\[range(0, maxSystemHealthEntityCount)\]</span></span> 
</dt> <dt>



<span data-ttu-id="5db3e-139">Plage de valeurs possibles pour le nombre d’entités d’intégrité du système.</span><span class="sxs-lookup"><span data-stu-id="5db3e-139">The range of possible values for the number of system health entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5db3e-140"><span id="maxEnforcerCount"></span><span id="maxenforcercount"></span><span id="MAXENFORCERCOUNT"></span>**maxEnforcerCount**</span><span class="sxs-lookup"><span data-stu-id="5db3e-140"><span id="maxEnforcerCount"></span><span id="maxenforcercount"></span><span id="MAXENFORCERCOUNT"></span>**maxEnforcerCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db3e-141">0x14</span><span class="sxs-lookup"><span data-stu-id="5db3e-141">0x14</span></span>
</dt> <dt>



<span data-ttu-id="5db3e-142">Nombre maximal d’entités d’application, telles que QEC.</span><span class="sxs-lookup"><span data-stu-id="5db3e-142">The maximum number of enforcement entities, such as QECs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5db3e-143"><span id="EnforcementEntityCount"></span><span id="enforcemententitycount"></span><span id="ENFORCEMENTENTITYCOUNT"></span>**EnforcementEntityCount**</span><span class="sxs-lookup"><span data-stu-id="5db3e-143"><span id="EnforcementEntityCount"></span><span id="enforcemententitycount"></span><span id="ENFORCEMENTENTITYCOUNT"></span>**EnforcementEntityCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db3e-144">\[Plage (0, maxEnforcerCount)\]</span><span class="sxs-lookup"><span data-stu-id="5db3e-144">\[range(0, maxEnforcerCount)\]</span></span>
</dt> <dt>



<span data-ttu-id="5db3e-145">Plage de valeurs possibles pour le nombre d’entités d’application.</span><span class="sxs-lookup"><span data-stu-id="5db3e-145">The range of possible values for the number of enforcement entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5db3e-146"><span id="maxPrivateDataSize"></span><span id="maxprivatedatasize"></span><span id="MAXPRIVATEDATASIZE"></span>**maxPrivateDataSize**</span><span class="sxs-lookup"><span data-stu-id="5db3e-146"><span id="maxPrivateDataSize"></span><span id="maxprivatedatasize"></span><span id="MAXPRIVATEDATASIZE"></span>**maxPrivateDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db3e-147">0xC8</span><span class="sxs-lookup"><span data-stu-id="5db3e-147">0xC8</span></span>
</dt> <dt>



<span data-ttu-id="5db3e-148">Taille maximale, en octets, d’une structure [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) .</span><span class="sxs-lookup"><span data-stu-id="5db3e-148">The maximum size, in bytes, of a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5db3e-149"><span id="maxConnectionCountPerEnforcer"></span><span id="maxconnectioncountperenforcer"></span><span id="MAXCONNECTIONCOUNTPERENFORCER"></span>**maxConnectionCountPerEnforcer**</span><span class="sxs-lookup"><span data-stu-id="5db3e-149"><span id="maxConnectionCountPerEnforcer"></span><span id="maxconnectioncountperenforcer"></span><span id="MAXCONNECTIONCOUNTPERENFORCER"></span>**maxConnectionCountPerEnforcer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db3e-150">0x14</span><span class="sxs-lookup"><span data-stu-id="5db3e-150">0x14</span></span>
</dt> <dt>



<span data-ttu-id="5db3e-151">Nombre maximal d’objets [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) associés à une entité d’application.</span><span class="sxs-lookup"><span data-stu-id="5db3e-151">The maximum number of [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) objects associated with an enforcement entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5db3e-152"><span id="maxCachedSoHCount"></span><span id="maxcachedsohcount"></span><span id="MAXCACHEDSOHCOUNT"></span>**maxCachedSoHCount**</span><span class="sxs-lookup"><span data-stu-id="5db3e-152"><span id="maxCachedSoHCount"></span><span id="maxcachedsohcount"></span><span id="MAXCACHEDSOHCOUNT"></span>**maxCachedSoHCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db3e-153">maxSystemHealthEntityCount \* maxEnforcerCount \* maxConnectionCountPerEnforcer</span><span class="sxs-lookup"><span data-stu-id="5db3e-153">maxSystemHealthEntityCount \* maxEnforcerCount \* maxConnectionCountPerEnforcer</span></span>
</dt> <dt>



<span data-ttu-id="5db3e-154">Nombre maximal de connexions SoH mises en cache pour toutes les entités d’intégrité du système et d’application.</span><span class="sxs-lookup"><span data-stu-id="5db3e-154">The maximum number of cached SoH connections for all system health and enforcement entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5db3e-155"><span id="freshSoHRequest"></span><span id="freshsohrequest"></span><span id="FRESHSOHREQUEST"></span>**freshSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="5db3e-155"><span id="freshSoHRequest"></span><span id="freshsohrequest"></span><span id="FRESHSOHREQUEST"></span>**freshSoHRequest**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db3e-156">0x1</span><span class="sxs-lookup"><span data-stu-id="5db3e-156">0x1</span></span>
</dt> <dt>



<span data-ttu-id="5db3e-157">Spécifie qu’un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh)est dû à une nouvelle demande, et non à une demande mise en cache.</span><span class="sxs-lookup"><span data-stu-id="5db3e-157">Specifies that an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh)is due to a new request, not a cached request.</span></span> <span data-ttu-id="5db3e-158">Cet indicateur est utilisé par l’agent NAP sur un objet [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="5db3e-158">This flag is used by the NAP agent on an [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5db3e-159"><span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span>**shaFixup**</span><span class="sxs-lookup"><span data-stu-id="5db3e-159"><span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span>**shaFixup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db3e-160">0x1</span><span class="sxs-lookup"><span data-stu-id="5db3e-160">0x1</span></span>
</dt> <dt>



<span data-ttu-id="5db3e-161">Spécifie que la correction est requise.</span><span class="sxs-lookup"><span data-stu-id="5db3e-161">Specifies that fix-up is required.</span></span> <span data-ttu-id="5db3e-162">Cet indicateur est utilisé par un SHA.</span><span class="sxs-lookup"><span data-stu-id="5db3e-162">This flag is used by a SHA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5db3e-163"><span id="failureCategoryCount"></span><span id="failurecategorycount"></span><span id="FAILURECATEGORYCOUNT"></span>**failureCategoryCount**</span><span class="sxs-lookup"><span data-stu-id="5db3e-163"><span id="failureCategoryCount"></span><span id="failurecategorycount"></span><span id="FAILURECATEGORYCOUNT"></span>**failureCategoryCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db3e-164">0x5</span><span class="sxs-lookup"><span data-stu-id="5db3e-164">0x5</span></span>
</dt> <dt>



<span data-ttu-id="5db3e-165">Nombre de catégories d’échec contenues dans une structure [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) .</span><span class="sxs-lookup"><span data-stu-id="5db3e-165">The number of failure categories contained within a [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5db3e-166"><span id="ComponentTypeEnforcementClientSoH"></span><span id="componenttypeenforcementclientsoh"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTSOH"></span>**ComponentTypeEnforcementClientSoH**</span><span class="sxs-lookup"><span data-stu-id="5db3e-166"><span id="ComponentTypeEnforcementClientSoH"></span><span id="componenttypeenforcementclientsoh"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTSOH"></span>**ComponentTypeEnforcementClientSoH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db3e-167">0x1</span><span class="sxs-lookup"><span data-stu-id="5db3e-167">0x1</span></span>
</dt> <dt>



<span data-ttu-id="5db3e-168">Le composant est un client de contrainte de mise en quarantaine (QEC) qui envoie un paquet [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) intrabande lors de l’authentification de la connexion.</span><span class="sxs-lookup"><span data-stu-id="5db3e-168">The component is a quarantine enforcement client (QEC) that sends an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet in-band during connection authentication.</span></span>

> [!Note]  
> <span data-ttu-id="5db3e-169">Cette valeur n’est pas utilisée par les Sha et les validateurs d’intégrité du système.</span><span class="sxs-lookup"><span data-stu-id="5db3e-169">This value is not used by SHAs and SHVs.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="5db3e-170"><span id="ComponentTypeEnforcementClientRp"></span><span id="componenttypeenforcementclientrp"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTRP"></span>**ComponentTypeEnforcementClientRp**</span><span class="sxs-lookup"><span data-stu-id="5db3e-170"><span id="ComponentTypeEnforcementClientRp"></span><span id="componenttypeenforcementclientrp"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTRP"></span>**ComponentTypeEnforcementClientRp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db3e-171">0x2</span><span class="sxs-lookup"><span data-stu-id="5db3e-171">0x2</span></span>
</dt> <dt>



<span data-ttu-id="5db3e-172">Le composant est un QEC qui implémente [**INapCertRelyingParty**](inapcertrelyingparty.md) et doit interagir avec le serveur de certificats d’intégrité (HCS) afin d’obtenir un certificat d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="5db3e-172">The component is a QEC that implements [**INapCertRelyingParty**](inapcertrelyingparty.md) and must interact with the Health Certificate Server (HCS) in order to obtain a health certificate.</span></span>

> [!Note]  
> <span data-ttu-id="5db3e-173">Cette valeur n’est pas utilisée par les Sha et les validateurs d’intégrité du système.</span><span class="sxs-lookup"><span data-stu-id="5db3e-173">This value is not used by SHAs and SHVs.</span></span>

 


</dt> </dl> </dd> </dl>

<span data-ttu-id="5db3e-174">Les constantes NAP suivantes sont définies dans NapEnforcementClient. h.</span><span class="sxs-lookup"><span data-stu-id="5db3e-174">The following NAP constants are defined in NapEnforcementClient.h.</span></span>

<dl> <dt>

<span data-ttu-id="5db3e-175"><span id="defaultProtocolMaxSize"></span><span id="defaultprotocolmaxsize"></span><span id="DEFAULTPROTOCOLMAXSIZE"></span>**defaultProtocolMaxSize**</span><span class="sxs-lookup"><span data-stu-id="5db3e-175"><span id="defaultProtocolMaxSize"></span><span id="defaultprotocolmaxsize"></span><span id="DEFAULTPROTOCOLMAXSIZE"></span>**defaultProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db3e-176">0x0FA0</span><span class="sxs-lookup"><span data-stu-id="5db3e-176">0x0FA0</span></span>
</dt> <dt>



<span data-ttu-id="5db3e-177">Taille maximale par défaut, en octets, d’un paquet SoH.</span><span class="sxs-lookup"><span data-stu-id="5db3e-177">The default maximum size, in bytes, of an SoH packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5db3e-178"><span id="maxProtocolMaxSize"></span><span id="maxprotocolmaxsize"></span><span id="MAXPROTOCOLMAXSIZE"></span>**maxProtocolMaxSize**</span><span class="sxs-lookup"><span data-stu-id="5db3e-178"><span id="maxProtocolMaxSize"></span><span id="maxprotocolmaxsize"></span><span id="MAXPROTOCOLMAXSIZE"></span>**maxProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db3e-179">0xFFFF</span><span class="sxs-lookup"><span data-stu-id="5db3e-179">0xFFFF</span></span>
</dt> <dt>



<span data-ttu-id="5db3e-180">Taille maximale possible, en octets, d’un paquet SoH.</span><span class="sxs-lookup"><span data-stu-id="5db3e-180">The maximum possible size, in bytes, of an SoH packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5db3e-181"><span id="minProtocolMaxSize"></span><span id="minprotocolmaxsize"></span><span id="MINPROTOCOLMAXSIZE"></span>**minProtocolMaxSize**</span><span class="sxs-lookup"><span data-stu-id="5db3e-181"><span id="minProtocolMaxSize"></span><span id="minprotocolmaxsize"></span><span id="MINPROTOCOLMAXSIZE"></span>**minProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db3e-182">0x012C</span><span class="sxs-lookup"><span data-stu-id="5db3e-182">0x012C</span></span>
</dt> <dt>



<span data-ttu-id="5db3e-183">Plus petite taille maximale possible, en octets, d’un paquet SoH.</span><span class="sxs-lookup"><span data-stu-id="5db3e-183">The smallest possible maximum size, in bytes, of an SoH packet.</span></span> <span data-ttu-id="5db3e-184">La taille réelle du paquet SoH peut être inférieure à **minProtocolMaxSize**.</span><span class="sxs-lookup"><span data-stu-id="5db3e-184">The actual size of the SoH packet may be smaller than **minProtocolMaxSize**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5db3e-185"><span id="ProtocolMaxSize"></span><span id="protocolmaxsize"></span><span id="PROTOCOLMAXSIZE"></span>**ProtocolMaxSize**</span><span class="sxs-lookup"><span data-stu-id="5db3e-185"><span id="ProtocolMaxSize"></span><span id="protocolmaxsize"></span><span id="PROTOCOLMAXSIZE"></span>**ProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db3e-186">Plage (minProtocolMaxSize, maxProtocolMaxSize)</span><span class="sxs-lookup"><span data-stu-id="5db3e-186">range(minProtocolMaxSize, maxProtocolMaxSize)</span></span>
</dt> <dt>



<span data-ttu-id="5db3e-187">Plage de valeurs possibles pour la taille maximale d’un paquet SoH.</span><span class="sxs-lookup"><span data-stu-id="5db3e-187">The range of possible values for the maximum size of a SoH packet.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5db3e-188">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5db3e-188">Requirements</span></span>



| <span data-ttu-id="5db3e-189">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5db3e-189">Requirement</span></span> | <span data-ttu-id="5db3e-190">Valeur</span><span class="sxs-lookup"><span data-stu-id="5db3e-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5db3e-191">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5db3e-191">Minimum supported client</span></span><br/> | <span data-ttu-id="5db3e-192">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5db3e-192">Windows Vista \[desktop apps only\]</span></span><br/>                                                                                                                      |
| <span data-ttu-id="5db3e-193">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5db3e-193">Minimum supported server</span></span><br/> | <span data-ttu-id="5db3e-194">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5db3e-194">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                |
| <span data-ttu-id="5db3e-195">En-tête</span><span class="sxs-lookup"><span data-stu-id="5db3e-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="5db3e-196"><dt>NapTypes. h ; </dt> <dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="5db3e-196"><dt>NapTypes.h; </dt> <dt>NapEnforcementClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5db3e-197">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5db3e-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5db3e-198">**Constantes NAP**</span><span class="sxs-lookup"><span data-stu-id="5db3e-198">**NAP Constants**</span></span>](nap-constants.md)
</dt> </dl>

 

 





