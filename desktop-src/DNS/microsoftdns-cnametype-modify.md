---
title: Modifier la méthode de la classe MicrosoftDNS_CNAMEType
description: La méthode modify met à jour un enregistrement de ressource de nom canonique (CNAMe).
ms.assetid: 7e550026-d901-44a0-86ac-520682232ccb
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_CNAMEType classe
- MicrosoftDNS_CNAMEType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_CNAMEType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ddbe1e1592c4331be808340c216954cd8d7b14f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465338"
---
# <a name="modify-method-of-the-microsoftdns_cnametype-class"></a><span data-ttu-id="e7b89-106">Modifier la méthode de la \_ classe CNAMEType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="e7b89-106">Modify method of the MicrosoftDNS\_CNAMEType class</span></span>

<span data-ttu-id="e7b89-107">La méthode **Modify** met à jour un enregistrement de ressource de nom canonique (CNAME).</span><span class="sxs-lookup"><span data-stu-id="e7b89-107">The **Modify** method updates a Canonical Name (CNAME) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7b89-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7b89-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 PrimaryName,
  [out, ref]     MicrosoftDNS_CNAMEType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="e7b89-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7b89-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7b89-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="e7b89-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e7b89-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="e7b89-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="e7b89-112">*PrimaryName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="e7b89-112">*PrimaryName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e7b89-113">Chaîne représentant le nom principal de l’enregistrement CNAMe.</span><span class="sxs-lookup"><span data-stu-id="e7b89-113">String representing the primary name for the CNAME record.</span></span>

</dd> <dt>

<span data-ttu-id="e7b89-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="e7b89-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e7b89-115">Référence à l’objet modifié.</span><span class="sxs-lookup"><span data-stu-id="e7b89-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7b89-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7b89-116">Return value</span></span>

<span data-ttu-id="e7b89-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e7b89-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7b89-118">Notes</span><span class="sxs-lookup"><span data-stu-id="e7b89-118">Remarks</span></span>

<span data-ttu-id="e7b89-119">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="e7b89-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7b89-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7b89-120">Requirements</span></span>



| <span data-ttu-id="e7b89-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7b89-121">Requirement</span></span> | <span data-ttu-id="e7b89-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7b89-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b89-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7b89-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e7b89-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7b89-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e7b89-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7b89-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e7b89-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7b89-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e7b89-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e7b89-127">Namespace</span></span><br/>                | <span data-ttu-id="e7b89-128">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="e7b89-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="e7b89-129">MOF</span><span class="sxs-lookup"><span data-stu-id="e7b89-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7b89-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7b89-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7b89-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7b89-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7b89-132">**MicrosoftDNS \_ CNAMEType**</span><span class="sxs-lookup"><span data-stu-id="e7b89-132">**MicrosoftDNS\_CNAMEType**</span></span>](microsoftdns-cnametype.md)
</dt> <dt>

[<span data-ttu-id="e7b89-133">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS CNAMEType**</span><span class="sxs-lookup"><span data-stu-id="e7b89-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_CNAMEType Class**</span></span>](microsoftdns-cnametype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="e7b89-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="e7b89-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





