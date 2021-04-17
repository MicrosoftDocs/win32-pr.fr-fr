---
title: Méthode GetObjectByTextRepresentation de la classe MicrosoftDNS_ResourceRecord
description: La méthode GetObjectByTextRepresentation récupère une instance existante de la classe MicrosoftDNS \_ ResourceRecord.
ms.assetid: d25e10de-81fa-4220-b2b8-d9a65298b629
keywords:
- Méthode GetObjectByTextRepresentation DNS
- Méthode GetObjectByTextRepresentation DNS, classe MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord de la classe DNS, méthode GetObjectByTextRepresentation
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2aea2588a70ff4bdab89eae58b65715152d6c7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465682"
---
# <a name="getobjectbytextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a><span data-ttu-id="120fc-106">Méthode GetObjectByTextRepresentation de la \_ classe MicrosoftDNS ResourceRecord</span><span class="sxs-lookup"><span data-stu-id="120fc-106">GetObjectByTextRepresentation method of the MicrosoftDNS\_ResourceRecord class</span></span>

<span data-ttu-id="120fc-107">La méthode **GetObjectByTextRepresentation** récupère une instance existante de la classe [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="120fc-107">The **GetObjectByTextRepresentation** method retrieves an existing instance of the [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="120fc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="120fc-108">Syntax</span></span>


```mof
void GetObjectByTextRepresentation(
  [in]  string                      DnsServerName,
  [in]  string                      ContainerName,
  [in]  string                      TextRepresentation,
  [out] MicrosoftDns_ResourceRecord RR
);
```



## <a name="parameters"></a><span data-ttu-id="120fc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="120fc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="120fc-110">*DnsServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="120fc-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="120fc-111">Nom du serveur DNS à partir duquel le RR doit être récupéré.</span><span class="sxs-lookup"><span data-stu-id="120fc-111">Name of the DNS Server from which the RR should be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="120fc-112">*ContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="120fc-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="120fc-113">Nom du conteneur à partir duquel l’enregistrement de ressource doit être obtenu.</span><span class="sxs-lookup"><span data-stu-id="120fc-113">Name of the container from which the RR should be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="120fc-114">*TextRepresentation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="120fc-114">*TextRepresentation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="120fc-115">Représentation textuelle du RR à récupérer.</span><span class="sxs-lookup"><span data-stu-id="120fc-115">Text representation of the RR to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="120fc-116">*RR* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="120fc-116">*RR* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="120fc-117">Référence à l’enregistrement de ressource instancié.</span><span class="sxs-lookup"><span data-stu-id="120fc-117">Reference to the instantiated RR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="120fc-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="120fc-118">Return value</span></span>

<span data-ttu-id="120fc-119">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="120fc-119">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="120fc-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="120fc-120">Requirements</span></span>



| <span data-ttu-id="120fc-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="120fc-121">Requirement</span></span> | <span data-ttu-id="120fc-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="120fc-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="120fc-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="120fc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="120fc-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="120fc-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="120fc-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="120fc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="120fc-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="120fc-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="120fc-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="120fc-127">Namespace</span></span><br/>                | <span data-ttu-id="120fc-128">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="120fc-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="120fc-129">MOF</span><span class="sxs-lookup"><span data-stu-id="120fc-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="120fc-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="120fc-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="120fc-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="120fc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="120fc-132">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="120fc-132">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="120fc-133">**Méthode CreateInstanceFromTextRepresentation de la \_ classe MicrosoftDNS ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="120fc-133">**CreateInstanceFromTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> </dl>

 

 





