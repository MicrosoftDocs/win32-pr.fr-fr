---
title: Modifier la méthode de la classe MicrosoftDNS_WINSType
description: La méthode modify met à jour un enregistrement de ressource WINS (Windows Internet Name Service).
ms.assetid: b61c429a-6b01-4b17-9312-bc5b69d1e76a
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_WINSType classe
- MicrosoftDNS_WINSType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1469d1a9d50c72cdf3699bdc2ab9b96f51dfce86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843866"
---
# <a name="modify-method-of-the-microsoftdns_winstype-class"></a><span data-ttu-id="ffa9e-106">Modifier la méthode de la \_ classe WINSType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="ffa9e-106">Modify method of the MicrosoftDNS\_WINSType class</span></span>

<span data-ttu-id="ffa9e-107">La méthode **Modify** met à jour un enregistrement de ressource WINS (Windows Internet Name Service).</span><span class="sxs-lookup"><span data-stu-id="ffa9e-107">The **Modify** method updates a Windows Internet Name Service (WINS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffa9e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffa9e-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint32                MappingFlag,
  [in, optional] uint32                LookupTimeout,
  [in, optional] uint32                CacheTimeout,
  [in, optional] string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="ffa9e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ffa9e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffa9e-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="ffa9e-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ffa9e-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="ffa9e-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="ffa9e-112">*MappingFlag* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="ffa9e-112">*MappingFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ffa9e-113">Indicateur de mappage WINS qui spécifie si l’enregistrement doit être inclus dans la réplication de zone.</span><span class="sxs-lookup"><span data-stu-id="ffa9e-113">WINS mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="ffa9e-114">Elle ne peut avoir que deux valeurs : 0x80000000 et 0x00010000 correspondant respectivement aux indicateurs de réplication et de non-réplication (enregistrement local).</span><span class="sxs-lookup"><span data-stu-id="ffa9e-114">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span> <span data-ttu-id="ffa9e-115">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="ffa9e-115">The following values are valid.</span></span>



| <span data-ttu-id="ffa9e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffa9e-116">Value</span></span>                                                                                                                                               | <span data-ttu-id="ffa9e-117">Signification</span><span class="sxs-lookup"><span data-stu-id="ffa9e-117">Meaning</span></span>                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <span data-ttu-id="ffa9e-118"><dt>**0x80000000**</dt></span><span class="sxs-lookup"><span data-stu-id="ffa9e-118"><dt>**0x80000000**</dt></span></span> </dl> | <span data-ttu-id="ffa9e-119">Indicateur de réplication</span><span class="sxs-lookup"><span data-stu-id="ffa9e-119">Replication flag</span></span><br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <span data-ttu-id="ffa9e-120"><dt>**0x00010000**</dt></span><span class="sxs-lookup"><span data-stu-id="ffa9e-120"><dt>**0x00010000**</dt></span></span> </dl> | <span data-ttu-id="ffa9e-121">Indicateur de non-réplication (enregistrement local)</span><span class="sxs-lookup"><span data-stu-id="ffa9e-121">No-replication (local record) flag</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ffa9e-122">*LookupTimeout* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="ffa9e-122">*LookupTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ffa9e-123">Durée, en secondes, pendant laquelle un serveur DNS tente de résoudre à l’aide de la recherche WINS.</span><span class="sxs-lookup"><span data-stu-id="ffa9e-123">Time, in seconds, that a DNS Server attempts resolution using WINS Look up.</span></span>

</dd> <dt>

<span data-ttu-id="ffa9e-124">*CacheTimeout* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="ffa9e-124">*CacheTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ffa9e-125">Durée, en secondes, pendant laquelle un serveur DNS qui utilise WINS peut mettre en cache la réponse du serveur WINS.</span><span class="sxs-lookup"><span data-stu-id="ffa9e-125">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="ffa9e-126">*WinsServers* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="ffa9e-126">*WinsServers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ffa9e-127">Liste des adresses IP séparées par des virgules des serveurs WINS utilisés dans les recherches WINS.</span><span class="sxs-lookup"><span data-stu-id="ffa9e-127">List of comma-separated IP addresses of WINS servers used in WINS Look ups.</span></span>

</dd> <dt>

<span data-ttu-id="ffa9e-128">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="ffa9e-128">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ffa9e-129">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="ffa9e-129">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffa9e-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ffa9e-130">Return value</span></span>

<span data-ttu-id="ffa9e-131">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ffa9e-131">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffa9e-132">Notes</span><span class="sxs-lookup"><span data-stu-id="ffa9e-132">Remarks</span></span>

<span data-ttu-id="ffa9e-133">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="ffa9e-133">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffa9e-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffa9e-134">Requirements</span></span>



| <span data-ttu-id="ffa9e-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ffa9e-135">Requirement</span></span> | <span data-ttu-id="ffa9e-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffa9e-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffa9e-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffa9e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ffa9e-138">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffa9e-138">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ffa9e-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffa9e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ffa9e-140">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ffa9e-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ffa9e-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ffa9e-141">Namespace</span></span><br/>                | <span data-ttu-id="ffa9e-142">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="ffa9e-142">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ffa9e-143">MOF</span><span class="sxs-lookup"><span data-stu-id="ffa9e-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffa9e-144"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ffa9e-144"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffa9e-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffa9e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffa9e-146">**MicrosoftDNS \_ WINSType**</span><span class="sxs-lookup"><span data-stu-id="ffa9e-146">**MicrosoftDNS\_WINSType**</span></span>](microsoftdns-winstype.md)
</dt> <dt>

[<span data-ttu-id="ffa9e-147">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS WINSType**</span><span class="sxs-lookup"><span data-stu-id="ffa9e-147">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="ffa9e-148">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="ffa9e-148">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





