---
title: Méthode CreateInstanceFromTextRepresentation de la classe MicrosoftDNS_ResourceRecord
description: La méthode CreateInstanceFromTextRepresentation instancie un \_ objet ResourceRecord MicrosoftDNS.
ms.assetid: 19600a9a-f75d-40ad-98e5-f81465d10f79
keywords:
- Méthode CreateInstanceFromTextRepresentation DNS
- Méthode CreateInstanceFromTextRepresentation DNS, classe MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord de la classe DNS, méthode CreateInstanceFromTextRepresentation
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a578d036180ecb1dc8a5e66bf853eec8845583f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032969"
---
# <a name="createinstancefromtextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a><span data-ttu-id="68087-106">Méthode CreateInstanceFromTextRepresentation de la \_ classe MicrosoftDNS ResourceRecord</span><span class="sxs-lookup"><span data-stu-id="68087-106">CreateInstanceFromTextRepresentation method of the MicrosoftDNS\_ResourceRecord class</span></span>

<span data-ttu-id="68087-107">La méthode **CreateInstanceFromTextRepresentation** instancie un [**objet \_ ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="68087-107">The **CreateInstanceFromTextRepresentation** method instantiates a [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="68087-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68087-108">Syntax</span></span>


```mof
void CreateInstanceFromTextRepresentation(
  [in]       string                      DnsServerName,
  [in]       string                      ContainerName,
  [in]       string                      TextRepresentation,
  [out, ref] MicrosoftDNS_ResourceRecord &RR
);
```



## <a name="parameters"></a><span data-ttu-id="68087-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68087-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68087-110">*DnsServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="68087-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68087-111">Nom du serveur DNS sur lequel le RR doit être créé.</span><span class="sxs-lookup"><span data-stu-id="68087-111">Name of the DNS Server on which the RR should be created.</span></span>

</dd> <dt>

<span data-ttu-id="68087-112">*ContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="68087-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68087-113">Nom du conteneur dans lequel le nouvel enregistrement de ressource doit être placé.</span><span class="sxs-lookup"><span data-stu-id="68087-113">Name of the container into which the new RR should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="68087-114">*TextRepresentation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="68087-114">*TextRepresentation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68087-115">Représentation textuelle de l’instance de RR à créer.</span><span class="sxs-lookup"><span data-stu-id="68087-115">Text representation of the RR instance to be created.</span></span>

</dd> <dt>

<span data-ttu-id="68087-116">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="68087-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="68087-117">Référence à l’enregistrement de ressource instancié.</span><span class="sxs-lookup"><span data-stu-id="68087-117">Reference to the instantiated RR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68087-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="68087-118">Return value</span></span>

<span data-ttu-id="68087-119">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="68087-119">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="68087-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68087-120">Requirements</span></span>



| <span data-ttu-id="68087-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68087-121">Requirement</span></span> | <span data-ttu-id="68087-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="68087-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68087-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68087-123">Minimum supported client</span></span><br/> | <span data-ttu-id="68087-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="68087-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="68087-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68087-125">Minimum supported server</span></span><br/> | <span data-ttu-id="68087-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68087-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="68087-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="68087-127">Namespace</span></span><br/>                | <span data-ttu-id="68087-128">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="68087-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="68087-129">MOF</span><span class="sxs-lookup"><span data-stu-id="68087-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68087-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68087-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68087-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68087-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68087-132">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="68087-132">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="68087-133">**Méthode GetObjectByTextRepresentation de la \_ classe MicrosoftDNS ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="68087-133">**GetObjectByTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





