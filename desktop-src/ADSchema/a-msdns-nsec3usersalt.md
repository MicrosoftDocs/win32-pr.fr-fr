---
title: MS-DNS-NSEC3-attribut sel utilisateur
description: Attribut qui définit une chaîne Salt NSEC3 spécifiée par l’utilisateur à utiliser lors de la signature de la zone DNS. S’il est vide, le Salt aléatoire est utilisé.
ms.assetid: b9829732-8a79-4f07-8644-9fe4ba05ba8f
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut de sel d’utilisateur MS-DNS-NSEC3
- Schéma AD de l’attribut msDNs-NSEC3UserSalt
topic_type:
- apiref
api_name:
- ms-DNS-NSEC3-User-Salt
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d28acb28dec95ef13afc37f9d7f26d713d5cf9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744756"
---
# <a name="ms-dns-nsec3-user-salt-attribute"></a><span data-ttu-id="4f329-106">MS-DNS-NSEC3-attribut sel utilisateur</span><span class="sxs-lookup"><span data-stu-id="4f329-106">ms-DNS-NSEC3-User-Salt attribute</span></span>

<span data-ttu-id="4f329-107">Attribut qui définit une chaîne Salt NSEC3 spécifiée par l’utilisateur à utiliser lors de la signature de la zone DNS.</span><span class="sxs-lookup"><span data-stu-id="4f329-107">An attribute that defines a user-specified NSEC3 salt string to use when signing the DNS zone.</span></span> <span data-ttu-id="4f329-108">S’il est vide, le Salt aléatoire est utilisé.</span><span class="sxs-lookup"><span data-stu-id="4f329-108">If empty, random salt will be used.</span></span>



| <span data-ttu-id="4f329-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="4f329-109">Entry</span></span> | <span data-ttu-id="4f329-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f329-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="4f329-111">CN</span><span class="sxs-lookup"><span data-stu-id="4f329-111">CN</span></span>                | <span data-ttu-id="4f329-112">MS-DNS-NSEC3-utilisateur-Salt</span><span class="sxs-lookup"><span data-stu-id="4f329-112">ms-DNS-NSEC3-User-Salt</span></span>                      |
| <span data-ttu-id="4f329-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4f329-113">Ldap-Display-Name</span></span> | <span data-ttu-id="4f329-114">msDN-NSEC3UserSalt</span><span class="sxs-lookup"><span data-stu-id="4f329-114">msDNS-NSEC3UserSalt</span></span>                         |
| <span data-ttu-id="4f329-115">Taille</span><span class="sxs-lookup"><span data-stu-id="4f329-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="4f329-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="4f329-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="4f329-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="4f329-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="4f329-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4f329-118">Attribute-Id</span></span>      | <span data-ttu-id="4f329-119">1.2.840.113556.1.4.2148</span><span class="sxs-lookup"><span data-stu-id="4f329-119">1.2.840.113556.1.4.2148</span></span>                     |
| <span data-ttu-id="4f329-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4f329-120">System-Id-Guid</span></span>    | <span data-ttu-id="4f329-121">aff16770-9622-4fbc-a128-3088777605b9</span><span class="sxs-lookup"><span data-stu-id="4f329-121">aff16770-9622-4fbc-a128-3088777605b9</span></span>        |
| <span data-ttu-id="4f329-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f329-122">Syntax</span></span>            | [<span data-ttu-id="4f329-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4f329-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="4f329-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="4f329-124">Implementations</span></span>

-   [<span data-ttu-id="4f329-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4f329-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="4f329-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4f329-126">Windows Server 2012</span></span>



| <span data-ttu-id="4f329-127">Entrée</span><span class="sxs-lookup"><span data-stu-id="4f329-127">Entry</span></span> | <span data-ttu-id="4f329-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f329-128">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="4f329-129">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4f329-129">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="4f329-130">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f329-130">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="4f329-131">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f329-131">System-Only</span></span>            | <span data-ttu-id="4f329-132">Faux</span><span class="sxs-lookup"><span data-stu-id="4f329-132">False</span></span>                                    |
| <span data-ttu-id="4f329-133">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4f329-133">Is-Single-Valued</span></span>       | <span data-ttu-id="4f329-134">Vrai</span><span class="sxs-lookup"><span data-stu-id="4f329-134">True</span></span>                                     |
| <span data-ttu-id="4f329-135">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4f329-135">Is Indexed</span></span>             | <span data-ttu-id="4f329-136">Faux</span><span class="sxs-lookup"><span data-stu-id="4f329-136">False</span></span>                                    |
| <span data-ttu-id="4f329-137">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4f329-137">In Global Catalog</span></span>      | <span data-ttu-id="4f329-138">Faux</span><span class="sxs-lookup"><span data-stu-id="4f329-138">False</span></span>                                    |
| <span data-ttu-id="4f329-139">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4f329-139">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f329-140">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4f329-140">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="4f329-141">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f329-141">Range-Lower</span></span>            | <span data-ttu-id="4f329-142">0</span><span class="sxs-lookup"><span data-stu-id="4f329-142">0</span></span>                                        |
| <span data-ttu-id="4f329-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f329-143">Range-Upper</span></span>            | <span data-ttu-id="4f329-144">510</span><span class="sxs-lookup"><span data-stu-id="4f329-144">510</span></span>                                      |
| <span data-ttu-id="4f329-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f329-145">Search-Flags</span></span>           | <span data-ttu-id="4f329-146">0x00000008</span><span class="sxs-lookup"><span data-stu-id="4f329-146">0x00000008</span></span>                               |
| <span data-ttu-id="4f329-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f329-147">System-Flags</span></span>           | <span data-ttu-id="4f329-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f329-148">0x00000010</span></span>                               |
| <span data-ttu-id="4f329-149">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4f329-149">Classes used in</span></span>        | [<span data-ttu-id="4f329-150">**Zone DNS**</span><span class="sxs-lookup"><span data-stu-id="4f329-150">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



 

 





