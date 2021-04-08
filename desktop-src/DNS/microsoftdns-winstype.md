---
title: Classe MicrosoftDNS_WINSType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement WINS (Windows Internet Name Service).
ms.assetid: 8f891d80-ee4d-4641-8a6c-159c78e5cf86
keywords:
- MicrosoftDNS_WINSType de la classe DNS
- MicrosoftDNS_WINSType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType
- MicrosoftDNS_WINSType.CreateInstanceFromPropertyData
- MicrosoftDNS_WINSType.Modify
- MicrosoftDNS_WINSType.MappingFlag
- MicrosoftDNS_WINSType.LookupTimeout
- MicrosoftDNS_WINSType.CacheTimeout
- MicrosoftDNS_WINSType.WinsServers
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce23132073305142948518327ea5b6c7e46f1289
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843865"
---
# <a name="microsoftdns_winstype-class"></a><span data-ttu-id="fcf72-105">MicrosoftDNS \_ WINSType, classe</span><span class="sxs-lookup"><span data-stu-id="fcf72-105">MicrosoftDNS\_WINSType class</span></span>

<span data-ttu-id="fcf72-106">Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement WINS (Windows Internet Name Service).</span><span class="sxs-lookup"><span data-stu-id="fcf72-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Windows Internet Name Service (WINS) record.</span></span>

