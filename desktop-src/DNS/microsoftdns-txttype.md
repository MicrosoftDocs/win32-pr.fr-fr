---
title: Classe MicrosoftDNS_TXTType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement texte (txt).
ms.assetid: e4bd445f-71c4-48dc-b210-e3ad4452d2e5
keywords:
- MicrosoftDNS_TXTType de la classe DNS
- MicrosoftDNS_TXTType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType
- MicrosoftDNS_TXTType.CreateInstanceFromPropertyData
- MicrosoftDNS_TXTType.Modify
- MicrosoftDNS_TXTType.DescriptiveText
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d89563240b8e6d6bedb51cbe802180cd7577b57e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513820"
---
# <a name="microsoftdns_txttype-class"></a><span data-ttu-id="185bd-105">MicrosoftDNS \_ TXTType, classe</span><span class="sxs-lookup"><span data-stu-id="185bd-105">MicrosoftDNS\_TXTType class</span></span>

<span data-ttu-id="185bd-106">Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement texte (txt).</span><span class="sxs-lookup"><span data-stu-id="185bd-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Text (TXT) record.</span></span>

<span data-ttu-id="185bd-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="185bd-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="185bd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="185bd-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_TXTType : MicrosoftDNS_ResourceRecord
{
  string DescriptiveText;
};
```

## <a name="members"></a><span data-ttu-id="185bd-109">Membres</span><span class="sxs-lookup"><span data-stu-id="185bd-109">Members</span></span>

<span data-ttu-id="185bd-110">La classe **MicrosoftDNS \_ TXTType** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="185bd-110">The **MicrosoftDNS\_TXTType** class has these types of members:</span></span>

-   [<span data-ttu-id="185bd-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="185bd-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="185bd-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="185bd-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="185bd-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="185bd-113">Methods</span></span>

<span data-ttu-id="185bd-114">La classe **MicrosoftDNS \_ TXTType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="185bd-114">The **MicrosoftDNS\_TXTType** class has these methods.</span></span>



| <span data-ttu-id="185bd-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="185bd-115">Method</span></span>                             | <span data-ttu-id="185bd-116">Description</span><span class="sxs-lookup"><span data-stu-id="185bd-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="185bd-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="185bd-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="185bd-118">Instancie un type TXT de RR en fonction des données contenues dans les paramètres d’entrée de la méthode : le nom du serveur DNS de l’enregistrement, le nom du conteneur, le nom du propriétaire, la classe (valeur par défaut = IN), la valeur de la durée de vie et le texte de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="185bd-118">Instantiates a TXT Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the record's text.</span></span> <span data-ttu-id="185bd-119">Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="185bd-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="185bd-120">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="185bd-120">Qualifiers: Implemented, static</span></span><br/>        |
| <span data-ttu-id="185bd-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="185bd-121">**Modify**</span></span>                         | <span data-ttu-id="185bd-122">Met à jour la durée de vie et le texte descriptif avec les valeurs spécifiées en tant que paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="185bd-122">Updates the TTL and Descriptive Text to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="185bd-123">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="185bd-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="185bd-124">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="185bd-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="185bd-125">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="185bd-125">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="185bd-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="185bd-126">Properties</span></span>

<span data-ttu-id="185bd-127">La classe **MicrosoftDNS \_ TXTType** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="185bd-127">The **MicrosoftDNS\_TXTType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="185bd-128">**DescriptiveText**</span><span class="sxs-lookup"><span data-stu-id="185bd-128">**DescriptiveText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="185bd-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="185bd-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="185bd-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="185bd-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="185bd-131">Texte descriptif, dont la sémantique dépend du domaine propriétaire.</span><span class="sxs-lookup"><span data-stu-id="185bd-131">Descriptive text, the semantics of which depend on the owner domain.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="185bd-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="185bd-132">Requirements</span></span>



| <span data-ttu-id="185bd-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="185bd-133">Requirement</span></span> | <span data-ttu-id="185bd-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="185bd-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="185bd-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="185bd-135">Minimum supported client</span></span><br/> | <span data-ttu-id="185bd-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="185bd-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="185bd-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="185bd-137">Minimum supported server</span></span><br/> | <span data-ttu-id="185bd-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="185bd-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="185bd-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="185bd-139">Namespace</span></span><br/>                | <span data-ttu-id="185bd-140">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="185bd-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="185bd-141">MOF</span><span class="sxs-lookup"><span data-stu-id="185bd-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="185bd-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="185bd-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="185bd-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="185bd-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="185bd-144">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS TXTType**</span><span class="sxs-lookup"><span data-stu-id="185bd-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="185bd-145">**Modifier la méthode de la \_ classe TXTType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="185bd-145">**Modify Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-modify.md)
</dt> <dt>

[<span data-ttu-id="185bd-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="185bd-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





