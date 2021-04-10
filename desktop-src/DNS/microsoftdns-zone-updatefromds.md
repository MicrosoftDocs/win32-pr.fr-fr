---
title: Méthode UpdateFromDS de la classe MicrosoftDNS_Zone
description: La méthode UpdateFromDS force une mise à jour de la zone à partir du service d’annuaire (DS).
ms.assetid: 471f0754-1221-4d1d-8ffd-36c1ab54b7e5
keywords:
- Méthode UpdateFromDS DNS
- Méthode UpdateFromDS DNS, classe MicrosoftDNS_Zone
- MicrosoftDNS_Zone de la classe DNS, méthode UpdateFromDS
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.UpdateFromDS
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8fd0ba4db9b182379ce2ec93508c7a3bab354a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106570"
---
# <a name="updatefromds-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="700e6-106">Méthode UpdateFromDS de la \_ classe de zone MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="700e6-106">UpdateFromDS method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="700e6-107">La méthode **UpdateFromDS** force une mise à jour de la zone à partir du service d’annuaire (DS).</span><span class="sxs-lookup"><span data-stu-id="700e6-107">The **UpdateFromDS** method forces an update of the zone from the Directory Service (DS).</span></span>

## <a name="syntax"></a><span data-ttu-id="700e6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="700e6-108">Syntax</span></span>


```mof
void UpdateFromDS();
```



## <a name="parameters"></a><span data-ttu-id="700e6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="700e6-109">Parameters</span></span>

<span data-ttu-id="700e6-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="700e6-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="700e6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="700e6-111">Return value</span></span>

<span data-ttu-id="700e6-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="700e6-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="700e6-113">Notes</span><span class="sxs-lookup"><span data-stu-id="700e6-113">Remarks</span></span>

<span data-ttu-id="700e6-114">Pour exécuter correctement cette méthode, ZoneType doit être égal à zéro et la zone doit être stockée sur le DS.</span><span class="sxs-lookup"><span data-stu-id="700e6-114">In order to successfully execute this method, the ZoneType must be zero, and the zone must be stored on the DS.</span></span>

## <a name="requirements"></a><span data-ttu-id="700e6-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="700e6-115">Requirements</span></span>



| <span data-ttu-id="700e6-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="700e6-116">Requirement</span></span> | <span data-ttu-id="700e6-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="700e6-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="700e6-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="700e6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="700e6-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="700e6-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="700e6-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="700e6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="700e6-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="700e6-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="700e6-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="700e6-122">Namespace</span></span><br/>                | <span data-ttu-id="700e6-123">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="700e6-123">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="700e6-124">MOF</span><span class="sxs-lookup"><span data-stu-id="700e6-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="700e6-125"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="700e6-125"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="700e6-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="700e6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="700e6-127">**\_Zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="700e6-127">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="700e6-128">**Méthode AgeAllRecords de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="700e6-128">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="700e6-129">**Méthode ChangeZoneType de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="700e6-129">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="700e6-130">**Méthode CreateZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="700e6-130">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="700e6-131">**Méthode ForceRefresh de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="700e6-131">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="700e6-132">**Méthode GetDistinguishedName de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="700e6-132">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="700e6-133">**Méthode PauseZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="700e6-133">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="700e6-134">**Méthode ReloadZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="700e6-134">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="700e6-135">**Méthode ResetSecondaries de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="700e6-135">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="700e6-136">**Méthode ResumeZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="700e6-136">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="700e6-137">**Méthode WriteBackZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="700e6-137">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





