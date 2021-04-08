---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_WKSType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource Well-Known services (WKS).
ms.assetid: 6d910716-74f9-48a0-b43c-3243f5518caf
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_WKSType
- MicrosoftDNS_WKSType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e27b62bd2008c58d283d0e7564fa7821c452cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843862"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_wkstype-class"></a><span data-ttu-id="c07bd-106">Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS WKSType</span><span class="sxs-lookup"><span data-stu-id="c07bd-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_WKSType class</span></span>

<span data-ttu-id="c07bd-107">La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource Well-Known services (WKS).</span><span class="sxs-lookup"><span data-stu-id="c07bd-107">The **CreateInstanceFromPropertyData** method instantiates a Well-Known Services (WKS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="c07bd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c07bd-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               InternetAddress,
  [in]           string               IPProtocol,
  [in]           string               Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="c07bd-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c07bd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c07bd-110">*DnsServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c07bd-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c07bd-111">Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="c07bd-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="c07bd-112">*ContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c07bd-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c07bd-113">Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="c07bd-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="c07bd-114">*OwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c07bd-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c07bd-115">Nom du propriétaire de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="c07bd-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="c07bd-116">*RecordClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c07bd-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c07bd-117">Classe de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="c07bd-117">Class of the RR.</span></span> <span data-ttu-id="c07bd-118">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="c07bd-118">Default value is 1.</span></span> <span data-ttu-id="c07bd-119">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="c07bd-119">The following values are valid.</span></span>



| <span data-ttu-id="c07bd-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c07bd-120">Value</span></span>                                                                                                | <span data-ttu-id="c07bd-121">Signification</span><span class="sxs-lookup"><span data-stu-id="c07bd-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="c07bd-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="c07bd-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="c07bd-123">DANS (Internet)</span><span class="sxs-lookup"><span data-stu-id="c07bd-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="c07bd-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="c07bd-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="c07bd-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="c07bd-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="c07bd-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="c07bd-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="c07bd-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="c07bd-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="c07bd-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="c07bd-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="c07bd-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="c07bd-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="c07bd-130">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c07bd-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c07bd-131">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="c07bd-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="c07bd-132">*InternetAddress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c07bd-132">*InternetAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c07bd-133">Adresse IP Internet pour le propriétaire de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c07bd-133">Internet IP address for the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="c07bd-134">*IPProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c07bd-134">*IPProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c07bd-135">Chaîne représentant le protocole IP pour cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c07bd-135">String representing the IP protocol for this record.</span></span> <span data-ttu-id="c07bd-136">Les valeurs valides sont UDP ou TCP.</span><span class="sxs-lookup"><span data-stu-id="c07bd-136">Valid values are UDP or TCP.</span></span>

</dd> <dt>

<span data-ttu-id="c07bd-137">*Services* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c07bd-137">*Services* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c07bd-138">Chaîne contenant tous les services utilisés par l’enregistrement du service bien connu (WKS).</span><span class="sxs-lookup"><span data-stu-id="c07bd-138">String containing all services used by the Well Known Service (WKS) record.</span></span>

</dd> <dt>

<span data-ttu-id="c07bd-139">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="c07bd-139">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c07bd-140">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="c07bd-140">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c07bd-141">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c07bd-141">Return value</span></span>

<span data-ttu-id="c07bd-142">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c07bd-142">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c07bd-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c07bd-143">Requirements</span></span>



| <span data-ttu-id="c07bd-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c07bd-144">Requirement</span></span> | <span data-ttu-id="c07bd-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="c07bd-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c07bd-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c07bd-146">Minimum supported client</span></span><br/> | <span data-ttu-id="c07bd-147">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c07bd-147">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c07bd-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c07bd-148">Minimum supported server</span></span><br/> | <span data-ttu-id="c07bd-149">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c07bd-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c07bd-150">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c07bd-150">Namespace</span></span><br/>                | <span data-ttu-id="c07bd-151">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="c07bd-151">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c07bd-152">MOF</span><span class="sxs-lookup"><span data-stu-id="c07bd-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c07bd-153"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c07bd-153"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c07bd-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c07bd-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c07bd-155">**MicrosoftDNS \_ WKSType**</span><span class="sxs-lookup"><span data-stu-id="c07bd-155">**MicrosoftDNS\_WKSType**</span></span>](microsoftdns-wkstype.md)
</dt> <dt>

[<span data-ttu-id="c07bd-156">**Modifier la méthode de la \_ classe WKSType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c07bd-156">**Modify Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-modify.md)
</dt> <dt>

[<span data-ttu-id="c07bd-157">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="c07bd-157">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





