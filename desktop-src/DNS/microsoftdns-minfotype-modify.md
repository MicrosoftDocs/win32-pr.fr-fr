---
title: Modifier la méthode de la classe MicrosoftDNS_MINFOType
description: La méthode modify met à jour un enregistrement de ressource d’informations de messagerie (MINFO).
ms.assetid: fbec0cd3-f735-44c6-b010-80f35cc33d98
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_MINFOType classe
- MicrosoftDNS_MINFOType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b59d7d1231ed88e61a0ecf94cef50041ca772f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464751"
---
# <a name="modify-method-of-the-microsoftdns_minfotype-class"></a><span data-ttu-id="e84b3-106">Modifier la méthode de la \_ classe MINFOType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="e84b3-106">Modify method of the MicrosoftDNS\_MINFOType class</span></span>

<span data-ttu-id="e84b3-107">La méthode **Modify** met à jour un enregistrement de ressource d’informations de messagerie (mInfo).</span><span class="sxs-lookup"><span data-stu-id="e84b3-107">The **Modify** method updates a Mail Information (MINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="e84b3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e84b3-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 ResponsibleMailbox,
  [in, optional] string                 ErrorMailbox,
  [out, ref]     MicrosoftDNS_MINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="e84b3-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e84b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e84b3-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="e84b3-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e84b3-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="e84b3-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="e84b3-112">*ResponsibleMailbox* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="e84b3-112">*ResponsibleMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e84b3-113">Nom de domaine complet spécifiant une boîte aux lettres responsable de la liste de distribution ou de la boîte aux lettres spécifiée dans le nom du propriétaire de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="e84b3-113">FQDN specifying a mailbox responsible for the mailing list or mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="e84b3-114">*ErrorMailbox* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="e84b3-114">*ErrorMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e84b3-115">Nom de domaine complet spécifiant une boîte aux lettres pour recevoir des messages d’erreur liés à la liste de diffusion ou à la boîte aux lettres spécifiée par le nom de propriétaire de l’enregistrement MINFO.</span><span class="sxs-lookup"><span data-stu-id="e84b3-115">FQDN specifying a mailbox to receive error messages related to either the mailing list, or to the mailbox specified by the owner name of the MINFO record.</span></span>

</dd> <dt>

<span data-ttu-id="e84b3-116">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="e84b3-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e84b3-117">Référence à l’objet modifié.</span><span class="sxs-lookup"><span data-stu-id="e84b3-117">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e84b3-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e84b3-118">Return value</span></span>

<span data-ttu-id="e84b3-119">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e84b3-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e84b3-120">Notes</span><span class="sxs-lookup"><span data-stu-id="e84b3-120">Remarks</span></span>

<span data-ttu-id="e84b3-121">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="e84b3-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="e84b3-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e84b3-122">Requirements</span></span>



| <span data-ttu-id="e84b3-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e84b3-123">Requirement</span></span> | <span data-ttu-id="e84b3-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="e84b3-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e84b3-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e84b3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e84b3-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e84b3-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e84b3-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e84b3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e84b3-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e84b3-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e84b3-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e84b3-129">Namespace</span></span><br/>                | <span data-ttu-id="e84b3-130">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="e84b3-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="e84b3-131">MOF</span><span class="sxs-lookup"><span data-stu-id="e84b3-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e84b3-132"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e84b3-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e84b3-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e84b3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e84b3-134">**MicrosoftDNS \_ MINFOType**</span><span class="sxs-lookup"><span data-stu-id="e84b3-134">**MicrosoftDNS\_MINFOType**</span></span>](microsoftdns-minfotype.md)
</dt> <dt>

[<span data-ttu-id="e84b3-135">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MINFOType**</span><span class="sxs-lookup"><span data-stu-id="e84b3-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="e84b3-136">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="e84b3-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





