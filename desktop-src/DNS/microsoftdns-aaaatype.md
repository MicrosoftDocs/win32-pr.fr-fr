---
title: Classe MicrosoftDNS_AAAAType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement d’adresse IPv6 (aaaa). L’enregistrement AAAA est généralement prononcé \ 0034 ; enregistrement Quad-a \ 0034 ;.
ms.assetid: e16a7a69-18df-43dc-add9-700a702724ce
keywords:
- MicrosoftDNS_AAAAType de la classe DNS
- MicrosoftDNS_AAAAType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType
- MicrosoftDNS_AAAAType.CreateInstanceFromPropertyData
- MicrosoftDNS_AAAAType.Modify
- MicrosoftDNS_AAAAType.IPv6Address
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0131177c342730c08868946c29356554cbfb9cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509321"
---
# <a name="microsoftdns_aaaatype-class"></a><span data-ttu-id="206be-106">MicrosoftDNS \_ AAAAType, classe</span><span class="sxs-lookup"><span data-stu-id="206be-106">MicrosoftDNS\_AAAAType class</span></span>

<span data-ttu-id="206be-107">Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement d’adresse IPv6 (aaaa).</span><span class="sxs-lookup"><span data-stu-id="206be-107">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an IPv6 Address (AAAA) record.</span></span> <span data-ttu-id="206be-108">L’enregistrement AAAA est couramment dit « enregistrement Quad-a ».</span><span class="sxs-lookup"><span data-stu-id="206be-108">The AAAA record is commonly pronounced "quad-a record".</span></span>

<span data-ttu-id="206be-109">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="206be-109">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="206be-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="206be-110">Syntax</span></span>

``` syntax
class MicrosoftDNS_AAAAType : MicrosoftDNS_ResourceRecord
{
  string IPv6Address;
};
```

## <a name="members"></a><span data-ttu-id="206be-111">Membres</span><span class="sxs-lookup"><span data-stu-id="206be-111">Members</span></span>

<span data-ttu-id="206be-112">La classe **MicrosoftDNS \_ AAAAType** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="206be-112">The **MicrosoftDNS\_AAAAType** class has these types of members:</span></span>

-   [<span data-ttu-id="206be-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="206be-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="206be-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="206be-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="206be-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="206be-115">Methods</span></span>

<span data-ttu-id="206be-116">La classe **MicrosoftDNS \_ AAAAType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="206be-116">The **MicrosoftDNS\_AAAAType** class has these methods.</span></span>



| <span data-ttu-id="206be-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="206be-117">Method</span></span>                             | <span data-ttu-id="206be-118">Description</span><span class="sxs-lookup"><span data-stu-id="206be-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="206be-119">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="206be-119">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="206be-120">Instancie un type « AAAA » de RR en fonction des données des paramètres d’entrée de la méthode : le nom du serveur DNS, le nom du conteneur, le propriétaire/nom d’hôte, la classe (valeur par défaut = IN), la valeur de durée de vie et l’adresse IPv6.</span><span class="sxs-lookup"><span data-stu-id="206be-120">Instantiates an 'AAAA' type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/Host Name, class (default = IN), time-to-live value, and the IPv6 address.</span></span> <span data-ttu-id="206be-121">Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="206be-121">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="206be-122">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="206be-122">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="206be-123">**Modify**</span><span class="sxs-lookup"><span data-stu-id="206be-123">**Modify**</span></span>                         | <span data-ttu-id="206be-124">Met à jour l’adresse TTL et IPv6 avec les valeurs spécifiées en tant que paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="206be-124">Updates the TTL and IPv6 address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="206be-125">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="206be-125">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="206be-126">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="206be-126">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="206be-127">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="206be-127">Qualifiers: Implemented</span></span><br/>      |



 

### <a name="properties"></a><span data-ttu-id="206be-128">Propriétés</span><span class="sxs-lookup"><span data-stu-id="206be-128">Properties</span></span>

<span data-ttu-id="206be-129">La classe **MicrosoftDNS \_ AAAAType** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="206be-129">The **MicrosoftDNS\_AAAAType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="206be-130">**IPv6Address**</span><span class="sxs-lookup"><span data-stu-id="206be-130">**IPv6Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="206be-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="206be-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="206be-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="206be-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="206be-133">Adresse IPv6 de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="206be-133">IPv6 address for the host.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="206be-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="206be-134">Requirements</span></span>



| <span data-ttu-id="206be-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="206be-135">Requirement</span></span> | <span data-ttu-id="206be-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="206be-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="206be-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="206be-137">Minimum supported client</span></span><br/> | <span data-ttu-id="206be-138">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="206be-138">None supported</span></span><br/>                                                              |
| <span data-ttu-id="206be-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="206be-139">Minimum supported server</span></span><br/> | <span data-ttu-id="206be-140">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="206be-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="206be-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="206be-141">Namespace</span></span><br/>                | <span data-ttu-id="206be-142">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="206be-142">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="206be-143">MOF</span><span class="sxs-lookup"><span data-stu-id="206be-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="206be-144"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="206be-144"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="206be-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="206be-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="206be-146">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS AAAAType**</span><span class="sxs-lookup"><span data-stu-id="206be-146">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="206be-147">**Modifier la méthode de la \_ classe AAAAType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="206be-147">**Modify Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-modify.md)
</dt> <dt>

[<span data-ttu-id="206be-148">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="206be-148">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





