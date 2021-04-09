---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_CNAMEType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource de nom canonique (CNAMe).
ms.assetid: b5a5e14a-fb30-4cdf-90d0-7ef446350ac6
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_CNAMEType
- MicrosoftDNS_CNAMEType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_CNAMEType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aceb65a76002651e98dd8751e0a5c0c56aca3e1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942132"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_cnametype-class"></a><span data-ttu-id="f41a0-106">Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS CNAMEType</span><span class="sxs-lookup"><span data-stu-id="f41a0-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_CNAMEType class</span></span>

<span data-ttu-id="f41a0-107">La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource de nom canonique (CNAME).</span><span class="sxs-lookup"><span data-stu-id="f41a0-107">The **CreateInstanceFromPropertyData** method instantiates a Canonical Name (CNAME) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="f41a0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f41a0-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           string                 PrimaryName,
  [out, ref]     MicrosoftDNS_CNAMEType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="f41a0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f41a0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f41a0-110">*DnsServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f41a0-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f41a0-111">Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="f41a0-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="f41a0-112">*ContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f41a0-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f41a0-113">Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="f41a0-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="f41a0-114">*OwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f41a0-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f41a0-115">Nom du propriétaire de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="f41a0-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="f41a0-116">*RecordClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f41a0-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f41a0-117">Classe de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="f41a0-117">Class of the RR.</span></span> <span data-ttu-id="f41a0-118">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="f41a0-118">Default value is 1.</span></span> <span data-ttu-id="f41a0-119">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="f41a0-119">The following values are valid.</span></span>



| <span data-ttu-id="f41a0-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f41a0-120">Value</span></span>                                                                                                | <span data-ttu-id="f41a0-121">Signification</span><span class="sxs-lookup"><span data-stu-id="f41a0-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="f41a0-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="f41a0-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="f41a0-123">DANS (Internet)</span><span class="sxs-lookup"><span data-stu-id="f41a0-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="f41a0-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="f41a0-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="f41a0-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="f41a0-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="f41a0-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="f41a0-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="f41a0-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="f41a0-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="f41a0-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="f41a0-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="f41a0-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="f41a0-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="f41a0-130">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f41a0-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f41a0-131">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="f41a0-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="f41a0-132">*PrimaryName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f41a0-132">*PrimaryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f41a0-133">Nom principal du RR CNAMe.</span><span class="sxs-lookup"><span data-stu-id="f41a0-133">Primary name of the CNAME RR.</span></span>

</dd> <dt>

<span data-ttu-id="f41a0-134">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="f41a0-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f41a0-135">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="f41a0-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f41a0-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f41a0-136">Return value</span></span>

<span data-ttu-id="f41a0-137">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f41a0-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f41a0-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f41a0-138">Requirements</span></span>



| <span data-ttu-id="f41a0-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f41a0-139">Requirement</span></span> | <span data-ttu-id="f41a0-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="f41a0-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f41a0-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f41a0-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f41a0-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f41a0-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f41a0-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f41a0-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f41a0-144">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f41a0-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f41a0-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f41a0-145">Namespace</span></span><br/>                | <span data-ttu-id="f41a0-146">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="f41a0-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f41a0-147">MOF</span><span class="sxs-lookup"><span data-stu-id="f41a0-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f41a0-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f41a0-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f41a0-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f41a0-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f41a0-150">**MicrosoftDNS \_ CNAMEType**</span><span class="sxs-lookup"><span data-stu-id="f41a0-150">**MicrosoftDNS\_CNAMEType**</span></span>](microsoftdns-cnametype.md)
</dt> <dt>

[<span data-ttu-id="f41a0-151">**Modifier la méthode de la \_ classe CNAMEType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="f41a0-151">**Modify Method of the MicrosoftDNS\_CNAMEType Class**</span></span>](microsoftdns-cnametype-modify.md)
</dt> <dt>

[<span data-ttu-id="f41a0-152">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="f41a0-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





