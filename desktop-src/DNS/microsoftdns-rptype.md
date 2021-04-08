---
title: Classe MicrosoftDNS_RPType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement de personne responsable (RP).
ms.assetid: 2b1c1bbc-a69f-4480-a7f2-6420240d4ad8
keywords:
- MicrosoftDNS_RPType de la classe DNS
- MicrosoftDNS_RPType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType
- MicrosoftDNS_RPType.CreateInstanceFromPropertyData
- MicrosoftDNS_RPType.Modify
- MicrosoftDNS_RPType.RPMailbox
- MicrosoftDNS_RPType.TXTDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9aae8686016d26cb9007b21a06c125d56ed5207f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843765"
---
# <a name="microsoftdns_rptype-class"></a><span data-ttu-id="dd844-105">MicrosoftDNS \_ RPType, classe</span><span class="sxs-lookup"><span data-stu-id="dd844-105">MicrosoftDNS\_RPType class</span></span>

<span data-ttu-id="dd844-106">Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement de personne responsable (RP).</span><span class="sxs-lookup"><span data-stu-id="dd844-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Responsible Person (RP) record.</span></span>

<span data-ttu-id="dd844-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="dd844-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd844-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd844-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_RPType : MicrosoftDNS_ResourceRecord
{
  string RPMailbox;
  string TXTDomainName;
};
```

## <a name="members"></a><span data-ttu-id="dd844-109">Membres</span><span class="sxs-lookup"><span data-stu-id="dd844-109">Members</span></span>

<span data-ttu-id="dd844-110">La classe **MicrosoftDNS \_ RPType** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="dd844-110">The **MicrosoftDNS\_RPType** class has these types of members:</span></span>

-   [<span data-ttu-id="dd844-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dd844-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="dd844-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dd844-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dd844-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dd844-113">Methods</span></span>

<span data-ttu-id="dd844-114">La classe **MicrosoftDNS \_ RPType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="dd844-114">The **MicrosoftDNS\_RPType** class has these methods.</span></span>



| <span data-ttu-id="dd844-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="dd844-115">Method</span></span>                             | <span data-ttu-id="dd844-116">Description</span><span class="sxs-lookup"><span data-stu-id="dd844-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd844-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="dd844-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="dd844-118">Instancie un type de ressource RP en fonction des données contenues dans les paramètres d’entrée de la méthode : le nom du serveur DNS, le nom du conteneur, le nom du propriétaire/de la personne responsable, la classe (valeur par défaut = IN), la valeur de durée de vie et les noms de domaine pour la boîte aux lettres et les emplacements des RR TXT de la personne.</span><span class="sxs-lookup"><span data-stu-id="dd844-118">Instantiates an RP Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/responsible person Name, class (default = IN), time-to-live value and the domain names for the person's mailbox and TXT RR locations.</span></span> <span data-ttu-id="dd844-119">Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="dd844-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="dd844-120">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="dd844-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="dd844-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="dd844-121">**Modify**</span></span>                         | <span data-ttu-id="dd844-122">Cette méthode met à jour les noms de domaine TTL, RP et TXT sur les valeurs spécifiées comme paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="dd844-122">This method updates the TTL, RP Mailbox and TXT Domain Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="dd844-123">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="dd844-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="dd844-124">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="dd844-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="dd844-125">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="dd844-125">Qualifiers: Implemented</span></span><br/>                                  |



 

### <a name="properties"></a><span data-ttu-id="dd844-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dd844-126">Properties</span></span>

<span data-ttu-id="dd844-127">La classe **MicrosoftDNS \_ RPType** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="dd844-127">The **MicrosoftDNS\_RPType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd844-128">**RPMailbox**</span><span class="sxs-lookup"><span data-stu-id="dd844-128">**RPMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd844-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dd844-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd844-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dd844-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd844-131">Nom de domaine complet spécifiant la boîte aux lettres pour la personne responsable.</span><span class="sxs-lookup"><span data-stu-id="dd844-131">FQDN specifying the mailbox for the responsible person.</span></span>

</dd> <dt>

<span data-ttu-id="dd844-132">**TXTDomainName**</span><span class="sxs-lookup"><span data-stu-id="dd844-132">**TXTDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd844-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dd844-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd844-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dd844-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd844-135">Nom de domaine complet pour lequel existent les enregistrements de ressource TXT.</span><span class="sxs-lookup"><span data-stu-id="dd844-135">FQDN for which TXT Resource Records exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd844-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd844-136">Requirements</span></span>



| <span data-ttu-id="dd844-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd844-137">Requirement</span></span> | <span data-ttu-id="dd844-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd844-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd844-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd844-139">Minimum supported client</span></span><br/> | <span data-ttu-id="dd844-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd844-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="dd844-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd844-141">Minimum supported server</span></span><br/> | <span data-ttu-id="dd844-142">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd844-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dd844-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="dd844-143">Namespace</span></span><br/>                | <span data-ttu-id="dd844-144">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="dd844-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="dd844-145">MOF</span><span class="sxs-lookup"><span data-stu-id="dd844-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd844-146"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd844-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd844-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd844-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd844-148">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS RPType**</span><span class="sxs-lookup"><span data-stu-id="dd844-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="dd844-149">**Modifier la méthode de la \_ classe RPType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="dd844-149">**Modify Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-modify.md)
</dt> <dt>

[<span data-ttu-id="dd844-150">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="dd844-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





