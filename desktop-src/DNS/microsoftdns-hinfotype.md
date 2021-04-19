---
title: Classe MicrosoftDNS_HINFOType
description: Sous-classe de l' \_ ResourceRecord MicrosoftDNS qui représente un enregistrement des informations sur l’hôte (HINFO).
ms.assetid: c6591010-0fe6-45b2-9032-9f847237ecf6
keywords:
- MicrosoftDNS_HINFOType de la classe DNS
- MicrosoftDNS_HINFOType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType
- MicrosoftDNS_HINFOType.CreateInstanceFromPropertyData
- MicrosoftDNS_HINFOType.Modify
- MicrosoftDNS_HINFOType.CPU
- MicrosoftDNS_HINFOType.OS
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3298e5a7f90dbaee24e5014b1a3aab76ad6997
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106545754"
---
# <a name="microsoftdns_hinfotype-class"></a><span data-ttu-id="8fe6c-105">MicrosoftDNS \_ HINFOType, classe</span><span class="sxs-lookup"><span data-stu-id="8fe6c-105">MicrosoftDNS\_HINFOType class</span></span>

<span data-ttu-id="8fe6c-106">Sous-classe de [**l' \_ ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md) qui représente un enregistrement des informations sur l’hôte (HINFO).</span><span class="sxs-lookup"><span data-stu-id="8fe6c-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Host Information (HINFO) record.</span></span>

<span data-ttu-id="8fe6c-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="8fe6c-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fe6c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8fe6c-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_HINFOType : MicrosoftDNS_ResourceRecord
{
  string CPU;
  string OS;
};
```

## <a name="members"></a><span data-ttu-id="8fe6c-109">Membres</span><span class="sxs-lookup"><span data-stu-id="8fe6c-109">Members</span></span>

<span data-ttu-id="8fe6c-110">La classe **MicrosoftDNS \_ HINFOType** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8fe6c-110">The **MicrosoftDNS\_HINFOType** class has these types of members:</span></span>

-   [<span data-ttu-id="8fe6c-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8fe6c-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="8fe6c-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8fe6c-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8fe6c-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8fe6c-113">Methods</span></span>

<span data-ttu-id="8fe6c-114">La classe **MicrosoftDNS \_ HINFOType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="8fe6c-114">The **MicrosoftDNS\_HINFOType** class has these methods.</span></span>



| <span data-ttu-id="8fe6c-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="8fe6c-115">Method</span></span>                             | <span data-ttu-id="8fe6c-116">Description</span><span class="sxs-lookup"><span data-stu-id="8fe6c-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fe6c-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="8fe6c-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="8fe6c-118">Instancie un HINFO de RR en fonction des données contenues dans les paramètres d’entrée de la méthode : le nom du serveur DNS, le nom du conteneur, le nom du propriétaire, la classe (valeur par défaut = IN), la valeur de la durée de vie et le processeur et les types de système d’exploitation de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="8fe6c-118">Instantiates an HINFO of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the host's CPU and operating system types.</span></span> <span data-ttu-id="8fe6c-119">Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="8fe6c-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="8fe6c-120">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="8fe6c-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="8fe6c-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="8fe6c-121">**Modify**</span></span>                         | <span data-ttu-id="8fe6c-122">Met à jour la durée de vie, le processeur et le système d’exploitation avec les valeurs spécifiées en tant que paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="8fe6c-122">Updates the TTL, CPU, and operating system to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="8fe6c-123">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="8fe6c-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="8fe6c-124">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="8fe6c-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="8fe6c-125">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="8fe6c-125">Qualifiers: Implemented</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="8fe6c-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8fe6c-126">Properties</span></span>

<span data-ttu-id="8fe6c-127">La classe **MicrosoftDNS \_ HINFOType** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="8fe6c-127">The **MicrosoftDNS\_HINFOType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8fe6c-128">**UC**</span><span class="sxs-lookup"><span data-stu-id="8fe6c-128">**CPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fe6c-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8fe6c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fe6c-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8fe6c-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fe6c-131">Type d’UC du propriétaire de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="8fe6c-131">CPU type of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="8fe6c-132">**SE**</span><span class="sxs-lookup"><span data-stu-id="8fe6c-132">**OS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fe6c-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8fe6c-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fe6c-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8fe6c-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fe6c-135">Système d’exploitation du propriétaire de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="8fe6c-135">Operating system of the record owner.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8fe6c-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fe6c-136">Requirements</span></span>



| <span data-ttu-id="8fe6c-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8fe6c-137">Requirement</span></span> | <span data-ttu-id="8fe6c-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fe6c-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fe6c-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fe6c-139">Minimum supported client</span></span><br/> | <span data-ttu-id="8fe6c-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fe6c-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8fe6c-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fe6c-141">Minimum supported server</span></span><br/> | <span data-ttu-id="8fe6c-142">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8fe6c-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8fe6c-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8fe6c-143">Namespace</span></span><br/>                | <span data-ttu-id="8fe6c-144">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="8fe6c-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="8fe6c-145">MOF</span><span class="sxs-lookup"><span data-stu-id="8fe6c-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fe6c-146"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8fe6c-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fe6c-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fe6c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fe6c-148">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS HINFOType**</span><span class="sxs-lookup"><span data-stu-id="8fe6c-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_HINFOType Class**</span></span>](microsoftdns-hinfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="8fe6c-149">**Modifier la méthode de la \_ classe HINFOType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="8fe6c-149">**Modify Method of the MicrosoftDNS\_HINFOType Class**</span></span>](microsoftdns-hinfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="8fe6c-150">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="8fe6c-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





