---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_HINFOType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource d’informations sur l’hôte (HINFO).
ms.assetid: dfc11ae8-5013-4b48-a1e9-78566dc32297
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_HINFOType
- MicrosoftDNS_HINFOType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2c8386a9c66ec94436fe4ae4c886ec62ff5b96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743157"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_hinfotype-class"></a><span data-ttu-id="c55f4-106">Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS HINFOType</span><span class="sxs-lookup"><span data-stu-id="c55f4-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_HINFOType class</span></span>

<span data-ttu-id="c55f4-107">La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource d’informations sur l’hôte (HINFO).</span><span class="sxs-lookup"><span data-stu-id="c55f4-107">The **CreateInstanceFromPropertyData** method instantiates a Host Information (HINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="c55f4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c55f4-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in, optional] string                 CPU,
  [in, optional] string                 OS,
  [out, ref]     MicrosoftDNS_HINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="c55f4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c55f4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c55f4-110">*DnsServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c55f4-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c55f4-111">Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="c55f4-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="c55f4-112">*ContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c55f4-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c55f4-113">Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="c55f4-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="c55f4-114">*OwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c55f4-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c55f4-115">Nom du propriétaire de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="c55f4-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="c55f4-116">*RecordClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c55f4-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c55f4-117">Classe de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="c55f4-117">Class of the RR.</span></span> <span data-ttu-id="c55f4-118">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="c55f4-118">Default value is 1.</span></span> <span data-ttu-id="c55f4-119">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="c55f4-119">The following values are valid.</span></span>



| <span data-ttu-id="c55f4-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c55f4-120">Value</span></span>                                                                                                | <span data-ttu-id="c55f4-121">Signification</span><span class="sxs-lookup"><span data-stu-id="c55f4-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="c55f4-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="c55f4-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="c55f4-123">DANS (Internet)</span><span class="sxs-lookup"><span data-stu-id="c55f4-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="c55f4-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="c55f4-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="c55f4-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="c55f4-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="c55f4-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="c55f4-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="c55f4-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="c55f4-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="c55f4-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="c55f4-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="c55f4-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="c55f4-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="c55f4-130">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c55f4-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c55f4-131">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="c55f4-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="c55f4-132">*Processeur* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c55f4-132">*CPU* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c55f4-133">Type d’UC du propriétaire de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c55f4-133">CPU type of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="c55f4-134">*Système d’exploitation* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c55f4-134">*OS* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c55f4-135">Système d’exploitation du propriétaire de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c55f4-135">Operating system of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="c55f4-136">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="c55f4-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c55f4-137">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="c55f4-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c55f4-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c55f4-138">Return value</span></span>

<span data-ttu-id="c55f4-139">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c55f4-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c55f4-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c55f4-140">Requirements</span></span>



| <span data-ttu-id="c55f4-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c55f4-141">Requirement</span></span> | <span data-ttu-id="c55f4-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="c55f4-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c55f4-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c55f4-143">Minimum supported client</span></span><br/> | <span data-ttu-id="c55f4-144">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c55f4-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c55f4-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c55f4-145">Minimum supported server</span></span><br/> | <span data-ttu-id="c55f4-146">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c55f4-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c55f4-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c55f4-147">Namespace</span></span><br/>                | <span data-ttu-id="c55f4-148">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="c55f4-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c55f4-149">MOF</span><span class="sxs-lookup"><span data-stu-id="c55f4-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c55f4-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c55f4-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c55f4-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c55f4-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c55f4-152">**MicrosoftDNS \_ HINFOType**</span><span class="sxs-lookup"><span data-stu-id="c55f4-152">**MicrosoftDNS\_HINFOType**</span></span>](microsoftdns-hinfotype.md)
</dt> <dt>

[<span data-ttu-id="c55f4-153">**Modifier la méthode de la \_ classe HINFOType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c55f4-153">**Modify Method of the MicrosoftDNS\_HINFOType Class**</span></span>](microsoftdns-hinfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="c55f4-154">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="c55f4-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





