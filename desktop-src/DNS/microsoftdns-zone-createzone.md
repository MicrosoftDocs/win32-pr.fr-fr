---
title: Méthode CreateZone de la classe MicrosoftDNS_Zone
description: La méthode CreateZone crée une zone DNS.
ms.assetid: 55756284-20ef-4d38-a8d9-357f53a6fa4d
keywords:
- Méthode CreateZone DNS
- Méthode CreateZone DNS, classe MicrosoftDNS_Zone
- MicrosoftDNS_Zone de la classe DNS, méthode CreateZone
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.CreateZone
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7e3780db9036e0fd7c87d91c769c3c6f5c6aaf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033036"
---
# <a name="createzone-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="5c002-106">Méthode CreateZone de la \_ classe de zone MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="5c002-106">CreateZone method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="5c002-107">La méthode **CreateZone** crée une zone DNS.</span><span class="sxs-lookup"><span data-stu-id="5c002-107">The **CreateZone** method creates a DNS zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c002-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c002-108">Syntax</span></span>


```mof
void CreateZone(
  [in]           string            ZoneName,
  [in]           uint32            ZoneType,
  [in]           boolean           DsIntegrated,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a><span data-ttu-id="5c002-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c002-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c002-110">*NomZone* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5c002-110">*ZoneName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c002-111">Chaîne représentant le nom de la zone.</span><span class="sxs-lookup"><span data-stu-id="5c002-111">String representing the name of the zone.</span></span>

</dd> <dt>

<span data-ttu-id="5c002-112">*ZoneType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5c002-112">*ZoneType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c002-113">Type de zone.</span><span class="sxs-lookup"><span data-stu-id="5c002-113">Type of zone.</span></span> <span data-ttu-id="5c002-114">Les valeurs suivantes sont valides :</span><span class="sxs-lookup"><span data-stu-id="5c002-114">Valid values are the following:</span></span>



| <span data-ttu-id="5c002-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c002-115">Value</span></span>                                                                        | <span data-ttu-id="5c002-116">Signification</span><span class="sxs-lookup"><span data-stu-id="5c002-116">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5c002-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5c002-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="5c002-118">AD intégré.</span><span class="sxs-lookup"><span data-stu-id="5c002-118">AD integrated.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="5c002-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5c002-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="5c002-120">Zone secondaire.</span><span class="sxs-lookup"><span data-stu-id="5c002-120">Secondary zone.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="5c002-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="5c002-121"><dt>3</dt></span></span> </dl> | <span data-ttu-id="5c002-122">Zone de stub.</span><span class="sxs-lookup"><span data-stu-id="5c002-122">Stub zone.</span></span><br/> <span data-ttu-id="5c002-123">**Windows Server 2003 :** Ce type de zone est introduit dans Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5c002-123">**Windows Server 2003:** This zone type is introduced in Windows Server 2003.</span></span><br/>      |
| <dl> <span data-ttu-id="5c002-124"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="5c002-124"><dt>4</dt></span></span> </dl> | <span data-ttu-id="5c002-125">Redirecteur de zone.</span><span class="sxs-lookup"><span data-stu-id="5c002-125">Zone forwarder.</span></span><br/> <span data-ttu-id="5c002-126">**Windows Server 2003 :** Ce type de zone est introduit dans Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5c002-126">**Windows Server 2003:** This zone type is introduced in Windows Server 2003.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5c002-127">*DsIntegrated* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5c002-127">*DsIntegrated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c002-128">Indique si les données de zone sont stockées dans le Active Directory ou dans des fichiers.</span><span class="sxs-lookup"><span data-stu-id="5c002-128">Indicates whether zone data is stored in the Active Directory or in files.</span></span> <span data-ttu-id="5c002-129">Si la valeur est TRUE, les données sont stockées dans le Active Directory ; Si la valeur est FALSe, les données sont stockées dans des fichiers.</span><span class="sxs-lookup"><span data-stu-id="5c002-129">If TRUE, the data is stored in the Active Directory; if FALSE, the data is stored in files.</span></span>

</dd> <dt>

<span data-ttu-id="5c002-130">*DataFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5c002-130">*DataFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5c002-131">Nom du fichier de données associé à la zone.</span><span class="sxs-lookup"><span data-stu-id="5c002-131">Name of the data file associated with the zone.</span></span>

</dd> <dt>

<span data-ttu-id="5c002-132">*Ipaddr* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5c002-132">*IpAddr* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5c002-133">Adresse IP du serveur DNS maître pour la zone.</span><span class="sxs-lookup"><span data-stu-id="5c002-133">IP address of the master DNS Server for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="5c002-134">*AdminEmailName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5c002-134">*AdminEmailName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5c002-135">Adresse de messagerie de l’administrateur responsable de la zone.</span><span class="sxs-lookup"><span data-stu-id="5c002-135">Email address of the administrator responsible for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="5c002-136">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="5c002-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="5c002-137">RR de type **MicrosoftDns \_ zone**.</span><span class="sxs-lookup"><span data-stu-id="5c002-137">RR of type **MicrosoftDns\_Zone**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c002-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5c002-138">Return value</span></span>

<span data-ttu-id="5c002-139">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5c002-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c002-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c002-140">Requirements</span></span>



| <span data-ttu-id="5c002-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c002-141">Requirement</span></span> | <span data-ttu-id="5c002-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c002-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c002-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c002-143">Minimum supported client</span></span><br/> | <span data-ttu-id="5c002-144">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c002-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5c002-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c002-145">Minimum supported server</span></span><br/> | <span data-ttu-id="5c002-146">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c002-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5c002-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5c002-147">Namespace</span></span><br/>                | <span data-ttu-id="5c002-148">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="5c002-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="5c002-149">MOF</span><span class="sxs-lookup"><span data-stu-id="5c002-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c002-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c002-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c002-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c002-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c002-152">**\_Zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="5c002-152">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="5c002-153">**Méthode AgeAllRecords de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="5c002-153">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="5c002-154">**Méthode ChangeZoneType de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="5c002-154">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="5c002-155">**Méthode ForceRefresh de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="5c002-155">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="5c002-156">**Méthode GetDistinguishedName de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="5c002-156">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="5c002-157">**Méthode PauseZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="5c002-157">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="5c002-158">**Méthode ReloadZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="5c002-158">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="5c002-159">**Méthode ResetSecondaries de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="5c002-159">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="5c002-160">**Méthode ResumeZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="5c002-160">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="5c002-161">**Méthode UpdateFromDS de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="5c002-161">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="5c002-162">**Méthode WriteBackZone de la \_ classe de zone MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="5c002-162">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





