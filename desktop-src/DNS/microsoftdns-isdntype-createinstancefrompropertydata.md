---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_ISDNType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource RNIS.
ms.assetid: cd3b98e3-a804-473e-8831-5f045d43a54f
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_ISDNType
- MicrosoftDNS_ISDNType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39f6adaaf374cac56d7d29d04d83c8765b0080ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508894"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_isdntype-class"></a><span data-ttu-id="e69ed-106">Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS ISDNType</span><span class="sxs-lookup"><span data-stu-id="e69ed-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_ISDNType class</span></span>

<span data-ttu-id="e69ed-107">La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource RNIS.</span><span class="sxs-lookup"><span data-stu-id="e69ed-107">The **CreateInstanceFromPropertyData** method instantiates an ISDN Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="e69ed-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e69ed-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           string                ISDNNumber,
  [in]           string                SubAddress,
  [out, ref]     MicrosoftDNS_ISDNType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="e69ed-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e69ed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e69ed-110">*DnsServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e69ed-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e69ed-111">Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="e69ed-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="e69ed-112">*ContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e69ed-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e69ed-113">Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="e69ed-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="e69ed-114">*OwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e69ed-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e69ed-115">Nom du propriétaire de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="e69ed-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="e69ed-116">*RecordClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="e69ed-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e69ed-117">Classe de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="e69ed-117">Class of the RR.</span></span> <span data-ttu-id="e69ed-118">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="e69ed-118">Default value is 1.</span></span> <span data-ttu-id="e69ed-119">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="e69ed-119">The following values are valid.</span></span>



| <span data-ttu-id="e69ed-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e69ed-120">Value</span></span>                                                                                                | <span data-ttu-id="e69ed-121">Signification</span><span class="sxs-lookup"><span data-stu-id="e69ed-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="e69ed-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="e69ed-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="e69ed-123">DANS (Internet)</span><span class="sxs-lookup"><span data-stu-id="e69ed-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="e69ed-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="e69ed-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="e69ed-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="e69ed-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="e69ed-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="e69ed-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="e69ed-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="e69ed-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="e69ed-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="e69ed-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="e69ed-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="e69ed-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="e69ed-130">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="e69ed-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e69ed-131">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="e69ed-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="e69ed-132">*ISDNNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e69ed-132">*ISDNNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e69ed-133">Numéro RNIS et DDI du propriétaire de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="e69ed-133">ISDN number and DDI of the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="e69ed-134">Sous- *adresse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e69ed-134">*SubAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e69ed-135">Sous-adresse du propriétaire, si elle est définie.</span><span class="sxs-lookup"><span data-stu-id="e69ed-135">Subaddress of the owner, if defined.</span></span>

</dd> <dt>

<span data-ttu-id="e69ed-136">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="e69ed-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e69ed-137">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="e69ed-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e69ed-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e69ed-138">Return value</span></span>

<span data-ttu-id="e69ed-139">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e69ed-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e69ed-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e69ed-140">Requirements</span></span>



| <span data-ttu-id="e69ed-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e69ed-141">Requirement</span></span> | <span data-ttu-id="e69ed-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="e69ed-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e69ed-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e69ed-143">Minimum supported client</span></span><br/> | <span data-ttu-id="e69ed-144">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e69ed-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e69ed-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e69ed-145">Minimum supported server</span></span><br/> | <span data-ttu-id="e69ed-146">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e69ed-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e69ed-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e69ed-147">Namespace</span></span><br/>                | <span data-ttu-id="e69ed-148">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="e69ed-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="e69ed-149">MOF</span><span class="sxs-lookup"><span data-stu-id="e69ed-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e69ed-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e69ed-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e69ed-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e69ed-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e69ed-152">**MicrosoftDNS \_ ISDNType**</span><span class="sxs-lookup"><span data-stu-id="e69ed-152">**MicrosoftDNS\_ISDNType**</span></span>](microsoftdns-isdntype.md)
</dt> <dt>

[<span data-ttu-id="e69ed-153">**Modifier la méthode de la \_ classe ISDNType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="e69ed-153">**Modify Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-modify.md)
</dt> <dt>

[<span data-ttu-id="e69ed-154">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="e69ed-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





