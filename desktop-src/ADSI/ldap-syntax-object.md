---
title: Objet de syntaxe LDAP
description: Le fournisseur LDAP utilise le mappage suivant entre la syntaxe LDAP et la syntaxe ADSI.
ms.assetid: a82cf8ab-9591-4489-87a6-ccfab0e01d61
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, fournisseurs de services, syntaxe de mappage à la syntaxe LDAP
- mappage de la syntaxe ADSI à la syntaxe LDAP ADSI
- syntaxe et mappage d’ADSI à ADSI LDAP
- ADSI du fournisseur de services LDAP, mappage de la syntaxe ADSI à la syntaxe LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2272a0805ec32fd7ade9c4584feefb64fb1467f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100569"
---
# <a name="ldap-syntax-object"></a><span data-ttu-id="5d20e-107">Objet de syntaxe LDAP</span><span class="sxs-lookup"><span data-stu-id="5d20e-107">LDAP Syntax Object</span></span>

<span data-ttu-id="5d20e-108">Le fournisseur LDAP utilise le mappage suivant entre la syntaxe LDAP et la syntaxe ADSI.</span><span class="sxs-lookup"><span data-stu-id="5d20e-108">The LDAP provider uses the following mapping between the LDAP syntax and ADSI syntax.</span></span>



| <span data-ttu-id="5d20e-109">Syntaxe LDAP</span><span class="sxs-lookup"><span data-stu-id="5d20e-109">LDAP Syntax</span></span>   | <span data-ttu-id="5d20e-110">Syntaxe ADSI (Automation)</span><span class="sxs-lookup"><span data-stu-id="5d20e-110">ADSI Syntax (Automation)</span></span>            |
|---------------|-------------------------------------|
| <span data-ttu-id="5d20e-111">ADsPath</span><span class="sxs-lookup"><span data-stu-id="5d20e-111">ADsPath</span></span>       | <span data-ttu-id="5d20e-112">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="5d20e-112">VT\_BSTR</span></span>                            |
| <span data-ttu-id="5d20e-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="5d20e-113">Boolean</span></span>       | <span data-ttu-id="5d20e-114">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="5d20e-114">VT\_BOOL</span></span>                            |
| <span data-ttu-id="5d20e-115">Compteur</span><span class="sxs-lookup"><span data-stu-id="5d20e-115">Counter</span></span>       | <span data-ttu-id="5d20e-116">VT \_</span><span class="sxs-lookup"><span data-stu-id="5d20e-116">VT\_I4</span></span>                              |
| <span data-ttu-id="5d20e-117">EmailAddress</span><span class="sxs-lookup"><span data-stu-id="5d20e-117">EmailAddress</span></span>  | <span data-ttu-id="5d20e-118">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="5d20e-118">VT\_BSTR</span></span>                            |
| <span data-ttu-id="5d20e-119">FaxNumber</span><span class="sxs-lookup"><span data-stu-id="5d20e-119">FaxNumber</span></span>     | <span data-ttu-id="5d20e-120">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="5d20e-120">VT\_BSTR</span></span>                            |
| <span data-ttu-id="5d20e-121">Integer</span><span class="sxs-lookup"><span data-stu-id="5d20e-121">Integer</span></span>       | <span data-ttu-id="5d20e-122">VT \_</span><span class="sxs-lookup"><span data-stu-id="5d20e-122">VT\_I4</span></span>                              |
| <span data-ttu-id="5d20e-123">Intervalle</span><span class="sxs-lookup"><span data-stu-id="5d20e-123">Interval</span></span>      | <span data-ttu-id="5d20e-124">VT \_</span><span class="sxs-lookup"><span data-stu-id="5d20e-124">VT\_I4</span></span>                              |
| <span data-ttu-id="5d20e-125">List</span><span class="sxs-lookup"><span data-stu-id="5d20e-125">List</span></span>          | <span data-ttu-id="5d20e-126">\_variante VT ( \_ tableau VT BSTR \| VT \_ )</span><span class="sxs-lookup"><span data-stu-id="5d20e-126">VT\_VARIANT (VT\_BSTR \| VT\_ARRAY)</span></span> |
| <span data-ttu-id="5d20e-127">Adresse</span><span class="sxs-lookup"><span data-stu-id="5d20e-127">NetAddress</span></span>    | <span data-ttu-id="5d20e-128">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="5d20e-128">VT\_BSTR</span></span>                            |
| <span data-ttu-id="5d20e-129">OctetString</span><span class="sxs-lookup"><span data-stu-id="5d20e-129">OctetString</span></span>   | <span data-ttu-id="5d20e-130">\_variante VT</span><span class="sxs-lookup"><span data-stu-id="5d20e-130">VT\_VARIANT</span></span>                         |
| <span data-ttu-id="5d20e-131">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="5d20e-131">Path</span></span>          | <span data-ttu-id="5d20e-132">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="5d20e-132">VT\_BSTR</span></span>                            |
| <span data-ttu-id="5d20e-133">PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="5d20e-133">PhoneNumber</span></span>   | <span data-ttu-id="5d20e-134">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="5d20e-134">VT\_BSTR</span></span>                            |
| <span data-ttu-id="5d20e-135">PostalAddress</span><span class="sxs-lookup"><span data-stu-id="5d20e-135">PostalAddress</span></span> | <span data-ttu-id="5d20e-136">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="5d20e-136">VT\_BSTR</span></span>                            |
| <span data-ttu-id="5d20e-137">SmallInterval</span><span class="sxs-lookup"><span data-stu-id="5d20e-137">SmallInterval</span></span> | <span data-ttu-id="5d20e-138">VT \_</span><span class="sxs-lookup"><span data-stu-id="5d20e-138">VT\_I4</span></span>                              |
| <span data-ttu-id="5d20e-139">String</span><span class="sxs-lookup"><span data-stu-id="5d20e-139">String</span></span>        | <span data-ttu-id="5d20e-140">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="5d20e-140">VT\_BSTR</span></span>                            |
| <span data-ttu-id="5d20e-141">Temps</span><span class="sxs-lookup"><span data-stu-id="5d20e-141">Time</span></span>          | <span data-ttu-id="5d20e-142">\_Date VT</span><span class="sxs-lookup"><span data-stu-id="5d20e-142">VT\_DATE</span></span>                            |



 

 

 




