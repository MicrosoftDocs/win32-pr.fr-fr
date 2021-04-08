---
title: Classe MicrosoftDNS_ATMAType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement d’adresse ATM dans le nom (ATMA).
ms.assetid: 3e9e4032-08a0-4a2e-bcff-f461b69a44d4
keywords:
- MicrosoftDNS_ATMAType de la classe DNS
- MicrosoftDNS_ATMAType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType
- MicrosoftDNS_ATMAType.CreateInstanceFromPropertyData
- MicrosoftDNS_ATMAType.Modify
- MicrosoftDNS_ATMAType.Format
- MicrosoftDNS_ATMAType.ATMAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 237dc4ecb657e79e835abcfdacf90844fb05c5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942134"
---
# <a name="microsoftdns_atmatype-class"></a><span data-ttu-id="7a6f5-105">MicrosoftDNS \_ ATMAType, classe</span><span class="sxs-lookup"><span data-stu-id="7a6f5-105">MicrosoftDNS\_ATMAType class</span></span>

<span data-ttu-id="7a6f5-106">Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement d’adresse ATM dans le nom (ATMA).</span><span class="sxs-lookup"><span data-stu-id="7a6f5-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an ATM Address to Name (ATMA) record.</span></span>

<span data-ttu-id="7a6f5-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a6f5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a6f5-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_ATMAType : MicrosoftDNS_ResourceRecord
{
  uint16 Format;
  string ATMAddress;
};
```

## <a name="members"></a><span data-ttu-id="7a6f5-109">Membres</span><span class="sxs-lookup"><span data-stu-id="7a6f5-109">Members</span></span>

<span data-ttu-id="7a6f5-110">La classe **MicrosoftDNS \_ ATMAType** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7a6f5-110">The **MicrosoftDNS\_ATMAType** class has these types of members:</span></span>

-   [<span data-ttu-id="7a6f5-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7a6f5-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="7a6f5-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7a6f5-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7a6f5-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7a6f5-113">Methods</span></span>

<span data-ttu-id="7a6f5-114">La classe **MicrosoftDNS \_ ATMAType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-114">The **MicrosoftDNS\_ATMAType** class has these methods.</span></span>



| <span data-ttu-id="7a6f5-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="7a6f5-115">Method</span></span>                             | <span data-ttu-id="7a6f5-116">Description</span><span class="sxs-lookup"><span data-stu-id="7a6f5-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a6f5-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="7a6f5-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="7a6f5-118">Instancie un enregistrement de ressource ATMA en fonction des données contenues dans les paramètres d’entrée de la méthode : le nom du serveur DNS, le nom du conteneur, le nom du propriétaire/nœud, la classe (valeur par défaut = IN), la valeur de durée de vie et le format et l’adresse ATM.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-118">Instantiates an ATMA Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/Node Name, class (default = IN), time-to-live value, and ATM format and address.</span></span> <span data-ttu-id="7a6f5-119">Retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-119">Returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="7a6f5-120">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="7a6f5-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="7a6f5-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="7a6f5-121">**Modify**</span></span>                         | <span data-ttu-id="7a6f5-122">Met à jour l’adresse TTL, format et ATMA avec les valeurs spécifiées en tant que paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-122">Updates the TTL, Format and ATMA Address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="7a6f5-123">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-123">If a new value for a parameter is not specified, the current value for the parameter is not changed.</span></span> <span data-ttu-id="7a6f5-124">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="7a6f5-125">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="7a6f5-125">Qualifiers: Implemented</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="7a6f5-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7a6f5-126">Properties</span></span>

<span data-ttu-id="7a6f5-127">La classe **MicrosoftDNS \_ ATMAType** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-127">The **MicrosoftDNS\_ATMAType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7a6f5-128">**ATMAddress**</span><span class="sxs-lookup"><span data-stu-id="7a6f5-128">**ATMAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a6f5-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7a6f5-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a6f5-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7a6f5-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a6f5-131">Chaîne de longueur variable d’octets contenant l’adresse ATM du nœud/propriétaire auquel appartient ce RR.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-131">Variable length string of octets containing the ATM address of the node/owner to which this RR pertains.</span></span> <span data-ttu-id="7a6f5-132">Les 4 premiers octets du tableau sont utilisés pour stocker la taille de la chaîne d’octets.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-132">The first 4 bytes of the array are used to store the size of the octet string.</span></span> <span data-ttu-id="7a6f5-133">L’octet le plus significatif est stocké à l’octet 0.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-133">The most significant byte is stored in byte 0.</span></span>

</dd> <dt>

<span data-ttu-id="7a6f5-134">**Format**</span><span class="sxs-lookup"><span data-stu-id="7a6f5-134">**Format**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a6f5-135">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7a6f5-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7a6f5-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7a6f5-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a6f5-137">Format d’adresse ATM.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-137">ATM address format.</span></span> <span data-ttu-id="7a6f5-138">Les valeurs valides sont : 0 indiquant le format AESA (ATM End System Address) et 1 indiquant le format E. 164.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-138">Valid values are: 0 indicating ATM End System Address (AESA) format and 1 indicating E.164 format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a6f5-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a6f5-139">Requirements</span></span>



| <span data-ttu-id="7a6f5-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a6f5-140">Requirement</span></span> | <span data-ttu-id="7a6f5-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a6f5-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a6f5-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a6f5-142">Minimum supported client</span></span><br/> | <span data-ttu-id="7a6f5-143">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a6f5-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7a6f5-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a6f5-144">Minimum supported server</span></span><br/> | <span data-ttu-id="7a6f5-145">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a6f5-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7a6f5-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7a6f5-146">Namespace</span></span><br/>                | <span data-ttu-id="7a6f5-147">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="7a6f5-147">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="7a6f5-148">MOF</span><span class="sxs-lookup"><span data-stu-id="7a6f5-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a6f5-149"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a6f5-149"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a6f5-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a6f5-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a6f5-151">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS ATMAType**</span><span class="sxs-lookup"><span data-stu-id="7a6f5-151">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="7a6f5-152">**Modifier la méthode de la \_ classe ATMAType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="7a6f5-152">**Modify Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-modify.md)
</dt> <dt>

[<span data-ttu-id="7a6f5-153">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="7a6f5-153">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





