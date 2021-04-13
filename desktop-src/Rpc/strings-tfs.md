---
title: Chaînes (RPC)
description: Trois types de chaînes et appel de procédure distante (RPC).
ms.assetid: 186cabeb-ea3f-4213-ba71-53afe91e6e14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207e20b1c343ded17b5d62db2321bee380463f20
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316061"
---
# <a name="strings-rpc"></a><span data-ttu-id="a12c9-103">Chaînes (RPC)</span><span class="sxs-lookup"><span data-stu-id="a12c9-103">Strings (RPC)</span></span>

<span data-ttu-id="a12c9-104">Il existe trois types de chaînes dénotés par les sous-chaînes de fin suivantes dans le caractère de format.</span><span class="sxs-lookup"><span data-stu-id="a12c9-104">There are three strings types denoted by the following ending sub-strings in the format character.</span></span>



| <span data-ttu-id="a12c9-105">Type</span><span class="sxs-lookup"><span data-stu-id="a12c9-105">Type</span></span>                  | <span data-ttu-id="a12c9-106">Substring</span><span class="sxs-lookup"><span data-stu-id="a12c9-106">Substring</span></span> |
|-----------------------|-----------|
| <span data-ttu-id="a12c9-107">Chaîne de caractères</span><span class="sxs-lookup"><span data-stu-id="a12c9-107">Character string</span></span>      | <span data-ttu-id="a12c9-108">CSTRING</span><span class="sxs-lookup"><span data-stu-id="a12c9-108">CSTRING</span></span>   |
| <span data-ttu-id="a12c9-109">Chaîne de caractères larges</span><span class="sxs-lookup"><span data-stu-id="a12c9-109">Wide character string</span></span> | <span data-ttu-id="a12c9-110">WSTRING</span><span class="sxs-lookup"><span data-stu-id="a12c9-110">WSTRING</span></span>   |
| <span data-ttu-id="a12c9-111">Structure de chaîne pouvant être</span><span class="sxs-lookup"><span data-stu-id="a12c9-111">String-able structure</span></span> | <span data-ttu-id="a12c9-112">SSTRING</span><span class="sxs-lookup"><span data-stu-id="a12c9-112">SSTRING</span></span>   |



 

### <a name="nonconformant-strings"></a><span data-ttu-id="a12c9-113">Chaînes non conformes</span><span class="sxs-lookup"><span data-stu-id="a12c9-113">Nonconformant Strings</span></span>

<span data-ttu-id="a12c9-114">Un exemple de chaîne non conforme est une **\[ chaîne \]** sur un tableau de taille fixe.</span><span class="sxs-lookup"><span data-stu-id="a12c9-114">An example of nonconformant string is a **\[string\]** on a fixed-size array.</span></span>

``` syntax
FC_CSTRING | FC _WSTRING 
FC_PAD 
string_size<2>
```

### <a name="conformant-strings"></a><span data-ttu-id="a12c9-115">Chaînes conformes</span><span class="sxs-lookup"><span data-stu-id="a12c9-115">Conformant Strings</span></span>

``` syntax
FC_C_CSTRING | FC_C_WSTRING
FC_PAD 
```

<span data-ttu-id="a12c9-116">–ou–</span><span class="sxs-lookup"><span data-stu-id="a12c9-116">–or–</span></span>

``` syntax
FC_C_CSTRING | FC_C_WSTRING 
FC_STRING_SIZED 
conformance_description<> 
```

<span data-ttu-id="a12c9-117">Le premier format décrit les chaînes courantes, comme un argument de **\[ type \] chaîne** \* .</span><span class="sxs-lookup"><span data-stu-id="a12c9-117">The first format describes common strings, like a **\[string\]** char \* argument.</span></span> <span data-ttu-id="a12c9-118">Une chaîne conforme dimensionnée possède la dernière Description.</span><span class="sxs-lookup"><span data-stu-id="a12c9-118">A sized conformant string has the latter description.</span></span>

<span data-ttu-id="a12c9-119">La description de la conformité \_<> est un descripteur de corrélation et contient 4 ou 6 octets selon que [**/Robust**](/windows/desktop/Midl/-robust) est utilisé ou non.</span><span class="sxs-lookup"><span data-stu-id="a12c9-119">The conformance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

### <a name="structure-strings"></a><span data-ttu-id="a12c9-120">Chaînes de structure</span><span class="sxs-lookup"><span data-stu-id="a12c9-120">Structure Strings</span></span>

<span data-ttu-id="a12c9-121">Voici une structure de chaîne pouvant être non conforme :</span><span class="sxs-lookup"><span data-stu-id="a12c9-121">The following is a nonconformant string-able structure:</span></span>

``` syntax
FC_SSTRING 
element_size<1> 
number_of_elements<2>
```

<span data-ttu-id="a12c9-122">Structure pouvant être convertie en chaîne :</span><span class="sxs-lookup"><span data-stu-id="a12c9-122">Conformant string-able structure:</span></span>

``` syntax
FC_C_SSTRING 
element_size<1>
```

<span data-ttu-id="a12c9-123">ni</span><span class="sxs-lookup"><span data-stu-id="a12c9-123">–or –</span></span>

``` syntax
FC_C_SSTRING 
elements_size<1> 
FC_STRING_SIZED FC_PAD 
conformance_description<>
```

<span data-ttu-id="a12c9-124">Cette dernière Description est destinée à une structure de chaîne pouvant être dimensionnée.</span><span class="sxs-lookup"><span data-stu-id="a12c9-124">The latter description is for a sized string-able structure.</span></span>

 

 