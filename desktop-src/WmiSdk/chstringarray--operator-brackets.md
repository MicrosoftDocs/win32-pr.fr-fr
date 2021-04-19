---
description: Ces opérateurs d’indice définissent ou obtiennent l’élément à l’index spécifié. Ces opérateurs sont un substitut pratique des méthodes SetAt et GetAt.
ms.assetid: 93b10bef-908e-4c5e-aac3-b13051b2e7c9
ms.tgt_platform: multiple
title: 'CHStringArray :: Operator [] (ChStrArr. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92b30768b9d013bfca672548a7c58b0eeffb455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529389"
---
# <a name="chstringarrayoperator--"></a><span data-ttu-id="70f4e-104">CHStringArray ::, opérateur \[\]</span><span class="sxs-lookup"><span data-stu-id="70f4e-104">CHStringArray::operator \[ \]</span></span>

<span data-ttu-id="70f4e-105">\[La classe [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="70f4e-105">\[The [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="70f4e-106">Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]</span><span class="sxs-lookup"><span data-stu-id="70f4e-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="70f4e-107">Ces opérateurs d’indice définissent ou obtiennent l’élément à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="70f4e-107">These subscript operators set or get the element at the specified index.</span></span> <span data-ttu-id="70f4e-108">Ces opérateurs sont un substitut pratique des méthodes [**setat**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr)) et [**GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int)) .</span><span class="sxs-lookup"><span data-stu-id="70f4e-108">These operators are a convenient substitute for the [**SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr)) and [**GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int)) methods.</span></span>

``` syntax
CHString& operator []( 
  int nIndex
);

CHString operator []( 
  int nIndex
) const;
```

## <a name="parameters"></a><span data-ttu-id="70f4e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70f4e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70f4e-110"><span id="nIndex"></span><span id="nindex"></span><span id="NINDEX"></span>*nIndex*</span><span class="sxs-lookup"><span data-stu-id="70f4e-110"><span id="nIndex"></span><span id="nindex"></span><span id="NINDEX"></span>*nIndex*</span></span>
</dt> <dd>

<span data-ttu-id="70f4e-111">Un index d’entiers supérieur ou égal à zéro et inférieur ou égal à la valeur retournée par [ **GetUpperBound**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)</span><span class="sxs-lookup"><span data-stu-id="70f4e-111">An integer index that is greater than or equal to zero and less than or equal to the value returned by [**GetUpperBound**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="70f4e-112">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="70f4e-112">Return Values</span></span>

<span data-ttu-id="70f4e-113">Les opérateurs d’indice retournent l’élément pointeur [**CHString**](chstring.md) actuellement à cet index.</span><span class="sxs-lookup"><span data-stu-id="70f4e-113">The subscript operators return the [**CHString**](chstring.md) pointer element currently at this index.</span></span>

## <a name="remarks"></a><span data-ttu-id="70f4e-114">Notes</span><span class="sxs-lookup"><span data-stu-id="70f4e-114">Remarks</span></span>

<span data-ttu-id="70f4e-115">Vous pouvez utiliser le premier opérateur, qui appelle des tableaux qui ne sont pas **const**, sur le côté droit (r-value) ou sur le côté gauche (valeur l) d’une instruction d’assignation.</span><span class="sxs-lookup"><span data-stu-id="70f4e-115">You can use the first operator, which calls for arrays that are not **const**, on either the right (r-value) or the left (l-value) side of an assignment statement.</span></span> <span data-ttu-id="70f4e-116">Le deuxième, qui appelle pour les tableaux **const** , peut être utilisé uniquement à droite.</span><span class="sxs-lookup"><span data-stu-id="70f4e-116">The second, which calls for **const** arrays, can be used only on the right.</span></span>

<span data-ttu-id="70f4e-117">La version de débogage de la bibliothèque déclare si l’indice (à gauche ou à droite d’une instruction d’assignation) est hors limites.</span><span class="sxs-lookup"><span data-stu-id="70f4e-117">The debug version of the library asserts if the subscript (either on the left or right side of an assignment statement) is out of bounds.</span></span>

## <a name="examples"></a><span data-ttu-id="70f4e-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="70f4e-118">Examples</span></span>

<span data-ttu-id="70f4e-119">L’exemple de code suivant illustre l’utilisation de [**CHStringArray :: \[ \] Operator**](/previous-versions/windows/desktop/legacy/aa384934(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="70f4e-119">The following code example shows the use of [**CHStringArray::operator \[\]**](/previous-versions/windows/desktop/legacy/aa384934(v=vs.85)).</span></span>


```C++
CHStringArray array;
CHString s;

array.Add( L"String 1" ); // Element 0 
array.Add( L"String 2" ); // Element 1 
s = array[0]; // Get element 0
assert( s == L"String 1" ); 

array[0] = L"String 3"; // Replace element 0 
assert( array[0] == L"String 3" );
```



## <a name="requirements"></a><span data-ttu-id="70f4e-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70f4e-120">Requirements</span></span>



| <span data-ttu-id="70f4e-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70f4e-121">Requirement</span></span> | <span data-ttu-id="70f4e-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="70f4e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70f4e-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70f4e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="70f4e-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="70f4e-124">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="70f4e-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70f4e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="70f4e-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70f4e-126">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="70f4e-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="70f4e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="70f4e-128"><dt>ChStrArr. h (inclure FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="70f4e-128"><dt>ChStrArr.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="70f4e-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="70f4e-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="70f4e-130"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70f4e-130"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="70f4e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="70f4e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70f4e-132"><dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70f4e-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70f4e-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70f4e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70f4e-134">**CHStringArray :: Add**</span><span class="sxs-lookup"><span data-stu-id="70f4e-134">**CHStringArray::Add**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-add)
</dt> <dt>

<span data-ttu-id="70f4e-135">[**CHStringArray :: GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))</span><span class="sxs-lookup"><span data-stu-id="70f4e-135">[**CHStringArray::GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))</span></span>
</dt> <dt>

<span data-ttu-id="70f4e-136">[**CHStringArray :: SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="70f4e-136">[**CHStringArray::SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))</span></span>
</dt> </dl>

