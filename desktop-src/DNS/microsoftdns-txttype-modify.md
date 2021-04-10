---
title: Modifier la méthode de la classe MicrosoftDNS_TXTType
description: La méthode modify met à jour un enregistrement de ressource texte (TXT).
ms.assetid: af61057e-95be-4290-83da-a63f01ead476
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_TXTType classe
- MicrosoftDNS_TXTType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 285dfb6d5323ca3775f981aecbf5a0170392cd3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103053"
---
# <a name="modify-method-of-the-microsoftdns_txttype-class"></a><span data-ttu-id="211e2-106">Modifier la méthode de la \_ classe TXTType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="211e2-106">Modify method of the MicrosoftDNS\_TXTType class</span></span>

<span data-ttu-id="211e2-107">La méthode **Modify** met à jour un enregistrement de ressource texte (txt).</span><span class="sxs-lookup"><span data-stu-id="211e2-107">The **Modify** method updates a Text (TXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="211e2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="211e2-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               DescriptiveText,
  [out, ref]     MicrosoftDNS_TXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="211e2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="211e2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="211e2-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="211e2-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="211e2-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="211e2-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="211e2-112">*DescriptiveText* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="211e2-112">*DescriptiveText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="211e2-113">Texte descriptif, dont la sémantique dépend du domaine propriétaire.</span><span class="sxs-lookup"><span data-stu-id="211e2-113">Descriptive text, the semantics of which depend on the owner domain.</span></span>

</dd> <dt>

<span data-ttu-id="211e2-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="211e2-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="211e2-115">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="211e2-115">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="211e2-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="211e2-116">Return value</span></span>

<span data-ttu-id="211e2-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="211e2-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="211e2-118">Notes</span><span class="sxs-lookup"><span data-stu-id="211e2-118">Remarks</span></span>

<span data-ttu-id="211e2-119">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="211e2-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="211e2-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="211e2-120">Requirements</span></span>



| <span data-ttu-id="211e2-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="211e2-121">Requirement</span></span> | <span data-ttu-id="211e2-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="211e2-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="211e2-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="211e2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="211e2-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="211e2-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="211e2-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="211e2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="211e2-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="211e2-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="211e2-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="211e2-127">Namespace</span></span><br/>                | <span data-ttu-id="211e2-128">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="211e2-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="211e2-129">MOF</span><span class="sxs-lookup"><span data-stu-id="211e2-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="211e2-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="211e2-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="211e2-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="211e2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="211e2-132">**MicrosoftDNS \_ TXTType**</span><span class="sxs-lookup"><span data-stu-id="211e2-132">**MicrosoftDNS\_TXTType**</span></span>](microsoftdns-txttype.md)
</dt> <dt>

[<span data-ttu-id="211e2-133">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS TXTType**</span><span class="sxs-lookup"><span data-stu-id="211e2-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="211e2-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="211e2-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





