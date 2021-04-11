---
title: Classe MicrosoftDNS_SOAType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement SOA (Start of Authority).
ms.assetid: a5e6b6d3-7f5d-42e2-b3ed-2786f7aafb14
keywords:
- MicrosoftDNS_SOAType de la classe DNS
- MicrosoftDNS_SOAType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_SOAType
- MicrosoftDNS_SOAType.Modify
- MicrosoftDNS_SOAType.SerialNumber
- MicrosoftDNS_SOAType.PrimaryServer
- MicrosoftDNS_SOAType.ResponsibleParty
- MicrosoftDNS_SOAType.RefreshInterval
- MicrosoftDNS_SOAType.RetryDelay
- MicrosoftDNS_SOAType.ExpireLimit
- MicrosoftDNS_SOAType.MinimumTTL
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a3e7cb617514e2ed7c8692a866cc80dfc639391
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032478"
---
# <a name="microsoftdns_soatype-class"></a><span data-ttu-id="065e9-105">MicrosoftDNS \_ SOAType, classe</span><span class="sxs-lookup"><span data-stu-id="065e9-105">MicrosoftDNS\_SOAType class</span></span>

<span data-ttu-id="065e9-106">Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement SOA (Start of Authority).</span><span class="sxs-lookup"><span data-stu-id="065e9-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Start Of Authority (SOA) record.</span></span>

<span data-ttu-id="065e9-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="065e9-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="065e9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="065e9-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_SOAType : MicrosoftDNS_ResourceRecord
{
  uint32 SerialNumber;
  string PrimaryServer;
  string ResponsibleParty;
  uint32 RefreshInterval;
  uint32 RetryDelay;
  uint32 ExpireLimit;
  uint32 MinimumTTL;
};
```

## <a name="members"></a><span data-ttu-id="065e9-109">Membres</span><span class="sxs-lookup"><span data-stu-id="065e9-109">Members</span></span>

<span data-ttu-id="065e9-110">La classe **MicrosoftDNS \_ SOAType** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="065e9-110">The **MicrosoftDNS\_SOAType** class has these types of members:</span></span>

-   [<span data-ttu-id="065e9-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="065e9-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="065e9-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="065e9-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="065e9-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="065e9-113">Methods</span></span>

<span data-ttu-id="065e9-114">La classe **MicrosoftDNS \_ SOAType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="065e9-114">The **MicrosoftDNS\_SOAType** class has these methods.</span></span>



| <span data-ttu-id="065e9-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="065e9-115">Method</span></span>     | <span data-ttu-id="065e9-116">Description</span><span class="sxs-lookup"><span data-stu-id="065e9-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="065e9-117">**Modify**</span><span class="sxs-lookup"><span data-stu-id="065e9-117">**Modify**</span></span> | <span data-ttu-id="065e9-118">Met à jour la durée de vie, le numéro de série SOA, le serveur principal, le tiers responsable, l’intervalle d’actualisation, le délai avant nouvelle tentative, la limite d’expiration et la durée de vie minimale (pour la zone) aux valeurs spécifiées comme paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="065e9-118">Updates the TTL, SOA Serial Number, Primary Server, Responsible Party, Refresh Interval, Retry Delay, Expire Limit and Minimum TTL (for the zone) to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="065e9-119">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="065e9-119">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="065e9-120">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="065e9-120">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="065e9-121">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="065e9-121">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="065e9-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="065e9-122">Properties</span></span>

<span data-ttu-id="065e9-123">La classe **MicrosoftDNS \_ SOAType** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="065e9-123">The **MicrosoftDNS\_SOAType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="065e9-124">**ExpireLimit**</span><span class="sxs-lookup"><span data-stu-id="065e9-124">**ExpireLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="065e9-125">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="065e9-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="065e9-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="065e9-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="065e9-127">Durée, en secondes, avant qu’une zone qui ne réponde ne soit plus faisant autorité.</span><span class="sxs-lookup"><span data-stu-id="065e9-127">Time, in seconds, before an unresponsive zone is no longer authoritative.</span></span>

</dd> <dt>

<span data-ttu-id="065e9-128">**MinimumTTL**</span><span class="sxs-lookup"><span data-stu-id="065e9-128">**MinimumTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="065e9-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="065e9-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="065e9-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="065e9-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="065e9-131">Limite inférieure de la durée, en secondes, pendant laquelle un serveur DNS ou un programme de résolution de mise en cache est autorisé à mettre en cache un enregistrement de ressource de la zone à laquelle cet enregistrement appartient.</span><span class="sxs-lookup"><span data-stu-id="065e9-131">Lower limit on the time, in seconds, that a DNS Server or Caching resolver are allowed to cache any resource record from the zone to which this record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="065e9-132">**PrimaryServer**</span><span class="sxs-lookup"><span data-stu-id="065e9-132">**PrimaryServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="065e9-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="065e9-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="065e9-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="065e9-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="065e9-135">Serveur DNS faisant autorité pour la zone à laquelle l’enregistrement appartient.</span><span class="sxs-lookup"><span data-stu-id="065e9-135">Authoritative DNS Server for the zone to which the record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="065e9-136">**RefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="065e9-136">**RefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="065e9-137">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="065e9-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="065e9-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="065e9-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="065e9-139">Durée, en secondes, avant l’actualisation de la zone contenant cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="065e9-139">Time, in seconds, before the zone containing this record should be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="065e9-140">**ResponsibleParty**</span><span class="sxs-lookup"><span data-stu-id="065e9-140">**ResponsibleParty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="065e9-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="065e9-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="065e9-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="065e9-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="065e9-143">Nom du tiers responsable de la zone à laquelle l’enregistrement appartient.</span><span class="sxs-lookup"><span data-stu-id="065e9-143">Name of the responsible party for the zone to which the record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="065e9-144">**RetryDelay**</span><span class="sxs-lookup"><span data-stu-id="065e9-144">**RetryDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="065e9-145">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="065e9-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="065e9-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="065e9-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="065e9-147">Durée, en secondes, avant la nouvelle tentative d’actualisation de la zone à laquelle cet enregistrement appartient.</span><span class="sxs-lookup"><span data-stu-id="065e9-147">Time, in seconds, before retrying a failed refresh of the zone to which this record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="065e9-148">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="065e9-148">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="065e9-149">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="065e9-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="065e9-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="065e9-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="065e9-151">Numéro de série de l’enregistrement SOA.</span><span class="sxs-lookup"><span data-stu-id="065e9-151">Serial number of the SOA record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="065e9-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="065e9-152">Requirements</span></span>



| <span data-ttu-id="065e9-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="065e9-153">Requirement</span></span> | <span data-ttu-id="065e9-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="065e9-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="065e9-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="065e9-155">Minimum supported client</span></span><br/> | <span data-ttu-id="065e9-156">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="065e9-156">None supported</span></span><br/>                                                              |
| <span data-ttu-id="065e9-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="065e9-157">Minimum supported server</span></span><br/> | <span data-ttu-id="065e9-158">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="065e9-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="065e9-159">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="065e9-159">Namespace</span></span><br/>                | <span data-ttu-id="065e9-160">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="065e9-160">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="065e9-161">MOF</span><span class="sxs-lookup"><span data-stu-id="065e9-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="065e9-162"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="065e9-162"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="065e9-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="065e9-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="065e9-164">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="065e9-164">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="065e9-165">**Modifier la méthode de la \_ classe SOAType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="065e9-165">**Modify Method of the MicrosoftDNS\_SOAType Class**</span></span>](microsoftdns-soatype-modify.md)
</dt> </dl>

 

 





