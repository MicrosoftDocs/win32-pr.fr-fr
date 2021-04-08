---
title: Modifier la méthode de la classe MicrosoftDNS_AAAAType
description: La méthode modify met à jour un enregistrement de ressource d’adresse IPv6 (AAAA).
ms.assetid: d58f8a88-8473-4b26-89f0-237d2457f00b
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_AAAAType classe
- MicrosoftDNS_AAAAType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc216233fe3d41e4f1e31fe0d471e766c4dc8476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843597"
---
# <a name="modify-method-of-the-microsoftdns_aaaatype-class"></a><span data-ttu-id="ec879-106">Modifier la méthode de la \_ classe AAAAType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="ec879-106">Modify method of the MicrosoftDNS\_AAAAType class</span></span>

<span data-ttu-id="ec879-107">La méthode **Modify** met à jour un enregistrement de ressource d’adresse IPv6 (aaaa).</span><span class="sxs-lookup"><span data-stu-id="ec879-107">The **Modify** method updates an IPv6 address (AAAA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec879-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec879-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] string                IPv6Address,
  [out, ref]     MicrosoftDNS_AAAAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="ec879-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec879-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec879-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="ec879-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ec879-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="ec879-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="ec879-112">*AdresseIPv6* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="ec879-112">*IPv6Address* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ec879-113">Adresse IPv6 de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="ec879-113">IPv6 address for the host.</span></span>

</dd> <dt>

<span data-ttu-id="ec879-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="ec879-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ec879-115">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="ec879-115">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec879-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ec879-116">Return value</span></span>

<span data-ttu-id="ec879-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ec879-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec879-118">Notes</span><span class="sxs-lookup"><span data-stu-id="ec879-118">Remarks</span></span>

<span data-ttu-id="ec879-119">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="ec879-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec879-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec879-120">Requirements</span></span>



| <span data-ttu-id="ec879-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec879-121">Requirement</span></span> | <span data-ttu-id="ec879-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec879-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec879-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec879-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ec879-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec879-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ec879-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec879-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ec879-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec879-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ec879-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ec879-127">Namespace</span></span><br/>                | <span data-ttu-id="ec879-128">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="ec879-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ec879-129">MOF</span><span class="sxs-lookup"><span data-stu-id="ec879-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec879-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ec879-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec879-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec879-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec879-132">**MicrosoftDNS \_ AAAAType**</span><span class="sxs-lookup"><span data-stu-id="ec879-132">**MicrosoftDNS\_AAAAType**</span></span>](microsoftdns-aaaatype.md)
</dt> <dt>

[<span data-ttu-id="ec879-133">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS AAAAType**</span><span class="sxs-lookup"><span data-stu-id="ec879-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="ec879-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="ec879-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





