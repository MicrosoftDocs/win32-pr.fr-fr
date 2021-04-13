---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_NXTType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource suivant (NXT).
ms.assetid: d0e4f3bf-f835-4341-a614-539975e6be11
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_NXTType
- MicrosoftDNS_NXTType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fee00cd0afdb6ac629a981dbdb586a30252eac1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465846"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_nxttype-class"></a><span data-ttu-id="c2cee-106">Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS NXTType</span><span class="sxs-lookup"><span data-stu-id="c2cee-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_NXTType class</span></span>

<span data-ttu-id="c2cee-107">La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource suivant (NXT).</span><span class="sxs-lookup"><span data-stu-id="c2cee-107">The **CreateInstanceFromPropertyData** method instantiates a Next (NXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2cee-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2cee-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               NextDomainName,
  [in]           string               Types,
  [out, ref]     MicrosoftDNS_NXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="c2cee-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2cee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2cee-110">*DnsServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c2cee-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2cee-111">Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="c2cee-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="c2cee-112">*ContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c2cee-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2cee-113">Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="c2cee-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="c2cee-114">*OwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c2cee-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2cee-115">Nom du propriétaire de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="c2cee-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="c2cee-116">*RecordClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c2cee-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c2cee-117">Classe de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="c2cee-117">Class of the RR.</span></span> <span data-ttu-id="c2cee-118">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="c2cee-118">Default value is 1.</span></span> <span data-ttu-id="c2cee-119">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="c2cee-119">The following values are valid.</span></span>



| <span data-ttu-id="c2cee-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2cee-120">Value</span></span>                                                                                                | <span data-ttu-id="c2cee-121">Signification</span><span class="sxs-lookup"><span data-stu-id="c2cee-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="c2cee-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="c2cee-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="c2cee-123">DANS (Internet)</span><span class="sxs-lookup"><span data-stu-id="c2cee-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="c2cee-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="c2cee-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="c2cee-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="c2cee-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="c2cee-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="c2cee-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="c2cee-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="c2cee-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="c2cee-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="c2cee-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="c2cee-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="c2cee-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="c2cee-130">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c2cee-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c2cee-131">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="c2cee-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="c2cee-132">*NextDomainName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c2cee-132">*NextDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2cee-133">Nom de domaine suivant.</span><span class="sxs-lookup"><span data-stu-id="c2cee-133">Next domain name.</span></span>

</dd> <dt>

<span data-ttu-id="c2cee-134">*Types* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c2cee-134">*Types* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2cee-135">Liste séparée par des espaces des mnémoniques de type RR pour le nom de propriétaire de l’enregistrement de ressource NXT.</span><span class="sxs-lookup"><span data-stu-id="c2cee-135">Space-separated list of the RR-type mnemonics for the owner name of the NXT Resource Record.</span></span>

</dd> <dt>

<span data-ttu-id="c2cee-136">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="c2cee-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c2cee-137">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="c2cee-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2cee-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c2cee-138">Return value</span></span>

<span data-ttu-id="c2cee-139">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c2cee-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2cee-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2cee-140">Requirements</span></span>



| <span data-ttu-id="c2cee-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2cee-141">Requirement</span></span> | <span data-ttu-id="c2cee-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2cee-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2cee-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2cee-143">Minimum supported client</span></span><br/> | <span data-ttu-id="c2cee-144">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2cee-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c2cee-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2cee-145">Minimum supported server</span></span><br/> | <span data-ttu-id="c2cee-146">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2cee-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c2cee-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c2cee-147">Namespace</span></span><br/>                | <span data-ttu-id="c2cee-148">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="c2cee-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c2cee-149">MOF</span><span class="sxs-lookup"><span data-stu-id="c2cee-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2cee-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2cee-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2cee-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2cee-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2cee-152">**MicrosoftDNS \_ NXTType**</span><span class="sxs-lookup"><span data-stu-id="c2cee-152">**MicrosoftDNS\_NXTType**</span></span>](microsoftdns-nxttype.md)
</dt> <dt>

[<span data-ttu-id="c2cee-153">**Modifier la méthode de la \_ classe NXTType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c2cee-153">**Modify Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-modify.md)
</dt> <dt>

[<span data-ttu-id="c2cee-154">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="c2cee-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





