---
title: Modifier la méthode de la classe MicrosoftDNS_NXTType
description: La méthode modify met à jour un enregistrement de ressource (NXT) suivant.
ms.assetid: 5a21b843-0761-4022-b00a-9dbcd6814454
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_NXTType classe
- MicrosoftDNS_NXTType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bab7bf8480c7e18914cac4f7ae0deb8a608090f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464750"
---
# <a name="modify-method-of-the-microsoftdns_nxttype-class"></a><span data-ttu-id="f3ef0-106">Modifier la méthode de la \_ classe NXTType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="f3ef0-106">Modify method of the MicrosoftDNS\_NXTType class</span></span>

<span data-ttu-id="f3ef0-107">La méthode **Modify** met à jour un enregistrement de ressource (NXT) suivant.</span><span class="sxs-lookup"><span data-stu-id="f3ef0-107">The **Modify** method updates a Next (NXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3ef0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3ef0-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               NextDomainName,
  [in]           string               Types,
  [out, ref]     MicrosoftDNS_NXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="f3ef0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3ef0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3ef0-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f3ef0-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f3ef0-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="f3ef0-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="f3ef0-112">*NextDomainName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f3ef0-112">*NextDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3ef0-113">Nom de domaine suivant.</span><span class="sxs-lookup"><span data-stu-id="f3ef0-113">Next domain name.</span></span>

</dd> <dt>

<span data-ttu-id="f3ef0-114">*Types* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f3ef0-114">*Types* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3ef0-115">Liste séparée par des espaces des mnémoniques de type RR pour le nom de propriétaire de l’enregistrement de ressource NXT.</span><span class="sxs-lookup"><span data-stu-id="f3ef0-115">Space-separated list of the RR-type mnemonics for the owner name of the NXT Resource Record.</span></span>

</dd> <dt>

<span data-ttu-id="f3ef0-116">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="f3ef0-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f3ef0-117">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="f3ef0-117">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3ef0-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f3ef0-118">Return value</span></span>

<span data-ttu-id="f3ef0-119">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f3ef0-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3ef0-120">Notes</span><span class="sxs-lookup"><span data-stu-id="f3ef0-120">Remarks</span></span>

<span data-ttu-id="f3ef0-121">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="f3ef0-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3ef0-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3ef0-122">Requirements</span></span>



| <span data-ttu-id="f3ef0-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3ef0-123">Requirement</span></span> | <span data-ttu-id="f3ef0-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3ef0-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3ef0-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3ef0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f3ef0-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3ef0-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f3ef0-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3ef0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f3ef0-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3ef0-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f3ef0-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f3ef0-129">Namespace</span></span><br/>                | <span data-ttu-id="f3ef0-130">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="f3ef0-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f3ef0-131">MOF</span><span class="sxs-lookup"><span data-stu-id="f3ef0-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3ef0-132"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3ef0-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3ef0-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3ef0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3ef0-134">**MicrosoftDNS \_ NXTType**</span><span class="sxs-lookup"><span data-stu-id="f3ef0-134">**MicrosoftDNS\_NXTType**</span></span>](microsoftdns-nxttype.md)
</dt> <dt>

[<span data-ttu-id="f3ef0-135">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS NXTType**</span><span class="sxs-lookup"><span data-stu-id="f3ef0-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="f3ef0-136">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="f3ef0-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





