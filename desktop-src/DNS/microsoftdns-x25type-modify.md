---
title: Modifier la méthode de la classe MicrosoftDNS_X25Type
description: La méthode modify met à jour un enregistrement de ressource X. 25 (X25).
ms.assetid: 2d82d67e-ae29-4ded-86fe-7db0ef5ed74f
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_X25Type classe
- MicrosoftDNS_X25Type de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_X25Type.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10db2fa770d3da8487a712e631c41fdd4256bf7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104410"
---
# <a name="modify-method-of-the-microsoftdns_x25type-class"></a><span data-ttu-id="b237f-106">Modifier la méthode de la \_ classe X25Type MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="b237f-106">Modify method of the MicrosoftDNS\_X25Type class</span></span>

<span data-ttu-id="b237f-107">La méthode **Modify** met à jour un enregistrement de ressource X. 25 (X25).</span><span class="sxs-lookup"><span data-stu-id="b237f-107">The **Modify** method updates an X.25 (X25) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="b237f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b237f-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] string               PSDNAddress,
  [out, ref]     MicrosoftDNS_X25Type &RR
);
```



## <a name="parameters"></a><span data-ttu-id="b237f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b237f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b237f-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b237f-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b237f-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="b237f-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="b237f-112">*PSDNAddress* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b237f-112">*PSDNAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b237f-113">Adresse PSDN du propriétaire de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="b237f-113">PSDN address of the owner of the RR.</span></span>

</dd> <dt>

<span data-ttu-id="b237f-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="b237f-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="b237f-115">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="b237f-115">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b237f-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b237f-116">Return value</span></span>

<span data-ttu-id="b237f-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b237f-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b237f-118">Notes</span><span class="sxs-lookup"><span data-stu-id="b237f-118">Remarks</span></span>

<span data-ttu-id="b237f-119">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="b237f-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="b237f-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b237f-120">Requirements</span></span>



| <span data-ttu-id="b237f-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b237f-121">Requirement</span></span> | <span data-ttu-id="b237f-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="b237f-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b237f-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b237f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b237f-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b237f-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b237f-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b237f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b237f-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b237f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b237f-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b237f-127">Namespace</span></span><br/>                | <span data-ttu-id="b237f-128">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="b237f-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="b237f-129">MOF</span><span class="sxs-lookup"><span data-stu-id="b237f-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b237f-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b237f-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b237f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b237f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b237f-132">**MicrosoftDNS \_ X25Type**</span><span class="sxs-lookup"><span data-stu-id="b237f-132">**MicrosoftDNS\_X25Type**</span></span>](microsoftdns-x25type.md)
</dt> <dt>

[<span data-ttu-id="b237f-133">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS X25Type**</span><span class="sxs-lookup"><span data-stu-id="b237f-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_X25Type Class**</span></span>](microsoftdns-x25type-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="b237f-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="b237f-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





