---
title: Classe MicrosoftDNS_AType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement d’adresse d’hôte (a).
ms.assetid: c7bd8a26-b0ac-49ef-9068-a0ecddeb6ef4
keywords:
- MicrosoftDNS_AType de la classe DNS
- MicrosoftDNS_AType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType
- MicrosoftDNS_AType.CreateInstanceFromPropertyData
- MicrosoftDNS_AType.Modify
- MicrosoftDNS_AType.IPAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e856968e2c3d4e581d69e0ac7bcbddc256424c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106536289"
---
# <a name="microsoftdns_atype-class"></a><span data-ttu-id="ef692-105">MicrosoftDNS \_ aType, classe</span><span class="sxs-lookup"><span data-stu-id="ef692-105">MicrosoftDNS\_AType class</span></span>

<span data-ttu-id="ef692-106">Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement d’adresse d’hôte (a).</span><span class="sxs-lookup"><span data-stu-id="ef692-106">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a host Address (A) record.</span></span>

<span data-ttu-id="ef692-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="ef692-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef692-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef692-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_AType : MicrosoftDNS_ResourceRecord
{
  string IPAddress;
};
```

## <a name="members"></a><span data-ttu-id="ef692-109">Membres</span><span class="sxs-lookup"><span data-stu-id="ef692-109">Members</span></span>

<span data-ttu-id="ef692-110">La classe **MicrosoftDNS \_ aType** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ef692-110">The **MicrosoftDNS\_AType** class has these types of members:</span></span>

-   [<span data-ttu-id="ef692-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ef692-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="ef692-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ef692-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ef692-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ef692-113">Methods</span></span>

<span data-ttu-id="ef692-114">La classe **MicrosoftDNS \_ aType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ef692-114">The **MicrosoftDNS\_AType** class has these methods.</span></span>



| <span data-ttu-id="ef692-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="ef692-115">Method</span></span>                             | <span data-ttu-id="ef692-116">Description</span><span class="sxs-lookup"><span data-stu-id="ef692-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef692-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="ef692-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="ef692-118">Instancie un enregistrement de ressource d’adresse d’hôte (A) en fonction des données des paramètres d’entrée de la méthode : le nom du serveur DNS, le nom du conteneur, le nom du propriétaire, la classe (valeur par défaut = IN), la valeur de durée de vie et l’adresse IP de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="ef692-118">Instantiates a Host Address (A) RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value and the IP address of the host.</span></span> <span data-ttu-id="ef692-119">Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="ef692-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="ef692-120">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="ef692-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="ef692-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="ef692-121">**Modify**</span></span>                         | <span data-ttu-id="ef692-122">Met à jour la durée de vie et l’adresse IP avec les valeurs spécifiées en tant que paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="ef692-122">Updates the TTL and IP address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="ef692-123">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="ef692-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="ef692-124">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="ef692-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="ef692-125">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="ef692-125">Qualifiers: Implemented</span></span><br/>             |



 

### <a name="properties"></a><span data-ttu-id="ef692-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ef692-126">Properties</span></span>

<span data-ttu-id="ef692-127">La classe **MicrosoftDNS \_ aType** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ef692-127">The **MicrosoftDNS\_AType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef692-128">**IPAddress**</span><span class="sxs-lookup"><span data-stu-id="ef692-128">**IPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef692-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ef692-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef692-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef692-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef692-131">Chaîne représentant l’adresse IPv4 de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="ef692-131">String representing the IPv4 address of the host.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef692-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef692-132">Requirements</span></span>



| <span data-ttu-id="ef692-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef692-133">Requirement</span></span> | <span data-ttu-id="ef692-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef692-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef692-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef692-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ef692-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef692-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ef692-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef692-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ef692-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef692-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ef692-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ef692-139">Namespace</span></span><br/>                | <span data-ttu-id="ef692-140">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="ef692-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ef692-141">MOF</span><span class="sxs-lookup"><span data-stu-id="ef692-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef692-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef692-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef692-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef692-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef692-144">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="ef692-144">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="ef692-145">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS aType**</span><span class="sxs-lookup"><span data-stu-id="ef692-145">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="ef692-146">**Modifier la méthode de la \_ classe aType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ef692-146">**Modify Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-modify.md)
</dt> </dl>

 

 





