---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_AType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource d’adresse (A).
ms.assetid: 81d67eba-f2c6-49c0-af29-be3f3724a973
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_AType
- MicrosoftDNS_AType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1d8d3e5c9d0ad4302da2243a3ef9611e295c86e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103714"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_atype-class"></a><span data-ttu-id="1e04b-106">Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS aType</span><span class="sxs-lookup"><span data-stu-id="1e04b-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_AType class</span></span>

<span data-ttu-id="1e04b-107">La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource d’adresse (A).</span><span class="sxs-lookup"><span data-stu-id="1e04b-107">The **CreateInstanceFromPropertyData** method instantiates an Address (A) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e04b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e04b-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string             DnsServerName,
  [in]           string             ContainerName,
  [in]           string             OwnerName,
  [in, optional] uint32             RecordClass = 1,
  [in, optional] uint32             TTL,
  [in]           string             IPAddress,
  [out, ref]     MicrosoftDNS_AType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="1e04b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e04b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e04b-110">*DnsServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e04b-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e04b-111">Nom de domaine complet (FQDN) ou adresse IP du serveur DNS qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="1e04b-111">Fully Qualified Domain Name (FQDN) or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="1e04b-112">*ContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e04b-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e04b-113">Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="1e04b-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="1e04b-114">*OwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e04b-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e04b-115">Nom de domaine complet du propriétaire pour le RR.</span><span class="sxs-lookup"><span data-stu-id="1e04b-115">Owner FQDN for the RR.</span></span>

> [!Note]  
> <span data-ttu-id="1e04b-116">N’utilisez pas le nom NetBIOS du propriétaire.</span><span class="sxs-lookup"><span data-stu-id="1e04b-116">Do not use the owner NetBIOS name.</span></span>

 

</dd> <dt>

<span data-ttu-id="1e04b-117">*RecordClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="1e04b-117">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1e04b-118">Classe de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="1e04b-118">Class of the RR.</span></span> <span data-ttu-id="1e04b-119">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="1e04b-119">Default value is 1.</span></span> <span data-ttu-id="1e04b-120">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="1e04b-120">The following values are valid.</span></span>



| <span data-ttu-id="1e04b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e04b-121">Value</span></span>                                                                                                | <span data-ttu-id="1e04b-122">Signification</span><span class="sxs-lookup"><span data-stu-id="1e04b-122">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="1e04b-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="1e04b-123"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="1e04b-124">DANS (Internet)</span><span class="sxs-lookup"><span data-stu-id="1e04b-124">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="1e04b-125"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="1e04b-125"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="1e04b-126">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="1e04b-126">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="1e04b-127"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="1e04b-127"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="1e04b-128">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="1e04b-128">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="1e04b-129"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="1e04b-129"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="1e04b-130">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="1e04b-130">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="1e04b-131">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="1e04b-131">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1e04b-132">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="1e04b-132">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="1e04b-133">*Adresse IP* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e04b-133">*IPAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e04b-134">Chaîne représentant l’adresse IP de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="1e04b-134">String representing the IP address of the host.</span></span>

</dd> <dt>

<span data-ttu-id="1e04b-135">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="1e04b-135">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="1e04b-136">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="1e04b-136">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e04b-137">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1e04b-137">Return value</span></span>

<span data-ttu-id="1e04b-138">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1e04b-138">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e04b-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e04b-139">Requirements</span></span>



| <span data-ttu-id="1e04b-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e04b-140">Requirement</span></span> | <span data-ttu-id="1e04b-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e04b-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e04b-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e04b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="1e04b-143">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e04b-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1e04b-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e04b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="1e04b-145">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e04b-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1e04b-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1e04b-146">Namespace</span></span><br/>                | <span data-ttu-id="1e04b-147">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="1e04b-147">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="1e04b-148">MOF</span><span class="sxs-lookup"><span data-stu-id="1e04b-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e04b-149"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e04b-149"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e04b-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e04b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e04b-151">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="1e04b-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="1e04b-152">**Modifier la méthode de la \_ classe aType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="1e04b-152">**Modify Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-modify.md)
</dt> </dl>

 

 





