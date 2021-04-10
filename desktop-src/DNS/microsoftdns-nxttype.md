---
title: Classe MicrosoftDNS_NXTType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un RR (NXT) suivant.
ms.assetid: bb24509e-083b-4432-89e3-501167f12299
keywords:
- MicrosoftDNS_NXTType de la classe DNS
- MicrosoftDNS_NXTType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType
- MicrosoftDNS_NXTType.CreateInstanceFromPropertyData
- MicrosoftDNS_NXTType.Modify
- MicrosoftDNS_NXTType.NextDomainName
- MicrosoftDNS_NXTType.Types
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79db82b3ae760c31d4e6fef80eb01469cb2bb41d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104164"
---
# <a name="microsoftdns_nxttype-class"></a><span data-ttu-id="086e1-105">MicrosoftDNS \_ NXTType, classe</span><span class="sxs-lookup"><span data-stu-id="086e1-105">MicrosoftDNS\_NXTType class</span></span>

<span data-ttu-id="086e1-106">Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un RR (NXT) suivant.</span><span class="sxs-lookup"><span data-stu-id="086e1-106">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Next (NXT) RR.</span></span>

<span data-ttu-id="086e1-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="086e1-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="086e1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="086e1-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_NXTType : MicrosoftDNS_ResourceRecord
{
  string NextDomainName;
  string Types;
};
```

## <a name="members"></a><span data-ttu-id="086e1-109">Membres</span><span class="sxs-lookup"><span data-stu-id="086e1-109">Members</span></span>

<span data-ttu-id="086e1-110">La classe **MicrosoftDNS \_ NXTType** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="086e1-110">The **MicrosoftDNS\_NXTType** class has these types of members:</span></span>

-   [<span data-ttu-id="086e1-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="086e1-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="086e1-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="086e1-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="086e1-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="086e1-113">Methods</span></span>

<span data-ttu-id="086e1-114">La classe **MicrosoftDNS \_ NXTType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="086e1-114">The **MicrosoftDNS\_NXTType** class has these methods.</span></span>



| <span data-ttu-id="086e1-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="086e1-115">Method</span></span>                             | <span data-ttu-id="086e1-116">Description</span><span class="sxs-lookup"><span data-stu-id="086e1-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="086e1-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="086e1-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="086e1-118">Instancie un enregistrement de ressource NXT basé sur les données dans les paramètres d’entrée de la méthode : le nom du serveur DNS, le nom du conteneur, le nom du propriétaire, la classe (valeur par défaut = IN), la valeur de durée de vie et l’indicateur de mappage WINS, le délai d’attente de la recherche inversée, le délai d’expiration du cache WINS et le nom</span><span class="sxs-lookup"><span data-stu-id="086e1-118">Instantiates an NXT Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out, and domain name to append.</span></span> <span data-ttu-id="086e1-119">Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="086e1-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="086e1-120">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="086e1-120">Qualifiers: Implemented, static</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="086e1-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="086e1-121">**Modify**</span></span>                         | <span data-ttu-id="086e1-122">Met à jour la durée de vie, l’indicateur de mappage, le délai d’attente de recherche, le délai d’attente du cache et le domaine de résultat sur les valeurs spécifiées comme paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="086e1-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Result Domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="086e1-123">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="086e1-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="086e1-124">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="086e1-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="086e1-125">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="086e1-125">Qualifiers: Implemented</span></span><br/> <span data-ttu-id="086e1-126">**Windows Server 2003 :** Cette méthode met également à jour les NextDomainName et les types avec les valeurs spécifiées en tant que paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="086e1-126">**Windows Server 2003:** This method also updates the NextDomainName and Types to the values specified as the input parameters of this method.</span></span><br/> <br/> |



 

### <a name="properties"></a><span data-ttu-id="086e1-127">Propriétés</span><span class="sxs-lookup"><span data-stu-id="086e1-127">Properties</span></span>

<span data-ttu-id="086e1-128">La classe **MicrosoftDNS \_ NXTType** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="086e1-128">The **MicrosoftDNS\_NXTType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="086e1-129">**NextDomainName**</span><span class="sxs-lookup"><span data-stu-id="086e1-129">**NextDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="086e1-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="086e1-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="086e1-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="086e1-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="086e1-132">Nom de domaine suivant.</span><span class="sxs-lookup"><span data-stu-id="086e1-132">Next domain name.</span></span>

</dd> <dt>

<span data-ttu-id="086e1-133">**Types**</span><span class="sxs-lookup"><span data-stu-id="086e1-133">**Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="086e1-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="086e1-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="086e1-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="086e1-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="086e1-136">Liste séparée par des espaces des mnémoniques de type RR pour le nom de propriétaire de l’enregistrement de ressource NXT.</span><span class="sxs-lookup"><span data-stu-id="086e1-136">Space-separated list of the RR-type mnemonics for the owner name of the NXT Resource Record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="086e1-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="086e1-137">Requirements</span></span>



| <span data-ttu-id="086e1-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="086e1-138">Requirement</span></span> | <span data-ttu-id="086e1-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="086e1-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="086e1-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="086e1-140">Minimum supported client</span></span><br/> | <span data-ttu-id="086e1-141">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="086e1-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="086e1-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="086e1-142">Minimum supported server</span></span><br/> | <span data-ttu-id="086e1-143">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="086e1-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="086e1-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="086e1-144">Namespace</span></span><br/>                | <span data-ttu-id="086e1-145">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="086e1-145">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="086e1-146">MOF</span><span class="sxs-lookup"><span data-stu-id="086e1-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="086e1-147"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="086e1-147"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="086e1-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="086e1-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="086e1-149">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS NXTType**</span><span class="sxs-lookup"><span data-stu-id="086e1-149">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="086e1-150">**Modifier la méthode de la \_ classe NXTType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="086e1-150">**Modify Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-modify.md)
</dt> <dt>

[<span data-ttu-id="086e1-151">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="086e1-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





