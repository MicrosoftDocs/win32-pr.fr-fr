---
title: Classe MicrosoftDNS_ISDNType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement RNIS.
ms.assetid: 8925042c-65d3-465f-aedd-9f7c862620b5
keywords:
- MicrosoftDNS_ISDNType de la classe DNS
- MicrosoftDNS_ISDNType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType
- MicrosoftDNS_ISDNType.CreateInstanceFromPropertyData
- MicrosoftDNS_ISDNType.Modify
- MicrosoftDNS_ISDNType.ISDNNumber
- MicrosoftDNS_ISDNType.SubAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4e8b50d75f7b6d57226247c978ced45e07b1acc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102957"
---
# <a name="microsoftdns_isdntype-class"></a><span data-ttu-id="4fc92-105">MicrosoftDNS \_ ISDNType, classe</span><span class="sxs-lookup"><span data-stu-id="4fc92-105">MicrosoftDNS\_ISDNType class</span></span>

<span data-ttu-id="4fc92-106">Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement RNIS.</span><span class="sxs-lookup"><span data-stu-id="4fc92-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an ISDN record.</span></span>

<span data-ttu-id="4fc92-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="4fc92-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fc92-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4fc92-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_ISDNType : MicrosoftDNS_ResourceRecord
{
  string ISDNNumber;
  string SubAddress;
};
```

## <a name="members"></a><span data-ttu-id="4fc92-109">Membres</span><span class="sxs-lookup"><span data-stu-id="4fc92-109">Members</span></span>

<span data-ttu-id="4fc92-110">La classe **MicrosoftDNS \_ ISDNType** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4fc92-110">The **MicrosoftDNS\_ISDNType** class has these types of members:</span></span>

-   [<span data-ttu-id="4fc92-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4fc92-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="4fc92-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4fc92-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4fc92-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4fc92-113">Methods</span></span>

<span data-ttu-id="4fc92-114">La classe **MicrosoftDNS \_ ISDNType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4fc92-114">The **MicrosoftDNS\_ISDNType** class has these methods.</span></span>



| <span data-ttu-id="4fc92-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="4fc92-115">Method</span></span>                             | <span data-ttu-id="4fc92-116">Description</span><span class="sxs-lookup"><span data-stu-id="4fc92-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fc92-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="4fc92-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="4fc92-118">Instancie un enregistrement de ressource RNIS en fonction des données contenues dans les paramètres d’entrée de la méthode : le nom du serveur DNS, le nom du conteneur, le nom du propriétaire, la classe (valeur par défaut = IN), la valeur de la durée de vie et le numéro RNIS et la sous-adresse du propriétaire.</span><span class="sxs-lookup"><span data-stu-id="4fc92-118">Instantiates an ISDN Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the ISDN number and subaddress of the owner.</span></span> <span data-ttu-id="4fc92-119">Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="4fc92-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="4fc92-120">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="4fc92-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="4fc92-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="4fc92-121">**Modify**</span></span>                         | <span data-ttu-id="4fc92-122">Met à jour la durée de vie, le numéro RNIS et la sous-adresse selon les valeurs spécifiées comme paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4fc92-122">Updates the TTL, ISDN Number, and Subaddress to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="4fc92-123">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="4fc92-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="4fc92-124">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="4fc92-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="4fc92-125">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="4fc92-125">Qualifiers: Implemented</span></span><br/>                   |



 

### <a name="properties"></a><span data-ttu-id="4fc92-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4fc92-126">Properties</span></span>

<span data-ttu-id="4fc92-127">La classe **MicrosoftDNS \_ ISDNType** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="4fc92-127">The **MicrosoftDNS\_ISDNType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4fc92-128">**ISDNNumber**</span><span class="sxs-lookup"><span data-stu-id="4fc92-128">**ISDNNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc92-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4fc92-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fc92-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4fc92-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fc92-131">Numéro RNIS et DDI du propriétaire de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="4fc92-131">ISDN number and DDI of the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="4fc92-132">**Sous-adresse**</span><span class="sxs-lookup"><span data-stu-id="4fc92-132">**SubAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc92-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4fc92-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fc92-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4fc92-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fc92-135">Sous-adresse du propriétaire, si elle est définie.</span><span class="sxs-lookup"><span data-stu-id="4fc92-135">Subaddress of the owner, if defined.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4fc92-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4fc92-136">Requirements</span></span>



| <span data-ttu-id="4fc92-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4fc92-137">Requirement</span></span> | <span data-ttu-id="4fc92-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="4fc92-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fc92-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4fc92-139">Minimum supported client</span></span><br/> | <span data-ttu-id="4fc92-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4fc92-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4fc92-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4fc92-141">Minimum supported server</span></span><br/> | <span data-ttu-id="4fc92-142">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4fc92-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4fc92-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4fc92-143">Namespace</span></span><br/>                | <span data-ttu-id="4fc92-144">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="4fc92-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="4fc92-145">MOF</span><span class="sxs-lookup"><span data-stu-id="4fc92-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4fc92-146"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4fc92-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fc92-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fc92-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fc92-148">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS ISDNType**</span><span class="sxs-lookup"><span data-stu-id="4fc92-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="4fc92-149">**Modifier la méthode de la \_ classe ISDNType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="4fc92-149">**Modify Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-modify.md)
</dt> <dt>

[<span data-ttu-id="4fc92-150">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="4fc92-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





