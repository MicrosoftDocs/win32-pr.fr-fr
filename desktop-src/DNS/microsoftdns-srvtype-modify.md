---
title: Modifier la méthode de la classe MicrosoftDNS_SRVType
description: La méthode modify met à jour un enregistrement de ressource de service (SRV).
ms.assetid: 626483c9-4b36-4e62-b9ad-dd7bb18f2e1e
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_SRVType classe
- MicrosoftDNS_SRVType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1174e7a8096d70a3e6305a5d24b9ae1f4915096e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033191"
---
# <a name="modify-method-of-the-microsoftdns_srvtype-class"></a><span data-ttu-id="33ad1-106">Modifier la méthode de la \_ classe SRVType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="33ad1-106">Modify method of the MicrosoftDNS\_SRVType class</span></span>

<span data-ttu-id="33ad1-107">La méthode **Modify** met à jour un enregistrement de ressource de service (SRV).</span><span class="sxs-lookup"><span data-stu-id="33ad1-107">The **Modify** method updates a Service (SRV) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="33ad1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33ad1-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Priority,
  [in, optional] uint16               Weight,
  [in, optional] uint16               Port,
  [in, optional] string               SRVDomainName,
  [out, ref]     MicrosoftDNS_SRVType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="33ad1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33ad1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33ad1-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="33ad1-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="33ad1-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="33ad1-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="33ad1-112">*Priorité* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="33ad1-112">*Priority* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="33ad1-113">Priorité de l’hôte cible spécifiée dans le nom du propriétaire.</span><span class="sxs-lookup"><span data-stu-id="33ad1-113">Priority of the target host specified in the owner name.</span></span> <span data-ttu-id="33ad1-114">Les nombres inférieurs impliquent des priorités plus élevées.</span><span class="sxs-lookup"><span data-stu-id="33ad1-114">Lower numbers imply higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="33ad1-115">*Poids* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="33ad1-115">*Weight* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="33ad1-116">Poids de l’hôte cible.</span><span class="sxs-lookup"><span data-stu-id="33ad1-116">Weight of the target host.</span></span> <span data-ttu-id="33ad1-117">Cela est utile lorsque vous sélectionnez parmi les hôtes qui ont la même priorité.</span><span class="sxs-lookup"><span data-stu-id="33ad1-117">This is useful when selecting among hosts that have the same priority.</span></span> <span data-ttu-id="33ad1-118">La probabilité d’utiliser cet hôte doit être proportionnelle à son poids.</span><span class="sxs-lookup"><span data-stu-id="33ad1-118">The chances of using this host should be proportional to its weight.</span></span>

</dd> <dt>

<span data-ttu-id="33ad1-119">*Port* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="33ad1-119">*Port* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="33ad1-120">Port utilisé sur l’hôte cible d’un service de protocole.</span><span class="sxs-lookup"><span data-stu-id="33ad1-120">Port used on the target host of a protocol service.</span></span>

</dd> <dt>

<span data-ttu-id="33ad1-121">*SRVDomainName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="33ad1-121">*SRVDomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="33ad1-122">Nom de domaine complet de l’hôte cible.</span><span class="sxs-lookup"><span data-stu-id="33ad1-122">FQDN of the target host.</span></span> <span data-ttu-id="33ad1-123">Une cible de \\ . \\ signifie que le service n’est pas disponible dans ce domaine.</span><span class="sxs-lookup"><span data-stu-id="33ad1-123">A target of \\.\\ means that the service is decidedly not available at this domain.</span></span>

</dd> <dt>

<span data-ttu-id="33ad1-124">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="33ad1-124">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="33ad1-125">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="33ad1-125">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33ad1-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="33ad1-126">Return value</span></span>

<span data-ttu-id="33ad1-127">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="33ad1-127">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="33ad1-128">Notes</span><span class="sxs-lookup"><span data-stu-id="33ad1-128">Remarks</span></span>

<span data-ttu-id="33ad1-129">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="33ad1-129">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="33ad1-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33ad1-130">Requirements</span></span>



| <span data-ttu-id="33ad1-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33ad1-131">Requirement</span></span> | <span data-ttu-id="33ad1-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="33ad1-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33ad1-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33ad1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="33ad1-134">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="33ad1-134">None supported</span></span><br/>                                                              |
| <span data-ttu-id="33ad1-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33ad1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="33ad1-136">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33ad1-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="33ad1-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="33ad1-137">Namespace</span></span><br/>                | <span data-ttu-id="33ad1-138">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="33ad1-138">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="33ad1-139">MOF</span><span class="sxs-lookup"><span data-stu-id="33ad1-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33ad1-140"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33ad1-140"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33ad1-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33ad1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33ad1-142">**MicrosoftDNS \_ SRVType**</span><span class="sxs-lookup"><span data-stu-id="33ad1-142">**MicrosoftDNS\_SRVType**</span></span>](microsoftdns-srvtype.md)
</dt> <dt>

[<span data-ttu-id="33ad1-143">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS SRVType**</span><span class="sxs-lookup"><span data-stu-id="33ad1-143">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="33ad1-144">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="33ad1-144">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





