---
title: Classe MicrosoftDNS_MGType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement de groupe de messagerie (mg).
ms.assetid: ce5795d1-e575-46ef-ad82-62b329e261d6
keywords:
- MicrosoftDNS_MGType de la classe DNS
- MicrosoftDNS_MGType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType
- MicrosoftDNS_MGType.CreateInstanceFromPropertyData
- MicrosoftDNS_MGType.Modify
- MicrosoftDNS_MGType.MGMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4772f8841977fbeae1f0bf609a65a9511bc704a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509370"
---
# <a name="microsoftdns_mgtype-class"></a><span data-ttu-id="87b93-105">MicrosoftDNS \_ MGType, classe</span><span class="sxs-lookup"><span data-stu-id="87b93-105">MicrosoftDNS\_MGType class</span></span>

<span data-ttu-id="87b93-106">Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement de groupe de messagerie (mg).</span><span class="sxs-lookup"><span data-stu-id="87b93-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Group (MG) record.</span></span>

<span data-ttu-id="87b93-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="87b93-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="87b93-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87b93-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MGType : MicrosoftDNS_ResourceRecord
{
  string MGMailbox;
};
```

## <a name="members"></a><span data-ttu-id="87b93-109">Membres</span><span class="sxs-lookup"><span data-stu-id="87b93-109">Members</span></span>

<span data-ttu-id="87b93-110">La classe **MicrosoftDNS \_ MGType** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="87b93-110">The **MicrosoftDNS\_MGType** class has these types of members:</span></span>

-   [<span data-ttu-id="87b93-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="87b93-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="87b93-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="87b93-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="87b93-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="87b93-113">Methods</span></span>

<span data-ttu-id="87b93-114">La classe **MicrosoftDNS \_ MGType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="87b93-114">The **MicrosoftDNS\_MGType** class has these methods.</span></span>



| <span data-ttu-id="87b93-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="87b93-115">Method</span></span>                             | <span data-ttu-id="87b93-116">Description</span><span class="sxs-lookup"><span data-stu-id="87b93-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87b93-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="87b93-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="87b93-118">Cette méthode instancie un type de RR MG basé sur les données contenues dans les paramètres d’entrée de la méthode : le nom du serveur DNS de l’enregistrement, le nom du conteneur, le nom du propriétaire du groupe de messagerie, la classe (valeur par défaut = IN), la valeur de durée de vie et le nom de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="87b93-118">This method instantiates an MG Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mail group, class (default = IN), time-to-live value and the mailbox name.</span></span> <span data-ttu-id="87b93-119">Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="87b93-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="87b93-120">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="87b93-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="87b93-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="87b93-121">**Modify**</span></span>                         | <span data-ttu-id="87b93-122">Cette méthode met à jour la boîte aux lettres TTL et MG avec les valeurs spécifiées comme paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="87b93-122">This method updates the TTL and MG Mailbox to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="87b93-123">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="87b93-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="87b93-124">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="87b93-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="87b93-125">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="87b93-125">Qualifiers: Implemented</span></span><br/>                |



 

### <a name="properties"></a><span data-ttu-id="87b93-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="87b93-126">Properties</span></span>

<span data-ttu-id="87b93-127">La classe **MicrosoftDNS \_ MGType** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="87b93-127">The **MicrosoftDNS\_MGType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="87b93-128">**MGMailbox**</span><span class="sxs-lookup"><span data-stu-id="87b93-128">**MGMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87b93-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="87b93-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87b93-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87b93-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87b93-131">Nom de domaine complet spécifiant une boîte aux lettres qui est membre du groupe de messagerie spécifié par le nom du propriétaire de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="87b93-131">FQDN specifying a mailbox that is a member of the mail group specified by the record's owner name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="87b93-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87b93-132">Requirements</span></span>



| <span data-ttu-id="87b93-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87b93-133">Requirement</span></span> | <span data-ttu-id="87b93-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="87b93-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87b93-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87b93-135">Minimum supported client</span></span><br/> | <span data-ttu-id="87b93-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="87b93-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="87b93-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87b93-137">Minimum supported server</span></span><br/> | <span data-ttu-id="87b93-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87b93-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="87b93-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="87b93-139">Namespace</span></span><br/>                | <span data-ttu-id="87b93-140">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="87b93-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="87b93-141">MOF</span><span class="sxs-lookup"><span data-stu-id="87b93-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87b93-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="87b93-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87b93-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87b93-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87b93-144">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MGType**</span><span class="sxs-lookup"><span data-stu-id="87b93-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="87b93-145">**Modifier la méthode de la \_ classe MGType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="87b93-145">**Modify Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-modify.md)
</dt> <dt>

[<span data-ttu-id="87b93-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="87b93-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





