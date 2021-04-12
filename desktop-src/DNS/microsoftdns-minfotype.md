---
title: Classe MicrosoftDNS_MINFOType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement d’informations de messagerie (mInfo).
ms.assetid: 9c4b70b8-f9cf-4dea-8d2d-43e0de002d52
keywords:
- MicrosoftDNS_MINFOType de la classe DNS
- MicrosoftDNS_MINFOType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType
- MicrosoftDNS_MINFOType.CreateInstanceFromPropertyData
- MicrosoftDNS_MINFOType.Modify
- MicrosoftDNS_MINFOType.ResponsibleMailbox
- MicrosoftDNS_MINFOType.ErrorMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a7d230db9da32ce47cd4cfaf99c4978c4e63385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105937"
---
# <a name="microsoftdns_minfotype-class"></a><span data-ttu-id="c9dd6-105">MicrosoftDNS \_ MINFOType, classe</span><span class="sxs-lookup"><span data-stu-id="c9dd6-105">MicrosoftDNS\_MINFOType class</span></span>

<span data-ttu-id="c9dd6-106">Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement d’informations de messagerie (mInfo).</span><span class="sxs-lookup"><span data-stu-id="c9dd6-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Information (MINFO) record.</span></span>

<span data-ttu-id="c9dd6-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="c9dd6-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9dd6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9dd6-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MINFOType : MicrosoftDNS_ResourceRecord
{
  string ResponsibleMailbox;
  string ErrorMailbox;
};
```

## <a name="members"></a><span data-ttu-id="c9dd6-109">Membres</span><span class="sxs-lookup"><span data-stu-id="c9dd6-109">Members</span></span>

<span data-ttu-id="c9dd6-110">La classe **MicrosoftDNS \_ MINFOType** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c9dd6-110">The **MicrosoftDNS\_MINFOType** class has these types of members:</span></span>

-   [<span data-ttu-id="c9dd6-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c9dd6-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c9dd6-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c9dd6-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c9dd6-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c9dd6-113">Methods</span></span>

<span data-ttu-id="c9dd6-114">La classe **MicrosoftDNS \_ MINFOType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c9dd6-114">The **MicrosoftDNS\_MINFOType** class has these methods.</span></span>



| <span data-ttu-id="c9dd6-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="c9dd6-115">Method</span></span>                             | <span data-ttu-id="c9dd6-116">Description</span><span class="sxs-lookup"><span data-stu-id="c9dd6-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9dd6-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="c9dd6-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="c9dd6-118">Instancie un type d’enregistrement de ressource MINFO en fonction des données contenues dans les paramètres d’entrée de la méthode : le nom du serveur DNS de l’enregistrement, le nom du conteneur, le nom du propriétaire de la liste/zone de messagerie, la classe (valeur par défaut = IN), la valeur de durée de vie et les boîtes aux lettres responsables et d’erreur.</span><span class="sxs-lookup"><span data-stu-id="c9dd6-118">Instantiates an MINFO Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mail list/box, class (default = IN), time-to-live value and the responsible and error mailboxes.</span></span> <span data-ttu-id="c9dd6-119">Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="c9dd6-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="c9dd6-120">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="c9dd6-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="c9dd6-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="c9dd6-121">**Modify**</span></span>                         | <span data-ttu-id="c9dd6-122">Cette méthode met à jour la durée de vie, la boîte aux lettres responsable et la boîte aux lettres d’erreur sur les valeurs spécifiées comme paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="c9dd6-122">This method updates the TTL, Responsible Mailbox, and Error Mailbox to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="c9dd6-123">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="c9dd6-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="c9dd6-124">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="c9dd6-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="c9dd6-125">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="c9dd6-125">Qualifiers: Implemented</span></span><br/>    |



 

### <a name="properties"></a><span data-ttu-id="c9dd6-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c9dd6-126">Properties</span></span>

<span data-ttu-id="c9dd6-127">La classe **MicrosoftDNS \_ MINFOType** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c9dd6-127">The **MicrosoftDNS\_MINFOType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c9dd6-128">**ErrorMailbox**</span><span class="sxs-lookup"><span data-stu-id="c9dd6-128">**ErrorMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9dd6-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c9dd6-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9dd6-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9dd6-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9dd6-131">Nom de domaine complet spécifiant une boîte aux lettres pour recevoir des messages d’erreur liés à la liste de diffusion ou à la boîte aux lettres spécifiée par le nom de propriétaire de l’enregistrement MINFO.</span><span class="sxs-lookup"><span data-stu-id="c9dd6-131">FQDN specifying a mailbox to receive error messages related to either the mailing list, or to the mailbox specified by the owner name of the MINFO record.</span></span>

</dd> <dt>

<span data-ttu-id="c9dd6-132">**ResponsibleMailbox**</span><span class="sxs-lookup"><span data-stu-id="c9dd6-132">**ResponsibleMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9dd6-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c9dd6-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9dd6-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9dd6-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9dd6-135">Nom de domaine complet spécifiant une boîte aux lettres responsable de la liste de distribution ou de la boîte aux lettres spécifiée dans le nom du propriétaire de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c9dd6-135">FQDN specifying a mailbox responsible for the mailing list or mailbox specified in the record's Owner Name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9dd6-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9dd6-136">Requirements</span></span>



| <span data-ttu-id="c9dd6-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9dd6-137">Requirement</span></span> | <span data-ttu-id="c9dd6-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9dd6-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9dd6-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9dd6-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c9dd6-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9dd6-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c9dd6-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9dd6-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c9dd6-142">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9dd6-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c9dd6-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c9dd6-143">Namespace</span></span><br/>                | <span data-ttu-id="c9dd6-144">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="c9dd6-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c9dd6-145">MOF</span><span class="sxs-lookup"><span data-stu-id="c9dd6-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9dd6-146"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9dd6-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9dd6-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9dd6-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9dd6-148">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MINFOType**</span><span class="sxs-lookup"><span data-stu-id="c9dd6-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="c9dd6-149">**Modifier la méthode de la \_ classe MINFOType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c9dd6-149">**Modify Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="c9dd6-150">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="c9dd6-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





