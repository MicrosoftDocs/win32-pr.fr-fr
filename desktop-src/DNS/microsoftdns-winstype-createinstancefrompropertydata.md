---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_WINSType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource WINS (Windows Internet Name Service).
ms.assetid: 0b41a6a5-0bb1-467b-9089-2c721d521887
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_WINSType
- MicrosoftDNS_WINSType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf584bd34f59391a49fd5f7ec13cb49e18ef68fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742245"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_winstype-class"></a><span data-ttu-id="ef13f-106">Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS WINSType</span><span class="sxs-lookup"><span data-stu-id="ef13f-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_WINSType class</span></span>

<span data-ttu-id="ef13f-107">La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource WINS (Windows Internet Name Service).</span><span class="sxs-lookup"><span data-stu-id="ef13f-107">The **CreateInstanceFromPropertyData** method instantiates a Windows Internet Name Service (WINS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef13f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef13f-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           uint32                MappingFlag,
  [in]           uint32                LookupTimeout,
  [in]           uint32                CacheTimeout,
  [in]           string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="ef13f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef13f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef13f-110">*DnsServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef13f-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef13f-111">Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="ef13f-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="ef13f-112">*ContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef13f-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef13f-113">Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="ef13f-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="ef13f-114">*OwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef13f-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef13f-115">Nom du propriétaire de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="ef13f-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="ef13f-116">*RecordClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="ef13f-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ef13f-117">Classe de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="ef13f-117">Class of the RR.</span></span> <span data-ttu-id="ef13f-118">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="ef13f-118">Default value is 1.</span></span> <span data-ttu-id="ef13f-119">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="ef13f-119">The following values are valid.</span></span>



| <span data-ttu-id="ef13f-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef13f-120">Value</span></span>                                                                                                | <span data-ttu-id="ef13f-121">Signification</span><span class="sxs-lookup"><span data-stu-id="ef13f-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="ef13f-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="ef13f-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="ef13f-123">DANS (Internet)</span><span class="sxs-lookup"><span data-stu-id="ef13f-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="ef13f-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="ef13f-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="ef13f-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="ef13f-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="ef13f-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="ef13f-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="ef13f-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="ef13f-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="ef13f-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="ef13f-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="ef13f-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="ef13f-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="ef13f-130">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="ef13f-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ef13f-131">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="ef13f-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="ef13f-132">*MappingFlag* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef13f-132">*MappingFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef13f-133">Indicateur de mappage WINS qui spécifie si l’enregistrement doit être inclus dans la réplication de zone.</span><span class="sxs-lookup"><span data-stu-id="ef13f-133">WINS mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="ef13f-134">Elle ne peut avoir que deux valeurs : 0x80000000 et 0x00010000 correspondant respectivement aux indicateurs de réplication et de non-réplication (enregistrement local).</span><span class="sxs-lookup"><span data-stu-id="ef13f-134">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span> <span data-ttu-id="ef13f-135">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="ef13f-135">The following values are valid.</span></span>



| <span data-ttu-id="ef13f-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef13f-136">Value</span></span>                                                                                                                                               | <span data-ttu-id="ef13f-137">Signification</span><span class="sxs-lookup"><span data-stu-id="ef13f-137">Meaning</span></span>                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <span data-ttu-id="ef13f-138"><dt>**0x80000000**</dt></span><span class="sxs-lookup"><span data-stu-id="ef13f-138"><dt>**0x80000000**</dt></span></span> </dl> | <span data-ttu-id="ef13f-139">Indicateur de réplication</span><span class="sxs-lookup"><span data-stu-id="ef13f-139">Replication flag</span></span><br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <span data-ttu-id="ef13f-140"><dt>**0x00010000**</dt></span><span class="sxs-lookup"><span data-stu-id="ef13f-140"><dt>**0x00010000**</dt></span></span> </dl> | <span data-ttu-id="ef13f-141">Indicateur de non-réplication (enregistrement local)</span><span class="sxs-lookup"><span data-stu-id="ef13f-141">No-replication (local record) flag</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ef13f-142">*LookupTimeout* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef13f-142">*LookupTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef13f-143">Durée, en secondes, pendant laquelle un serveur DNS tente de résoudre à l’aide de la recherche WINS.</span><span class="sxs-lookup"><span data-stu-id="ef13f-143">Time, in seconds, that a DNS Server attempts resolution using WINS Look up.</span></span>

</dd> <dt>

<span data-ttu-id="ef13f-144">*CacheTimeout* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef13f-144">*CacheTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef13f-145">Durée, en secondes, pendant laquelle un serveur DNS qui utilise WINS peut mettre en cache la réponse du serveur WINS.</span><span class="sxs-lookup"><span data-stu-id="ef13f-145">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="ef13f-146">*WinsServers* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef13f-146">*WinsServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef13f-147">Liste des adresses IP séparées par des virgules des serveurs WINS utilisés dans les recherches WINS.</span><span class="sxs-lookup"><span data-stu-id="ef13f-147">List of comma-separated IP addresses of WINS servers used in WINS Look ups.</span></span>

</dd> <dt>

<span data-ttu-id="ef13f-148">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="ef13f-148">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ef13f-149">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="ef13f-149">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef13f-150">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef13f-150">Return value</span></span>

<span data-ttu-id="ef13f-151">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ef13f-151">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef13f-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef13f-152">Requirements</span></span>



| <span data-ttu-id="ef13f-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef13f-153">Requirement</span></span> | <span data-ttu-id="ef13f-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef13f-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef13f-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef13f-155">Minimum supported client</span></span><br/> | <span data-ttu-id="ef13f-156">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef13f-156">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ef13f-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef13f-157">Minimum supported server</span></span><br/> | <span data-ttu-id="ef13f-158">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef13f-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ef13f-159">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ef13f-159">Namespace</span></span><br/>                | <span data-ttu-id="ef13f-160">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="ef13f-160">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ef13f-161">MOF</span><span class="sxs-lookup"><span data-stu-id="ef13f-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef13f-162"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef13f-162"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef13f-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef13f-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef13f-164">**MicrosoftDNS \_ WINSType**</span><span class="sxs-lookup"><span data-stu-id="ef13f-164">**MicrosoftDNS\_WINSType**</span></span>](microsoftdns-winstype.md)
</dt> <dt>

[<span data-ttu-id="ef13f-165">**Modifier la méthode de la \_ classe WINSType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ef13f-165">**Modify Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-modify.md)
</dt> <dt>

[<span data-ttu-id="ef13f-166">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="ef13f-166">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





