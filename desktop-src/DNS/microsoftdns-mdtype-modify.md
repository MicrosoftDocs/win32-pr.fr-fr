---
title: Modifier la méthode de la classe MicrosoftDNS_MDType
description: La méthode modify met à jour un enregistrement de ressource de l’agent de messagerie pour le domaine (MD).
ms.assetid: d14c8ada-d715-489f-9956-a940b94006e5
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_MDType classe
- MicrosoftDNS_MDType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_MDType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78ed5e3a8d7f819447d256ba3bce31f4eaa6986a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103609"
---
# <a name="modify-method-of-the-microsoftdns_mdtype-class"></a><span data-ttu-id="5047c-106">Modifier la méthode de la \_ classe MDType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="5047c-106">Modify method of the MicrosoftDNS\_MDType class</span></span>

<span data-ttu-id="5047c-107">La méthode **Modify** met à jour un enregistrement de ressource de l’agent de messagerie pour le domaine (MD).</span><span class="sxs-lookup"><span data-stu-id="5047c-107">The **Modify** method updates a Mail Agent for Domain (MD) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="5047c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5047c-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MDHost,
  [out, ref]     MicrosoftDNS_MDType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="5047c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5047c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5047c-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5047c-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5047c-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="5047c-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="5047c-112">*MDHost* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5047c-112">*MDHost* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5047c-113">Chaîne représentant l’hôte de remise de courrier.</span><span class="sxs-lookup"><span data-stu-id="5047c-113">String representing the mail delivery host.</span></span>

</dd> <dt>

<span data-ttu-id="5047c-114">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="5047c-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="5047c-115">Référence à l’objet modifié.</span><span class="sxs-lookup"><span data-stu-id="5047c-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5047c-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5047c-116">Return value</span></span>

<span data-ttu-id="5047c-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5047c-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5047c-118">Notes</span><span class="sxs-lookup"><span data-stu-id="5047c-118">Remarks</span></span>

<span data-ttu-id="5047c-119">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="5047c-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="5047c-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5047c-120">Requirements</span></span>



| <span data-ttu-id="5047c-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5047c-121">Requirement</span></span> | <span data-ttu-id="5047c-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="5047c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5047c-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5047c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5047c-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5047c-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5047c-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5047c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5047c-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5047c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5047c-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5047c-127">Namespace</span></span><br/>                | <span data-ttu-id="5047c-128">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="5047c-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="5047c-129">MOF</span><span class="sxs-lookup"><span data-stu-id="5047c-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5047c-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5047c-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5047c-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5047c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5047c-132">**MicrosoftDNS \_ MDType**</span><span class="sxs-lookup"><span data-stu-id="5047c-132">**MicrosoftDNS\_MDType**</span></span>](microsoftdns-mdtype.md)
</dt> <dt>

[<span data-ttu-id="5047c-133">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MDType**</span><span class="sxs-lookup"><span data-stu-id="5047c-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MDType Class**</span></span>](microsoftdns-mdtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="5047c-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="5047c-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





