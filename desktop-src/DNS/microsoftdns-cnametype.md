---
title: Classe MicrosoftDNS_CNAMEType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement de nom canonique (CNAME).
ms.assetid: 93a972e3-abb1-425f-beb7-32abe7d0b485
keywords:
- MicrosoftDNS_CNAMEType de la classe DNS
- MicrosoftDNS_CNAMEType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_CNAMEType
- MicrosoftDNS_CNAMEType.CreateInstanceFromPropertyData
- MicrosoftDNS_CNAMEType.Modify
- MicrosoftDNS_CNAMEType.PrimaryName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dca8729c2c750e1cef774b5f0f3eadc3e2f6fbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843593"
---
# <a name="microsoftdns_cnametype-class"></a><span data-ttu-id="d5d44-105">MicrosoftDNS \_ CNAMEType, classe</span><span class="sxs-lookup"><span data-stu-id="d5d44-105">MicrosoftDNS\_CNAMEType class</span></span>

<span data-ttu-id="d5d44-106">Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement de nom canonique (CNAME).</span><span class="sxs-lookup"><span data-stu-id="d5d44-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Canonical Name (CNAME) record.</span></span>

<span data-ttu-id="d5d44-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="d5d44-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5d44-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5d44-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_CNAMEType : MicrosoftDNS_ResourceRecord
{
  string PrimaryName;
};
```

## <a name="members"></a><span data-ttu-id="d5d44-109">Membres</span><span class="sxs-lookup"><span data-stu-id="d5d44-109">Members</span></span>

<span data-ttu-id="d5d44-110">La classe **MicrosoftDNS \_ CNAMEType** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d5d44-110">The **MicrosoftDNS\_CNAMEType** class has these types of members:</span></span>

-   [<span data-ttu-id="d5d44-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d5d44-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="d5d44-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d5d44-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d5d44-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d5d44-113">Methods</span></span>

<span data-ttu-id="d5d44-114">La classe **MicrosoftDNS \_ CNAMEType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d5d44-114">The **MicrosoftDNS\_CNAMEType** class has these methods.</span></span>



| <span data-ttu-id="d5d44-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="d5d44-115">Method</span></span>                             | <span data-ttu-id="d5d44-116">Description</span><span class="sxs-lookup"><span data-stu-id="d5d44-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                    |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5d44-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="d5d44-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="d5d44-118">Instancie un enregistrement de ressource CNAMe en fonction des données contenues dans les paramètres d’entrée de la méthode : le nom du serveur DNS, le nom du conteneur, le nom du propriétaire, la classe (valeur par défaut = IN), la valeur de la durée de vie et le nom principal de l’enregistrement CNAMe.</span><span class="sxs-lookup"><span data-stu-id="d5d44-118">Instantiates a CNAME Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the primary name of the CNAME record.</span></span> <span data-ttu-id="d5d44-119">Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="d5d44-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="d5d44-120">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="d5d44-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="d5d44-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="d5d44-121">**Modify**</span></span>                         | <span data-ttu-id="d5d44-122">Met à jour la durée de vie et le nom principal avec les valeurs spécifiées en tant que paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="d5d44-122">Updates the TTL and Primary Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="d5d44-123">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="d5d44-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="d5d44-124">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="d5d44-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="d5d44-125">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="d5d44-125">Qualifiers: Implemented</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="d5d44-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d5d44-126">Properties</span></span>

<span data-ttu-id="d5d44-127">La classe **MicrosoftDNS \_ CNAMEType** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d5d44-127">The **MicrosoftDNS\_CNAMEType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d5d44-128">**PrimaryName**</span><span class="sxs-lookup"><span data-stu-id="d5d44-128">**PrimaryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d44-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d5d44-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d5d44-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d5d44-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d5d44-131">Nom canonique ou nom principal du propriétaire de l’enregistrement CNAMe.</span><span class="sxs-lookup"><span data-stu-id="d5d44-131">Canonical, or primary name for the owner of the CNAME record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5d44-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5d44-132">Requirements</span></span>



| <span data-ttu-id="d5d44-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5d44-133">Requirement</span></span> | <span data-ttu-id="d5d44-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5d44-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5d44-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5d44-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d5d44-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5d44-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d5d44-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5d44-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d5d44-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5d44-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d5d44-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d5d44-139">Namespace</span></span><br/>                | <span data-ttu-id="d5d44-140">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="d5d44-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d5d44-141">MOF</span><span class="sxs-lookup"><span data-stu-id="d5d44-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5d44-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5d44-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5d44-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5d44-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5d44-144">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS CNAMEType**</span><span class="sxs-lookup"><span data-stu-id="d5d44-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_CNAMEType Class**</span></span>](microsoftdns-cnametype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="d5d44-145">**Modifier la méthode de la \_ classe CNAMEType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="d5d44-145">**Modify Method of the MicrosoftDNS\_CNAMEType Class**</span></span>](microsoftdns-cnametype-modify.md)
</dt> <dt>

[<span data-ttu-id="d5d44-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="d5d44-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





