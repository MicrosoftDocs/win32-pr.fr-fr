---
title: attribut ms-DS-ManagedPassword
description: Cet attribut construit retourne un objet BLOB qui contient les mots de passe en texte clair précédents et actuels, TimeUntilEpochExpires et TimeUntilNextScheduledUpdate pour un MSA de groupe.
ms.assetid: bcabb20f-46f3-4c15-b71b-a8dfc43678bc
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-ManagedPassword
- Schéma Active Directory de l’attribut msDS-ManagedPassword
topic_type:
- apiref
api_name:
- ms-DS-ManagedPassword
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a440f1849e01ae4930b72441f75b17ce51a0566b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107812"
---
# <a name="ms-ds-managedpassword-attribute"></a><span data-ttu-id="36080-105">attribut ms-DS-ManagedPassword</span><span class="sxs-lookup"><span data-stu-id="36080-105">ms-DS-ManagedPassword attribute</span></span>

<span data-ttu-id="36080-106">Cet attribut construit retourne un objet BLOB qui contient les mots de passe en texte clair précédents et actuels, TimeUntilEpochExpires et TimeUntilNextScheduledUpdate pour un MSA de groupe.</span><span class="sxs-lookup"><span data-stu-id="36080-106">This constructed attribute returns a blob that contains the clear-text previous and current password, TimeUntilEpochExpires, and TimeUntilNextScheduledUpdate for a group MSA.</span></span>



| <span data-ttu-id="36080-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="36080-107">Entry</span></span> | <span data-ttu-id="36080-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="36080-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="36080-109">CN</span><span class="sxs-lookup"><span data-stu-id="36080-109">CN</span></span>                | <span data-ttu-id="36080-110">ms-DS-ManagedPassword</span><span class="sxs-lookup"><span data-stu-id="36080-110">ms-DS-ManagedPassword</span></span>                                 |
| <span data-ttu-id="36080-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="36080-111">Ldap-Display-Name</span></span> | <span data-ttu-id="36080-112">msDS-ManagedPassword</span><span class="sxs-lookup"><span data-stu-id="36080-112">msDS-ManagedPassword</span></span>                                  |
| <span data-ttu-id="36080-113">Taille</span><span class="sxs-lookup"><span data-stu-id="36080-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="36080-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="36080-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="36080-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="36080-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="36080-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="36080-116">Attribute-Id</span></span>      | <span data-ttu-id="36080-117">1.2.840.113556.1.4.2196</span><span class="sxs-lookup"><span data-stu-id="36080-117">1.2.840.113556.1.4.2196</span></span>                               |
| <span data-ttu-id="36080-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="36080-118">System-Id-Guid</span></span>    | <span data-ttu-id="36080-119">e362ed86-b728-0842-b27d-2dea7a9df218</span><span class="sxs-lookup"><span data-stu-id="36080-119">e362ed86-b728-0842-b27d-2dea7a9df218</span></span>                  |
| <span data-ttu-id="36080-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36080-120">Syntax</span></span>            | [<span data-ttu-id="36080-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="36080-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="36080-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="36080-122">Implementations</span></span>

-   [<span data-ttu-id="36080-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="36080-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="36080-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="36080-124">Windows Server 2012</span></span>



| <span data-ttu-id="36080-125">Entrée</span><span class="sxs-lookup"><span data-stu-id="36080-125">Entry</span></span> | <span data-ttu-id="36080-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="36080-126">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="36080-127">ID de lien</span><span class="sxs-lookup"><span data-stu-id="36080-127">Link-Id</span></span>                | \-                                                                                          |
| <span data-ttu-id="36080-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36080-128">MAPI-Id</span></span>                | \-                                                                                          |
| <span data-ttu-id="36080-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="36080-129">System-Only</span></span>            | <span data-ttu-id="36080-130">Faux</span><span class="sxs-lookup"><span data-stu-id="36080-130">False</span></span>                                                                                       |
| <span data-ttu-id="36080-131">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="36080-131">Is-Single-Valued</span></span>       | <span data-ttu-id="36080-132">Vrai</span><span class="sxs-lookup"><span data-stu-id="36080-132">True</span></span>                                                                                        |
| <span data-ttu-id="36080-133">Est indexé</span><span class="sxs-lookup"><span data-stu-id="36080-133">Is Indexed</span></span>             | <span data-ttu-id="36080-134">Faux</span><span class="sxs-lookup"><span data-stu-id="36080-134">False</span></span>                                                                                       |
| <span data-ttu-id="36080-135">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="36080-135">In Global Catalog</span></span>      | <span data-ttu-id="36080-136">Faux</span><span class="sxs-lookup"><span data-stu-id="36080-136">False</span></span>                                                                                       |
| <span data-ttu-id="36080-137">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="36080-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="36080-138">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="36080-138">O:BAG:BAD:S:</span></span>                                                                                |
| <span data-ttu-id="36080-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36080-139">Range-Lower</span></span>            | \-                                                                                          |
| <span data-ttu-id="36080-140">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36080-140">Range-Upper</span></span>            | \-                                                                                          |
| <span data-ttu-id="36080-141">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36080-141">Search-Flags</span></span>           | <span data-ttu-id="36080-142">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36080-142">0x00000000</span></span>                                                                                  |
| <span data-ttu-id="36080-143">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36080-143">System-Flags</span></span>           | <span data-ttu-id="36080-144">0x00000014</span><span class="sxs-lookup"><span data-stu-id="36080-144">0x00000014</span></span>                                                                                  |
| <span data-ttu-id="36080-145">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="36080-145">Classes used in</span></span>        | [<span data-ttu-id="36080-146">**ms-DS-Group-Managed-service-account**</span><span class="sxs-lookup"><span data-stu-id="36080-146">**ms-DS-Group-Managed-Service-Account**</span></span>](c-msds-groupmanagedserviceaccount.md)<br/> |



 

 





