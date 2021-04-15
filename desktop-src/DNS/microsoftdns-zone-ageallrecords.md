---
title: Méthode AgeAllRecords de la classe MicrosoftDNS_Zone
description: La méthode AgeAllRecords active l’antériorité pour tout ou partie des enregistrements non NS et non SOA dans une zone.
ms.assetid: 0e0df1ab-6c7c-4bc4-b292-8f89095970eb
keywords:
- Méthode AgeAllRecords DNS
- Méthode AgeAllRecords DNS, classe MicrosoftDNS_Zone
- MicrosoftDNS_Zone de la classe DNS, méthode AgeAllRecords
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.AgeAllRecords
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c70a1435f96091070b2aee4ed7f079e5a6529a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466482"
---
# <a name="ageallrecords-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="6d636-106">Méthode AgeAllRecords de la \_ classe de zone MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="6d636-106">AgeAllRecords method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="6d636-107">La méthode **AgeAllRecords** active l’antériorité pour tout ou partie des enregistrements non NS et non SOA dans une zone.</span><span class="sxs-lookup"><span data-stu-id="6d636-107">The **AgeAllRecords** method enables aging for some or all non-NS and non-SOA records in a zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d636-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d636-108">Syntax</span></span>


```mof
uint32 AgeAllRecords(
  [in, optional] string  NodeName,
  [in, optional] boolean ApplyToSubtree
);
```



## <a name="parameters"></a><span data-ttu-id="6d636-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d636-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d636-110">*Nodename* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="6d636-110">*NodeName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6d636-111">Nom du nœud à vieillir.</span><span class="sxs-lookup"><span data-stu-id="6d636-111">Name of the node to age.</span></span>

</dd> <dt>

<span data-ttu-id="6d636-112">*ApplyToSubtree* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="6d636-112">*ApplyToSubtree* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6d636-113">Spécifie si l’antériorité doit s’appliquer à tous les enregistrements dans la sous-arborescence.</span><span class="sxs-lookup"><span data-stu-id="6d636-113">Specifies whether aging should apply to all records in the subtree.</span></span> <span data-ttu-id="6d636-114">Affectez la valeur TRUE pour appliquer l’antériorité à tous les enregistrements de la sous-arborescence, en commençant par NodeName.</span><span class="sxs-lookup"><span data-stu-id="6d636-114">Set to TRUE to apply aging to all records in the subtree, beginning with NodeName.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d636-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6d636-115">Return value</span></span>

<span data-ttu-id="6d636-116">ERREUR \_ : la datation a été effectuée avec succès.</span><span class="sxs-lookup"><span data-stu-id="6d636-116">ERROR\_SUCCESS indicates the aging was successfully completed.</span></span> <span data-ttu-id="6d636-117">Toute autre valeur est un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="6d636-117">Any other value is an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d636-118">Notes</span><span class="sxs-lookup"><span data-stu-id="6d636-118">Remarks</span></span>

<span data-ttu-id="6d636-119">Si *nodename* n’est pas spécifié, tous les enregistrements sont soumis au vieillissement et au nettoyage.</span><span class="sxs-lookup"><span data-stu-id="6d636-119">If *NodeName* is not specified, all records will be subject to aging and scavenging.</span></span>

<span data-ttu-id="6d636-120">Si *nodename* est spécifié et que *ApplyToSubtree* n’est pas spécifié ou défini à zéro, les enregistrements au niveau du nœud spécifié seront soumis au vieillissement et au nettoyage.</span><span class="sxs-lookup"><span data-stu-id="6d636-120">If *NodeName* is specified and *ApplyToSubtree* is not specified or set to zero, records at the specified node will be subjected to aging and scavenging.</span></span>

<span data-ttu-id="6d636-121">Si *nodename* est spécifié et que *ApplyToSubtree* a la valeur 1, tous les enregistrements de la sous-arborescence commençant à *nodename* sont soumis à la datation et au nettoyage.</span><span class="sxs-lookup"><span data-stu-id="6d636-121">If *NodeName* is specified and *ApplyToSubtree* is set to 1, all records of the subtree starting at *NodeName* will be subjected to aging and scavenging.</span></span> <span data-ttu-id="6d636-122">L’horodatage est défini sur l’heure actuelle pour tous les enregistrements de ressource non-NS et non SOA avec le ou les noms de propriétaires identifiés par les paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="6d636-122">The time stamp is set to the current time for all non-NS and non-SOA RRs with the owner name(s) identified by the input parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d636-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d636-123">Requirements</span></span>



| <span data-ttu-id="6d636-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d636-124">Requirement</span></span> | <span data-ttu-id="6d636-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d636-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d636-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d636-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6d636-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d636-127">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6d636-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d636-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6d636-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d636-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6d636-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6d636-130">Namespace</span></span><br/>                | <span data-ttu-id="6d636-131">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="6d636-131">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="6d636-132">MOF</span><span class="sxs-lookup"><span data-stu-id="6d636-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d636-133"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d636-133"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d636-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d636-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d636-135">**\_Zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6d636-135">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="6d636-136">**Méthode ChangeZoneType de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6d636-136">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="6d636-137">**Méthode CreateZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6d636-137">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="6d636-138">**Méthode ForceRefresh de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6d636-138">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="6d636-139">**Méthode GetDistinguishedName de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6d636-139">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="6d636-140">**Méthode PauseZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6d636-140">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="6d636-141">**Méthode ReloadZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6d636-141">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="6d636-142">**Méthode ResetSecondaries de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6d636-142">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="6d636-143">**Méthode ResumeZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6d636-143">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="6d636-144">**Méthode UpdateFromDS de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6d636-144">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="6d636-145">**Méthode WriteBackZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6d636-145">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





