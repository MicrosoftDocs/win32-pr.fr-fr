---
title: attribut ms-DS-claim-type-application-to-Class
description: Pour un objet de type de revendication, cet attribut lié pointe vers les classes d’entité de sécurité Active Directory pour lesquelles des revendications doivent être émises. (Par exemple, un lien vers la classe d’utilisateur).
ms.assetid: 2323b120-c7b4-41ea-a04f-5791d6b55813
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory d’attribut de type « demande-application » ms-DS-claim-type
- Schéma Active Directory de l’attribut msDS-ClaimTypeAppliesToClass
topic_type:
- apiref
api_name:
- ms-DS-Claim-Type-Applies-To-Class
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72b5d440b492f5a9b120420bddba31375aec877b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514289"
---
# <a name="ms-ds-claim-type-applies-to-class-attribute"></a><span data-ttu-id="233b0-106">attribut ms-DS-claim-type-application-to-Class</span><span class="sxs-lookup"><span data-stu-id="233b0-106">ms-DS-Claim-Type-Applies-To-Class attribute</span></span>

<span data-ttu-id="233b0-107">Pour un objet de type de revendication, cet attribut lié pointe vers les classes d’entité de sécurité Active Directory pour lesquelles des revendications doivent être émises.</span><span class="sxs-lookup"><span data-stu-id="233b0-107">For a claim type object, this linked attribute points to the AD security principal classes that for which claims should be issued.</span></span> <span data-ttu-id="233b0-108">(Par exemple, un lien vers la classe d’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="233b0-108">(For example, a link to the user class).</span></span>



| <span data-ttu-id="233b0-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="233b0-109">Entry</span></span> | <span data-ttu-id="233b0-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="233b0-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="233b0-111">CN</span><span class="sxs-lookup"><span data-stu-id="233b0-111">CN</span></span>                | <span data-ttu-id="233b0-112">ms-DS-claim-type-s’applique à classe</span><span class="sxs-lookup"><span data-stu-id="233b0-112">ms-DS-Claim-Type-Applies-To-Class</span></span>       |
| <span data-ttu-id="233b0-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="233b0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="233b0-114">msDS-ClaimTypeAppliesToClass</span><span class="sxs-lookup"><span data-stu-id="233b0-114">msDS-ClaimTypeAppliesToClass</span></span>            |
| <span data-ttu-id="233b0-115">Taille</span><span class="sxs-lookup"><span data-stu-id="233b0-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="233b0-116">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="233b0-116">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="233b0-117">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="233b0-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="233b0-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="233b0-118">Attribute-Id</span></span>      | <span data-ttu-id="233b0-119">1.2.840.113556.1.4.2100</span><span class="sxs-lookup"><span data-stu-id="233b0-119">1.2.840.113556.1.4.2100</span></span>                 |
| <span data-ttu-id="233b0-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="233b0-120">System-Id-Guid</span></span>    | <span data-ttu-id="233b0-121">6afb0e4c-d876-437c-aeb6-c3e41454c272</span><span class="sxs-lookup"><span data-stu-id="233b0-121">6afb0e4c-d876-437c-aeb6-c3e41454c272</span></span>    |
| <span data-ttu-id="233b0-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="233b0-122">Syntax</span></span>            | [<span data-ttu-id="233b0-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="233b0-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="233b0-124">Implémentations</span><span class="sxs-lookup"><span data-stu-id="233b0-124">Implementations</span></span>

-   [<span data-ttu-id="233b0-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="233b0-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="233b0-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="233b0-126">Windows Server 2012</span></span>



| <span data-ttu-id="233b0-127">Entrée</span><span class="sxs-lookup"><span data-stu-id="233b0-127">Entry</span></span> | <span data-ttu-id="233b0-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="233b0-128">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="233b0-129">ID de lien</span><span class="sxs-lookup"><span data-stu-id="233b0-129">Link-Id</span></span>                | <span data-ttu-id="233b0-130">2176</span><span class="sxs-lookup"><span data-stu-id="233b0-130">2176</span></span>                                                    |
| <span data-ttu-id="233b0-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="233b0-131">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="233b0-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="233b0-132">System-Only</span></span>            | <span data-ttu-id="233b0-133">Faux</span><span class="sxs-lookup"><span data-stu-id="233b0-133">False</span></span>                                                   |
| <span data-ttu-id="233b0-134">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="233b0-134">Is-Single-Valued</span></span>       | <span data-ttu-id="233b0-135">Faux</span><span class="sxs-lookup"><span data-stu-id="233b0-135">False</span></span>                                                   |
| <span data-ttu-id="233b0-136">Est indexé</span><span class="sxs-lookup"><span data-stu-id="233b0-136">Is Indexed</span></span>             | <span data-ttu-id="233b0-137">Faux</span><span class="sxs-lookup"><span data-stu-id="233b0-137">False</span></span>                                                   |
| <span data-ttu-id="233b0-138">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="233b0-138">In Global Catalog</span></span>      | <span data-ttu-id="233b0-139">Faux</span><span class="sxs-lookup"><span data-stu-id="233b0-139">False</span></span>                                                   |
| <span data-ttu-id="233b0-140">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="233b0-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="233b0-141">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="233b0-141">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="233b0-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="233b0-142">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="233b0-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="233b0-143">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="233b0-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="233b0-144">Search-Flags</span></span>           | <span data-ttu-id="233b0-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="233b0-145">0x00000000</span></span>                                              |
| <span data-ttu-id="233b0-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="233b0-146">System-Flags</span></span>           | <span data-ttu-id="233b0-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="233b0-147">0x00000010</span></span>                                              |
| <span data-ttu-id="233b0-148">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="233b0-148">Classes used in</span></span>        | [<span data-ttu-id="233b0-149">**ms-DS-claim-type**</span><span class="sxs-lookup"><span data-stu-id="233b0-149">**ms-DS-Claim-Type**</span></span>](c-msds-claimtype.md)<br/> |



 

 





