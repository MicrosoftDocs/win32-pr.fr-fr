---
title: Méthode ChangeZoneType de la classe MicrosoftDNS_Zone
description: La méthode ChangeZoneType modifie le type d’une zone.
ms.assetid: a0a9f495-fdbb-4258-a313-ee9551da762f
keywords:
- Méthode ChangeZoneType DNS
- Méthode ChangeZoneType DNS, classe MicrosoftDNS_Zone
- MicrosoftDNS_Zone de la classe DNS, méthode ChangeZoneType
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ChangeZoneType
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1611eda876532f32534e24257478b3a5986af3aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032738"
---
# <a name="changezonetype-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="25ff4-106">Méthode ChangeZoneType de la \_ classe de zone MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="25ff4-106">ChangeZoneType method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="25ff4-107">La méthode **ChangeZoneType** modifie le type d’une zone.</span><span class="sxs-lookup"><span data-stu-id="25ff4-107">The **ChangeZoneType** method changes the type of a zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="25ff4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25ff4-108">Syntax</span></span>


```mof
void ChangeZoneType(
  [in]           uint32            ZoneType,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a><span data-ttu-id="25ff4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25ff4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25ff4-110">*ZoneType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="25ff4-110">*ZoneType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25ff4-111">Type de zone.</span><span class="sxs-lookup"><span data-stu-id="25ff4-111">Type of zone.</span></span> <span data-ttu-id="25ff4-112">Les valeurs suivantes sont valides :</span><span class="sxs-lookup"><span data-stu-id="25ff4-112">Valid values are the following:</span></span>



| <span data-ttu-id="25ff4-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="25ff4-113">Value</span></span>                                                                        | <span data-ttu-id="25ff4-114">Signification</span><span class="sxs-lookup"><span data-stu-id="25ff4-114">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="25ff4-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="25ff4-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="25ff4-116">Zone principale.</span><span class="sxs-lookup"><span data-stu-id="25ff4-116">Primary zone.</span></span><br/>   |
| <dl> <span data-ttu-id="25ff4-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="25ff4-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="25ff4-118">Zone secondaire.</span><span class="sxs-lookup"><span data-stu-id="25ff4-118">Secondary zone.</span></span><br/> |
| <dl> <span data-ttu-id="25ff4-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="25ff4-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="25ff4-120">Zone de stub.</span><span class="sxs-lookup"><span data-stu-id="25ff4-120">Stub zone.</span></span><br/>      |
| <dl> <span data-ttu-id="25ff4-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="25ff4-121"><dt>3</dt></span></span> </dl> | <span data-ttu-id="25ff4-122">Redirecteur de zone.</span><span class="sxs-lookup"><span data-stu-id="25ff4-122">Zone forwarder.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="25ff4-123">*DataFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="25ff4-123">*DataFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="25ff4-124">Nom du fichier de données associé à la zone.</span><span class="sxs-lookup"><span data-stu-id="25ff4-124">Name of the data file associated with the zone.</span></span>

</dd> <dt>

<span data-ttu-id="25ff4-125">*Ipaddr* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="25ff4-125">*IpAddr* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="25ff4-126">Adresse IP du serveur DNS maître pour la zone.</span><span class="sxs-lookup"><span data-stu-id="25ff4-126">IP address of the mater DNS Server for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="25ff4-127">*AdminEmailName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="25ff4-127">*AdminEmailName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="25ff4-128">Adresse de messagerie de l’administrateur responsable de la zone.</span><span class="sxs-lookup"><span data-stu-id="25ff4-128">Email address of the administrator responsible for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="25ff4-129">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="25ff4-129">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="25ff4-130">RR de type **MicrosoftDns \_ zone**.</span><span class="sxs-lookup"><span data-stu-id="25ff4-130">RR of type **MicrosoftDns\_Zone**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25ff4-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="25ff4-131">Return value</span></span>

<span data-ttu-id="25ff4-132">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="25ff4-132">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="25ff4-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25ff4-133">Requirements</span></span>



| <span data-ttu-id="25ff4-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25ff4-134">Requirement</span></span> | <span data-ttu-id="25ff4-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="25ff4-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25ff4-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25ff4-136">Minimum supported client</span></span><br/> | <span data-ttu-id="25ff4-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="25ff4-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="25ff4-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25ff4-138">Minimum supported server</span></span><br/> | <span data-ttu-id="25ff4-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25ff4-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="25ff4-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="25ff4-140">Namespace</span></span><br/>                | <span data-ttu-id="25ff4-141">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="25ff4-141">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="25ff4-142">MOF</span><span class="sxs-lookup"><span data-stu-id="25ff4-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25ff4-143"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25ff4-143"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25ff4-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25ff4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25ff4-145">**\_Zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="25ff4-145">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="25ff4-146">**Méthode AgeAllRecords de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="25ff4-146">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="25ff4-147">**Méthode CreateZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="25ff4-147">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="25ff4-148">**Méthode ForceRefresh de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="25ff4-148">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="25ff4-149">**Méthode GetDistinguishedName de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="25ff4-149">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="25ff4-150">**Méthode PauseZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="25ff4-150">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="25ff4-151">**Méthode ReloadZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="25ff4-151">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="25ff4-152">**Méthode ResetSecondaries de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="25ff4-152">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="25ff4-153">**Méthode ResumeZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="25ff4-153">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="25ff4-154">**Méthode UpdateFromDS de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="25ff4-154">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="25ff4-155">**Méthode WriteBackZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="25ff4-155">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





