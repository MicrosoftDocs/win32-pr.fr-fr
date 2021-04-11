---
title: Modifier la méthode de la classe MicrosoftDNS_WINSRType
description: La méthode modify met à jour un enregistrement de ressource WINSR de recherche inversée (WINSr).
ms.assetid: 28be0045-5b0d-4434-a2a9-b56191f1e213
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_WINSRType classe
- MicrosoftDNS_WINSRType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02d89c3cd191262136035f9006853e2f1a7f7dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105934"
---
# <a name="modify-method-of-the-microsoftdns_winsrtype-class"></a><span data-ttu-id="6c86d-106">Modifier la méthode de la \_ classe WINSRType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="6c86d-106">Modify method of the MicrosoftDNS\_WINSRType class</span></span>

<span data-ttu-id="6c86d-107">La méthode **Modify** met à jour un enregistrement de ressource WINSR de recherche inversée (WINSR).</span><span class="sxs-lookup"><span data-stu-id="6c86d-107">The **Modify** method updates a WINS Reverse Look up (WINSR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c86d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c86d-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint32                 MappingFlag,
  [in, optional] uint32                 LookupTimeout,
  [in, optional] uint32                 CacheTimeout,
  [in, optional] string                 ResultDomain,
  [out, ref]     MicrosoftDNS_WINSRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="6c86d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c86d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c86d-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="6c86d-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6c86d-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="6c86d-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="6c86d-112">*MappingFlag* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="6c86d-112">*MappingFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6c86d-113">Indicateur de mappage WINSr qui spécifie si l’enregistrement doit être inclus dans la réplication de zone.</span><span class="sxs-lookup"><span data-stu-id="6c86d-113">WINSR mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="6c86d-114">Elle ne peut avoir que deux valeurs : 0x80000000 et 0x00010000 correspondant respectivement aux indicateurs de réplication et de non-réplication (enregistrement local).</span><span class="sxs-lookup"><span data-stu-id="6c86d-114">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="6c86d-115">*LookupTimeout* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="6c86d-115">*LookupTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6c86d-116">Délai d’attente, en secondes, pour un serveur DNS à l’aide de la recherche inversée WINS.</span><span class="sxs-lookup"><span data-stu-id="6c86d-116">Time out, in seconds, for a DNS Server using WINS Reverse Look up.</span></span>

</dd> <dt>

<span data-ttu-id="6c86d-117">*CacheTimeout* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="6c86d-117">*CacheTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6c86d-118">Durée, en secondes, pendant laquelle un serveur DNS utilisant WINS recherche peut mettre en cache la réponse du serveur WINS.</span><span class="sxs-lookup"><span data-stu-id="6c86d-118">Time, in seconds, a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="6c86d-119">*ResultDomain* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="6c86d-119">*ResultDomain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6c86d-120">Nom de domaine à ajouter aux noms NetBIOS retournés.</span><span class="sxs-lookup"><span data-stu-id="6c86d-120">Domain name to append to returned NetBIOS names.</span></span>

</dd> <dt>

<span data-ttu-id="6c86d-121">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="6c86d-121">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="6c86d-122">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="6c86d-122">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c86d-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6c86d-123">Return value</span></span>

<span data-ttu-id="6c86d-124">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6c86d-124">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c86d-125">Notes</span><span class="sxs-lookup"><span data-stu-id="6c86d-125">Remarks</span></span>

<span data-ttu-id="6c86d-126">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="6c86d-126">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c86d-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c86d-127">Requirements</span></span>



| <span data-ttu-id="6c86d-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c86d-128">Requirement</span></span> | <span data-ttu-id="6c86d-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c86d-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c86d-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c86d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6c86d-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c86d-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6c86d-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c86d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6c86d-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6c86d-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6c86d-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6c86d-134">Namespace</span></span><br/>                | <span data-ttu-id="6c86d-135">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="6c86d-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="6c86d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="6c86d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c86d-137"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c86d-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c86d-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c86d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c86d-139">**MicrosoftDNS \_ WINSRType**</span><span class="sxs-lookup"><span data-stu-id="6c86d-139">**MicrosoftDNS\_WINSRType**</span></span>](microsoftdns-winsrtype.md)
</dt> <dt>

[<span data-ttu-id="6c86d-140">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS WINSRType**</span><span class="sxs-lookup"><span data-stu-id="6c86d-140">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="6c86d-141">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="6c86d-141">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





