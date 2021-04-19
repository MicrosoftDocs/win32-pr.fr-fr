---
title: Méthode ForceRefresh de la classe MicrosoftDNS_Zone
description: La méthode ForceRefresh force une mise à jour du serveur DNS secondaire à partir du serveur maître.
ms.assetid: 8dde1703-53c3-4d1e-bfb3-f6d5d1666740
keywords:
- Méthode ForceRefresh DNS
- Méthode ForceRefresh DNS, classe MicrosoftDNS_Zone
- MicrosoftDNS_Zone de la classe DNS, méthode ForceRefresh
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ForceRefresh
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85390230b0a0852ee479bc8b7e396972f6e69080
ms.sourcegitcommit: 03fb201e1ea36e353c335ff063ed993fb5993e61
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515519"
---
# <a name="forcerefresh-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="46846-106">Méthode ForceRefresh de la \_ classe de zone MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="46846-106">ForceRefresh method of the MicrosoftDNS\_Zone class</span></span>

> [!NOTE]
> <span data-ttu-id="46846-107">Cet article contient des références au terme serveur maître, un terme que Microsoft n’utilise plus.</span><span class="sxs-lookup"><span data-stu-id="46846-107">This article contains references to the term master server, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="46846-108">Lorsque le terme sera supprimé du logiciel, nous le supprimerons de cet article.</span><span class="sxs-lookup"><span data-stu-id="46846-108">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="46846-109">La méthode **ForceRefresh** force une mise à jour du serveur DNS secondaire à partir du serveur maître.</span><span class="sxs-lookup"><span data-stu-id="46846-109">The **ForceRefresh** method forces an update of the secondary DNS Server from the master server.</span></span>

## <a name="syntax"></a><span data-ttu-id="46846-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46846-110">Syntax</span></span>


```mof
void ForceRefresh();
```



## <a name="parameters"></a><span data-ttu-id="46846-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46846-111">Parameters</span></span>

<span data-ttu-id="46846-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="46846-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="46846-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="46846-113">Return value</span></span>

<span data-ttu-id="46846-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="46846-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="46846-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46846-115">Requirements</span></span>



| <span data-ttu-id="46846-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46846-116">Requirement</span></span> | <span data-ttu-id="46846-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="46846-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46846-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46846-118">Minimum supported client</span></span><br/> | <span data-ttu-id="46846-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="46846-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="46846-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46846-120">Minimum supported server</span></span><br/> | <span data-ttu-id="46846-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46846-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="46846-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="46846-122">Namespace</span></span><br/>                | <span data-ttu-id="46846-123">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="46846-123">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="46846-124">MOF</span><span class="sxs-lookup"><span data-stu-id="46846-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46846-125"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46846-125"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46846-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46846-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46846-127">**\_Zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="46846-127">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="46846-128">**Méthode AgeAllRecords de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="46846-128">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="46846-129">**Méthode ChangeZoneType de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="46846-129">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="46846-130">**Méthode CreateZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="46846-130">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="46846-131">**Méthode GetDistinguishedName de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="46846-131">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="46846-132">**Méthode PauseZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="46846-132">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="46846-133">**Méthode ReloadZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="46846-133">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="46846-134">**Méthode ResetSecondaries de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="46846-134">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="46846-135">**Méthode ResumeZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="46846-135">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="46846-136">**Méthode UpdateFromDS de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="46846-136">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="46846-137">**Méthode WriteBackZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="46846-137">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





