---
title: Classe MicrosoftDNS_MFType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement de l’agent de transfert du courrier pour le domaine (MF).
ms.assetid: 0ba0fddd-c316-4a5b-ad65-6344dbe949c1
keywords:
- MicrosoftDNS_MFType de la classe DNS
- MicrosoftDNS_MFType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType
- MicrosoftDNS_MFType.CreateInstanceFromPropertyData
- MicrosoftDNS_MFType.Modify
- MicrosoftDNS_MFType.MFHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e030f695e95ee736b1c53a345201e0bd1addfe3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104740"
---
# <a name="microsoftdns_mftype-class"></a><span data-ttu-id="4f687-105">MicrosoftDNS \_ MFType, classe</span><span class="sxs-lookup"><span data-stu-id="4f687-105">MicrosoftDNS\_MFType class</span></span>

<span data-ttu-id="4f687-106">Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement de l’agent de transfert du courrier pour le domaine (MF).</span><span class="sxs-lookup"><span data-stu-id="4f687-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Forwarding Agent for Domain (MF) record.</span></span>

<span data-ttu-id="4f687-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="4f687-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f687-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f687-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MFType : MicrosoftDNS_ResourceRecord
{
  string MFHost;
};
```

## <a name="members"></a><span data-ttu-id="4f687-109">Membres</span><span class="sxs-lookup"><span data-stu-id="4f687-109">Members</span></span>

<span data-ttu-id="4f687-110">La classe **MicrosoftDNS \_ MFType** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4f687-110">The **MicrosoftDNS\_MFType** class has these types of members:</span></span>

-   [<span data-ttu-id="4f687-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4f687-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="4f687-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4f687-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4f687-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4f687-113">Methods</span></span>

<span data-ttu-id="4f687-114">La classe **MicrosoftDNS \_ MFType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4f687-114">The **MicrosoftDNS\_MFType** class has these methods.</span></span>



| <span data-ttu-id="4f687-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="4f687-115">Method</span></span>                             | <span data-ttu-id="4f687-116">Description</span><span class="sxs-lookup"><span data-stu-id="4f687-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f687-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="4f687-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="4f687-118">Cette méthode instancie un type MF de RR en fonction des données contenues dans les paramètres d’entrée de la méthode : le nom du serveur DNS de l’enregistrement, le nom du conteneur, le nom du propriétaire du domaine, la classe (valeur par défaut = IN), la valeur de la durée de vie et l’hôte de l’agent de messagerie.</span><span class="sxs-lookup"><span data-stu-id="4f687-118">This method instantiates an MF Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the domain, class (default = IN), time-to-live value and the host of the mail agent.</span></span> <span data-ttu-id="4f687-119">Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="4f687-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="4f687-120">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="4f687-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="4f687-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="4f687-121">**Modify**</span></span>                         | <span data-ttu-id="4f687-122">Cette méthode met à jour l’hôte TTL et MF avec les valeurs spécifiées en tant que paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4f687-122">This method updates the TTL and MF Host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="4f687-123">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="4f687-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="4f687-124">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="4f687-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="4f687-125">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="4f687-125">Qualifiers: Implemented</span></span><br/>                         |



 

### <a name="properties"></a><span data-ttu-id="4f687-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4f687-126">Properties</span></span>

<span data-ttu-id="4f687-127">La classe **MicrosoftDNS \_ MFType** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="4f687-127">The **MicrosoftDNS\_MFType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f687-128">**MFHost**</span><span class="sxs-lookup"><span data-stu-id="4f687-128">**MFHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f687-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4f687-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f687-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f687-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f687-131">Nom de domaine complet spécifiant un ordinateur hôte avec un agent de messagerie qui va accepter le courrier pour le transfert vers le domaine spécifié.</span><span class="sxs-lookup"><span data-stu-id="4f687-131">FQDN specifying a host with a mail agent that will accept mail for forwarding to the specified domain.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f687-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f687-132">Requirements</span></span>



| <span data-ttu-id="4f687-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f687-133">Requirement</span></span> | <span data-ttu-id="4f687-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f687-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f687-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f687-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4f687-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f687-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4f687-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f687-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4f687-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f687-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4f687-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4f687-139">Namespace</span></span><br/>                | <span data-ttu-id="4f687-140">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="4f687-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="4f687-141">MOF</span><span class="sxs-lookup"><span data-stu-id="4f687-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f687-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f687-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f687-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f687-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f687-144">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MFType**</span><span class="sxs-lookup"><span data-stu-id="4f687-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="4f687-145">**Modifier la méthode de la \_ classe MFType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="4f687-145">**Modify Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-modify.md)
</dt> <dt>

[<span data-ttu-id="4f687-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="4f687-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





