---
title: Classe MicrosoftDNS_X25Type
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement X. 25 (X25).
ms.assetid: 1213dfd7-30b3-413e-b723-f4284fa0b416
keywords:
- MicrosoftDNS_X25Type de la classe DNS
- MicrosoftDNS_X25Type de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_X25Type
- MicrosoftDNS_X25Type.CreateInstanceFromPropertyData
- MicrosoftDNS_X25Type.Modify
- MicrosoftDNS_X25Type.PSDNAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e584119dbd45d5d6c7fae347c506c42fcda4fff7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106529081"
---
# <a name="microsoftdns_x25type-class"></a><span data-ttu-id="177c3-105">MicrosoftDNS \_ X25Type, classe</span><span class="sxs-lookup"><span data-stu-id="177c3-105">MicrosoftDNS\_X25Type class</span></span>

<span data-ttu-id="177c3-106">Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement X. 25 (X25).</span><span class="sxs-lookup"><span data-stu-id="177c3-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an X.25 (X25) record.</span></span>

<span data-ttu-id="177c3-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="177c3-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="177c3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="177c3-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_X25Type : MicrosoftDNS_ResourceRecord
{
  string PSDNAddress;
};
```

## <a name="members"></a><span data-ttu-id="177c3-109">Membres</span><span class="sxs-lookup"><span data-stu-id="177c3-109">Members</span></span>

<span data-ttu-id="177c3-110">La classe **MicrosoftDNS \_ X25Type** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="177c3-110">The **MicrosoftDNS\_X25Type** class has these types of members:</span></span>

-   [<span data-ttu-id="177c3-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="177c3-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="177c3-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="177c3-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="177c3-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="177c3-113">Methods</span></span>

<span data-ttu-id="177c3-114">La classe **MicrosoftDNS \_ X25Type** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="177c3-114">The **MicrosoftDNS\_X25Type** class has these methods.</span></span>



| <span data-ttu-id="177c3-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="177c3-115">Method</span></span>                             | <span data-ttu-id="177c3-116">Description</span><span class="sxs-lookup"><span data-stu-id="177c3-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="177c3-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="177c3-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="177c3-118">Instancie un type « X25 » de RR en fonction des données des paramètres d’entrée de la méthode : le nom du serveur DNS de l’enregistrement, le nom du conteneur, le nom du propriétaire, la classe (valeur par défaut = IN), la valeur de la durée de vie et l’adresse PSDN.</span><span class="sxs-lookup"><span data-stu-id="177c3-118">Instantiates an 'X25' Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the PSDN address.</span></span> <span data-ttu-id="177c3-119">Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="177c3-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="177c3-120">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="177c3-120">Qualifiers: Implemented, static</span></span><br/>              |
| <span data-ttu-id="177c3-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="177c3-121">**Modify**</span></span>                         | <span data-ttu-id="177c3-122">Cette méthode met à jour les adresses TTL et PSDN avec les valeurs spécifiées en tant que paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="177c3-122">This method updates the TTL and PSDN Address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="177c3-123">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="177c3-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="177c3-124">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="177c3-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="177c3-125">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="177c3-125">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="177c3-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="177c3-126">Properties</span></span>

<span data-ttu-id="177c3-127">La classe **MicrosoftDNS \_ X25Type** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="177c3-127">The **MicrosoftDNS\_X25Type** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="177c3-128">**PSDNAddress**</span><span class="sxs-lookup"><span data-stu-id="177c3-128">**PSDNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="177c3-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="177c3-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="177c3-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="177c3-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="177c3-131">Adresse PSDN du propriétaire de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="177c3-131">PSDN address of the owner of the RR.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="177c3-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="177c3-132">Requirements</span></span>



| <span data-ttu-id="177c3-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="177c3-133">Requirement</span></span> | <span data-ttu-id="177c3-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="177c3-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="177c3-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="177c3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="177c3-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="177c3-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="177c3-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="177c3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="177c3-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="177c3-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="177c3-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="177c3-139">Namespace</span></span><br/>                | <span data-ttu-id="177c3-140">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="177c3-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="177c3-141">MOF</span><span class="sxs-lookup"><span data-stu-id="177c3-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="177c3-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="177c3-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="177c3-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="177c3-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="177c3-144">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS X25Type**</span><span class="sxs-lookup"><span data-stu-id="177c3-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_X25Type Class**</span></span>](microsoftdns-x25type-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="177c3-145">**Modifier la méthode de la \_ classe X25Type MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="177c3-145">**Modify Method of the MicrosoftDNS\_X25Type Class**</span></span>](microsoftdns-x25type-modify.md)
</dt> <dt>

[<span data-ttu-id="177c3-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="177c3-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





