---
title: Classe MicrosoftDNS_WKSType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement Well-Known services (WKS).
ms.assetid: 7bbfd518-d473-4127-949b-9133a43ac7a7
keywords:
- MicrosoftDNS_WKSType de la classe DNS
- MicrosoftDNS_WKSType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType
- MicrosoftDNS_WKSType.CreateInstanceFromPropertyData
- MicrosoftDNS_WKSType.Modify
- MicrosoftDNS_WKSType.InternetAddress
- MicrosoftDNS_WKSType.IPProtocol
- MicrosoftDNS_WKSType.Services
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f7fde08721bb8bb62b93f72b792060b06c15dad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942367"
---
# <a name="microsoftdns_wkstype-class"></a><span data-ttu-id="f5997-105">MicrosoftDNS \_ WKSType, classe</span><span class="sxs-lookup"><span data-stu-id="f5997-105">MicrosoftDNS\_WKSType class</span></span>

<span data-ttu-id="f5997-106">Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement Well-Known services (WKS).</span><span class="sxs-lookup"><span data-stu-id="f5997-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Well-Known Services (WKS) record.</span></span>

<span data-ttu-id="f5997-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="f5997-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5997-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5997-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_WKSType : MicrosoftDNS_ResourceRecord
{
  string InternetAddress;
  string IPProtocol;
  string Services;
};
```

## <a name="members"></a><span data-ttu-id="f5997-109">Membres</span><span class="sxs-lookup"><span data-stu-id="f5997-109">Members</span></span>

<span data-ttu-id="f5997-110">La classe **MicrosoftDNS \_ WKSType** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f5997-110">The **MicrosoftDNS\_WKSType** class has these types of members:</span></span>

-   [<span data-ttu-id="f5997-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f5997-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="f5997-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f5997-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f5997-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f5997-113">Methods</span></span>

<span data-ttu-id="f5997-114">La classe **MicrosoftDNS \_ WKSType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="f5997-114">The **MicrosoftDNS\_WKSType** class has these methods.</span></span>



| <span data-ttu-id="f5997-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="f5997-115">Method</span></span>                             | <span data-ttu-id="f5997-116">Description</span><span class="sxs-lookup"><span data-stu-id="f5997-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5997-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="f5997-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="f5997-118">Instancie un type WKS de RR en fonction des données contenues dans les paramètres d’entrée de la méthode : le nom du serveur DNS de l’enregistrement, le nom du conteneur, le nom du propriétaire, la classe (valeur par défaut = IN), la valeur de la durée de vie et l’adresse Internet du propriétaire, le protocole IP et le masque de bits du port.</span><span class="sxs-lookup"><span data-stu-id="f5997-118">Instantiates a WKS Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the owner's Internet Address, IP protocol and port bit mask.</span></span> <span data-ttu-id="f5997-119">Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="f5997-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="f5997-120">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="f5997-120">Qualifiers: Implemented, static</span></span><br/>  |
| <span data-ttu-id="f5997-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="f5997-121">**Modify**</span></span>                         | <span data-ttu-id="f5997-122">Cette méthode met à jour la durée de vie, l’adresse Internet, le protocole IP et les services avec les valeurs spécifiées en tant que paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="f5997-122">This method updates the TTL, Internet Address, IP Protocol, and Services to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="f5997-123">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="f5997-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="f5997-124">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="f5997-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="f5997-125">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="f5997-125">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f5997-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f5997-126">Properties</span></span>

<span data-ttu-id="f5997-127">La classe **MicrosoftDNS \_ WKSType** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="f5997-127">The **MicrosoftDNS\_WKSType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f5997-128">**InternetAddress**</span><span class="sxs-lookup"><span data-stu-id="f5997-128">**InternetAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5997-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f5997-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5997-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f5997-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5997-131">Adresse IP Internet pour le propriétaire de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f5997-131">Internet IP address for the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="f5997-132">**IPProtocol**</span><span class="sxs-lookup"><span data-stu-id="f5997-132">**IPProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5997-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f5997-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5997-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f5997-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5997-135">Chaîne représentant le protocole IP pour cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f5997-135">String representing the IP protocol for this record.</span></span> <span data-ttu-id="f5997-136">Les valeurs valides sont UDP ou TCP.</span><span class="sxs-lookup"><span data-stu-id="f5997-136">Valid values are UDP or TCP.</span></span>

</dd> <dt>

<span data-ttu-id="f5997-137">**Services**</span><span class="sxs-lookup"><span data-stu-id="f5997-137">**Services**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5997-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f5997-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5997-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f5997-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5997-140">Chaîne contenant tous les services utilisés par l’enregistrement du service bien connu (WKS).</span><span class="sxs-lookup"><span data-stu-id="f5997-140">String containing all services used by the Well Known Service (WKS) record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5997-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5997-141">Requirements</span></span>



| <span data-ttu-id="f5997-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5997-142">Requirement</span></span> | <span data-ttu-id="f5997-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5997-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5997-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5997-144">Minimum supported client</span></span><br/> | <span data-ttu-id="f5997-145">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5997-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f5997-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5997-146">Minimum supported server</span></span><br/> | <span data-ttu-id="f5997-147">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5997-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f5997-148">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f5997-148">Namespace</span></span><br/>                | <span data-ttu-id="f5997-149">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="f5997-149">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f5997-150">MOF</span><span class="sxs-lookup"><span data-stu-id="f5997-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5997-151"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5997-151"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5997-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5997-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5997-153">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS WKSType**</span><span class="sxs-lookup"><span data-stu-id="f5997-153">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="f5997-154">**Modifier la méthode de la \_ classe WKSType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="f5997-154">**Modify Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-modify.md)
</dt> <dt>

[<span data-ttu-id="f5997-155">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="f5997-155">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





