---
title: Méthodes de propriété IADsMembers (IADs. h)
description: Les méthodes de l’interface IADsMembers lisent et écrivent les propriétés décrites dans cette rubrique. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: ed4e98e5-053c-4d3b-bcd0-3add96bbe120
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsMembers ADSI
topic_type:
- apiref
api_name:
- IADsMembers Property Methods
- IADsMembers.Count
- IADsMembers.get_Count
- IADsMembers.Filter
- IADsMembers.get_Filter
- IADsMembers.put_Filter
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af047d6fe52fdd7d808b1d7e5dbfb35303d3ff59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509545"
---
# <a name="iadsmembers-property-methods"></a><span data-ttu-id="059a9-105">Méthodes de propriété IADsMembers</span><span class="sxs-lookup"><span data-stu-id="059a9-105">IADsMembers Property Methods</span></span>

<span data-ttu-id="059a9-106">Les méthodes de l’interface [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) lisent et écrivent les propriétés décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="059a9-106">The methods of the [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) interface read and write the properties described in this topic.</span></span> <span data-ttu-id="059a9-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="059a9-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="059a9-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="059a9-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="059a9-109">**Count**</span><span class="sxs-lookup"><span data-stu-id="059a9-109">**Count**</span></span>
<span data-ttu-id="059a9-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="059a9-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="059a9-111">Indique le nombre d’éléments dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="059a9-111">Indicates the number of items in the container.</span></span> <span data-ttu-id="059a9-112">Si le filtre est défini, Count retourne uniquement le nombre d’éléments qui correspondent à la description du filtre.</span><span class="sxs-lookup"><span data-stu-id="059a9-112">If the filter is set then count returns only the number of items that fit the filter description.</span></span>

<dt>

<span data-ttu-id="059a9-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="059a9-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="059a9-114">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="059a9-114">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* plCountr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="059a9-115">**Filter**</span><span class="sxs-lookup"><span data-stu-id="059a9-115">**Filter**</span></span>
<span data-ttu-id="059a9-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="059a9-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="059a9-117">Indique le filtre.</span><span class="sxs-lookup"><span data-stu-id="059a9-117">Indicates the filter.</span></span> <span data-ttu-id="059a9-118">La syntaxe des entrées dans le tableau de filtres est identique à celle du filtre utilisé sur l’interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="059a9-118">The syntax of the entries in the filter array is the same as the Filter used on the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface.</span></span>

<dt>

<span data-ttu-id="059a9-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="059a9-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="059a9-120">Type de données de script : **variante**</span><span class="sxs-lookup"><span data-stu-id="059a9-120">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Filter(
  [out] VARIANT* pvFilter
);
HRESULT put_Filter(
  [in] VARIANT vFilter
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="059a9-121">Notes</span><span class="sxs-lookup"><span data-stu-id="059a9-121">Remarks</span></span>

<span data-ttu-id="059a9-122">Les fournisseurs système ADSI ne prennent pas en charge la méthode de propriété **IADsMembers :: obten \_ Count** .</span><span class="sxs-lookup"><span data-stu-id="059a9-122">The ADSI system providers do not support the **IADsMembers::get\_Count** property method.</span></span>

## <a name="examples"></a><span data-ttu-id="059a9-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="059a9-123">Examples</span></span>

<span data-ttu-id="059a9-124">L’exemple de code suivant montre comment utiliser les méthodes de propriété de cette interface.</span><span class="sxs-lookup"><span data-stu-id="059a9-124">The following code example shows how to use the property methods of this interface.</span></span>


```VB
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://myComputer/someGroup")
grp.members.filter = Array("user")
For Each usr In grp.Members
    MsgBox usr.Name & "," & usr.Class & "," & usr.AdsPath
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```



<span data-ttu-id="059a9-125">L’exemple de code suivant utilise la méthode de **\_ filtre IADsMembers ::p ut** pour préparer une énumération de la collection de membres d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="059a9-125">The following code example uses the **IADsMembers::put\_Filter** method to prepare for an enumeration of the collection of members of a group.</span></span>


```C++
IADsGroup *pGroup;
HRESULT hr = S_OK;

LPWSTR grpPath = L"WinNT://myComputer/someGroup";
hr = ADsGetObject(grpPath,IID_IADsGroup,(void**)&pGroup);
if(FAILED(hr)){goto Cleanup;}

IADsMembers *pMembers;
hr = pGroup->Members(&pMembers);
if(FAILED(hr)){goto Cleanup;}

hr = pGroup->Release();

SAFEARRAY *sa = CreateSafeArray(L"user");
hr = pMembers->put_Filter(sa);
if(FAILED(hr)){goto Cleanup;}

hr = EnumMembers(pMembers);    // For more information, and a 
                               // code example, see 
                               // IADsMembers::get__NewEnum.
if(FAILED(hr)){goto Cleanup;}

Cleanup:
    if(pGroup) pGroup->Release();
    if(pMembers) pMembers->Release();
    return hr;
```



## <a name="requirements"></a><span data-ttu-id="059a9-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="059a9-126">Requirements</span></span>



| <span data-ttu-id="059a9-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="059a9-127">Requirement</span></span> | <span data-ttu-id="059a9-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="059a9-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="059a9-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="059a9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="059a9-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="059a9-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="059a9-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="059a9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="059a9-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="059a9-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="059a9-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="059a9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="059a9-134"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="059a9-134"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="059a9-135">DLL</span><span class="sxs-lookup"><span data-stu-id="059a9-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="059a9-136"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="059a9-136"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="059a9-137">IID</span><span class="sxs-lookup"><span data-stu-id="059a9-137">IID</span></span><br/>                      | <span data-ttu-id="059a9-138">IID \_ IADsMembers est défini en tant que 451A0030-72EC-11CF-B03B-00AA006E0975</span><span class="sxs-lookup"><span data-stu-id="059a9-138">IID\_IADsMembers is defined as 451A0030-72EC-11CF-B03B-00AA006E0975</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="059a9-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="059a9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="059a9-140">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="059a9-140">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[<span data-ttu-id="059a9-141">**IADsMembers :: obtient la \_ \_ NewEnum**</span><span class="sxs-lookup"><span data-stu-id="059a9-141">**IADsMembers::get\_\_NewEnum**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsmembers-get__newenum)
</dt> <dt>

[<span data-ttu-id="059a9-142">**IADsMembers**</span><span class="sxs-lookup"><span data-stu-id="059a9-142">**IADsMembers**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsmembers)
</dt> <dt>

[<span data-ttu-id="059a9-143">Méthodes de propriété d’interface</span><span class="sxs-lookup"><span data-stu-id="059a9-143">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





