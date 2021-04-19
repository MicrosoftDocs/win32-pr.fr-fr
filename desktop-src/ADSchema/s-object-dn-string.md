---
title: Syntaxe Object (DN-String)
description: Chaîne d’octets qui contient une valeur de chaîne et un DN.
ms.assetid: 7a5ce9f3-ac97-4936-868a-6b18f202972f
ms.tgt_platform: multiple
keywords:
- Syntaxe d’objet (DN-String) schéma Active Directory
topic_type:
- apiref
api_name:
- Object(DN-String)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823da21325abdc426d5f58df4cdf04de19fc68b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514266"
---
# <a name="objectdn-string-syntax"></a><span data-ttu-id="f5138-104">Syntaxe Object (DN-String)</span><span class="sxs-lookup"><span data-stu-id="f5138-104">Object(DN-String) syntax</span></span>

<span data-ttu-id="f5138-105">Chaîne d’octets qui contient une valeur de chaîne et un DN.</span><span class="sxs-lookup"><span data-stu-id="f5138-105">An octet string that contains a string value and a DN.</span></span>



| <span data-ttu-id="f5138-106">Entrée</span><span class="sxs-lookup"><span data-stu-id="f5138-106">Entry</span></span> | <span data-ttu-id="f5138-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5138-107">Value</span></span> |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f5138-108">Nom</span><span class="sxs-lookup"><span data-stu-id="f5138-108">Name</span></span>         | <span data-ttu-id="f5138-109">Object(DN-String)</span><span class="sxs-lookup"><span data-stu-id="f5138-109">Object(DN-String)</span></span>                                                                  |
| <span data-ttu-id="f5138-110">ID de syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5138-110">Syntax ID</span></span>    | <span data-ttu-id="f5138-111">2.5.5.14</span><span class="sxs-lookup"><span data-stu-id="f5138-111">2.5.5.14</span></span>                                                                           |
| <span data-ttu-id="f5138-112">ID OM</span><span class="sxs-lookup"><span data-stu-id="f5138-112">OM ID</span></span>        | <span data-ttu-id="f5138-113">127</span><span class="sxs-lookup"><span data-stu-id="f5138-113">127</span></span>                                                                                |
| <span data-ttu-id="f5138-114">Type MAPI</span><span class="sxs-lookup"><span data-stu-id="f5138-114">MAPI Type</span></span>    | \-                                                                                 |
| <span data-ttu-id="f5138-115">Type ADS</span><span class="sxs-lookup"><span data-stu-id="f5138-115">ADS Type</span></span>     | <span data-ttu-id="f5138-116">ADSTYPE \_ DN \_ avec \_ chaîne</span><span class="sxs-lookup"><span data-stu-id="f5138-116">ADSTYPE\_DN\_WITH\_STRING</span></span>                                                          |
| <span data-ttu-id="f5138-117">Type de variante</span><span class="sxs-lookup"><span data-stu-id="f5138-117">Variant Type</span></span> | <span data-ttu-id="f5138-118">\_distribution vt</span><span class="sxs-lookup"><span data-stu-id="f5138-118">VT\_DISPATCH</span></span>                                                                       |
| <span data-ttu-id="f5138-119">SDS, type</span><span class="sxs-lookup"><span data-stu-id="f5138-119">SDS Type</span></span>     | <span data-ttu-id="f5138-120">Objet COM pouvant être casté en [**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring).</span><span class="sxs-lookup"><span data-stu-id="f5138-120">A COM object that can be cast to an [**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring).</span></span> |



## <a name="remarks"></a><span data-ttu-id="f5138-121">Notes</span><span class="sxs-lookup"><span data-stu-id="f5138-121">Remarks</span></span>

<span data-ttu-id="f5138-122">Une valeur avec cette syntaxe a le format suivant :</span><span class="sxs-lookup"><span data-stu-id="f5138-122">A value with this syntax has the following format:</span></span>

``` syntax
S:<char count>:<string value>:<object DN>
```

<span data-ttu-id="f5138-123">où « &lt; nombre &gt; de caractères » est le nombre de caractères dans la &lt; chaîne « valeur de chaîne &gt; », et « &lt; objet DN &gt; » est un nom unique d’un objet dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f5138-123">where "&lt;char count&gt;" is the number of characters in the "&lt;string value&gt;" string, and "&lt;object DN&gt;" is a distinguished name of an object in Active Directory.</span></span> <span data-ttu-id="f5138-124">Active Directory met à jour le DN si l’objet auquel il fait référence est déplacé ou renommé.</span><span class="sxs-lookup"><span data-stu-id="f5138-124">Active Directory updates the DN if the object that it refers to is moved or renamed.</span></span>

## <a name="see-also"></a><span data-ttu-id="f5138-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5138-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5138-126">**IADsDNWithString**</span><span class="sxs-lookup"><span data-stu-id="f5138-126">**IADsDNWithString**</span></span>](/windows/desktop/api/iads/nn-iads-iadsdnwithstring)
</dt> </dl>

 

 
