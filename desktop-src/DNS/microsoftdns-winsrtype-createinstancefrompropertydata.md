---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_WINSRType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource de recherche inversée WINS (WINSr).
ms.assetid: e14e81be-fc5c-4a6f-b6d1-cb3ce5005e00
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_WINSRType
- MicrosoftDNS_WINSRType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c35863e00ace6c0772383604d0fbdfd7915cd02c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104731"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_winsrtype-class"></a><span data-ttu-id="34525-106">Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS WINSRType</span><span class="sxs-lookup"><span data-stu-id="34525-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_WINSRType class</span></span>

<span data-ttu-id="34525-107">La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource de recherche inversée WINS (WINSR).</span><span class="sxs-lookup"><span data-stu-id="34525-107">The **CreateInstanceFromPropertyData** method instantiates a WINS Reverse Lookup (WINSR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="34525-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34525-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           uint32                 MappingFlag,
  [in]           uint32                 LookupTimeout,
  [in]           uint32                 CacheTimeout,
  [in]           string                 ResultDomain,
  [out, ref]     MicrosoftDNS_WINSRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="34525-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34525-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34525-110">*DnsServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34525-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34525-111">Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="34525-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="34525-112">*ContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34525-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34525-113">Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="34525-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="34525-114">*OwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34525-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34525-115">Nom du propriétaire de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="34525-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="34525-116">*RecordClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="34525-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="34525-117">Classe de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="34525-117">Class of the RR.</span></span> <span data-ttu-id="34525-118">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="34525-118">Default value is 1.</span></span> <span data-ttu-id="34525-119">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="34525-119">The following values are valid.</span></span>



| <span data-ttu-id="34525-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="34525-120">Value</span></span>                                                                                                | <span data-ttu-id="34525-121">Signification</span><span class="sxs-lookup"><span data-stu-id="34525-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="34525-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="34525-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="34525-123">DANS (Internet)</span><span class="sxs-lookup"><span data-stu-id="34525-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="34525-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="34525-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="34525-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="34525-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="34525-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="34525-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="34525-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="34525-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="34525-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="34525-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="34525-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="34525-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="34525-130">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="34525-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="34525-131">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="34525-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="34525-132">*MappingFlag* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34525-132">*MappingFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34525-133">Indicateur de mappage WINSr qui spécifie si l’enregistrement doit être inclus dans la réplication de zone.</span><span class="sxs-lookup"><span data-stu-id="34525-133">WINSR mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="34525-134">Elle ne peut avoir que deux valeurs : 0x80000000 et 0x00010000 correspondant respectivement aux indicateurs de réplication et de non-réplication (enregistrement local).</span><span class="sxs-lookup"><span data-stu-id="34525-134">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="34525-135">*LookupTimeout* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34525-135">*LookupTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34525-136">Délai d’attente, en secondes, pour un serveur DNS à l’aide de la recherche inversée WINS.</span><span class="sxs-lookup"><span data-stu-id="34525-136">Time out, in seconds, for a DNS Server using WINS Reverse Look up.</span></span>

</dd> <dt>

<span data-ttu-id="34525-137">*CacheTimeout* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34525-137">*CacheTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34525-138">Durée, en secondes, pendant laquelle un serveur DNS utilisant WINS recherche peut mettre en cache la réponse du serveur WINS.</span><span class="sxs-lookup"><span data-stu-id="34525-138">Time, in seconds, a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="34525-139">*ResultDomain* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34525-139">*ResultDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34525-140">Nom de domaine à ajouter aux noms NetBIOS retournés.</span><span class="sxs-lookup"><span data-stu-id="34525-140">Domain name to append to returned NetBIOS names.</span></span>

</dd> <dt>

<span data-ttu-id="34525-141">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="34525-141">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="34525-142">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="34525-142">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34525-143">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="34525-143">Return value</span></span>

<span data-ttu-id="34525-144">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="34525-144">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="34525-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34525-145">Requirements</span></span>



| <span data-ttu-id="34525-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34525-146">Requirement</span></span> | <span data-ttu-id="34525-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="34525-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="34525-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34525-148">Minimum supported client</span></span><br/> | <span data-ttu-id="34525-149">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="34525-149">None supported</span></span><br/>                                                              |
| <span data-ttu-id="34525-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34525-150">Minimum supported server</span></span><br/> | <span data-ttu-id="34525-151">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="34525-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="34525-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="34525-152">Namespace</span></span><br/>                | <span data-ttu-id="34525-153">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="34525-153">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="34525-154">MOF</span><span class="sxs-lookup"><span data-stu-id="34525-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="34525-155"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="34525-155"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34525-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34525-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34525-157">**MicrosoftDNS \_ WINSRType**</span><span class="sxs-lookup"><span data-stu-id="34525-157">**MicrosoftDNS\_WINSRType**</span></span>](microsoftdns-winsrtype.md)
</dt> <dt>

[<span data-ttu-id="34525-158">**Modifier la méthode de la \_ classe WINSRType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="34525-158">**Modify Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="34525-159">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="34525-159">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





