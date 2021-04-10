---
title: Classe MicrosoftDNS_MBType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement de ressource de boîte aux lettres (MB).
ms.assetid: b8f3b106-58f4-44b8-b2db-b00f1a495641
keywords:
- MicrosoftDNS_MBType de la classe DNS
- MicrosoftDNS_MBType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType
- MicrosoftDNS_MBType.CreateInstanceFromPropertyData
- MicrosoftDNS_MBType.Modify
- MicrosoftDNS_MBType.MBHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89ad6599ad058f65beba961f00c1bd6c43663487
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942285"
---
# <a name="microsoftdns_mbtype-class"></a><span data-ttu-id="68bf0-105">MicrosoftDNS \_ MBType, classe</span><span class="sxs-lookup"><span data-stu-id="68bf0-105">MicrosoftDNS\_MBType class</span></span>

<span data-ttu-id="68bf0-106">Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement de ressource de boîte aux lettres (MB).</span><span class="sxs-lookup"><span data-stu-id="68bf0-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mailbox (MB) resource record.</span></span>

<span data-ttu-id="68bf0-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="68bf0-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="68bf0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68bf0-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MBType : MicrosoftDNS_ResourceRecord
{
  string MBHost;
};
```

## <a name="members"></a><span data-ttu-id="68bf0-109">Membres</span><span class="sxs-lookup"><span data-stu-id="68bf0-109">Members</span></span>

<span data-ttu-id="68bf0-110">La classe **MicrosoftDNS \_ MBType** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="68bf0-110">The **MicrosoftDNS\_MBType** class has these types of members:</span></span>

-   [<span data-ttu-id="68bf0-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="68bf0-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="68bf0-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="68bf0-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="68bf0-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="68bf0-113">Methods</span></span>

<span data-ttu-id="68bf0-114">La classe **MicrosoftDNS \_ MBType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="68bf0-114">The **MicrosoftDNS\_MBType** class has these methods.</span></span>



| <span data-ttu-id="68bf0-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="68bf0-115">Method</span></span>                             | <span data-ttu-id="68bf0-116">Description</span><span class="sxs-lookup"><span data-stu-id="68bf0-116">Description</span></span>                                                                                                                                                                                                                                                                                                                               |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68bf0-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="68bf0-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="68bf0-118">Instancie un RR MB basé sur les données des paramètres d’entrée de la méthode : le nom du serveur DNS de l’enregistrement, le nom du conteneur, le nom du propriétaire de la boîte aux lettres, la classe (valeur par défaut = IN), la valeur de durée de vie et l’hôte de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="68bf0-118">Instantiates an MB RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mailbox, class (default = IN), time-to-live value and the mailbox host.</span></span> <span data-ttu-id="68bf0-119">Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="68bf0-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="68bf0-120">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="68bf0-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="68bf0-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="68bf0-121">**Modify**</span></span>                         | <span data-ttu-id="68bf0-122">Met à jour l’hôte TTL et MB avec les valeurs spécifiées en tant que paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="68bf0-122">Updates the TTL and MB host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="68bf0-123">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="68bf0-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="68bf0-124">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="68bf0-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="68bf0-125">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="68bf0-125">Qualifiers: Implemented</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="68bf0-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="68bf0-126">Properties</span></span>

<span data-ttu-id="68bf0-127">La classe **MicrosoftDNS \_ MBType** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="68bf0-127">The **MicrosoftDNS\_MBType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68bf0-128">**MBHost**</span><span class="sxs-lookup"><span data-stu-id="68bf0-128">**MBHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68bf0-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="68bf0-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68bf0-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68bf0-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68bf0-131">Nom de domaine complet qui spécifie un hôte de la boîte aux lettres spécifiée dans le nom du propriétaire de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="68bf0-131">FQDN that specifies a host of the mailbox specified in the record's Owner Name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="68bf0-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68bf0-132">Requirements</span></span>



| <span data-ttu-id="68bf0-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68bf0-133">Requirement</span></span> | <span data-ttu-id="68bf0-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="68bf0-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68bf0-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68bf0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="68bf0-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="68bf0-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="68bf0-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68bf0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="68bf0-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68bf0-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="68bf0-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="68bf0-139">Namespace</span></span><br/>                | <span data-ttu-id="68bf0-140">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="68bf0-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="68bf0-141">MOF</span><span class="sxs-lookup"><span data-stu-id="68bf0-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68bf0-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68bf0-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68bf0-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68bf0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68bf0-144">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MBType**</span><span class="sxs-lookup"><span data-stu-id="68bf0-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="68bf0-145">**Modifier la méthode de la \_ classe MBType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="68bf0-145">**Modify Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="68bf0-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="68bf0-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





