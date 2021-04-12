---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_RTType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource d’itinéraire (RT).
ms.assetid: 1ebb0543-d031-4430-acbe-708c4931b7a4
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_RTType
- MicrosoftDNS_RTType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c3b8d71c41fefa9b78aa9a469ee1426c553e1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508685"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_rttype-class"></a><span data-ttu-id="a1305-106">Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS RTType</span><span class="sxs-lookup"><span data-stu-id="a1305-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_RTType class</span></span>

<span data-ttu-id="a1305-107">La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource d’itinéraire (RT).</span><span class="sxs-lookup"><span data-stu-id="a1305-107">The **CreateInstanceFromPropertyData** method instantiates a Route Through (RT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1305-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1305-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           uint16              Preference,
  [in]           string              IntermediateHost,
  [out, ref]     MicrosoftDNS_RTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="a1305-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a1305-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1305-110">*DnsServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a1305-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1305-111">Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="a1305-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="a1305-112">*ContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a1305-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1305-113">Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="a1305-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="a1305-114">*OwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a1305-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1305-115">Nom du propriétaire de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="a1305-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="a1305-116">*RecordClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="a1305-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a1305-117">Classe de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="a1305-117">Class of the RR.</span></span> <span data-ttu-id="a1305-118">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="a1305-118">Default value is 1.</span></span> <span data-ttu-id="a1305-119">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="a1305-119">The following values are valid.</span></span>



| <span data-ttu-id="a1305-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1305-120">Value</span></span>                                                                                                | <span data-ttu-id="a1305-121">Signification</span><span class="sxs-lookup"><span data-stu-id="a1305-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="a1305-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="a1305-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="a1305-123">DANS (Internet)</span><span class="sxs-lookup"><span data-stu-id="a1305-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="a1305-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="a1305-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="a1305-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="a1305-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="a1305-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="a1305-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="a1305-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="a1305-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="a1305-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="a1305-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="a1305-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="a1305-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="a1305-130">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="a1305-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a1305-131">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="a1305-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="a1305-132">*Préférence* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a1305-132">*Preference* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1305-133">Préférence donnée à ce RR, parmi d’autres au même propriétaire.</span><span class="sxs-lookup"><span data-stu-id="a1305-133">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="a1305-134">Les valeurs les plus basses sont préférées.</span><span class="sxs-lookup"><span data-stu-id="a1305-134">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="a1305-135">*IntermediateHost* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a1305-135">*IntermediateHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1305-136">Nom de domaine complet spécifiant un hôte qui servira de intermédiaire pour atteindre l’hôte spécifié par le propriétaire.</span><span class="sxs-lookup"><span data-stu-id="a1305-136">FQDN specifying a host to serve as an intermediate in reaching the host specified by owner.</span></span>

</dd> <dt>

<span data-ttu-id="a1305-137">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="a1305-137">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="a1305-138">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="a1305-138">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1305-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a1305-139">Return value</span></span>

<span data-ttu-id="a1305-140">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a1305-140">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1305-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1305-141">Requirements</span></span>



| <span data-ttu-id="a1305-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1305-142">Requirement</span></span> | <span data-ttu-id="a1305-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1305-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1305-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1305-144">Minimum supported client</span></span><br/> | <span data-ttu-id="a1305-145">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1305-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a1305-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1305-146">Minimum supported server</span></span><br/> | <span data-ttu-id="a1305-147">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1305-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a1305-148">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a1305-148">Namespace</span></span><br/>                | <span data-ttu-id="a1305-149">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="a1305-149">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="a1305-150">MOF</span><span class="sxs-lookup"><span data-stu-id="a1305-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1305-151"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a1305-151"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1305-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1305-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1305-153">**MicrosoftDNS \_ RTType**</span><span class="sxs-lookup"><span data-stu-id="a1305-153">**MicrosoftDNS\_RTType**</span></span>](microsoftdns-rttype.md)
</dt> <dt>

[<span data-ttu-id="a1305-154">**Modifier la méthode de la \_ classe RTType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="a1305-154">**Modify Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-modify.md)
</dt> <dt>

[<span data-ttu-id="a1305-155">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="a1305-155">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





