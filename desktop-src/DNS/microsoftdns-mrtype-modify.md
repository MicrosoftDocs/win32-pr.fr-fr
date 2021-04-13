---
title: Modifier la méthode de la classe MicrosoftDNS_MRType
description: La méthode modify met à jour un enregistrement de ressource de changement de nom de boîte aux lettres (MR).
ms.assetid: eb833735-d485-4603-9976-305244537acd
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_MRType classe
- MicrosoftDNS_MRType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 996692301e8446b3fd67e20eca036cd085e83b03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465226"
---
# <a name="modify-method-of-the-microsoftdns_mrtype-class"></a><span data-ttu-id="302c6-106">Modifier la méthode de la \_ classe MRType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="302c6-106">Modify method of the MicrosoftDNS\_MRType class</span></span>

<span data-ttu-id="302c6-107">La méthode **Modify** met à jour un enregistrement de ressource de changement de nom de boîte aux lettres (Mr).</span><span class="sxs-lookup"><span data-stu-id="302c6-107">The **Modify** method updates a Mailbox Rename (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="302c6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="302c6-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in]           string              MRMailbox,
  [out, ref]     MicrosoftDNS_MRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="302c6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="302c6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="302c6-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="302c6-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="302c6-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="302c6-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="302c6-112">*MRMailbox* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="302c6-112">*MRMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="302c6-113">Nom de domaine complet spécifiant une boîte aux lettres qui est le nom correct de la boîte aux lettres spécifiée dans le nom du propriétaire de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="302c6-113">FQDN specifying a mailbox that is the proper rename of the mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="302c6-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="302c6-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="302c6-115">Référence à l’objet modifié.</span><span class="sxs-lookup"><span data-stu-id="302c6-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="302c6-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="302c6-116">Return value</span></span>

<span data-ttu-id="302c6-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="302c6-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="302c6-118">Notes</span><span class="sxs-lookup"><span data-stu-id="302c6-118">Remarks</span></span>

<span data-ttu-id="302c6-119">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="302c6-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="302c6-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="302c6-120">Requirements</span></span>



| <span data-ttu-id="302c6-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="302c6-121">Requirement</span></span> | <span data-ttu-id="302c6-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="302c6-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="302c6-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="302c6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="302c6-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="302c6-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="302c6-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="302c6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="302c6-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="302c6-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="302c6-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="302c6-127">Namespace</span></span><br/>                | <span data-ttu-id="302c6-128">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="302c6-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="302c6-129">MOF</span><span class="sxs-lookup"><span data-stu-id="302c6-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="302c6-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="302c6-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="302c6-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="302c6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="302c6-132">**MicrosoftDNS \_ MRType**</span><span class="sxs-lookup"><span data-stu-id="302c6-132">**MicrosoftDNS\_MRType**</span></span>](microsoftdns-mrtype.md)
</dt> <dt>

[<span data-ttu-id="302c6-133">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MRType**</span><span class="sxs-lookup"><span data-stu-id="302c6-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="302c6-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="302c6-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





