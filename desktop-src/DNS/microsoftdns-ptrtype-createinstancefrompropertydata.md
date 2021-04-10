---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_PTRType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource pointeur (PTR).
ms.assetid: ff8beaca-fa0d-4294-8dab-3aa62baa3fe3
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_PTRType
- MicrosoftDNS_PTRType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_PTRType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6123b503fff1548b7fee3f643920b49ebacf636c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103608"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_ptrtype-class"></a><span data-ttu-id="af548-106">Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS PTRType</span><span class="sxs-lookup"><span data-stu-id="af548-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_PTRType class</span></span>

<span data-ttu-id="af548-107">La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource pointeur (PTR).</span><span class="sxs-lookup"><span data-stu-id="af548-107">The **CreateInstanceFromPropertyData** method instantiates a Pointer (PTR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="af548-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af548-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               PTRDomainName,
  [out, ref]     MicrosoftDNS_PTRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="af548-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af548-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af548-110">*DnsServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af548-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af548-111">Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="af548-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="af548-112">*ContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af548-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af548-113">Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="af548-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="af548-114">*OwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af548-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af548-115">Nom du propriétaire de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="af548-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="af548-116">*RecordClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="af548-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="af548-117">Classe de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="af548-117">Class of the RR.</span></span> <span data-ttu-id="af548-118">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="af548-118">Default value is 1.</span></span> <span data-ttu-id="af548-119">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="af548-119">The following values are valid.</span></span>



| <span data-ttu-id="af548-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="af548-120">Value</span></span>                                                                                                | <span data-ttu-id="af548-121">Signification</span><span class="sxs-lookup"><span data-stu-id="af548-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="af548-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="af548-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="af548-123">DANS (Internet)</span><span class="sxs-lookup"><span data-stu-id="af548-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="af548-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="af548-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="af548-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="af548-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="af548-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="af548-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="af548-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="af548-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="af548-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="af548-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="af548-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="af548-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="af548-130">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="af548-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="af548-131">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="af548-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="af548-132">*PTRDomainName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af548-132">*PTRDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af548-133">Chaîne représentant l’adresse de nom de domaine de l’enregistrement PTR.</span><span class="sxs-lookup"><span data-stu-id="af548-133">String representing the domain name address of the PTR record.</span></span>

</dd> <dt>

<span data-ttu-id="af548-134">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="af548-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="af548-135">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="af548-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af548-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="af548-136">Return value</span></span>

<span data-ttu-id="af548-137">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="af548-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="af548-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af548-138">Requirements</span></span>



| <span data-ttu-id="af548-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af548-139">Requirement</span></span> | <span data-ttu-id="af548-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="af548-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af548-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af548-141">Minimum supported client</span></span><br/> | <span data-ttu-id="af548-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="af548-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="af548-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af548-143">Minimum supported server</span></span><br/> | <span data-ttu-id="af548-144">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af548-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="af548-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="af548-145">Namespace</span></span><br/>                | <span data-ttu-id="af548-146">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="af548-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="af548-147">MOF</span><span class="sxs-lookup"><span data-stu-id="af548-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af548-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af548-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af548-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af548-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af548-150">**MicrosoftDNS \_ PTRType**</span><span class="sxs-lookup"><span data-stu-id="af548-150">**MicrosoftDNS\_PTRType**</span></span>](microsoftdns-ptrtype.md)
</dt> <dt>

[<span data-ttu-id="af548-151">**Modifier la méthode de la \_ classe PTRType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="af548-151">**Modify Method of the MicrosoftDNS\_PTRType Class**</span></span>](microsoftdns-ptrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="af548-152">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="af548-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





