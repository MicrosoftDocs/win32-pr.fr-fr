---
description: L’opérateur de concaténation + = joint les caractères à la fin de cette chaîne. L’opérateur accepte un autre objet CHString, un pointeur de caractère ou un caractère unique.
ms.assetid: 026ff9af-4cda-4261-aa27-e215d49b80ce
ms.tgt_platform: multiple
title: 'CHString :: Operator + = (ChString. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683ca6b6264169cd156e89c3447c63fa59f03585
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538685"
---
# <a name="chstringoperator"></a><span data-ttu-id="e882d-104">CHString :: Operator + =</span><span class="sxs-lookup"><span data-stu-id="e882d-104">CHString::operator+=</span></span>

<span data-ttu-id="e882d-105">\[La classe [**CHString**](chstring.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="e882d-105">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="e882d-106">Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]</span><span class="sxs-lookup"><span data-stu-id="e882d-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="e882d-107">L’opérateur de concaténation + = joint les caractères à la fin de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="e882d-107">The += concatenation operator joins characters to the end of this string.</span></span> <span data-ttu-id="e882d-108">L’opérateur accepte un autre objet [**CHString**](chstring.md) , un pointeur de caractère ou un caractère unique.</span><span class="sxs-lookup"><span data-stu-id="e882d-108">The operator accepts another [**CHString**](chstring.md) object, a character pointer, or a single character.</span></span>

``` syntax
const CHString& operator +=(
  const CHString& string )
throw( CHeap_Exception );

const CHString& operator +=(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator +=(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString operator +=(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a><span data-ttu-id="e882d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e882d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e882d-110"><span id="string"></span><span id="STRING"></span>*chaîne*</span><span class="sxs-lookup"><span data-stu-id="e882d-110"><span id="string"></span><span id="STRING"></span>*string*</span></span>
</dt> <dd>

<span data-ttu-id="e882d-111">Chaîne [**CHString**](chstring.md) qui effectue la concaténation à cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="e882d-111">A [**CHString**](chstring.md) string that concatenates to this string.</span></span>

</dd> <dt>

<span data-ttu-id="e882d-112"><span id="ch"></span><span id="CH"></span>*cascade*</span><span class="sxs-lookup"><span data-stu-id="e882d-112"><span id="ch"></span><span id="CH"></span>*ch*</span></span>
</dt> <dd>

<span data-ttu-id="e882d-113">Caractère à concaténer à cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="e882d-113">A character to concatenate to this string.</span></span>

</dd> <dt>

<span data-ttu-id="e882d-114"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span><span class="sxs-lookup"><span data-stu-id="e882d-114"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span></span>
</dt> <dd>

<span data-ttu-id="e882d-115">Pointeur vers une chaîne se terminant par un caractère **null** à concaténer à cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="e882d-115">Pointer to a **NULL**-terminated string to concatenate to this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e882d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e882d-116">Remarks</span></span>

<span data-ttu-id="e882d-117">Sachez que les exceptions de mémoire peuvent se produire chaque fois que vous utilisez cet opérateur de concaténation, car un nouveau stockage peut être alloué pour les caractères ajoutés à cet objet [**CHString**](chstring.md) .</span><span class="sxs-lookup"><span data-stu-id="e882d-117">Be aware that memory exceptions can occur whenever you use this concatenation operator because new storage may be allocated for characters added to this [**CHString**](chstring.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="e882d-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="e882d-118">Examples</span></span>

<span data-ttu-id="e882d-119">L’exemple suivant illustre l’utilisation de **CHString :: Operator + =**:</span><span class="sxs-lookup"><span data-stu-id="e882d-119">The following example shows the use of **CHString::operator +=**:</span></span>


```C++
CHString s( L"abc" );
assert( ( s += L"def" ) == L"abcdef" );
```



## <a name="requirements"></a><span data-ttu-id="e882d-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e882d-120">Requirements</span></span>



| <span data-ttu-id="e882d-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e882d-121">Requirement</span></span> | <span data-ttu-id="e882d-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e882d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e882d-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e882d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e882d-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e882d-124">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="e882d-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e882d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e882d-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e882d-126">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="e882d-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="e882d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e882d-128"><dt>ChString. h (inclure FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e882d-128"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e882d-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e882d-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="e882d-130"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e882d-130"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="e882d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e882d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e882d-132"><dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e882d-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e882d-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e882d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e882d-134">**CHString**</span><span class="sxs-lookup"><span data-stu-id="e882d-134">**CHString**</span></span>](chstring.md)
</dt> </dl>

 

