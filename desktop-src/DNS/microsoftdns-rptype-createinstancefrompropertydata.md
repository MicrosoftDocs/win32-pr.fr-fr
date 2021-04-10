---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_RPType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource de personne responsable (RP).
ms.assetid: 6d9366c3-fc82-4c1f-8fa3-c107f6a1ff74
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_RPType
- MicrosoftDNS_RPType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c150a8a91a7a94fbea8492faea08b61d437a4c9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200557"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_rptype-class"></a><span data-ttu-id="06a04-106">Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS RPType</span><span class="sxs-lookup"><span data-stu-id="06a04-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_RPType class</span></span>

<span data-ttu-id="06a04-107">La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource de personne responsable (RP).</span><span class="sxs-lookup"><span data-stu-id="06a04-107">The **CreateInstanceFromPropertyData** method instantiates a Responsible Person (RP) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="06a04-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06a04-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              RPMailbox,
  [in]           string              TXTDomainName,
  [out, ref]     MicrosoftDNS_RPType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="06a04-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06a04-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06a04-110">*DnsServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06a04-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06a04-111">Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="06a04-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="06a04-112">*ContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06a04-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06a04-113">Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="06a04-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="06a04-114">*OwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06a04-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06a04-115">Nom du propriétaire de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="06a04-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="06a04-116">*RecordClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="06a04-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06a04-117">Classe de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="06a04-117">Class of the RR.</span></span> <span data-ttu-id="06a04-118">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="06a04-118">Default value is 1.</span></span> <span data-ttu-id="06a04-119">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="06a04-119">The following values are valid.</span></span>



| <span data-ttu-id="06a04-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="06a04-120">Value</span></span>                                                                                                | <span data-ttu-id="06a04-121">Signification</span><span class="sxs-lookup"><span data-stu-id="06a04-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="06a04-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="06a04-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="06a04-123">DANS (Internet)</span><span class="sxs-lookup"><span data-stu-id="06a04-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="06a04-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="06a04-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="06a04-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="06a04-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="06a04-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="06a04-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="06a04-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="06a04-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="06a04-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="06a04-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="06a04-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="06a04-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="06a04-130">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="06a04-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06a04-131">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="06a04-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="06a04-132">*RPMailbox* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06a04-132">*RPMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06a04-133">Nom de domaine complet spécifiant la boîte aux lettres pour la personne responsable.</span><span class="sxs-lookup"><span data-stu-id="06a04-133">FQDN specifying the mailbox for the responsible person.</span></span>

</dd> <dt>

<span data-ttu-id="06a04-134">*TXTDomainName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06a04-134">*TXTDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06a04-135">Nom de domaine complet pour lequel existent les enregistrements de ressource TXT.</span><span class="sxs-lookup"><span data-stu-id="06a04-135">FQDN for which TXT Resource Records exist.</span></span>

</dd> <dt>

<span data-ttu-id="06a04-136">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="06a04-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="06a04-137">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="06a04-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06a04-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="06a04-138">Return value</span></span>

<span data-ttu-id="06a04-139">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="06a04-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="06a04-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06a04-140">Requirements</span></span>



| <span data-ttu-id="06a04-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06a04-141">Requirement</span></span> | <span data-ttu-id="06a04-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="06a04-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06a04-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06a04-143">Minimum supported client</span></span><br/> | <span data-ttu-id="06a04-144">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="06a04-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="06a04-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06a04-145">Minimum supported server</span></span><br/> | <span data-ttu-id="06a04-146">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06a04-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="06a04-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="06a04-147">Namespace</span></span><br/>                | <span data-ttu-id="06a04-148">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="06a04-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="06a04-149">MOF</span><span class="sxs-lookup"><span data-stu-id="06a04-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06a04-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06a04-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06a04-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06a04-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06a04-152">**MicrosoftDNS \_ RPType**</span><span class="sxs-lookup"><span data-stu-id="06a04-152">**MicrosoftDNS\_RPType**</span></span>](microsoftdns-rptype.md)
</dt> <dt>

[<span data-ttu-id="06a04-153">**Modifier la méthode de la \_ classe RPType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="06a04-153">**Modify Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-modify.md)
</dt> <dt>

[<span data-ttu-id="06a04-154">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="06a04-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





