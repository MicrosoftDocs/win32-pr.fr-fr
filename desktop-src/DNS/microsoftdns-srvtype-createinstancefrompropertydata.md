---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_SRVType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource de service (SRV).
ms.assetid: ef55faa8-1109-4c96-98ac-2b01b940fa5c
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_SRVType
- MicrosoftDNS_SRVType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 607ed606bf12e9e2a6f90a6e7f309aa708b7f230
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743381"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_srvtype-class"></a><span data-ttu-id="a35e8-106">Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS SRVType</span><span class="sxs-lookup"><span data-stu-id="a35e8-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_SRVType class</span></span>

<span data-ttu-id="a35e8-107">La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource de service (SRV).</span><span class="sxs-lookup"><span data-stu-id="a35e8-107">The **CreateInstanceFromPropertyData** method instantiates a Service (SRV) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="a35e8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a35e8-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               Priority,
  [in]           uint16               Weight,
  [in]           uint16               Port,
  [in]           string               SRVDomainName,
  [out, ref]     MicrosoftDNS_SRVType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="a35e8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a35e8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a35e8-110">*DnsServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a35e8-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a35e8-111">Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="a35e8-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="a35e8-112">*ContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a35e8-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a35e8-113">Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="a35e8-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="a35e8-114">*OwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a35e8-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a35e8-115">Nom du propriétaire de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="a35e8-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="a35e8-116">*RecordClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="a35e8-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a35e8-117">Classe de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="a35e8-117">Class of the RR.</span></span> <span data-ttu-id="a35e8-118">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="a35e8-118">Default value is 1.</span></span> <span data-ttu-id="a35e8-119">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="a35e8-119">The following values are valid.</span></span>



| <span data-ttu-id="a35e8-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a35e8-120">Value</span></span>                                                                                                | <span data-ttu-id="a35e8-121">Signification</span><span class="sxs-lookup"><span data-stu-id="a35e8-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="a35e8-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="a35e8-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="a35e8-123">DANS (Internet)</span><span class="sxs-lookup"><span data-stu-id="a35e8-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="a35e8-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="a35e8-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="a35e8-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="a35e8-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="a35e8-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="a35e8-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="a35e8-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="a35e8-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="a35e8-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="a35e8-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="a35e8-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="a35e8-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="a35e8-130">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="a35e8-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a35e8-131">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="a35e8-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="a35e8-132">*Priorité* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a35e8-132">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a35e8-133">Priorité de l’hôte cible spécifiée dans le nom du propriétaire.</span><span class="sxs-lookup"><span data-stu-id="a35e8-133">Priority of the target host specified in the owner name.</span></span> <span data-ttu-id="a35e8-134">Les nombres inférieurs impliquent des priorités plus élevées.</span><span class="sxs-lookup"><span data-stu-id="a35e8-134">Lower numbers imply higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="a35e8-135">*Poids* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a35e8-135">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a35e8-136">Poids de l’hôte cible.</span><span class="sxs-lookup"><span data-stu-id="a35e8-136">Weight of the target host.</span></span> <span data-ttu-id="a35e8-137">Cela est utile lorsque vous sélectionnez parmi les hôtes qui ont la même priorité.</span><span class="sxs-lookup"><span data-stu-id="a35e8-137">This is useful when selecting among hosts that have the same priority.</span></span> <span data-ttu-id="a35e8-138">La probabilité d’utiliser cet hôte doit être proportionnelle à son poids.</span><span class="sxs-lookup"><span data-stu-id="a35e8-138">The chances of using this host should be proportional to its weight.</span></span>

</dd> <dt>

<span data-ttu-id="a35e8-139">*Port* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a35e8-139">*Port* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a35e8-140">Port utilisé sur l’hôte cible d’un service de protocole.</span><span class="sxs-lookup"><span data-stu-id="a35e8-140">Port used on the target host of a protocol service.</span></span>

</dd> <dt>

<span data-ttu-id="a35e8-141">*SRVDomainName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a35e8-141">*SRVDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a35e8-142">Nom de domaine complet de l’hôte cible.</span><span class="sxs-lookup"><span data-stu-id="a35e8-142">FQDN of the target host.</span></span> <span data-ttu-id="a35e8-143">Une cible de \\ . \\ signifie que le service n’est pas disponible dans ce domaine.</span><span class="sxs-lookup"><span data-stu-id="a35e8-143">A target of \\.\\ means that the service is decidedly not available at this domain.</span></span>

</dd> <dt>

<span data-ttu-id="a35e8-144">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="a35e8-144">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="a35e8-145">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="a35e8-145">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a35e8-146">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a35e8-146">Return value</span></span>

<span data-ttu-id="a35e8-147">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a35e8-147">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a35e8-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a35e8-148">Requirements</span></span>



| <span data-ttu-id="a35e8-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a35e8-149">Requirement</span></span> | <span data-ttu-id="a35e8-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="a35e8-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a35e8-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a35e8-151">Minimum supported client</span></span><br/> | <span data-ttu-id="a35e8-152">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a35e8-152">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a35e8-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a35e8-153">Minimum supported server</span></span><br/> | <span data-ttu-id="a35e8-154">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a35e8-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a35e8-155">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a35e8-155">Namespace</span></span><br/>                | <span data-ttu-id="a35e8-156">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="a35e8-156">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="a35e8-157">MOF</span><span class="sxs-lookup"><span data-stu-id="a35e8-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a35e8-158"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a35e8-158"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a35e8-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a35e8-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a35e8-160">**MicrosoftDNS \_ SRVType**</span><span class="sxs-lookup"><span data-stu-id="a35e8-160">**MicrosoftDNS\_SRVType**</span></span>](microsoftdns-srvtype.md)
</dt> <dt>

[<span data-ttu-id="a35e8-161">**Modifier la méthode de la \_ classe SRVType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="a35e8-161">**Modify Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-modify.md)
</dt> <dt>

[<span data-ttu-id="a35e8-162">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="a35e8-162">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





