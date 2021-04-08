---
title: Classe MicrosoftDNS_MDType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un agent de messagerie pour un enregistrement de domaine (MD).
ms.assetid: 11242372-65fe-44ee-845b-2430aec59127
keywords:
- MicrosoftDNS_MDType de la classe DNS
- MicrosoftDNS_MDType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_MDType
- MicrosoftDNS_MDType.CreateInstanceFromPropertyData
- MicrosoftDNS_MDType.Modify
- MicrosoftDNS_MDType.MDHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7641fda7a223fed7c2dc9229c5a3449c575e84ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843537"
---
# <a name="microsoftdns_mdtype-class"></a><span data-ttu-id="99e35-105">MicrosoftDNS \_ MDType, classe</span><span class="sxs-lookup"><span data-stu-id="99e35-105">MicrosoftDNS\_MDType class</span></span>

<span data-ttu-id="99e35-106">Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un agent de messagerie pour un enregistrement de domaine (MD).</span><span class="sxs-lookup"><span data-stu-id="99e35-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Agent for Domain (MD) record.</span></span>

<span data-ttu-id="99e35-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="99e35-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="99e35-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99e35-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MDType : MicrosoftDNS_ResourceRecord
{
  string MDHost;
};
```

## <a name="members"></a><span data-ttu-id="99e35-109">Membres</span><span class="sxs-lookup"><span data-stu-id="99e35-109">Members</span></span>

<span data-ttu-id="99e35-110">La classe **MicrosoftDNS \_ MDType** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="99e35-110">The **MicrosoftDNS\_MDType** class has these types of members:</span></span>

-   [<span data-ttu-id="99e35-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="99e35-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="99e35-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="99e35-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="99e35-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="99e35-113">Methods</span></span>

<span data-ttu-id="99e35-114">La classe **MicrosoftDNS \_ MDType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="99e35-114">The **MicrosoftDNS\_MDType** class has these methods.</span></span>



| <span data-ttu-id="99e35-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="99e35-115">Method</span></span>                             | <span data-ttu-id="99e35-116">Description</span><span class="sxs-lookup"><span data-stu-id="99e35-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99e35-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="99e35-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="99e35-118">Instancie un enregistrement de ressource DNS MD en fonction des données contenues dans les paramètres d’entrée de la méthode : le nom du serveur DNS de l’enregistrement, le nom du conteneur, le nom du propriétaire du domaine, la classe (valeur par défaut = IN), la valeur de durée de vie et l’hôte de l’agent de messagerie.</span><span class="sxs-lookup"><span data-stu-id="99e35-118">Instantiates a DNS MD Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the domain, class (default = IN), time-to-live value and the host of the mail agent.</span></span> <span data-ttu-id="99e35-119">Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="99e35-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="99e35-120">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="99e35-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="99e35-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="99e35-121">**Modify**</span></span>                         | <span data-ttu-id="99e35-122">Met à jour les hôtes TTL et MD avec les valeurs spécifiées en tant que paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="99e35-122">Updates the TTL and MD host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="99e35-123">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="99e35-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="99e35-124">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="99e35-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="99e35-125">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="99e35-125">Qualifiers: Implemented</span></span><br/>                                 |



 

### <a name="properties"></a><span data-ttu-id="99e35-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="99e35-126">Properties</span></span>

<span data-ttu-id="99e35-127">La classe **MicrosoftDNS \_ MDType** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="99e35-127">The **MicrosoftDNS\_MDType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="99e35-128">**MDHost**</span><span class="sxs-lookup"><span data-stu-id="99e35-128">**MDHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99e35-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="99e35-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="99e35-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="99e35-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="99e35-131">Nom de domaine complet qui spécifie un hôte avec un agent de messagerie capable de transmettre des messages pour le domaine spécifié.</span><span class="sxs-lookup"><span data-stu-id="99e35-131">FQDN that specifies a host with a mail agent capable of delivering mail for the specified domain.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="99e35-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99e35-132">Requirements</span></span>



| <span data-ttu-id="99e35-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99e35-133">Requirement</span></span> | <span data-ttu-id="99e35-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="99e35-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99e35-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99e35-135">Minimum supported client</span></span><br/> | <span data-ttu-id="99e35-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="99e35-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="99e35-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99e35-137">Minimum supported server</span></span><br/> | <span data-ttu-id="99e35-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="99e35-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="99e35-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="99e35-139">Namespace</span></span><br/>                | <span data-ttu-id="99e35-140">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="99e35-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="99e35-141">MOF</span><span class="sxs-lookup"><span data-stu-id="99e35-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99e35-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="99e35-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99e35-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99e35-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99e35-144">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MDType**</span><span class="sxs-lookup"><span data-stu-id="99e35-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MDType Class**</span></span>](microsoftdns-mdtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="99e35-145">**Modifier la méthode de la \_ classe MDType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="99e35-145">**Modify Method of the MicrosoftDNS\_MDType Class**</span></span>](microsoftdns-mdtype-modify.md)
</dt> <dt>

[<span data-ttu-id="99e35-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="99e35-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





