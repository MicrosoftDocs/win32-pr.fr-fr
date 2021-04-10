---
title: Méthode ReloadZone de la classe MicrosoftDNS_Zone
description: La méthode ReloadZone recharge la zone DNS à partir de sa base de données.
ms.assetid: 9fb3c216-563c-4603-a29a-27627ac644d8
keywords:
- Méthode ReloadZone DNS
- Méthode ReloadZone DNS, classe MicrosoftDNS_Zone
- MicrosoftDNS_Zone de la classe DNS, méthode ReloadZone
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ReloadZone
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60e22d9becc5084407267e75d713082ce5dcbb73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942448"
---
# <a name="reloadzone-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="cb3a0-106">Méthode ReloadZone de la \_ classe de zone MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="cb3a0-106">ReloadZone method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="cb3a0-107">La méthode **ReloadZone** recharge la zone DNS à partir de sa base de données.</span><span class="sxs-lookup"><span data-stu-id="cb3a0-107">The **ReloadZone** method reloads the DNS Zone from its database.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb3a0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb3a0-108">Syntax</span></span>


```mof
void ReloadZone();
```



## <a name="parameters"></a><span data-ttu-id="cb3a0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb3a0-109">Parameters</span></span>

<span data-ttu-id="cb3a0-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="cb3a0-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cb3a0-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cb3a0-111">Return value</span></span>

<span data-ttu-id="cb3a0-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="cb3a0-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb3a0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb3a0-113">Requirements</span></span>



| <span data-ttu-id="cb3a0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb3a0-114">Requirement</span></span> | <span data-ttu-id="cb3a0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb3a0-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb3a0-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb3a0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cb3a0-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb3a0-117">None supported</span></span><br/>                                                              |
| <span data-ttu-id="cb3a0-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb3a0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cb3a0-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb3a0-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cb3a0-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cb3a0-120">Namespace</span></span><br/>                | <span data-ttu-id="cb3a0-121">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="cb3a0-121">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="cb3a0-122">MOF</span><span class="sxs-lookup"><span data-stu-id="cb3a0-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb3a0-123"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb3a0-123"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb3a0-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb3a0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb3a0-125">**\_Zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="cb3a0-125">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="cb3a0-126">**Méthode AgeAllRecords de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="cb3a0-126">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="cb3a0-127">**Méthode ChangeZoneType de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="cb3a0-127">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="cb3a0-128">**Méthode CreateZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="cb3a0-128">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="cb3a0-129">**Méthode ForceRefresh de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="cb3a0-129">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="cb3a0-130">**Méthode GetDistinguishedName de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="cb3a0-130">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="cb3a0-131">**Méthode PauseZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="cb3a0-131">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="cb3a0-132">**Méthode ResetSecondaries de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="cb3a0-132">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="cb3a0-133">**Méthode ResumeZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="cb3a0-133">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="cb3a0-134">**Méthode UpdateFromDS de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="cb3a0-134">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="cb3a0-135">**Méthode WriteBackZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="cb3a0-135">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





