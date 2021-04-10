---
title: Méthode ResetSecondaries de la classe MicrosoftDNS_Zone
description: La méthode ResetSecondaries réinitialise les adresses IP des serveurs DNS secondaires dans la zone.
ms.assetid: b9a47714-f180-40cf-831a-f59e804a4ca2
keywords:
- Méthode ResetSecondaries DNS
- Méthode ResetSecondaries DNS, classe MicrosoftDNS_Zone
- MicrosoftDNS_Zone de la classe DNS, méthode ResetSecondaries
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ResetSecondaries
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a78d65b2153782c38d6d91d34f642860e896ed1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942447"
---
# <a name="resetsecondaries-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="77103-106">Méthode ResetSecondaries de la \_ classe de zone MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="77103-106">ResetSecondaries method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="77103-107">La méthode **ResetSecondaries** réinitialise les adresses IP des serveurs DNS secondaires dans la zone.</span><span class="sxs-lookup"><span data-stu-id="77103-107">The **ResetSecondaries** method resets the IP addresses for secondary DNS Servers in the zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="77103-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77103-108">Syntax</span></span>


```mof
void ResetSecondaries(
  [in]       string            SecondaryServers[],
  [in]       uint32            SecureSecondaries,
  [in]       string            NotifyServers[],
  [in]       uint32            Notify,
  [out, ref] MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a><span data-ttu-id="77103-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77103-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77103-110">*SecondaryServers* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77103-110">*SecondaryServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77103-111">Tableau d’adresses IP pour les serveurs DNS secondaires.</span><span class="sxs-lookup"><span data-stu-id="77103-111">Array of IP addresses for secondary DNS Servers.</span></span>

</dd> <dt>

<span data-ttu-id="77103-112">*SecureSecondaries* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77103-112">*SecureSecondaries* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77103-113">Spécifie la sécurité à appliquer et doit être l’une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="77103-113">Specifies the security to be applied and must be one of the following:</span></span>

-   <span data-ttu-id="77103-114">SECSECURE de la ZONE \_ \_ pas de \_ sécurité</span><span class="sxs-lookup"><span data-stu-id="77103-114">ZONE\_SECSECURE\_NO\_SECURITY</span></span>
-   <span data-ttu-id="77103-115">ZONE \_ SECSECURE \_ NS \_ uniquement</span><span class="sxs-lookup"><span data-stu-id="77103-115">ZONE\_SECSECURE\_NS\_ONLY</span></span>
-   <span data-ttu-id="77103-116">Liste des SECSECURE de ZONE \_ \_ \_ uniquement</span><span class="sxs-lookup"><span data-stu-id="77103-116">ZONE\_SECSECURE\_LIST\_ONLY</span></span>
-   <span data-ttu-id="77103-117">ZONE \_ SECSECURE \_ no \_ XFR</span><span class="sxs-lookup"><span data-stu-id="77103-117">ZONE\_SECSECURE\_NO\_XFR</span></span>

</dd> <dt>

<span data-ttu-id="77103-118">*NotifyServers* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77103-118">*NotifyServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77103-119">Adresse IP des serveurs DNS à notifier en cas de modification de la zone.</span><span class="sxs-lookup"><span data-stu-id="77103-119">IP address of DNS Servers to be notified when the zone changes.</span></span>

</dd> <dt>

<span data-ttu-id="77103-120">*Notifier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77103-120">*Notify* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77103-121">Paramètre de notification et doit avoir l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="77103-121">Notification setting and must be one of the following:</span></span>

-   <span data-ttu-id="77103-122">notification de ZONE \_ \_ désactivée</span><span class="sxs-lookup"><span data-stu-id="77103-122">ZONE\_NOTIFY\_OFF</span></span>
-   <span data-ttu-id="77103-123">\_notifier \_ tous les secondaires de zone \_</span><span class="sxs-lookup"><span data-stu-id="77103-123">ZONE\_NOTIFY\_ALL\_SECONDARIES</span></span>
-   <span data-ttu-id="77103-124">\_liste des notifications de zone \_ \_ uniquement</span><span class="sxs-lookup"><span data-stu-id="77103-124">ZONE\_NOTIFY\_LIST\_ONLY</span></span>

</dd> <dt>

<span data-ttu-id="77103-125">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="77103-125">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="77103-126">RR de type [**MicrosoftDNS \_ zone**](microsoftdns-zone.md).</span><span class="sxs-lookup"><span data-stu-id="77103-126">RR of type [**MicrosoftDNS\_Zone**](microsoftdns-zone.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77103-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="77103-127">Return value</span></span>

<span data-ttu-id="77103-128">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="77103-128">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="77103-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77103-129">Requirements</span></span>



| <span data-ttu-id="77103-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77103-130">Requirement</span></span> | <span data-ttu-id="77103-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="77103-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="77103-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77103-132">Minimum supported client</span></span><br/> | <span data-ttu-id="77103-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="77103-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="77103-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77103-134">Minimum supported server</span></span><br/> | <span data-ttu-id="77103-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77103-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="77103-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="77103-136">Namespace</span></span><br/>                | <span data-ttu-id="77103-137">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="77103-137">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="77103-138">MOF</span><span class="sxs-lookup"><span data-stu-id="77103-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77103-139"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="77103-139"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77103-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77103-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77103-141">**\_Zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="77103-141">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="77103-142">**Méthode AgeAllRecords de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="77103-142">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="77103-143">**Méthode ChangeZoneType de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="77103-143">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="77103-144">**Méthode CreateZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="77103-144">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="77103-145">**Méthode ForceRefresh de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="77103-145">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="77103-146">**Méthode GetDistinguishedName de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="77103-146">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="77103-147">**Méthode PauseZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="77103-147">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="77103-148">**Méthode ReloadZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="77103-148">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="77103-149">**Méthode ResumeZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="77103-149">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="77103-150">**Méthode UpdateFromDS de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="77103-150">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="77103-151">**Méthode WriteBackZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="77103-151">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





