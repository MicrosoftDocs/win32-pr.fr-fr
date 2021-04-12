---
title: Modifier la méthode de la classe MicrosoftDNS_ATMAType
description: La méthode modify met à jour un enregistrement de ressource d’adresse ATM en nom (ATMA).
ms.assetid: 202fc38d-fb8f-4044-bb7d-9e041cbde8ec
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_ATMAType classe
- MicrosoftDNS_ATMAType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d784e9421641dc53d64bb39a2e97b0d9ef257b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032872"
---
# <a name="modify-method-of-the-microsoftdns_atmatype-class"></a><span data-ttu-id="85d21-106">Modifier la méthode de la \_ classe ATMAType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="85d21-106">Modify method of the MicrosoftDNS\_ATMAType class</span></span>

<span data-ttu-id="85d21-107">La méthode **Modify** met à jour un enregistrement de ressource d’adresse ATM en nom (ATMA).</span><span class="sxs-lookup"><span data-stu-id="85d21-107">The **Modify** method updates an ATM Address to Name (ATMA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="85d21-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85d21-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint16                Format,
  [in, optional] string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="85d21-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85d21-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85d21-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="85d21-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="85d21-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="85d21-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="85d21-112">*Format* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="85d21-112">*Format* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="85d21-113">Format d’adresse ATM.</span><span class="sxs-lookup"><span data-stu-id="85d21-113">ATM address format.</span></span> <span data-ttu-id="85d21-114">Deux valeurs possibles pour FORMAT sont : 0 indiquant le format AESA (ATM End System Address) et 1 indiquant le format E. 164.</span><span class="sxs-lookup"><span data-stu-id="85d21-114">Two possible values for FORMAT are: 0 indicating ATM End System Address (AESA) format and 1 indicating E.164 format.</span></span>

</dd> <dt>

<span data-ttu-id="85d21-115">*ATMAddress* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="85d21-115">*ATMAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="85d21-116">Chaîne de longueur variable d’octets contenant l’adresse ATM du nœud/propriétaire auquel appartient ce RR.</span><span class="sxs-lookup"><span data-stu-id="85d21-116">Variable length string of octets containing the ATM address of the node/owner to which this RR pertains.</span></span> <span data-ttu-id="85d21-117">Les quatre premiers octets du tableau sont utilisés pour stocker la taille de la chaîne d’octets.</span><span class="sxs-lookup"><span data-stu-id="85d21-117">The first four bytes of the array are used to store the size of the octet string.</span></span> <span data-ttu-id="85d21-118">L’octet le plus significatif est stocké à l’octet 0.</span><span class="sxs-lookup"><span data-stu-id="85d21-118">The most significant byte is stored in byte 0.</span></span>

</dd> <dt>

<span data-ttu-id="85d21-119">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="85d21-119">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="85d21-120">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="85d21-120">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85d21-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="85d21-121">Return value</span></span>

<span data-ttu-id="85d21-122">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="85d21-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85d21-123">Notes</span><span class="sxs-lookup"><span data-stu-id="85d21-123">Remarks</span></span>

<span data-ttu-id="85d21-124">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="85d21-124">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="85d21-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85d21-125">Requirements</span></span>



| <span data-ttu-id="85d21-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85d21-126">Requirement</span></span> | <span data-ttu-id="85d21-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="85d21-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85d21-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85d21-128">Minimum supported client</span></span><br/> | <span data-ttu-id="85d21-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="85d21-129">None supported</span></span><br/>                                                              |
| <span data-ttu-id="85d21-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85d21-130">Minimum supported server</span></span><br/> | <span data-ttu-id="85d21-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85d21-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="85d21-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="85d21-132">Namespace</span></span><br/>                | <span data-ttu-id="85d21-133">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="85d21-133">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="85d21-134">MOF</span><span class="sxs-lookup"><span data-stu-id="85d21-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85d21-135"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="85d21-135"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85d21-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85d21-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85d21-137">**MicrosoftDNS \_ ATMAType**</span><span class="sxs-lookup"><span data-stu-id="85d21-137">**MicrosoftDNS\_ATMAType**</span></span>](microsoftdns-atmatype.md)
</dt> <dt>

[<span data-ttu-id="85d21-138">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS ATMAType**</span><span class="sxs-lookup"><span data-stu-id="85d21-138">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="85d21-139">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="85d21-139">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





