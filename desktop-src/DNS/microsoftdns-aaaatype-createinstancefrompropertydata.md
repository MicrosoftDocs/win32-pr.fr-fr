---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_AAAAType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource d’adresse IPv6 (AAAA).
ms.assetid: 3f2774d8-1eb6-4300-95e2-f918fc6612e0
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_AAAAType
- MicrosoftDNS_AAAAType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9232506b52795521300e827701f685e351d8ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508578"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_aaaatype-class"></a><span data-ttu-id="edd3a-106">Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS AAAAType</span><span class="sxs-lookup"><span data-stu-id="edd3a-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_AAAAType class</span></span>

<span data-ttu-id="edd3a-107">La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource d’adresse IPv6 (aaaa).</span><span class="sxs-lookup"><span data-stu-id="edd3a-107">The **CreateInstanceFromPropertyData** method instantiates an IPv6 address (AAAA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="edd3a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="edd3a-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           string                IPv6Address,
  [out, ref]     MicrosoftDNS_AAAAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="edd3a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="edd3a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edd3a-110">*DnsServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="edd3a-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edd3a-111">Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="edd3a-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="edd3a-112">*ContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="edd3a-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edd3a-113">Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="edd3a-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="edd3a-114">*OwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="edd3a-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edd3a-115">Nom du propriétaire de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="edd3a-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="edd3a-116">*RecordClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="edd3a-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="edd3a-117">Classe de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="edd3a-117">Class of the RR.</span></span> <span data-ttu-id="edd3a-118">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="edd3a-118">Default value is 1.</span></span> <span data-ttu-id="edd3a-119">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="edd3a-119">The following values are valid.</span></span>



| <span data-ttu-id="edd3a-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="edd3a-120">Value</span></span>                                                                                                | <span data-ttu-id="edd3a-121">Signification</span><span class="sxs-lookup"><span data-stu-id="edd3a-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="edd3a-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="edd3a-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="edd3a-123">DANS (Internet)</span><span class="sxs-lookup"><span data-stu-id="edd3a-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="edd3a-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="edd3a-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="edd3a-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="edd3a-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="edd3a-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="edd3a-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="edd3a-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="edd3a-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="edd3a-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="edd3a-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="edd3a-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="edd3a-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="edd3a-130">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="edd3a-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="edd3a-131">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="edd3a-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="edd3a-132">*AdresseIPv6* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="edd3a-132">*IPv6Address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edd3a-133">Adresse IPv6 de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="edd3a-133">IPv6 address for the host.</span></span>

</dd> <dt>

<span data-ttu-id="edd3a-134">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="edd3a-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="edd3a-135">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="edd3a-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edd3a-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="edd3a-136">Return value</span></span>

<span data-ttu-id="edd3a-137">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="edd3a-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="edd3a-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="edd3a-138">Requirements</span></span>



| <span data-ttu-id="edd3a-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="edd3a-139">Requirement</span></span> | <span data-ttu-id="edd3a-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="edd3a-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="edd3a-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="edd3a-141">Minimum supported client</span></span><br/> | <span data-ttu-id="edd3a-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="edd3a-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="edd3a-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="edd3a-143">Minimum supported server</span></span><br/> | <span data-ttu-id="edd3a-144">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="edd3a-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="edd3a-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="edd3a-145">Namespace</span></span><br/>                | <span data-ttu-id="edd3a-146">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="edd3a-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="edd3a-147">MOF</span><span class="sxs-lookup"><span data-stu-id="edd3a-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="edd3a-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="edd3a-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edd3a-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edd3a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edd3a-150">**MicrosoftDNS \_ AAAAType**</span><span class="sxs-lookup"><span data-stu-id="edd3a-150">**MicrosoftDNS\_AAAAType**</span></span>](microsoftdns-aaaatype.md)
</dt> <dt>

[<span data-ttu-id="edd3a-151">**Modifier la méthode de la \_ classe AAAAType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="edd3a-151">**Modify Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-modify.md)
</dt> <dt>

[<span data-ttu-id="edd3a-152">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="edd3a-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





