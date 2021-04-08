---
title: Modifier la méthode de la classe MicrosoftDNS_MBType
description: La méthode modify met à jour un enregistrement de ressource de boîte aux lettres (MB).
ms.assetid: ee76031c-ac1b-4ebb-9fb2-3b64553867cc
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_MBType classe
- MicrosoftDNS_MBType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 135d6f0fcb0faf5c1e8da152798863c8cecc8641
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741989"
---
# <a name="modify-method-of-the-microsoftdns_mbtype-class"></a><span data-ttu-id="ef2de-106">Modifier la méthode de la \_ classe MBType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="ef2de-106">Modify method of the MicrosoftDNS\_MBType class</span></span>

<span data-ttu-id="ef2de-107">La méthode **Modify** met à jour un enregistrement de ressource de boîte aux lettres (MB).</span><span class="sxs-lookup"><span data-stu-id="ef2de-107">The **Modify** method updates a Mailbox (MB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef2de-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef2de-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in]           string              MBHost,
  [out, ref]     MicrosoftDNS_MBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="ef2de-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef2de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef2de-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="ef2de-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ef2de-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="ef2de-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="ef2de-112">*MBHost* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef2de-112">*MBHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef2de-113">Chaîne représentant le nom d’hôte de la boîte aux lettres pour l’enregistrement MB.</span><span class="sxs-lookup"><span data-stu-id="ef2de-113">String representing the mailbox host name for the MB record.</span></span>

</dd> <dt>

<span data-ttu-id="ef2de-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="ef2de-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ef2de-115">Référence à l’objet modifié.</span><span class="sxs-lookup"><span data-stu-id="ef2de-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef2de-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef2de-116">Return value</span></span>

<span data-ttu-id="ef2de-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ef2de-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef2de-118">Notes</span><span class="sxs-lookup"><span data-stu-id="ef2de-118">Remarks</span></span>

<span data-ttu-id="ef2de-119">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="ef2de-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef2de-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef2de-120">Requirements</span></span>



| <span data-ttu-id="ef2de-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef2de-121">Requirement</span></span> | <span data-ttu-id="ef2de-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef2de-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef2de-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef2de-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ef2de-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef2de-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ef2de-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef2de-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ef2de-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef2de-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ef2de-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ef2de-127">Namespace</span></span><br/>                | <span data-ttu-id="ef2de-128">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="ef2de-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ef2de-129">MOF</span><span class="sxs-lookup"><span data-stu-id="ef2de-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef2de-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef2de-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef2de-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef2de-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef2de-132">**MicrosoftDNS \_ MBType**</span><span class="sxs-lookup"><span data-stu-id="ef2de-132">**MicrosoftDNS\_MBType**</span></span>](microsoftdns-mbtype.md)
</dt> <dt>

[<span data-ttu-id="ef2de-133">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MBType**</span><span class="sxs-lookup"><span data-stu-id="ef2de-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="ef2de-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="ef2de-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





