---
description: L’opérateur de concaténation + joint deux chaînes et retourne un objet CHString.
ms.assetid: b7ed6379-ccfa-40f9-9607-d9033179b674
ms.tgt_platform: multiple
title: 'CHString :: Operator + (ChString. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5053a4d3059a66cb2c8e4a89a3bdd531d5f42de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758218"
---
# <a name="chstringoperator"></a><span data-ttu-id="21239-103">CHString :: Operator +</span><span class="sxs-lookup"><span data-stu-id="21239-103">CHString::operator+</span></span>

<span data-ttu-id="21239-104">\[La classe [**CHString**](chstring.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="21239-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="21239-105">Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]</span><span class="sxs-lookup"><span data-stu-id="21239-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="21239-106">L’opérateur de concaténation + joint deux chaînes et retourne un objet [**CHString**](chstring.md) .</span><span class="sxs-lookup"><span data-stu-id="21239-106">The + concatenation operator joins two strings and returns a [**CHString**](chstring.md) object.</span></span>

``` syntax
friend CHString operator +(
  const CHString& str1,
  const CHString& str2 )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  WCHAR ch )
throw( CHeap_Exception );

friend CHString operator +(
  WCHAR ch,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  LPCWSTR lpsz )
throw( CHeap_Exception );

friend CHString operator +(
  LPCWSTR lpsz,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  char ch )
throw( CHeap_Exception );

friend CHString operator +(
  char ch,
  const CHString& str )
throw( CHeap_Exception );
```

## <a name="parameters"></a><span data-ttu-id="21239-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="21239-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21239-108"><span id="str__str1__str2"></span><span id="STR__STR1__STR2"></span>*Str, str1, str2*</span><span class="sxs-lookup"><span data-stu-id="21239-108"><span id="str__str1__str2"></span><span id="STR__STR1__STR2"></span>*str, str1, str2*</span></span>
</dt> <dd>

<span data-ttu-id="21239-109">Chaînes [**CHString**](chstring.md) concaténées.</span><span class="sxs-lookup"><span data-stu-id="21239-109">[**CHString**](chstring.md) strings that are concatenated.</span></span>

</dd> <dt>

<span data-ttu-id="21239-110"><span id="ch"></span><span id="CH"></span>*cascade*</span><span class="sxs-lookup"><span data-stu-id="21239-110"><span id="ch"></span><span id="CH"></span>*ch*</span></span>
</dt> <dd>

<span data-ttu-id="21239-111">Caractère qui effectue une concaténation en une chaîne ou une chaîne concaténée à un caractère.</span><span class="sxs-lookup"><span data-stu-id="21239-111">A character that concatenates to a string or a string that concatenates to a character.</span></span>

</dd> <dt>

<span data-ttu-id="21239-112"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span><span class="sxs-lookup"><span data-stu-id="21239-112"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span></span>
</dt> <dd>

<span data-ttu-id="21239-113">Pointeur vers une chaîne de caractères se terminant par **null**.</span><span class="sxs-lookup"><span data-stu-id="21239-113">Pointer to a **NULL**-terminated character string.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="21239-114">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="21239-114">Return Values</span></span>

<span data-ttu-id="21239-115">Cet opérateur de concaténation retourne un objet [**CHString**](chstring.md) qui est le résultat temporaire de la concaténation.</span><span class="sxs-lookup"><span data-stu-id="21239-115">This concatenation operator returns a [**CHString**](chstring.md) object that is the temporary result of the concatenation.</span></span> <span data-ttu-id="21239-116">Cette valeur de retour permet de combiner plusieurs concaténations dans la même expression.</span><span class="sxs-lookup"><span data-stu-id="21239-116">This return value makes it possible to combine several concatenations in the same expression.</span></span>

## <a name="remarks"></a><span data-ttu-id="21239-117">Notes</span><span class="sxs-lookup"><span data-stu-id="21239-117">Remarks</span></span>

<span data-ttu-id="21239-118">L’une des deux chaînes d’arguments doit être un objet [**CHString**](chstring.md) ; l’autre peut être un pointeur de caractère ou un caractère.</span><span class="sxs-lookup"><span data-stu-id="21239-118">One of the two argument strings must be a [**CHString**](chstring.md) object; the other can be a character pointer or a character.</span></span> <span data-ttu-id="21239-119">Sachez que les exceptions de mémoire peuvent se produire chaque fois que vous utilisez l’opérateur de concaténation, car un nouveau stockage peut être alloué pour contenir des données temporaires.</span><span class="sxs-lookup"><span data-stu-id="21239-119">Be aware that memory exceptions can occur whenever you use the concatenation operator because new storage may be allocated to hold temporary data.</span></span>

## <a name="examples"></a><span data-ttu-id="21239-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="21239-120">Examples</span></span>

<span data-ttu-id="21239-121">L’exemple de code suivant illustre l’utilisation de **CHString :: Operator +**:</span><span class="sxs-lookup"><span data-stu-id="21239-121">The following code example shows the use of **CHString::operator +**:</span></span>


```C++
CHString s1( L"abc" );
CHString s2( L"def" );
assert( (s1 + s2 ) == L"abcdef" );

CHString s3;
s3 = CHString( L"abc" ) + "def" ; // Correct
s3 = "abc" + "def"; // Wrong. The first argument must be a CHString.
```



## <a name="requirements"></a><span data-ttu-id="21239-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21239-122">Requirements</span></span>



| <span data-ttu-id="21239-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21239-123">Requirement</span></span> | <span data-ttu-id="21239-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="21239-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21239-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21239-125">Minimum supported client</span></span><br/> | <span data-ttu-id="21239-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21239-126">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="21239-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21239-127">Minimum supported server</span></span><br/> | <span data-ttu-id="21239-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21239-128">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="21239-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="21239-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="21239-130"><dt>ChString. h (inclure FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21239-130"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="21239-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="21239-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="21239-132"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21239-132"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="21239-133">DLL</span><span class="sxs-lookup"><span data-stu-id="21239-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21239-134"><dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21239-134"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21239-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21239-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21239-136">**CHString**</span><span class="sxs-lookup"><span data-stu-id="21239-136">**CHString**</span></span>](chstring.md)
</dt> </dl>

 

