---
title: Classe MicrosoftDNS_RTType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement d’itinéraire (RT).
ms.assetid: 986e2bbf-4f45-4611-906e-66079fda7f4c
keywords:
- MicrosoftDNS_RTType de la classe DNS
- MicrosoftDNS_RTType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType
- MicrosoftDNS_RTType.CreateInstanceFromPropertyData
- MicrosoftDNS_RTType.Modify
- MicrosoftDNS_RTType.Preference
- MicrosoftDNS_RTType.IntermediateHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d867185d8ce07a54a47eb5ea7591ec8d68a11059
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942279"
---
# <a name="microsoftdns_rttype-class"></a><span data-ttu-id="6f169-105">MicrosoftDNS \_ RTType, classe</span><span class="sxs-lookup"><span data-stu-id="6f169-105">MicrosoftDNS\_RTType class</span></span>

<span data-ttu-id="6f169-106">Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement d’itinéraire (RT).</span><span class="sxs-lookup"><span data-stu-id="6f169-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Route Through (RT) record.</span></span>

<span data-ttu-id="6f169-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="6f169-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f169-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f169-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_RTType : MicrosoftDNS_ResourceRecord
{
  uint16 Preference;
  string IntermediateHost;
};
```

## <a name="members"></a><span data-ttu-id="6f169-109">Membres</span><span class="sxs-lookup"><span data-stu-id="6f169-109">Members</span></span>

<span data-ttu-id="6f169-110">La classe **MicrosoftDNS \_ RTType** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6f169-110">The **MicrosoftDNS\_RTType** class has these types of members:</span></span>

-   [<span data-ttu-id="6f169-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6f169-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="6f169-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6f169-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6f169-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6f169-113">Methods</span></span>

<span data-ttu-id="6f169-114">La classe **MicrosoftDNS \_ RTType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="6f169-114">The **MicrosoftDNS\_RTType** class has these methods.</span></span>



| <span data-ttu-id="6f169-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="6f169-115">Method</span></span>                             | <span data-ttu-id="6f169-116">Description</span><span class="sxs-lookup"><span data-stu-id="6f169-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f169-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="6f169-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="6f169-118">Instancie un type RT de RR en fonction des données contenues dans les paramètres d’entrée de la méthode : le nom du serveur DNS de l’enregistrement, le nom du conteneur, le propriétaire/nom d’hôte, la classe (valeur par défaut = IN), la valeur de durée de vie, la préférence d’enregistrement et le nom d’hôte intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="6f169-118">Instantiates an RT Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/host Name, class (default = IN), time-to-live value, record preference and intermediate host name.</span></span> <span data-ttu-id="6f169-119">Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="6f169-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="6f169-120">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="6f169-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="6f169-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="6f169-121">**Modify**</span></span>                         | <span data-ttu-id="6f169-122">Met à jour la durée de vie, la préférence et l’hôte intermédiaire sur les valeurs spécifiées comme paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="6f169-122">Updates the TTL, Preference, and Intermediate Host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="6f169-123">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="6f169-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="6f169-124">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="6f169-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="6f169-125">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="6f169-125">Qualifiers: Implemented</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="6f169-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6f169-126">Properties</span></span>

<span data-ttu-id="6f169-127">La classe **MicrosoftDNS \_ RTType** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6f169-127">The **MicrosoftDNS\_RTType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f169-128">**IntermediateHost**</span><span class="sxs-lookup"><span data-stu-id="6f169-128">**IntermediateHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f169-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6f169-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f169-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f169-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f169-131">Nom de domaine complet spécifiant un hôte qui servira de intermédiaire pour atteindre l’hôte spécifié par le propriétaire.</span><span class="sxs-lookup"><span data-stu-id="6f169-131">FQDN specifying a host to serve as an intermediate in reaching the host specified by owner.</span></span>

</dd> <dt>

<span data-ttu-id="6f169-132">**Relatives**</span><span class="sxs-lookup"><span data-stu-id="6f169-132">**Preference**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f169-133">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f169-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f169-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f169-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f169-135">Préférence donnée à ce RR, parmi d’autres au même propriétaire.</span><span class="sxs-lookup"><span data-stu-id="6f169-135">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="6f169-136">Les valeurs les plus basses sont préférées.</span><span class="sxs-lookup"><span data-stu-id="6f169-136">Lower values are preferred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f169-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f169-137">Requirements</span></span>



| <span data-ttu-id="6f169-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f169-138">Requirement</span></span> | <span data-ttu-id="6f169-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f169-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f169-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f169-140">Minimum supported client</span></span><br/> | <span data-ttu-id="6f169-141">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f169-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6f169-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f169-142">Minimum supported server</span></span><br/> | <span data-ttu-id="6f169-143">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f169-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6f169-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6f169-144">Namespace</span></span><br/>                | <span data-ttu-id="6f169-145">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="6f169-145">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="6f169-146">MOF</span><span class="sxs-lookup"><span data-stu-id="6f169-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f169-147"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f169-147"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f169-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f169-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f169-149">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS RTType**</span><span class="sxs-lookup"><span data-stu-id="6f169-149">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="6f169-150">**Modifier la méthode de la \_ classe RTType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6f169-150">**Modify Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-modify.md)
</dt> <dt>

[<span data-ttu-id="6f169-151">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="6f169-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





