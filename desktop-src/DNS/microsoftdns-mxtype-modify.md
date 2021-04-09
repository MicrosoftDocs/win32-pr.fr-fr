---
title: Modifier la méthode de la classe MicrosoftDNS_MXType
description: La méthode modify met à jour un enregistrement de ressource de serveur de messagerie (MR).
ms.assetid: 40267ac9-0392-4e08-a5d2-145ee9639c39
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_MXType classe
- MicrosoftDNS_MXType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a665d0673e048eff684b4c985b54a1c57e030a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942803"
---
# <a name="modify-method-of-the-microsoftdns_mxtype-class"></a><span data-ttu-id="be40d-106">Modifier la méthode de la \_ classe MXType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="be40d-106">Modify method of the MicrosoftDNS\_MXType class</span></span>

<span data-ttu-id="be40d-107">La méthode **Modify** met à jour un enregistrement de ressource de serveur de messagerie (Mr).</span><span class="sxs-lookup"><span data-stu-id="be40d-107">The **Modify** method updates a Mail Exchanger (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="be40d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be40d-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              MailExchange,
  [out, ref]     MicrosoftDNS_MXType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="be40d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be40d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be40d-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="be40d-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="be40d-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="be40d-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="be40d-112">*Préférence* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="be40d-112">*Preference* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="be40d-113">Préférence donnée à ce RR, parmi d’autres au même propriétaire.</span><span class="sxs-lookup"><span data-stu-id="be40d-113">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="be40d-114">Les valeurs les plus basses sont préférées.</span><span class="sxs-lookup"><span data-stu-id="be40d-114">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="be40d-115">*MailExchange* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="be40d-115">*MailExchange* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="be40d-116">Nom de domaine complet spécifiant un ordinateur hôte prêt à agir comme échange de messagerie pour le nom du propriétaire.</span><span class="sxs-lookup"><span data-stu-id="be40d-116">FQDN specifying a host willing to act as a mail exchange for the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="be40d-117">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="be40d-117">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="be40d-118">Référence à l’objet modifié.</span><span class="sxs-lookup"><span data-stu-id="be40d-118">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be40d-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be40d-119">Return value</span></span>

<span data-ttu-id="be40d-120">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="be40d-120">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="be40d-121">Notes</span><span class="sxs-lookup"><span data-stu-id="be40d-121">Remarks</span></span>

<span data-ttu-id="be40d-122">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="be40d-122">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="be40d-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be40d-123">Requirements</span></span>



| <span data-ttu-id="be40d-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be40d-124">Requirement</span></span> | <span data-ttu-id="be40d-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="be40d-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be40d-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be40d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="be40d-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="be40d-127">None supported</span></span><br/>                                                              |
| <span data-ttu-id="be40d-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be40d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="be40d-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be40d-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="be40d-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="be40d-130">Namespace</span></span><br/>                | <span data-ttu-id="be40d-131">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="be40d-131">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="be40d-132">MOF</span><span class="sxs-lookup"><span data-stu-id="be40d-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be40d-133"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be40d-133"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be40d-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be40d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be40d-135">**MicrosoftDNS \_ MXType**</span><span class="sxs-lookup"><span data-stu-id="be40d-135">**MicrosoftDNS\_MXType**</span></span>](microsoftdns-mxtype.md)
</dt> <dt>

[<span data-ttu-id="be40d-136">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MXType**</span><span class="sxs-lookup"><span data-stu-id="be40d-136">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="be40d-137">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="be40d-137">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





