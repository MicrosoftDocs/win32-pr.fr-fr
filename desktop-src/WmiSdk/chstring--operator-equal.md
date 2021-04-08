---
description: L’opérateur d’assignation CHString (=) réinitialise un objet CHString existant avec de nouvelles données.
ms.assetid: 6864aacf-ac18-4b5a-be3e-3a0d8bb31e74
ms.tgt_platform: multiple
title: 'CHString :: Operator = (ChString. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9abfa9ea2b72aa8f6830d9fb6388861c8c3b82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034620"
---
# <a name="chstringoperator"></a><span data-ttu-id="b9da4-103">CHString :: Operator =</span><span class="sxs-lookup"><span data-stu-id="b9da4-103">CHString::operator=</span></span>

<span data-ttu-id="b9da4-104">\[La classe [**CHString**](chstring.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="b9da4-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="b9da4-105">Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]</span><span class="sxs-lookup"><span data-stu-id="b9da4-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="b9da4-106">L’opérateur d’assignation [**CHString**](chstring.md) (=) réinitialise un objet CHString existant avec de nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="b9da4-106">The [**CHString**](chstring.md) assignment (=) operator reinitializes an existing CHString object with new data.</span></span>

``` syntax
const CHString& operator =(
  const CHString& stringSrc )
throw( CHeap_Exception );

const CHString& operator =(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator =(
  const unsigned char* psz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  CHString *p )
throw( CHeap_Exception );

const CHString& operator =(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a><span data-ttu-id="b9da4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9da4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9da4-108"><span id="stringSrc__p"></span><span id="stringsrc__p"></span><span id="STRINGSRC__P"></span>*stringSrc*, *p*</span><span class="sxs-lookup"><span data-stu-id="b9da4-108"><span id="stringSrc__p"></span><span id="stringsrc__p"></span><span id="STRINGSRC__P"></span>*stringSrc*, *p*</span></span>
</dt> <dd>

<span data-ttu-id="b9da4-109">Assigne une chaîne [**CHString**](chstring.md) à cet objet.</span><span class="sxs-lookup"><span data-stu-id="b9da4-109">Assigns a [**CHString**](chstring.md) string to this object.</span></span>

</dd> <dt>

<span data-ttu-id="b9da4-110"><span id="ch"></span><span id="CH"></span>*cascade*</span><span class="sxs-lookup"><span data-stu-id="b9da4-110"><span id="ch"></span><span id="CH"></span>*ch*</span></span>
</dt> <dd>

<span data-ttu-id="b9da4-111">Assigne un caractère à cet objet.</span><span class="sxs-lookup"><span data-stu-id="b9da4-111">Assigns a character to this object.</span></span>

</dd> <dt>

<span data-ttu-id="b9da4-112"><span id="lpsz__psz"></span><span id="LPSZ__PSZ"></span>*lpsz*, *PSZ*</span><span class="sxs-lookup"><span data-stu-id="b9da4-112"><span id="lpsz__psz"></span><span id="LPSZ__PSZ"></span>*lpsz*, *psz*</span></span>
</dt> <dd>

<span data-ttu-id="b9da4-113">Assigne une chaîne terminée par le caractère **null** à cet objet.</span><span class="sxs-lookup"><span data-stu-id="b9da4-113">Assigns a **NULL**-terminated string to this object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9da4-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b9da4-114">Remarks</span></span>

<span data-ttu-id="b9da4-115">Si la chaîne de destination (autrement dit, le côté gauche) est déjà suffisamment grande pour stocker les nouvelles données, aucune nouvelle allocation de mémoire n’est effectuée.</span><span class="sxs-lookup"><span data-stu-id="b9da4-115">If the destination string (that is, the left side) is already large enough to store the new data, no new memory allocation is performed.</span></span> <span data-ttu-id="b9da4-116">Toutefois, des exceptions de mémoire peuvent se produire chaque fois que vous utilisez l’opérateur d’assignation, car un nouveau stockage est souvent alloué pour contenir l’objet [**CHString**](chstring.md) résultant.</span><span class="sxs-lookup"><span data-stu-id="b9da4-116">However, memory exceptions can occur whenever you use the assignment operator because new storage is often allocated to hold the resulting [**CHString**](chstring.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="b9da4-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="b9da4-117">Examples</span></span>

<span data-ttu-id="b9da4-118">L’exemple de code suivant illustre l’utilisation de **CHString :: Operator =**:</span><span class="sxs-lookup"><span data-stu-id="b9da4-118">The following code example shows the use of **CHString::operator =**:</span></span>


```C++
CHString s1, s2;        // Empty CHString objects

s1 = L"cat";            // s1 = "cat"
s2 = s1;                // s1 and s2 each = "cat"
s1 = L"the " + s1;      // Or expressions
s1 = 'x';               // Or just individual characters
```



## <a name="requirements"></a><span data-ttu-id="b9da4-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9da4-119">Requirements</span></span>



| <span data-ttu-id="b9da4-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9da4-120">Requirement</span></span> | <span data-ttu-id="b9da4-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9da4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9da4-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9da4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b9da4-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9da4-123">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="b9da4-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9da4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b9da4-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9da4-125">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="b9da4-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="b9da4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9da4-127"><dt>ChString. h (inclure FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b9da4-127"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b9da4-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b9da4-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="b9da4-129"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9da4-129"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="b9da4-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b9da4-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9da4-131"><dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9da4-131"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9da4-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9da4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9da4-133">**CHString**</span><span class="sxs-lookup"><span data-stu-id="b9da4-133">**CHString**</span></span>](chstring.md)
</dt> </dl>

 

