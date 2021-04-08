---
title: Modifier la méthode de la classe MicrosoftDNS_HINFOType
description: La méthode modify met à jour un enregistrement de ressource d’informations sur l’hôte (HINFO).
ms.assetid: 8f8148f3-804f-4f99-8e79-606cd3cea660
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_HINFOType classe
- MicrosoftDNS_HINFOType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29a01eb94d82d080142d3496bab5f7f0b9acac8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741548"
---
# <a name="modify-method-of-the-microsoftdns_hinfotype-class"></a><span data-ttu-id="5afde-106">Modifier la méthode de la \_ classe HINFOType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="5afde-106">Modify method of the MicrosoftDNS\_HINFOType class</span></span>

<span data-ttu-id="5afde-107">La méthode **Modify** met à jour un enregistrement de ressource d’informations sur l’hôte (HINFO).</span><span class="sxs-lookup"><span data-stu-id="5afde-107">The **Modify** method updates a Host Information (HINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="5afde-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5afde-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 CPU,
  [in, optional] string                 OS,
  [out, ref]     MicrosoftDNS_HINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="5afde-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5afde-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5afde-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5afde-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5afde-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="5afde-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="5afde-112">*Processeur* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5afde-112">*CPU* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5afde-113">Type d’UC du propriétaire de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="5afde-113">CPU type of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="5afde-114">*Système d’exploitation* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5afde-114">*OS* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5afde-115">Système d’exploitation du propriétaire de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="5afde-115">Operating system of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="5afde-116">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="5afde-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="5afde-117">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="5afde-117">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5afde-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5afde-118">Return value</span></span>

<span data-ttu-id="5afde-119">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5afde-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5afde-120">Notes</span><span class="sxs-lookup"><span data-stu-id="5afde-120">Remarks</span></span>

<span data-ttu-id="5afde-121">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="5afde-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="5afde-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5afde-122">Requirements</span></span>



| <span data-ttu-id="5afde-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5afde-123">Requirement</span></span> | <span data-ttu-id="5afde-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="5afde-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5afde-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5afde-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5afde-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5afde-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5afde-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5afde-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5afde-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5afde-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5afde-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5afde-129">Namespace</span></span><br/>                | <span data-ttu-id="5afde-130">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="5afde-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="5afde-131">MOF</span><span class="sxs-lookup"><span data-stu-id="5afde-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5afde-132"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5afde-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5afde-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5afde-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5afde-134">**MicrosoftDNS \_ HINFOType**</span><span class="sxs-lookup"><span data-stu-id="5afde-134">**MicrosoftDNS\_HINFOType**</span></span>](microsoftdns-hinfotype.md)
</dt> <dt>

[<span data-ttu-id="5afde-135">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS HINFOType**</span><span class="sxs-lookup"><span data-stu-id="5afde-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_HINFOType Class**</span></span>](microsoftdns-hinfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="5afde-136">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="5afde-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