<span data-ttu-id="fcf72-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="fcf72-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcf72-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fcf72-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_WINSType : MicrosoftDNS_ResourceRecord
{
  uint32 MappingFlag;
  uint32 LookupTimeout;
  uint32 CacheTimeout;
  string WinsServers;
};
```

## <a name="members"></a><span data-ttu-id="fcf72-109">Membres</span><span class="sxs-lookup"><span data-stu-id="fcf72-109">Members</span></span>

<span data-ttu-id="fcf72-110">La classe **MicrosoftDNS \_ WINSType** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fcf72-110">The **MicrosoftDNS\_WINSType** class has these types of members:</span></span>

-   [<span data-ttu-id="fcf72-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fcf72-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="fcf72-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fcf72-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fcf72-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fcf72-113">Methods</span></span>

<span data-ttu-id="fcf72-114">La classe **MicrosoftDNS \_ WINSType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="fcf72-114">The **MicrosoftDNS\_WINSType** class has these methods.</span></span>



| <span data-ttu-id="fcf72-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="fcf72-115">Method</span></span>                             | <span data-ttu-id="fcf72-116">Description</span><span class="sxs-lookup"><span data-stu-id="fcf72-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcf72-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="fcf72-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="fcf72-118">Instancie un type WINS de RR en fonction des données contenues dans les paramètres d’entrée de la méthode : le nom du serveur DNS, le nom du conteneur, le nom du propriétaire, la classe (valeur par défaut = IN), la valeur de durée de vie et l’indicateur de mappage WINS, le délai d’attente de la recherche, le délai d’expiration du cache et la liste</span><span class="sxs-lookup"><span data-stu-id="fcf72-118">Instantiates a WINS Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, look-up time out, cache time out and list of IP addresses for look up.</span></span> <span data-ttu-id="fcf72-119">Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="fcf72-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="fcf72-120">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="fcf72-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="fcf72-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="fcf72-121">**Modify**</span></span>                         | <span data-ttu-id="fcf72-122">Met à jour les valeurs spécifiées en tant que paramètres d’entrée de cette méthode pour la durée de vie, l’indicateur de mappage, le délai d’attente de recherche, le délai d’attente du cache et les serveurs WINS.</span><span class="sxs-lookup"><span data-stu-id="fcf72-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Wins Servers to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="fcf72-123">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="fcf72-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="fcf72-124">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="fcf72-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="fcf72-125">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="fcf72-125">Qualifiers: Implemented</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="fcf72-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fcf72-126">Properties</span></span>

<span data-ttu-id="fcf72-127">La classe **MicrosoftDNS \_ WINSType** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fcf72-127">The **MicrosoftDNS\_WINSType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fcf72-128">**CacheTimeout**</span><span class="sxs-lookup"><span data-stu-id="fcf72-128">**CacheTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcf72-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fcf72-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fcf72-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fcf72-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcf72-131">Durée, en secondes, pendant laquelle un serveur DNS qui utilise WINS peut mettre en cache la réponse du serveur WINS.</span><span class="sxs-lookup"><span data-stu-id="fcf72-131">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="fcf72-132">**LookupTimeout**</span><span class="sxs-lookup"><span data-stu-id="fcf72-132">**LookupTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcf72-133">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fcf72-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fcf72-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fcf72-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcf72-135">Durée, en secondes, pendant laquelle un serveur DNS tente de résoudre à l’aide de la recherche WINS.</span><span class="sxs-lookup"><span data-stu-id="fcf72-135">Time, in seconds, that a DNS Server attempts resolution using WINS Look up.</span></span>

</dd> <dt>

<span data-ttu-id="fcf72-136">**MappingFlag**</span><span class="sxs-lookup"><span data-stu-id="fcf72-136">**MappingFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcf72-137">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fcf72-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fcf72-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fcf72-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcf72-139">Indicateur de mappage WINS qui spécifie si l’enregistrement doit être inclus dans la réplication de zone.</span><span class="sxs-lookup"><span data-stu-id="fcf72-139">WINS mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="fcf72-140">Elle ne peut avoir que deux valeurs : 0x80000000 et 0x00010000 correspondant respectivement aux indicateurs de réplication et de non-réplication (enregistrement local).</span><span class="sxs-lookup"><span data-stu-id="fcf72-140">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span> <span data-ttu-id="fcf72-141">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="fcf72-141">The following values are valid.</span></span>



| <span data-ttu-id="fcf72-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="fcf72-142">Value</span></span>                                                                                                                                               | <span data-ttu-id="fcf72-143">Signification</span><span class="sxs-lookup"><span data-stu-id="fcf72-143">Meaning</span></span>                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <span data-ttu-id="fcf72-144"><dt>**0x80000000**</dt></span><span class="sxs-lookup"><span data-stu-id="fcf72-144"><dt>**0x80000000**</dt></span></span> </dl> | <span data-ttu-id="fcf72-145">Indicateur de réplication</span><span class="sxs-lookup"><span data-stu-id="fcf72-145">Replication flag</span></span><br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <span data-ttu-id="fcf72-146"><dt>**0x00010000**</dt></span><span class="sxs-lookup"><span data-stu-id="fcf72-146"><dt>**0x00010000**</dt></span></span> </dl> | <span data-ttu-id="fcf72-147">Indicateur de non-réplication (enregistrement local)</span><span class="sxs-lookup"><span data-stu-id="fcf72-147">No-replication (local record) flag</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fcf72-148">**WinsServers**</span><span class="sxs-lookup"><span data-stu-id="fcf72-148">**WinsServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcf72-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fcf72-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fcf72-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fcf72-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcf72-151">Liste des adresses IP séparées par des virgules des serveurs WINS utilisés dans les recherches WINS.</span><span class="sxs-lookup"><span data-stu-id="fcf72-151">List of comma-separated IP addresses of WINS servers used in WINS Look ups.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fcf72-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fcf72-152">Requirements</span></span>



| <span data-ttu-id="fcf72-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fcf72-153">Requirement</span></span> | <span data-ttu-id="fcf72-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="fcf72-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fcf72-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fcf72-155">Minimum supported client</span></span><br/> | <span data-ttu-id="fcf72-156">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fcf72-156">None supported</span></span><br/>                                                              |
| <span data-ttu-id="fcf72-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fcf72-157">Minimum supported server</span></span><br/> | <span data-ttu-id="fcf72-158">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fcf72-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fcf72-159">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fcf72-159">Namespace</span></span><br/>                | <span data-ttu-id="fcf72-160">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="fcf72-160">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="fcf72-161">MOF</span><span class="sxs-lookup"><span data-stu-id="fcf72-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fcf72-162"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fcf72-162"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcf72-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fcf72-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcf72-164">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS WINSType**</span><span class="sxs-lookup"><span data-stu-id="fcf72-164">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="fcf72-165">**Modifier la méthode de la \_ classe WINSType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="fcf72-165">**Modify Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-modify.md)
</dt> <dt>

[<span data-ttu-id="fcf72-166">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="fcf72-166">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





