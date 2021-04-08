---
title: Modifier la méthode de la classe MicrosoftDNS_WKSType
description: La méthode modify met à jour un enregistrement de ressource Well-Known services (WKS).
ms.assetid: 3a9100eb-dc90-45bb-9739-14026da100fd
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_WKSType classe
- MicrosoftDNS_WKSType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30f7cf58a231d93288a3cdc170fa857bb12687af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843861"
---
# <a name="modify-method-of-the-microsoftdns_wkstype-class"></a><span data-ttu-id="f8e13-106">Modifier la méthode de la \_ classe WKSType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="f8e13-106">Modify method of the MicrosoftDNS\_WKSType class</span></span>

<span data-ttu-id="f8e13-107">La méthode **Modify** met à jour un enregistrement de ressource Well-Known services (WKS).</span><span class="sxs-lookup"><span data-stu-id="f8e13-107">The **Modify** method updates a Well-Known Services (WKS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8e13-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8e13-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               InternetAddress,
  [in, optional] uint8                IPProtocol,
  [in, optional] uint8                Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="f8e13-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8e13-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8e13-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f8e13-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f8e13-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="f8e13-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="f8e13-112">*InternetAddress* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f8e13-112">*InternetAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f8e13-113">Adresse IP Internet pour le propriétaire de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f8e13-113">Internet IP address for the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="f8e13-114">*IPProtocol* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f8e13-114">*IPProtocol* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f8e13-115">Chaîne représentant le protocole IP pour cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f8e13-115">String representing the IP protocol for this record.</span></span> <span data-ttu-id="f8e13-116">Les valeurs valides sont UDP ou TCP.</span><span class="sxs-lookup"><span data-stu-id="f8e13-116">Valid values are UDP or TCP.</span></span>

</dd> <dt>

<span data-ttu-id="f8e13-117">*Services* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f8e13-117">*Services* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f8e13-118">Chaîne contenant tous les services utilisés par l’enregistrement du service bien connu (WKS).</span><span class="sxs-lookup"><span data-stu-id="f8e13-118">String containing all services used by the Well Known Service (WKS) record.</span></span>

</dd> <dt>

<span data-ttu-id="f8e13-119">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="f8e13-119">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f8e13-120">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="f8e13-120">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8e13-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f8e13-121">Return value</span></span>

<span data-ttu-id="f8e13-122">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f8e13-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8e13-123">Notes</span><span class="sxs-lookup"><span data-stu-id="f8e13-123">Remarks</span></span>

<span data-ttu-id="f8e13-124">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="f8e13-124">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8e13-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8e13-125">Requirements</span></span>



| <span data-ttu-id="f8e13-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8e13-126">Requirement</span></span> | <span data-ttu-id="f8e13-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8e13-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8e13-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8e13-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f8e13-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8e13-129">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f8e13-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8e13-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f8e13-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8e13-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f8e13-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f8e13-132">Namespace</span></span><br/>                | <span data-ttu-id="f8e13-133">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="f8e13-133">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f8e13-134">MOF</span><span class="sxs-lookup"><span data-stu-id="f8e13-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8e13-135"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8e13-135"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8e13-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8e13-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8e13-137">**MicrosoftDNS \_ WKSType**</span><span class="sxs-lookup"><span data-stu-id="f8e13-137">**MicrosoftDNS\_WKSType**</span></span>](microsoftdns-wkstype.md)
</dt> <dt>

[<span data-ttu-id="f8e13-138">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS WKSType**</span><span class="sxs-lookup"><span data-stu-id="f8e13-138">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="f8e13-139">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="f8e13-139">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





