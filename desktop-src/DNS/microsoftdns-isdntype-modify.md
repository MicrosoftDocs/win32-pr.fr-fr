---
title: Modifier la méthode de la classe MicrosoftDNS_ISDNType
description: La méthode modify met à jour un enregistrement de ressource RNIS.
ms.assetid: 09e23853-ca92-43a3-8bd9-7de10eb5eddc
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_ISDNType classe
- MicrosoftDNS_ISDNType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c369a6650c834ff9f35af6389c346daec86a954
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941695"
---
# <a name="modify-method-of-the-microsoftdns_isdntype-class"></a><span data-ttu-id="fe95d-106">Modifier la méthode de la \_ classe ISDNType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="fe95d-106">Modify method of the MicrosoftDNS\_ISDNType class</span></span>

<span data-ttu-id="fe95d-107">La méthode **Modify** met à jour un enregistrement de ressource RNIS.</span><span class="sxs-lookup"><span data-stu-id="fe95d-107">The **Modify** method updates an ISDN Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe95d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe95d-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] string                ISDNNumber,
  [in, optional] string                SubAddress,
  [out, ref]     MicrosoftDNS_ISDNType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="fe95d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe95d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe95d-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="fe95d-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fe95d-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="fe95d-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="fe95d-112">*ISDNNumber* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="fe95d-112">*ISDNNumber* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fe95d-113">Numéro RNIS et DDI du propriétaire de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="fe95d-113">ISDN number and DDI of the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="fe95d-114">Sous- *adresse* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="fe95d-114">*SubAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fe95d-115">Sous-adresse du propriétaire, si elle est définie.</span><span class="sxs-lookup"><span data-stu-id="fe95d-115">Subaddress of the owner, if defined.</span></span>

</dd> <dt>

<span data-ttu-id="fe95d-116">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="fe95d-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="fe95d-117">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="fe95d-117">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe95d-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fe95d-118">Return value</span></span>

<span data-ttu-id="fe95d-119">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="fe95d-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe95d-120">Notes</span><span class="sxs-lookup"><span data-stu-id="fe95d-120">Remarks</span></span>

<span data-ttu-id="fe95d-121">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="fe95d-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe95d-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe95d-122">Requirements</span></span>



| <span data-ttu-id="fe95d-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe95d-123">Requirement</span></span> | <span data-ttu-id="fe95d-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe95d-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe95d-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe95d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fe95d-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe95d-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="fe95d-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe95d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fe95d-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe95d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fe95d-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fe95d-129">Namespace</span></span><br/>                | <span data-ttu-id="fe95d-130">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="fe95d-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="fe95d-131">MOF</span><span class="sxs-lookup"><span data-stu-id="fe95d-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe95d-132"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe95d-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe95d-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe95d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe95d-134">**MicrosoftDNS \_ ISDNType**</span><span class="sxs-lookup"><span data-stu-id="fe95d-134">**MicrosoftDNS\_ISDNType**</span></span>](microsoftdns-isdntype.md)
</dt> <dt>

[<span data-ttu-id="fe95d-135">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS ISDNType**</span><span class="sxs-lookup"><span data-stu-id="fe95d-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="fe95d-136">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="fe95d-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





