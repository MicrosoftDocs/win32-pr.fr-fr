---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_MFType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource de l’agent de transfert de messagerie pour le domaine (MF).
ms.assetid: e669d065-bfba-4a86-8519-2317e03ed4ee
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_MFType
- MicrosoftDNS_MFType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26cafc766a6ea6419432b279f5389721f6572b44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942104"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mftype-class"></a><span data-ttu-id="6f7bc-106">Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MFType</span><span class="sxs-lookup"><span data-stu-id="6f7bc-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MFType class</span></span>

<span data-ttu-id="6f7bc-107">La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource de l’agent de transfert de messagerie pour le domaine (MF).</span><span class="sxs-lookup"><span data-stu-id="6f7bc-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Forwarding Agent for Domain (MF) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f7bc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f7bc-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              MFHost,
  [out, ref]     MicrosoftDNS_MFType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="6f7bc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f7bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f7bc-110">*DnsServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6f7bc-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f7bc-111">Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="6f7bc-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="6f7bc-112">*ContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6f7bc-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f7bc-113">Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="6f7bc-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="6f7bc-114">*OwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6f7bc-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f7bc-115">Nom du propriétaire de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="6f7bc-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="6f7bc-116">*RecordClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="6f7bc-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6f7bc-117">Classe de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="6f7bc-117">Class of the RR.</span></span> <span data-ttu-id="6f7bc-118">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="6f7bc-118">Default value is 1.</span></span> <span data-ttu-id="6f7bc-119">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="6f7bc-119">The following values are valid.</span></span>



| <span data-ttu-id="6f7bc-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f7bc-120">Value</span></span>                                                                                                | <span data-ttu-id="6f7bc-121">Signification</span><span class="sxs-lookup"><span data-stu-id="6f7bc-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="6f7bc-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="6f7bc-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="6f7bc-123">DANS (Internet)</span><span class="sxs-lookup"><span data-stu-id="6f7bc-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="6f7bc-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="6f7bc-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="6f7bc-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="6f7bc-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="6f7bc-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="6f7bc-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="6f7bc-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="6f7bc-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="6f7bc-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="6f7bc-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="6f7bc-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="6f7bc-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="6f7bc-130">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="6f7bc-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6f7bc-131">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="6f7bc-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="6f7bc-132">*MFHost* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6f7bc-132">*MFHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f7bc-133">Nom de l’hôte qui fournit l’agent de transfert du courrier.</span><span class="sxs-lookup"><span data-stu-id="6f7bc-133">Name of the host that provides the mail forwarding agent.</span></span>

</dd> <dt>

<span data-ttu-id="6f7bc-134">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="6f7bc-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="6f7bc-135">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="6f7bc-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f7bc-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6f7bc-136">Return value</span></span>

<span data-ttu-id="6f7bc-137">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6f7bc-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f7bc-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f7bc-138">Requirements</span></span>



| <span data-ttu-id="6f7bc-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f7bc-139">Requirement</span></span> | <span data-ttu-id="6f7bc-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f7bc-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f7bc-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f7bc-141">Minimum supported client</span></span><br/> | <span data-ttu-id="6f7bc-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f7bc-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6f7bc-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f7bc-143">Minimum supported server</span></span><br/> | <span data-ttu-id="6f7bc-144">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f7bc-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6f7bc-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6f7bc-145">Namespace</span></span><br/>                | <span data-ttu-id="6f7bc-146">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="6f7bc-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="6f7bc-147">MOF</span><span class="sxs-lookup"><span data-stu-id="6f7bc-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f7bc-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f7bc-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f7bc-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f7bc-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f7bc-150">**MicrosoftDNS \_ MFType**</span><span class="sxs-lookup"><span data-stu-id="6f7bc-150">**MicrosoftDNS\_MFType**</span></span>](microsoftdns-mftype.md)
</dt> <dt>

[<span data-ttu-id="6f7bc-151">**Modifier la méthode de la \_ classe MFType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6f7bc-151">**Modify Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-modify.md)
</dt> <dt>

[<span data-ttu-id="6f7bc-152">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="6f7bc-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





