---
title: Modifier la méthode de la classe MicrosoftDNS_SOAType
description: La méthode modify met à jour un enregistrement de ressource SOA (Start of Authority).
ms.assetid: 531b770d-9ac9-43da-8595-fbc175b51b23
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_SOAType classe
- MicrosoftDNS_SOAType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_SOAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff40abc7f4e93b7122a1c48889c17f9efc4f625
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032479"
---
# <a name="modify-method-of-the-microsoftdns_soatype-class"></a><span data-ttu-id="216d6-106">Modifier la méthode de la \_ classe SOAType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="216d6-106">Modify method of the MicrosoftDNS\_SOAType class</span></span>

<span data-ttu-id="216d6-107">La méthode **Modify** met à jour un enregistrement de ressource SOA (Start of Authority).</span><span class="sxs-lookup"><span data-stu-id="216d6-107">The **Modify** method updates a Start Of Authority (SOA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="216d6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="216d6-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               SerialNumber,
  [in, optional] string               PrimaryServer,
  [in, optional] string               ResponsibleParty,
  [in, optional] uint32               RefreshInterval,
  [in, optional] uint32               RetryDelay,
  [in, optional] uint32               ExpireLimit,
  [in, optional] uint32               MinimumTTL,
  [out, ref]     MicrosoftDNS_SOAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="216d6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="216d6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="216d6-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="216d6-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="216d6-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="216d6-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="216d6-112">*SerialNumber* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="216d6-112">*SerialNumber* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="216d6-113">Numéro de série SOA représentant le nombre de fois que la zone a été mise à jour, utilisée par les [*serveurs secondaires*](s-gly.md) pour déterminer si le transfert de zone est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="216d6-113">SOA serial number representing the number of times the zone has been updated, used by [*secondary servers*](s-gly.md) to determine whether zone transfer is necessary.</span></span>

</dd> <dt>

<span data-ttu-id="216d6-114">*PrimaryServer* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="216d6-114">*PrimaryServer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="216d6-115">Nom du serveur principal.</span><span class="sxs-lookup"><span data-stu-id="216d6-115">Name of the primary server.</span></span>

</dd> <dt>

<span data-ttu-id="216d6-116">*ResponsibleParty* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="216d6-116">*ResponsibleParty* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="216d6-117">Adresse de la boîte aux lettres du tiers responsable, sous la forme alias. Domain, par exemple xyz.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="216d6-117">Mailbox address of the responsible party, in the form of alias.domain, such as xyz.microsoft.com.</span></span> <span data-ttu-id="216d6-118">Notez l’utilisation d’un point plutôt que d’un symbole arobase (@).</span><span class="sxs-lookup"><span data-stu-id="216d6-118">Note the use of a period rather than an at symbol (@).</span></span>

</dd> <dt>

<span data-ttu-id="216d6-119">*RefreshInterval* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="216d6-119">*RefreshInterval* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="216d6-120">Durée, en secondes, avant l’actualisation de la zone contenant cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="216d6-120">Time, in seconds, before the zone containing this record should be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="216d6-121">*RetryDelay* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="216d6-121">*RetryDelay* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="216d6-122">Durée, en secondes, pendant laquelle le serveur DNS doit différer entre les tentatives de résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="216d6-122">Time, in seconds, the DNS Server should delay between name resolution attempts.</span></span>

</dd> <dt>

<span data-ttu-id="216d6-123">*ExpireLimit* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="216d6-123">*ExpireLimit* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="216d6-124">Durée, en secondes, pendant laquelle les serveurs secondaires doivent attendre une réponse du serveur principal avant d’ignorer leurs copies du fichier de zone comme étant non valides.</span><span class="sxs-lookup"><span data-stu-id="216d6-124">Time, in seconds, that secondary servers should wait for a response from the primary server before discarding their copies of the zone file as invalid.</span></span>

</dd> <dt>

<span data-ttu-id="216d6-125">*MinimumTTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="216d6-125">*MinimumTTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="216d6-126">Durée de vie (en secondes) appliquée aux enregistrements de ressources de la zone qui ne spécifient pas leur propre durée de vie.</span><span class="sxs-lookup"><span data-stu-id="216d6-126">TTL time, in seconds, applied to resource records in the zone that do not specify their own TTL.</span></span>

</dd> <dt>

<span data-ttu-id="216d6-127">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="216d6-127">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="216d6-128">Référence à l’objet modifié</span><span class="sxs-lookup"><span data-stu-id="216d6-128">Reference to the modified object</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="216d6-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="216d6-129">Return value</span></span>

<span data-ttu-id="216d6-130">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="216d6-130">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="216d6-131">Notes</span><span class="sxs-lookup"><span data-stu-id="216d6-131">Remarks</span></span>

<span data-ttu-id="216d6-132">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="216d6-132">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="216d6-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="216d6-133">Requirements</span></span>



| <span data-ttu-id="216d6-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="216d6-134">Requirement</span></span> | <span data-ttu-id="216d6-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="216d6-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="216d6-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="216d6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="216d6-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="216d6-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="216d6-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="216d6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="216d6-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="216d6-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="216d6-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="216d6-140">Namespace</span></span><br/>                | <span data-ttu-id="216d6-141">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="216d6-141">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="216d6-142">MOF</span><span class="sxs-lookup"><span data-stu-id="216d6-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="216d6-143"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="216d6-143"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="216d6-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="216d6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="216d6-145">**MicrosoftDNS \_ SOAType**</span><span class="sxs-lookup"><span data-stu-id="216d6-145">**MicrosoftDNS\_SOAType**</span></span>](microsoftdns-soatype.md)
</dt> <dt>

[<span data-ttu-id="216d6-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="216d6-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





