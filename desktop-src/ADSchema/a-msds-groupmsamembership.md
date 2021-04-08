---
title: attribut ms-DS-GroupMSAMembership
description: Cet attribut est utilisé pour les vérifications d’accès afin de déterminer si un demandeur a l’autorisation de récupérer le mot de passe d’un MSA de groupe.
ms.assetid: 1512826d-fb7e-4039-ad93-f9334fd1d485
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-GroupMSAMembership
- Schéma Active Directory de l’attribut msDS-GroupMSAMembership
topic_type:
- apiref
api_name:
- ms-DS-GroupMSAMembership
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184f7f682d5360a0524f58e07c3f468b96e15b14
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103943174"
---
# <a name="ms-ds-groupmsamembership-attribute"></a><span data-ttu-id="53707-105">attribut ms-DS-GroupMSAMembership</span><span class="sxs-lookup"><span data-stu-id="53707-105">ms-DS-GroupMSAMembership attribute</span></span>

<span data-ttu-id="53707-106">Cet attribut est utilisé pour les vérifications d’accès afin de déterminer si un demandeur a l’autorisation de récupérer le mot de passe d’un MSA de groupe.</span><span class="sxs-lookup"><span data-stu-id="53707-106">This attribute is used for access checks to determine if a requestor has permission to retrieve the password for a group MSA.</span></span>



| <span data-ttu-id="53707-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="53707-107">Entry</span></span> | <span data-ttu-id="53707-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="53707-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="53707-109">CN</span><span class="sxs-lookup"><span data-stu-id="53707-109">CN</span></span>                | <span data-ttu-id="53707-110">ms-DS-GroupMSAMembership</span><span class="sxs-lookup"><span data-stu-id="53707-110">ms-DS-GroupMSAMembership</span></span>                            |
| <span data-ttu-id="53707-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="53707-111">Ldap-Display-Name</span></span> | <span data-ttu-id="53707-112">msDS-GroupMSAMembership</span><span class="sxs-lookup"><span data-stu-id="53707-112">msDS-GroupMSAMembership</span></span>                             |
| <span data-ttu-id="53707-113">Taille</span><span class="sxs-lookup"><span data-stu-id="53707-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="53707-114">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="53707-114">Update Privilege</span></span>  | \-                                                  |
| <span data-ttu-id="53707-115">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="53707-115">Update Frequency</span></span>  | \-                                                  |
| <span data-ttu-id="53707-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="53707-116">Attribute-Id</span></span>      | <span data-ttu-id="53707-117">1.2.840.113556.1.4.2200</span><span class="sxs-lookup"><span data-stu-id="53707-117">1.2.840.113556.1.4.2200</span></span>                             |
| <span data-ttu-id="53707-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="53707-118">System-Id-Guid</span></span>    | <span data-ttu-id="53707-119">888eedd6-ce04-df40-b462-b8a50e41ba38</span><span class="sxs-lookup"><span data-stu-id="53707-119">888eedd6-ce04-df40-b462-b8a50e41ba38</span></span>                |
| <span data-ttu-id="53707-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53707-120">Syntax</span></span>            | [<span data-ttu-id="53707-121">**String(NT-Sec-Desc)**</span><span class="sxs-lookup"><span data-stu-id="53707-121">**String(NT-Sec-Desc)**</span></span>](s-string-nt-sec-desc.md) |



## <a name="implementations"></a><span data-ttu-id="53707-122">Implémentations</span><span class="sxs-lookup"><span data-stu-id="53707-122">Implementations</span></span>

-   [<span data-ttu-id="53707-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="53707-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="53707-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="53707-124">Windows Server 2012</span></span>



| <span data-ttu-id="53707-125">Entrée</span><span class="sxs-lookup"><span data-stu-id="53707-125">Entry</span></span> | <span data-ttu-id="53707-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="53707-126">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="53707-127">ID de lien</span><span class="sxs-lookup"><span data-stu-id="53707-127">Link-Id</span></span>                | \-                                                                                          |
| <span data-ttu-id="53707-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53707-128">MAPI-Id</span></span>                | \-                                                                                          |
| <span data-ttu-id="53707-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="53707-129">System-Only</span></span>            | <span data-ttu-id="53707-130">Faux</span><span class="sxs-lookup"><span data-stu-id="53707-130">False</span></span>                                                                                       |
| <span data-ttu-id="53707-131">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="53707-131">Is-Single-Valued</span></span>       | <span data-ttu-id="53707-132">Vrai</span><span class="sxs-lookup"><span data-stu-id="53707-132">True</span></span>                                                                                        |
| <span data-ttu-id="53707-133">Est indexé</span><span class="sxs-lookup"><span data-stu-id="53707-133">Is Indexed</span></span>             | <span data-ttu-id="53707-134">Faux</span><span class="sxs-lookup"><span data-stu-id="53707-134">False</span></span>                                                                                       |
| <span data-ttu-id="53707-135">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="53707-135">In Global Catalog</span></span>      | <span data-ttu-id="53707-136">Faux</span><span class="sxs-lookup"><span data-stu-id="53707-136">False</span></span>                                                                                       |
| <span data-ttu-id="53707-137">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="53707-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="53707-138">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="53707-138">O:BAG:BAD:S:</span></span>                                                                                |
| <span data-ttu-id="53707-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53707-139">Range-Lower</span></span>            | \-                                                                                          |
| <span data-ttu-id="53707-140">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53707-140">Range-Upper</span></span>            | \-                                                                                          |
| <span data-ttu-id="53707-141">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53707-141">Search-Flags</span></span>           | <span data-ttu-id="53707-142">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53707-142">0x00000000</span></span>                                                                                  |
| <span data-ttu-id="53707-143">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53707-143">System-Flags</span></span>           | <span data-ttu-id="53707-144">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53707-144">0x00000010</span></span>                                                                                  |
| <span data-ttu-id="53707-145">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="53707-145">Classes used in</span></span>        | [<span data-ttu-id="53707-146">**ms-DS-Group-Managed-service-account**</span><span class="sxs-lookup"><span data-stu-id="53707-146">**ms-DS-Group-Managed-Service-Account**</span></span>](c-msds-groupmanagedserviceaccount.md)<br/> |



 

 





