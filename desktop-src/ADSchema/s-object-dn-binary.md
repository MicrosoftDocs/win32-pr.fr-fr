---
title: Syntaxe Object (DN-Binary)
description: Chaîne d’octets qui contient une valeur binaire et un nom unique (DN).
ms.assetid: 1d7efc17-a99a-41bf-9812-9e8a2b2b6644
ms.tgt_platform: multiple
keywords:
- Syntaxe de l’objet (DN-Binary) AD Schema
topic_type:
- apiref
api_name:
- Object(DN-Binary)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e96f640ad729f203362df906bcc6afe6b82e7e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104106702"
---
# <a name="objectdn-binary-syntax"></a><span data-ttu-id="2a669-104">Syntaxe Object (DN-Binary)</span><span class="sxs-lookup"><span data-stu-id="2a669-104">Object(DN-Binary) syntax</span></span>

<span data-ttu-id="2a669-105">Chaîne d’octets qui contient une valeur binaire et un nom unique (DN).</span><span class="sxs-lookup"><span data-stu-id="2a669-105">An octet string that contains a binary value and a distinguished name (DN).</span></span>



| <span data-ttu-id="2a669-106">Entrée</span><span class="sxs-lookup"><span data-stu-id="2a669-106">Entry</span></span> | <span data-ttu-id="2a669-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a669-107">Value</span></span> |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2a669-108">Nom</span><span class="sxs-lookup"><span data-stu-id="2a669-108">Name</span></span>         | <span data-ttu-id="2a669-109">Object(DN-Binary)</span><span class="sxs-lookup"><span data-stu-id="2a669-109">Object(DN-Binary)</span></span>                                                                  |
| <span data-ttu-id="2a669-110">ID de syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a669-110">Syntax ID</span></span>    | <span data-ttu-id="2a669-111">2.5.5.7</span><span class="sxs-lookup"><span data-stu-id="2a669-111">2.5.5.7</span></span>                                                                            |
| <span data-ttu-id="2a669-112">ID OM</span><span class="sxs-lookup"><span data-stu-id="2a669-112">OM ID</span></span>        | <span data-ttu-id="2a669-113">127</span><span class="sxs-lookup"><span data-stu-id="2a669-113">127</span></span>                                                                                |
| <span data-ttu-id="2a669-114">Type MAPI</span><span class="sxs-lookup"><span data-stu-id="2a669-114">MAPI Type</span></span>    | <span data-ttu-id="2a669-115">TSTRING</span><span class="sxs-lookup"><span data-stu-id="2a669-115">TSTRING</span></span>                                                                            |
| <span data-ttu-id="2a669-116">Type ADS</span><span class="sxs-lookup"><span data-stu-id="2a669-116">ADS Type</span></span>     | <span data-ttu-id="2a669-117">ADSTYPE \_ DN \_ avec \_ binaire</span><span class="sxs-lookup"><span data-stu-id="2a669-117">ADSTYPE\_DN\_WITH\_BINARY</span></span>                                                          |
| <span data-ttu-id="2a669-118">Type de variante</span><span class="sxs-lookup"><span data-stu-id="2a669-118">Variant Type</span></span> | <span data-ttu-id="2a669-119">\_distribution vt</span><span class="sxs-lookup"><span data-stu-id="2a669-119">VT\_DISPATCH</span></span>                                                                       |
| <span data-ttu-id="2a669-120">SDS, type</span><span class="sxs-lookup"><span data-stu-id="2a669-120">SDS Type</span></span>     | <span data-ttu-id="2a669-121">Objet COM pouvant être casté en [**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary).</span><span class="sxs-lookup"><span data-stu-id="2a669-121">A COM object that can be cast to an [**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary).</span></span> |



## <a name="remarks"></a><span data-ttu-id="2a669-122">Notes</span><span class="sxs-lookup"><span data-stu-id="2a669-122">Remarks</span></span>

<span data-ttu-id="2a669-123">Une valeur avec cette syntaxe a le format suivant :</span><span class="sxs-lookup"><span data-stu-id="2a669-123">A value with this syntax has the following format:</span></span>

``` syntax
B:<char count>:<binary value>:<object DN>
```

<span data-ttu-id="2a669-124">où « &lt; nombre &gt; de caractères » est le nombre de chiffres hexadécimaux dans « &lt; valeur binaire &gt; », « &lt; valeur binaire &gt; » est la représentation hexadécimale de la valeur binaire, et « &lt; objet DN &gt; » est un nom unique.</span><span class="sxs-lookup"><span data-stu-id="2a669-124">where "&lt;char count&gt;" is the number of hexadecimal digits in "&lt;binary value&gt;", "&lt;binary value&gt;" is the hexadecimal representation of the binary value, and "&lt;object DN&gt;" is a distinguished name.</span></span> <span data-ttu-id="2a669-125">Active Directory met automatiquement à jour le DN si l’objet auquel il fait référence est déplacé ou renommé.</span><span class="sxs-lookup"><span data-stu-id="2a669-125">Active Directory automatically updates the DN if the object that it refers to is moved or renamed.</span></span> <span data-ttu-id="2a669-126">Pour plus d’informations et pour obtenir un exemple de code qui utilise cette syntaxe, consultez [activation de la liaison avec renommage sécurisé avec la propriété otherWellKnownObjects](/windows/desktop/AD/enabling-rename-safe-binding-with-the-otherwellknownobjects-property).</span><span class="sxs-lookup"><span data-stu-id="2a669-126">For more information and a code example that uses this syntax, see [Enabling Rename-safe Binding with the otherWellKnownObjects Property](/windows/desktop/AD/enabling-rename-safe-binding-with-the-otherwellknownobjects-property).</span></span>

## <a name="see-also"></a><span data-ttu-id="2a669-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a669-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a669-128">**IADsDNWithBinary**</span><span class="sxs-lookup"><span data-stu-id="2a669-128">**IADsDNWithBinary**</span></span>](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary)
</dt> </dl>

 

 
