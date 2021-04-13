---
title: Modifier la méthode de la classe MicrosoftDNS_MFType
description: La méthode modify met à jour un enregistrement de ressource de l’agent de transfert de messagerie pour le domaine (MF).
ms.assetid: b4bc43a5-6f43-487d-ad6c-3e01d5b2b6b8
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_MFType classe
- MicrosoftDNS_MFType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec0a363290580c7cecf47dbe00c6dd7895d23dbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466058"
---
# <a name="modify-method-of-the-microsoftdns_mftype-class"></a><span data-ttu-id="95af1-106">Modifier la méthode de la \_ classe MFType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="95af1-106">Modify method of the MicrosoftDNS\_MFType class</span></span>

<span data-ttu-id="95af1-107">La méthode **Modify** met à jour un enregistrement de ressource de l’agent de transfert de messagerie pour le domaine (MF).</span><span class="sxs-lookup"><span data-stu-id="95af1-107">The **Modify** method updates a Mail Forwarding Agent for Domain (MF) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="95af1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95af1-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MFHost,
  [out, ref]     MicrosoftDNS_MFType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="95af1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95af1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95af1-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="95af1-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="95af1-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="95af1-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="95af1-112">*MFHost* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="95af1-112">*MFHost* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="95af1-113">Nom de l’hôte qui fournit l’agent de transfert du courrier.</span><span class="sxs-lookup"><span data-stu-id="95af1-113">Name of the host that provides the mail forwarding agent.</span></span>

</dd> <dt>

<span data-ttu-id="95af1-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="95af1-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="95af1-115">Référence à l’objet modifié.</span><span class="sxs-lookup"><span data-stu-id="95af1-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95af1-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="95af1-116">Return value</span></span>

<span data-ttu-id="95af1-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="95af1-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="95af1-118">Notes</span><span class="sxs-lookup"><span data-stu-id="95af1-118">Remarks</span></span>

<span data-ttu-id="95af1-119">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="95af1-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="95af1-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95af1-120">Requirements</span></span>



| <span data-ttu-id="95af1-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95af1-121">Requirement</span></span> | <span data-ttu-id="95af1-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="95af1-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="95af1-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95af1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="95af1-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="95af1-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="95af1-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95af1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="95af1-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95af1-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="95af1-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="95af1-127">Namespace</span></span><br/>                | <span data-ttu-id="95af1-128">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="95af1-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="95af1-129">MOF</span><span class="sxs-lookup"><span data-stu-id="95af1-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95af1-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="95af1-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95af1-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95af1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95af1-132">**MicrosoftDNS \_ MFType**</span><span class="sxs-lookup"><span data-stu-id="95af1-132">**MicrosoftDNS\_MFType**</span></span>](microsoftdns-mftype.md)
</dt> <dt>

[<span data-ttu-id="95af1-133">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MFType**</span><span class="sxs-lookup"><span data-stu-id="95af1-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="95af1-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="95af1-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





