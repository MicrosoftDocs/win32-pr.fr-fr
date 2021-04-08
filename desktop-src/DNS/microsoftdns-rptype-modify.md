---
title: Modifier la méthode de la classe MicrosoftDNS_RPType
description: La méthode modify met à jour un enregistrement de ressource de personne responsable (RP).
ms.assetid: a779b905-922c-42ff-b3d9-318b3a848230
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_RPType classe
- MicrosoftDNS_RPType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ec575424e6e26c79f8d6a27e62732cad6ddc57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843766"
---
# <a name="modify-method-of-the-microsoftdns_rptype-class"></a><span data-ttu-id="55b87-106">Modifier la méthode de la \_ classe RPType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="55b87-106">Modify method of the MicrosoftDNS\_RPType class</span></span>

<span data-ttu-id="55b87-107">La méthode **Modify** met à jour un enregistrement de ressource de personne responsable (RP).</span><span class="sxs-lookup"><span data-stu-id="55b87-107">The **Modify** method updates a Responsible Person (RP) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="55b87-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55b87-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              RPMailbox,
  [in, optional] string              TXTDomainName,
  [out, ref]     MicrosoftDNS_RPType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="55b87-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55b87-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55b87-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="55b87-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="55b87-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="55b87-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="55b87-112">*RPMailbox* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="55b87-112">*RPMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="55b87-113">Nom de domaine complet spécifiant la boîte aux lettres pour la personne responsable.</span><span class="sxs-lookup"><span data-stu-id="55b87-113">FQDN specifying the mailbox for the responsible person.</span></span>

</dd> <dt>

<span data-ttu-id="55b87-114">*TXTDomainName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="55b87-114">*TXTDomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="55b87-115">Nom de domaine complet pour lequel existent les enregistrements de ressource TXT.</span><span class="sxs-lookup"><span data-stu-id="55b87-115">FQDN for which TXT Resource Records exist.</span></span>

</dd> <dt>

<span data-ttu-id="55b87-116">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="55b87-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="55b87-117">Référence à l’objet modifié.</span><span class="sxs-lookup"><span data-stu-id="55b87-117">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55b87-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="55b87-118">Return value</span></span>

<span data-ttu-id="55b87-119">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="55b87-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="55b87-120">Notes</span><span class="sxs-lookup"><span data-stu-id="55b87-120">Remarks</span></span>

<span data-ttu-id="55b87-121">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="55b87-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="55b87-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55b87-122">Requirements</span></span>



| <span data-ttu-id="55b87-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55b87-123">Requirement</span></span> | <span data-ttu-id="55b87-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="55b87-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="55b87-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55b87-125">Minimum supported client</span></span><br/> | <span data-ttu-id="55b87-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="55b87-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="55b87-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55b87-127">Minimum supported server</span></span><br/> | <span data-ttu-id="55b87-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55b87-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="55b87-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="55b87-129">Namespace</span></span><br/>                | <span data-ttu-id="55b87-130">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="55b87-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="55b87-131">MOF</span><span class="sxs-lookup"><span data-stu-id="55b87-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55b87-132"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55b87-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55b87-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55b87-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55b87-134">**MicrosoftDNS \_ RPType**</span><span class="sxs-lookup"><span data-stu-id="55b87-134">**MicrosoftDNS\_RPType**</span></span>](microsoftdns-rptype.md)
</dt> <dt>

[<span data-ttu-id="55b87-135">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS RPType**</span><span class="sxs-lookup"><span data-stu-id="55b87-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="55b87-136">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="55b87-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





