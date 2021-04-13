---
title: Classe MicrosoftDNS_WINSRType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement WINS inversé (WINSR).
ms.assetid: e611dc63-838f-4a79-baca-febd27612111
keywords:
- MicrosoftDNS_WINSRType de la classe DNS
- MicrosoftDNS_WINSRType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType
- MicrosoftDNS_WINSRType.CreateInstanceFromPropertyData
- MicrosoftDNS_WINSRType.Modify
- MicrosoftDNS_WINSRType.MappingFlag
- MicrosoftDNS_WINSRType.LookupTimeout
- MicrosoftDNS_WINSRType.CacheTimeout
- MicrosoftDNS_WINSRType.ResultDomain
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9500c6a36a1c3a7cc243f1cbcfbc0edca6cecf2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385203"
---
# <a name="microsoftdns_winsrtype-class"></a><span data-ttu-id="a18c6-105">MicrosoftDNS \_ WINSRType, classe</span><span class="sxs-lookup"><span data-stu-id="a18c6-105">MicrosoftDNS\_WINSRType class</span></span>

<span data-ttu-id="a18c6-106">Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement WINS inversé (WINSR).</span><span class="sxs-lookup"><span data-stu-id="a18c6-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a WINS Reverse Look-up (WINSR) record.</span></span>

<span data-ttu-id="a18c6-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="a18c6-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a18c6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a18c6-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_WINSRType : MicrosoftDNS_ResourceRecord
{
  uint32 MappingFlag;
  uint32 LookupTimeout;
  uint32 CacheTimeout;
  string ResultDomain;
};
```

## <a name="members"></a><span data-ttu-id="a18c6-109">Membres</span><span class="sxs-lookup"><span data-stu-id="a18c6-109">Members</span></span>

<span data-ttu-id="a18c6-110">La classe **MicrosoftDNS \_ WINSRType** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a18c6-110">The **MicrosoftDNS\_WINSRType** class has these types of members:</span></span>

-   [<span data-ttu-id="a18c6-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a18c6-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="a18c6-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a18c6-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a18c6-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a18c6-113">Methods</span></span>

<span data-ttu-id="a18c6-114">La classe **MicrosoftDNS \_ WINSRType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a18c6-114">The **MicrosoftDNS\_WINSRType** class has these methods.</span></span>



| <span data-ttu-id="a18c6-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="a18c6-115">Method</span></span>                             | <span data-ttu-id="a18c6-116">Description</span><span class="sxs-lookup"><span data-stu-id="a18c6-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                     |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a18c6-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="a18c6-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="a18c6-118">Instancie un type de RR WINSr basé sur les données des paramètres d’entrée de la méthode : le nom du serveur DNS, le nom du conteneur, le nom du propriétaire, la classe (valeur par défaut = IN), la valeur de durée de vie et l’indicateur de mappage WINS, le délai de recherche inverse, le délai d’expiration du cache WINS et le nom de domaine à ajouter</span><span class="sxs-lookup"><span data-stu-id="a18c6-118">Instantiates a WINSR Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out and domain name to append.</span></span> <span data-ttu-id="a18c6-119">Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="a18c6-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="a18c6-120">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="a18c6-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="a18c6-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="a18c6-121">**Modify**</span></span>                         | <span data-ttu-id="a18c6-122">Met à jour la durée de vie, l’indicateur de mappage, le délai d’attente de recherche, le délai d’attente du cache et le domaine de résultat sur les valeurs spécifiées comme paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="a18c6-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Result Domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="a18c6-123">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="a18c6-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="a18c6-124">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="a18c6-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="a18c6-125">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="a18c6-125">Qualifiers: Implemented</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="a18c6-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a18c6-126">Properties</span></span>

<span data-ttu-id="a18c6-127">La classe **MicrosoftDNS \_ WINSRType** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a18c6-127">The **MicrosoftDNS\_WINSRType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a18c6-128">**CacheTimeout**</span><span class="sxs-lookup"><span data-stu-id="a18c6-128">**CacheTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a18c6-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a18c6-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a18c6-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a18c6-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a18c6-131">Durée, en secondes, pendant laquelle un serveur DNS qui utilise WINS peut mettre en cache la réponse du serveur WINS.</span><span class="sxs-lookup"><span data-stu-id="a18c6-131">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="a18c6-132">**LookupTimeout**</span><span class="sxs-lookup"><span data-stu-id="a18c6-132">**LookupTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a18c6-133">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a18c6-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a18c6-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a18c6-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a18c6-135">Délai d’attente, en secondes, pour un serveur DNS à l’aide de la recherche inversée WINS.</span><span class="sxs-lookup"><span data-stu-id="a18c6-135">Time out, in seconds, for a DNS Server using WINS Reverse Look up.</span></span>

</dd> <dt>

<span data-ttu-id="a18c6-136">**MappingFlag**</span><span class="sxs-lookup"><span data-stu-id="a18c6-136">**MappingFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a18c6-137">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a18c6-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a18c6-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a18c6-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a18c6-139">Indicateur de mappage WINSr qui spécifie si l’enregistrement doit être inclus dans la réplication de zone.</span><span class="sxs-lookup"><span data-stu-id="a18c6-139">WINSR mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="a18c6-140">Elle ne peut avoir que deux valeurs : 0x80000000 et 0x00010000 correspondant respectivement aux indicateurs de réplication et de non-réplication (enregistrement local).</span><span class="sxs-lookup"><span data-stu-id="a18c6-140">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="a18c6-141">**ResultDomain**</span><span class="sxs-lookup"><span data-stu-id="a18c6-141">**ResultDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a18c6-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a18c6-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a18c6-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a18c6-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a18c6-144">Nom de domaine à ajouter aux noms NetBIOS retournés.</span><span class="sxs-lookup"><span data-stu-id="a18c6-144">Domain name to append to returned NetBIOS names.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a18c6-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a18c6-145">Requirements</span></span>



| <span data-ttu-id="a18c6-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a18c6-146">Requirement</span></span> | <span data-ttu-id="a18c6-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="a18c6-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a18c6-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a18c6-148">Minimum supported client</span></span><br/> | <span data-ttu-id="a18c6-149">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a18c6-149">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a18c6-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a18c6-150">Minimum supported server</span></span><br/> | <span data-ttu-id="a18c6-151">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a18c6-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a18c6-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a18c6-152">Namespace</span></span><br/>                | <span data-ttu-id="a18c6-153">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="a18c6-153">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="a18c6-154">MOF</span><span class="sxs-lookup"><span data-stu-id="a18c6-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a18c6-155"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a18c6-155"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a18c6-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a18c6-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a18c6-157">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS WINSRType**</span><span class="sxs-lookup"><span data-stu-id="a18c6-157">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="a18c6-158">**Modifier la méthode de la \_ classe WINSRType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="a18c6-158">**Modify Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="a18c6-159">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="a18c6-159">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





