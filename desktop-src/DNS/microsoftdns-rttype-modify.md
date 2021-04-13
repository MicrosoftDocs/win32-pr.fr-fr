---
title: Modifier la méthode de la classe MicrosoftDNS_RTType
description: La méthode modify met à jour un enregistrement de ressource route through (RT).
ms.assetid: 80053ae6-8ce8-4aa1-be2b-aac9daa5dae3
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_RTType classe
- MicrosoftDNS_RTType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8267bf1dc256ec95a456978643226ab5c01af93f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508682"
---
# <a name="modify-method-of-the-microsoftdns_rttype-class"></a><span data-ttu-id="87ec7-106">Modifier la méthode de la \_ classe RTType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="87ec7-106">Modify method of the MicrosoftDNS\_RTType class</span></span>

<span data-ttu-id="87ec7-107">La méthode **Modify** met à jour un enregistrement de ressource route through (RT).</span><span class="sxs-lookup"><span data-stu-id="87ec7-107">The **Modify** method updates a Route Through (RT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="87ec7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87ec7-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              IntermediateHost,
  [out, ref]     MicrosoftDNS_RTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="87ec7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87ec7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87ec7-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="87ec7-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="87ec7-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="87ec7-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="87ec7-112">*Préférence* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="87ec7-112">*Preference* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="87ec7-113">Préférence donnée à ce RR, parmi d’autres au même propriétaire.</span><span class="sxs-lookup"><span data-stu-id="87ec7-113">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="87ec7-114">Les valeurs les plus basses sont préférées.</span><span class="sxs-lookup"><span data-stu-id="87ec7-114">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="87ec7-115">*IntermediateHost* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="87ec7-115">*IntermediateHost* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="87ec7-116">Nom de domaine complet spécifiant un hôte qui servira de intermédiaire pour atteindre l’hôte spécifié par le propriétaire.</span><span class="sxs-lookup"><span data-stu-id="87ec7-116">FQDN specifying a host to serve as an intermediate in reaching the host specified by owner.</span></span>

</dd> <dt>

<span data-ttu-id="87ec7-117">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="87ec7-117">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="87ec7-118">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="87ec7-118">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87ec7-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="87ec7-119">Return value</span></span>

<span data-ttu-id="87ec7-120">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="87ec7-120">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="87ec7-121">Notes</span><span class="sxs-lookup"><span data-stu-id="87ec7-121">Remarks</span></span>

<span data-ttu-id="87ec7-122">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="87ec7-122">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="87ec7-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87ec7-123">Requirements</span></span>



| <span data-ttu-id="87ec7-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87ec7-124">Requirement</span></span> | <span data-ttu-id="87ec7-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="87ec7-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87ec7-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87ec7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="87ec7-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="87ec7-127">None supported</span></span><br/>                                                              |
| <span data-ttu-id="87ec7-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87ec7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="87ec7-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87ec7-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="87ec7-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="87ec7-130">Namespace</span></span><br/>                | <span data-ttu-id="87ec7-131">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="87ec7-131">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="87ec7-132">MOF</span><span class="sxs-lookup"><span data-stu-id="87ec7-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87ec7-133"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="87ec7-133"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87ec7-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87ec7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87ec7-135">**MicrosoftDNS \_ RTType**</span><span class="sxs-lookup"><span data-stu-id="87ec7-135">**MicrosoftDNS\_RTType**</span></span>](microsoftdns-rttype.md)
</dt> <dt>

[<span data-ttu-id="87ec7-136">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS RTType**</span><span class="sxs-lookup"><span data-stu-id="87ec7-136">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="87ec7-137">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="87ec7-137">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





