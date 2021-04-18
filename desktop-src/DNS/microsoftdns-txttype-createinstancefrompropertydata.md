---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_TXTType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource texte (TXT).
ms.assetid: f518bb07-e64f-4240-a7b8-9363374b83d6
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_TXTType
- MicrosoftDNS_TXTType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f23f9790189ca182cd65d9fe34890c31a90921d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509550"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_txttype-class"></a><span data-ttu-id="10d92-106">Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS TXTType</span><span class="sxs-lookup"><span data-stu-id="10d92-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_TXTType class</span></span>

<span data-ttu-id="10d92-107">La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource texte (txt).</span><span class="sxs-lookup"><span data-stu-id="10d92-107">The **CreateInstanceFromPropertyData** method instantiates a Text (TXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="10d92-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10d92-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               DescriptiveText,
  [out, ref]     MicrosoftDNS_TXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="10d92-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="10d92-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10d92-110">*DnsServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="10d92-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10d92-111">Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="10d92-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="10d92-112">*ContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="10d92-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10d92-113">Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="10d92-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="10d92-114">*OwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="10d92-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10d92-115">Nom du propriétaire de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="10d92-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="10d92-116">*RecordClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="10d92-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="10d92-117">Classe de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="10d92-117">Class of the RR.</span></span> <span data-ttu-id="10d92-118">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="10d92-118">Default value is 1.</span></span> <span data-ttu-id="10d92-119">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="10d92-119">The following values are valid.</span></span>



| <span data-ttu-id="10d92-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="10d92-120">Value</span></span>                                                                                                | <span data-ttu-id="10d92-121">Signification</span><span class="sxs-lookup"><span data-stu-id="10d92-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="10d92-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="10d92-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="10d92-123">DANS (Internet)</span><span class="sxs-lookup"><span data-stu-id="10d92-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="10d92-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="10d92-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="10d92-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="10d92-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="10d92-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="10d92-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="10d92-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="10d92-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="10d92-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="10d92-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="10d92-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="10d92-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="10d92-130">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="10d92-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="10d92-131">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="10d92-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="10d92-132">*DescriptiveText* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="10d92-132">*DescriptiveText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10d92-133">Texte descriptif, dont la sémantique dépend du domaine propriétaire.</span><span class="sxs-lookup"><span data-stu-id="10d92-133">Descriptive text, the semantics of which depend on the owner domain.</span></span>

</dd> <dt>

<span data-ttu-id="10d92-134">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="10d92-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="10d92-135">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="10d92-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10d92-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="10d92-136">Return value</span></span>

<span data-ttu-id="10d92-137">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="10d92-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="10d92-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10d92-138">Requirements</span></span>



| <span data-ttu-id="10d92-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10d92-139">Requirement</span></span> | <span data-ttu-id="10d92-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="10d92-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="10d92-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10d92-141">Minimum supported client</span></span><br/> | <span data-ttu-id="10d92-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="10d92-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="10d92-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10d92-143">Minimum supported server</span></span><br/> | <span data-ttu-id="10d92-144">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="10d92-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="10d92-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="10d92-145">Namespace</span></span><br/>                | <span data-ttu-id="10d92-146">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="10d92-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="10d92-147">MOF</span><span class="sxs-lookup"><span data-stu-id="10d92-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10d92-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10d92-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10d92-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10d92-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10d92-150">**MicrosoftDNS \_ TXTType**</span><span class="sxs-lookup"><span data-stu-id="10d92-150">**MicrosoftDNS\_TXTType**</span></span>](microsoftdns-txttype.md)
</dt> <dt>

[<span data-ttu-id="10d92-151">**Modifier la méthode de la \_ classe TXTType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="10d92-151">**Modify Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-modify.md)
</dt> <dt>

[<span data-ttu-id="10d92-152">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="10d92-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





