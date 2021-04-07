---
title: attribut de descripteur de clé MS-DNS
description: Attribut qui contient l’ensemble des descripteurs de clé de signature DNSSEC (SKDs) utilisés par le serveur DNS pour générer des clés et signer la zone DNS.
ms.assetid: ebfa200c-9201-4b2a-addd-dfd032cb9425
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory des attributs de descripteurs de signature-clé MS-DNS
- Schéma AD de l’attribut msDNs-SigningKeyDescriptors
topic_type:
- apiref
api_name:
- ms-DNS-Signing-Key-Descriptors
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c49893f7b05aaba736b912b4ef1f217af5d98e0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845190"
---
# <a name="ms-dns-signing-key-descriptors-attribute"></a><span data-ttu-id="f91c6-105">attribut de descripteur de clé MS-DNS</span><span class="sxs-lookup"><span data-stu-id="f91c6-105">ms-DNS-Signing-Key-Descriptors attribute</span></span>

<span data-ttu-id="f91c6-106">Attribut qui contient l’ensemble des descripteurs de clé de signature DNSSEC (SKDs) utilisés par le serveur DNS pour générer des clés et signer la zone DNS.</span><span class="sxs-lookup"><span data-stu-id="f91c6-106">An attribute that contains the set of DNSSEC Signing Key Descriptors (SKDs) used by the DNS server to generate keys and sign the DNS zone.</span></span>



| <span data-ttu-id="f91c6-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="f91c6-107">Entry</span></span> | <span data-ttu-id="f91c6-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="f91c6-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="f91c6-109">CN</span><span class="sxs-lookup"><span data-stu-id="f91c6-109">CN</span></span>                | <span data-ttu-id="f91c6-110">MS-DNS-signature-descripteurs</span><span class="sxs-lookup"><span data-stu-id="f91c6-110">ms-DNS-Signing-Key-Descriptors</span></span>                        |
| <span data-ttu-id="f91c6-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f91c6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f91c6-112">msDN-SigningKeyDescriptors</span><span class="sxs-lookup"><span data-stu-id="f91c6-112">msDNS-SigningKeyDescriptors</span></span>                           |
| <span data-ttu-id="f91c6-113">Taille</span><span class="sxs-lookup"><span data-stu-id="f91c6-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="f91c6-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="f91c6-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="f91c6-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="f91c6-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="f91c6-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f91c6-116">Attribute-Id</span></span>      | <span data-ttu-id="f91c6-117">1.2.840.113556.1.4.2143</span><span class="sxs-lookup"><span data-stu-id="f91c6-117">1.2.840.113556.1.4.2143</span></span>                               |
| <span data-ttu-id="f91c6-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f91c6-118">System-Id-Guid</span></span>    | <span data-ttu-id="f91c6-119">3443d8cd-e5b6-4f3b-b098-659a0214a079</span><span class="sxs-lookup"><span data-stu-id="f91c6-119">3443d8cd-e5b6-4f3b-b098-659a0214a079</span></span>                  |
| <span data-ttu-id="f91c6-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f91c6-120">Syntax</span></span>            | [<span data-ttu-id="f91c6-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="f91c6-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="f91c6-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="f91c6-122">Implementations</span></span>

-   [<span data-ttu-id="f91c6-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f91c6-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="f91c6-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f91c6-124">Windows Server 2012</span></span>



| <span data-ttu-id="f91c6-125">Entrée</span><span class="sxs-lookup"><span data-stu-id="f91c6-125">Entry</span></span> | <span data-ttu-id="f91c6-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f91c6-126">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f91c6-127">ID de lien</span><span class="sxs-lookup"><span data-stu-id="f91c6-127">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f91c6-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f91c6-128">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f91c6-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="f91c6-129">System-Only</span></span>            | <span data-ttu-id="f91c6-130">Faux</span><span class="sxs-lookup"><span data-stu-id="f91c6-130">False</span></span>                                    |
| <span data-ttu-id="f91c6-131">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="f91c6-131">Is-Single-Valued</span></span>       | <span data-ttu-id="f91c6-132">Faux</span><span class="sxs-lookup"><span data-stu-id="f91c6-132">False</span></span>                                    |
| <span data-ttu-id="f91c6-133">Est indexé</span><span class="sxs-lookup"><span data-stu-id="f91c6-133">Is Indexed</span></span>             | <span data-ttu-id="f91c6-134">Faux</span><span class="sxs-lookup"><span data-stu-id="f91c6-134">False</span></span>                                    |
| <span data-ttu-id="f91c6-135">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="f91c6-135">In Global Catalog</span></span>      | <span data-ttu-id="f91c6-136">Faux</span><span class="sxs-lookup"><span data-stu-id="f91c6-136">False</span></span>                                    |
| <span data-ttu-id="f91c6-137">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="f91c6-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="f91c6-138">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="f91c6-138">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f91c6-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f91c6-139">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f91c6-140">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f91c6-140">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f91c6-141">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f91c6-141">Search-Flags</span></span>           | <span data-ttu-id="f91c6-142">0x00000008</span><span class="sxs-lookup"><span data-stu-id="f91c6-142">0x00000008</span></span>                               |
| <span data-ttu-id="f91c6-143">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f91c6-143">System-Flags</span></span>           | <span data-ttu-id="f91c6-144">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f91c6-144">0x00000010</span></span>                               |
| <span data-ttu-id="f91c6-145">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="f91c6-145">Classes used in</span></span>        | [<span data-ttu-id="f91c6-146">**Zone DNS**</span><span class="sxs-lookup"><span data-stu-id="f91c6-146">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



 

 





