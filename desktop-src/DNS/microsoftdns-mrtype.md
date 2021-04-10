---
title: Classe MicrosoftDNS_MRType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement de renommage de boîte aux lettres (Mr).
ms.assetid: fa5da18f-121b-477b-8876-6e337382e9b8
keywords:
- MicrosoftDNS_MRType de la classe DNS
- MicrosoftDNS_MRType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType
- MicrosoftDNS_MRType.CreateInstanceFromPropertyData
- MicrosoftDNS_MRType.Modify
- MicrosoftDNS_MRType.MRMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 732f0e6f51963f5ae810e4730406a94264fdde47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105256"
---
# <a name="microsoftdns_mrtype-class"></a><span data-ttu-id="3d3b6-105">MicrosoftDNS \_ MRType, classe</span><span class="sxs-lookup"><span data-stu-id="3d3b6-105">MicrosoftDNS\_MRType class</span></span>

<span data-ttu-id="3d3b6-106">Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement de renommage de boîte aux lettres (Mr).</span><span class="sxs-lookup"><span data-stu-id="3d3b6-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mailbox Rename (MR) record.</span></span>

<span data-ttu-id="3d3b6-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="3d3b6-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d3b6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d3b6-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MRType : MicrosoftDNS_ResourceRecord
{
  string MRMailbox;
};
```

## <a name="members"></a><span data-ttu-id="3d3b6-109">Membres</span><span class="sxs-lookup"><span data-stu-id="3d3b6-109">Members</span></span>

<span data-ttu-id="3d3b6-110">La classe **MicrosoftDNS \_ MRType** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3d3b6-110">The **MicrosoftDNS\_MRType** class has these types of members:</span></span>

-   [<span data-ttu-id="3d3b6-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3d3b6-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="3d3b6-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3d3b6-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3d3b6-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3d3b6-113">Methods</span></span>

<span data-ttu-id="3d3b6-114">La classe **MicrosoftDNS \_ MRType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="3d3b6-114">The **MicrosoftDNS\_MRType** class has these methods.</span></span>



| <span data-ttu-id="3d3b6-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="3d3b6-115">Method</span></span>                             | <span data-ttu-id="3d3b6-116">Description</span><span class="sxs-lookup"><span data-stu-id="3d3b6-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d3b6-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="3d3b6-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="3d3b6-118">Cette méthode instancie un type « MR » de RR en fonction des données des paramètres d’entrée de la méthode : le nom du serveur DNS de l’enregistrement, le nom du conteneur, le nom du propriétaire de la boîte aux lettres, la classe (valeur par défaut = IN), la valeur de durée de vie et le nom de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="3d3b6-118">This method instantiates an 'MR' Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mailbox, class (default = IN), time-to-live value and the mailbox rename.</span></span> <span data-ttu-id="3d3b6-119">Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="3d3b6-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="3d3b6-120">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="3d3b6-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="3d3b6-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="3d3b6-121">**Modify**</span></span>                         | <span data-ttu-id="3d3b6-122">Cette méthode met à jour la durée de vie et la boîte aux lettres MR avec les valeurs spécifiées en tant que paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="3d3b6-122">This method updates the TTL and MR Mailbox to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="3d3b6-123">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="3d3b6-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="3d3b6-124">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="3d3b6-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="3d3b6-125">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="3d3b6-125">Qualifiers: Implemented</span></span><br/>                 |



 

### <a name="properties"></a><span data-ttu-id="3d3b6-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3d3b6-126">Properties</span></span>

<span data-ttu-id="3d3b6-127">La classe **MicrosoftDNS \_ MRType** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="3d3b6-127">The **MicrosoftDNS\_MRType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3d3b6-128">**MRMailbox**</span><span class="sxs-lookup"><span data-stu-id="3d3b6-128">**MRMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d3b6-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3d3b6-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d3b6-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3d3b6-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d3b6-131">Nom de domaine complet spécifiant une boîte aux lettres qui est le nom correct de la boîte aux lettres spécifiée dans le nom du propriétaire de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="3d3b6-131">FQDN specifying a mailbox that is the proper rename of the mailbox specified in the record's owner name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3d3b6-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d3b6-132">Requirements</span></span>



| <span data-ttu-id="3d3b6-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d3b6-133">Requirement</span></span> | <span data-ttu-id="3d3b6-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d3b6-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d3b6-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d3b6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3d3b6-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d3b6-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3d3b6-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d3b6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3d3b6-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3d3b6-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3d3b6-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3d3b6-139">Namespace</span></span><br/>                | <span data-ttu-id="3d3b6-140">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="3d3b6-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="3d3b6-141">MOF</span><span class="sxs-lookup"><span data-stu-id="3d3b6-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d3b6-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d3b6-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d3b6-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d3b6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d3b6-144">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MRType**</span><span class="sxs-lookup"><span data-stu-id="3d3b6-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="3d3b6-145">**Modifier la méthode de la \_ classe MRType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="3d3b6-145">**Modify Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="3d3b6-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="3d3b6-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





