---
title: Classe MicrosoftDNS_MXType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement de ressource de messagerie (Mr).
ms.assetid: 7c147628-5bda-48dd-beb4-e630d1886da8
keywords:
- MicrosoftDNS_MXType de la classe DNS
- MicrosoftDNS_MXType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType
- MicrosoftDNS_MXType.CreateInstanceFromPropertyData
- MicrosoftDNS_MXType.Modify
- MicrosoftDNS_MXType.Preference
- MicrosoftDNS_MXType.MailExchange
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652743178b71b2f9fed296ecfa4427f85b5cf1c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942130"
---
# <a name="microsoftdns_mxtype-class"></a><span data-ttu-id="5876f-105">MicrosoftDNS \_ MXType, classe</span><span class="sxs-lookup"><span data-stu-id="5876f-105">MicrosoftDNS\_MXType class</span></span>

<span data-ttu-id="5876f-106">Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement de ressource de messagerie (Mr).</span><span class="sxs-lookup"><span data-stu-id="5876f-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Exchanger (MR) RR.</span></span>

<span data-ttu-id="5876f-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="5876f-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5876f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5876f-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MXType : MicrosoftDNS_ResourceRecord
{
  uint16 Preference;
  string MailExchange;
};
```

## <a name="members"></a><span data-ttu-id="5876f-109">Membres</span><span class="sxs-lookup"><span data-stu-id="5876f-109">Members</span></span>

<span data-ttu-id="5876f-110">La classe **MicrosoftDNS \_ MXType** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5876f-110">The **MicrosoftDNS\_MXType** class has these types of members:</span></span>

-   [<span data-ttu-id="5876f-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5876f-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="5876f-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5876f-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5876f-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5876f-113">Methods</span></span>

<span data-ttu-id="5876f-114">La classe **MicrosoftDNS \_ MXType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="5876f-114">The **MicrosoftDNS\_MXType** class has these methods.</span></span>



| <span data-ttu-id="5876f-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="5876f-115">Method</span></span>                             | <span data-ttu-id="5876f-116">Description</span><span class="sxs-lookup"><span data-stu-id="5876f-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5876f-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="5876f-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="5876f-118">Instancie un type MX de RR en fonction des données contenues dans les paramètres d’entrée de la méthode : le nom du serveur DNS, le nom du conteneur, le nom du propriétaire, la classe (valeur par défaut = IN), la valeur de la durée de vie, la préférence d’enregistrement et le nom d’hôte qui sont prêts pour l’échange de courrier.</span><span class="sxs-lookup"><span data-stu-id="5876f-118">Instantiates an MX Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, record preference, and host name willing to be a mail exchange.</span></span> <span data-ttu-id="5876f-119">Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="5876f-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="5876f-120">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="5876f-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="5876f-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="5876f-121">**Modify**</span></span>                         | <span data-ttu-id="5876f-122">Met à jour la durée de vie, la préférence et l’échange de messages avec les valeurs spécifiées comme paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="5876f-122">Updates the TTL, Preference, and Mail Exchange to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="5876f-123">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="5876f-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="5876f-124">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="5876f-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="5876f-125">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="5876f-125">Qualifiers: Implemented</span></span><br/>                         |



 

### <a name="properties"></a><span data-ttu-id="5876f-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5876f-126">Properties</span></span>

<span data-ttu-id="5876f-127">La classe **MicrosoftDNS \_ MXType** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5876f-127">The **MicrosoftDNS\_MXType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5876f-128">**MailExchange**</span><span class="sxs-lookup"><span data-stu-id="5876f-128">**MailExchange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5876f-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5876f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5876f-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5876f-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5876f-131">Nom de domaine complet spécifiant un ordinateur hôte prêt à agir comme échange de messagerie pour le nom du propriétaire.</span><span class="sxs-lookup"><span data-stu-id="5876f-131">FQDN specifying a host willing to act as a mail exchange for the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="5876f-132">**Relatives**</span><span class="sxs-lookup"><span data-stu-id="5876f-132">**Preference**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5876f-133">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5876f-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5876f-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5876f-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5876f-135">Préférence donnée à ce RR, parmi d’autres au même propriétaire.</span><span class="sxs-lookup"><span data-stu-id="5876f-135">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="5876f-136">Les valeurs les plus basses sont préférées.</span><span class="sxs-lookup"><span data-stu-id="5876f-136">Lower values are preferred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5876f-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5876f-137">Requirements</span></span>



| <span data-ttu-id="5876f-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5876f-138">Requirement</span></span> | <span data-ttu-id="5876f-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="5876f-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5876f-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5876f-140">Minimum supported client</span></span><br/> | <span data-ttu-id="5876f-141">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5876f-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5876f-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5876f-142">Minimum supported server</span></span><br/> | <span data-ttu-id="5876f-143">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5876f-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5876f-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5876f-144">Namespace</span></span><br/>                | <span data-ttu-id="5876f-145">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="5876f-145">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="5876f-146">MOF</span><span class="sxs-lookup"><span data-stu-id="5876f-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5876f-147"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5876f-147"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5876f-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5876f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5876f-149">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MXType**</span><span class="sxs-lookup"><span data-stu-id="5876f-149">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="5876f-150">**Modifier la méthode de la \_ classe MXType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="5876f-150">**Modify Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-modify.md)
</dt> <dt>

[<span data-ttu-id="5876f-151">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="5876f-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





