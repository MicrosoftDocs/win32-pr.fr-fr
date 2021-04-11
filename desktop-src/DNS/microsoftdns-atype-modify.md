---
title: Modifier la méthode de la classe MicrosoftDNS_AType
description: La méthode modify met à jour la durée de vie et l’adresse IP d’un enregistrement de ressource d’adresse d’hôte (A).
ms.assetid: fe01549d-7135-499d-a5a5-cd31ea106f53
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_AType classe
- MicrosoftDNS_AType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ffda093ed843cfd655711100321c9876120519c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032871"
---
# <a name="modify-method-of-the-microsoftdns_atype-class"></a><span data-ttu-id="4e56a-106">Modifier la méthode de la \_ classe aType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="4e56a-106">Modify method of the MicrosoftDNS\_AType class</span></span>

<span data-ttu-id="4e56a-107">La méthode **Modify** met à jour la durée de vie et l’adresse IP d’un enregistrement de ressource d’adresse d’hôte (a).</span><span class="sxs-lookup"><span data-stu-id="4e56a-107">The **Modify** method updates the TTL and IP address of a host Address (A) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e56a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e56a-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32             TTL,
  [in, optional] string             IPAddress,
  [out, ref]     MicrosoftDNS_AType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="4e56a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e56a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e56a-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="4e56a-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4e56a-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="4e56a-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="4e56a-112">*Adresse IP* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="4e56a-112">*IPAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4e56a-113">Chaîne représentant l’adresse IP de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="4e56a-113">String representing the IP address of the host.</span></span>

</dd> <dt>

<span data-ttu-id="4e56a-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="4e56a-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="4e56a-115">Référence à l’objet modifié.</span><span class="sxs-lookup"><span data-stu-id="4e56a-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e56a-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4e56a-116">Return value</span></span>

<span data-ttu-id="4e56a-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4e56a-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e56a-118">Notes</span><span class="sxs-lookup"><span data-stu-id="4e56a-118">Remarks</span></span>

<span data-ttu-id="4e56a-119">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="4e56a-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e56a-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e56a-120">Requirements</span></span>



| <span data-ttu-id="4e56a-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e56a-121">Requirement</span></span> | <span data-ttu-id="4e56a-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e56a-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e56a-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e56a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4e56a-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e56a-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4e56a-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e56a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4e56a-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e56a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4e56a-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4e56a-127">Namespace</span></span><br/>                | <span data-ttu-id="4e56a-128">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="4e56a-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="4e56a-129">MOF</span><span class="sxs-lookup"><span data-stu-id="4e56a-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e56a-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e56a-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e56a-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e56a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e56a-132">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="4e56a-132">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="4e56a-133">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS aType**</span><span class="sxs-lookup"><span data-stu-id="4e56a-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> </dl>

 

 





