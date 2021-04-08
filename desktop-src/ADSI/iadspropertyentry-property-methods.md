---
title: Méthodes de propriété IADsPropertyEntry (IADs. h)
description: Fournir l’accès aux propriétés suivantes.
ms.assetid: 73b0f6d4-55db-46cf-a781-e10bc4fcf2db
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsPropertyEntry ADSI
topic_type:
- apiref
api_name:
- IADsPropertyEntry Property Methods
- IADsPropertyEntry.Name
- IADsPropertyEntry.get_Name
- IADsPropertyEntry.put_Name
- IADsPropertyEntry.ADsType
- IADsPropertyEntry.get_ADsType
- IADsPropertyEntry.put_ADsType
- IADsPropertyEntry.ControlCode
- IADsPropertyEntry.get_ControlCode
- IADsPropertyEntry.put_ControlCode
- IADsPropertyEntry.Values
- IADsPropertyEntry.get_Values
- IADsPropertyEntry.put_Values
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e82344b2b659395bb14c0500fde3214530e000
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844293"
---
# <a name="iadspropertyentry-property-methods"></a><span data-ttu-id="64cde-104">Méthodes de propriété IADsPropertyEntry</span><span class="sxs-lookup"><span data-stu-id="64cde-104">IADsPropertyEntry Property Methods</span></span>

<span data-ttu-id="64cde-105">Les méthodes de propriété de l’interface [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) fournissent l’accès aux propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="64cde-105">The property methods of the [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) interface provide access to the following properties.</span></span> <span data-ttu-id="64cde-106">Pour plus d’informations sur les méthodes de propriété, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="64cde-106">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="64cde-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="64cde-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="64cde-108">**ADsType**</span><span class="sxs-lookup"><span data-stu-id="64cde-108">**ADsType**</span></span>
<span data-ttu-id="64cde-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="64cde-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="64cde-110">Type de données de la propriété **Name** .</span><span class="sxs-lookup"><span data-stu-id="64cde-110">The data type of the **Name** property.</span></span> <span data-ttu-id="64cde-111">Les valeurs du type de données sont définies dans l’énumération [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) .</span><span class="sxs-lookup"><span data-stu-id="64cde-111">The values of the data type is defined in the [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) enumeration.</span></span>

<dt>

<span data-ttu-id="64cde-112">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="64cde-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="64cde-113">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="64cde-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsType(
  [out] LONG* plADsType
);
HRESULT put_ADsType(
  [in] LONG lADsType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="64cde-114">**ControlCode**</span><span class="sxs-lookup"><span data-stu-id="64cde-114">**ControlCode**</span></span>
<span data-ttu-id="64cde-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="64cde-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="64cde-116">Constante qui spécifie l’opération à effectuer sur la propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="64cde-116">A constant that specifies the operation to be performed on the named property.</span></span> <span data-ttu-id="64cde-117">La valeur est définie dans l’énumération enum de l' [**\_ opération de propriété \_ \_ ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) .</span><span class="sxs-lookup"><span data-stu-id="64cde-117">The value is defined in the [**ADS\_PROPERTY\_OPERATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) enumeration.</span></span>

<dt>

<span data-ttu-id="64cde-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="64cde-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="64cde-119">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="64cde-119">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ControlCode(
  [out] LONG* pControlCode
);
HRESULT put_ControlCode(
  [in] LONG lnControlCode
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="64cde-120">**Nom**</span><span class="sxs-lookup"><span data-stu-id="64cde-120">**Name**</span></span>
<span data-ttu-id="64cde-121"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="64cde-121"></dt> <dd> <dl></span></span>

<span data-ttu-id="64cde-122">Nom de l’entrée de propriété.</span><span class="sxs-lookup"><span data-stu-id="64cde-122">Name of the property entry.</span></span> <span data-ttu-id="64cde-123">Ce nom doit correspondre au nom d’un attribut tel que défini dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="64cde-123">This name should correspond to the name of an attribute as defined in the schema.</span></span>

<dt>

<span data-ttu-id="64cde-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="64cde-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="64cde-125">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="64cde-125">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] BSTR* pbstrName
);
HRESULT put_Name(
  [in] BSTR bstrName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="64cde-126">**Valeurs**</span><span class="sxs-lookup"><span data-stu-id="64cde-126">**Values**</span></span>
<span data-ttu-id="64cde-127"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="64cde-127"></dt> <dd> <dl></span></span>

<span data-ttu-id="64cde-128">Tableau de **variants** .</span><span class="sxs-lookup"><span data-stu-id="64cde-128">A **VARIANT** array.</span></span> <span data-ttu-id="64cde-129">Chaque élément de ce tableau représente une valeur de la propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="64cde-129">Each element in this array represents a value of the named property.</span></span> <span data-ttu-id="64cde-130">Ces valeurs de propriété sont représentées par les objets ADSI qui implémentent les interfaces [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) et [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) .</span><span class="sxs-lookup"><span data-stu-id="64cde-130">Such property values are represented by ADSI objects implementing the [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) and [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) interfaces.</span></span> <span data-ttu-id="64cde-131">Par conséquent, le tableau **Variant** contient un tableau de pointeurs vers l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) sur les objets ADSI qui implémentent les interfaces **IADsPropertyValue** et **IADsPropertyValue2** .</span><span class="sxs-lookup"><span data-stu-id="64cde-131">Therefore, the **VARIANT** array holds an array of pointers to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface on the ADSI objects implementing the **IADsPropertyValue** and **IADsPropertyValue2** interfaces.</span></span>

<dt>

<span data-ttu-id="64cde-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="64cde-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="64cde-133">Type de données de script : **variante**</span><span class="sxs-lookup"><span data-stu-id="64cde-133">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Values(
  [out] VARIANT* pvValues
);
HRESULT put_Values(
  [in] VARIANT vValues
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="64cde-134">Notes</span><span class="sxs-lookup"><span data-stu-id="64cde-134">Remarks</span></span>

<span data-ttu-id="64cde-135">Chaque méthode de propriété prend en charge les valeurs de retour **HRESULT** standard, y compris les valeurs \_ OK.</span><span class="sxs-lookup"><span data-stu-id="64cde-135">Each property method supports the standard **HRESULT** return values, including S\_OK.</span></span> <span data-ttu-id="64cde-136">Pour plus d’informations sur les autres valeurs de retour, consultez [codes d’erreur ADSI](adsi-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="64cde-136">For more information about other return values, see [ADSI Error Codes](adsi-error-codes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="64cde-137">Exemples</span><span class="sxs-lookup"><span data-stu-id="64cde-137">Examples</span></span>

<span data-ttu-id="64cde-138">L’exemple de code suivant montre comment récupérer une propriété nommée à partir du cache et comment créer une nouvelle entrée de propriété.</span><span class="sxs-lookup"><span data-stu-id="64cde-138">The following code example shows how to retrieve a named property from the cache and create a new property entry.</span></span>


```VB
 
Dim propList As IADsPropertyList
Dim propEntry As IADsPropertyEntry
Dim propVal As IADsPropertyValue

On Error GoTo Cleanup

'------------------------------------------------------------
'----- Getting IADsPropertyEntry ----------------------------
'------------------------------------------------------------
 
' Create the property list object.
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
propList.GetInfo
 
' Get a named property entry object.
Set propEntry = propList.GetPropertyItem("dc", ADSTYPE_CASE_IGNORE_STRING)

' Insert code to do something with propEntry
Set propEntry = Nothing
 
'------------------------------------------------------------
'---- Setting IADsPropertyEntry -----------------------------
'------------------------------------------------------------
 
' Create a property value object.
Set propVal = New PropertyValue
 
'---- Property Value -----
propVal.CaseIgnoreString = "Fabrikam, Inc - Seattle, WA"
propVal.ADsType = ADSTYPE_CASE_IGNORE_STRING
 
'---- Create a new Property Entry ----
Set propEntry = New PropertyEntry
propEntry.Name = "adminDescription"
propEntry.Values = Array(propVal)
propEntry.ControlCode = ADS_PROPERTY_UPDATE
propEntry.ADsType = ADS_CASE_IGNORE_STRING
 
' ---- Put the newly created property entry to the cache ----
propList.PutPropertyItem (propEntry)
 
' Commit the entry to the directory store.
propList.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set propList = Nothing
    Set propEntry = Nothing
    Set propVal = Nothing
```



<span data-ttu-id="64cde-139">L’exemple de code suivant montre comment obtenir une propriété nommée à partir d’un cache.</span><span class="sxs-lookup"><span data-stu-id="64cde-139">The following code example shows how to get a named property from a cache.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
IADsPropertyList *pList = NULL;
IADsPropertyEntry *pEntry = NULL;
IADs *pObj = NULL;
VARIANT var;
long valType = ADSTYPE_CASE_IGNORE_STRING;
 
VariantInit(&var);
 
// Bind to directory object.
HRESULT hr = ADsGetObject(L"LDAP://dc01/DC=Fabrikam,DC=com",
                          IID_IADsPropertyList,
                          (void**)&pList);
if(FAILED(hr)){return;}
 
// Initialize the property cache.
hr = pList->QueryInterface(IID_IADs,(void**)&pObj);
if(FAILED(hr)){goto Cleanup;}
pObj->GetInfo();
pObj->Release();
 
// Get a property entry.
hr = pList->GetPropertyItem(CComBSTR("description"), valType, &var);
pList->Release();
if(FAILED(hr)){goto Cleanup;}
hr = V_DISPATCH(&var)->QueryInterface(IID_IADsPropertyEntry,
                                      (void**)&pEntry);
VariantClear(&var);
if(FAILED(hr)){goto Cleanup;}
 
// Get the name and the type of the property entry.
BSTR nm = NULL;
hr = pEntry->get_Name(&nm);
printf("Property name = %S\n",nm);
VariantClear(&var);
long at;
hr = pEntry->get_ADsType(&at);
printf("Property type = %d\n",a);

Cleanup:
    if(nm)
        SysFreeString(nm);

    if(pList)
        pList->Release();

    if(pEntry)
        pEntry->Release();

    if(pObj)
        pObj->Release();

    VariantClear(&var);
```



## <a name="requirements"></a><span data-ttu-id="64cde-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64cde-140">Requirements</span></span>



| <span data-ttu-id="64cde-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64cde-141">Requirement</span></span> | <span data-ttu-id="64cde-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="64cde-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64cde-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64cde-143">Minimum supported client</span></span><br/> | <span data-ttu-id="64cde-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64cde-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="64cde-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64cde-145">Minimum supported server</span></span><br/> | <span data-ttu-id="64cde-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64cde-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="64cde-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="64cde-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="64cde-148"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="64cde-148"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="64cde-149">DLL</span><span class="sxs-lookup"><span data-stu-id="64cde-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64cde-150"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64cde-150"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="64cde-151">IID</span><span class="sxs-lookup"><span data-stu-id="64cde-151">IID</span></span><br/>                      | <span data-ttu-id="64cde-152">IID \_ IADsPropertyEntry est défini en tant que 05792C8E-941F-11D0-8529-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="64cde-152">IID\_IADsPropertyEntry is defined as 05792C8E-941F-11D0-8529-00C04FD8D503</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="64cde-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64cde-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64cde-154">**ENUM de l' \_ opération de propriété ADS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="64cde-154">**ADS\_PROPERTY\_OPERATION\_ENUM**</span></span>](/windows/win32/api/iads/ne-iads-ads_property_operation_enum)
</dt> <dt>

[<span data-ttu-id="64cde-155">Codes d’erreur ADSI</span><span class="sxs-lookup"><span data-stu-id="64cde-155">ADSI Error Codes</span></span>](adsi-error-codes.md)
</dt> <dt>

[<span data-ttu-id="64cde-156">**ADSTYPEENUM**</span><span class="sxs-lookup"><span data-stu-id="64cde-156">**ADSTYPEENUM**</span></span>](/windows/win32/api/iads/ne-iads-adstypeenum)
</dt> <dt>

[<span data-ttu-id="64cde-157">**IADsPropertyEntry**</span><span class="sxs-lookup"><span data-stu-id="64cde-157">**IADsPropertyEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)
</dt> <dt>

[<span data-ttu-id="64cde-158">**IADsPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="64cde-158">**IADsPropertyValue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)
</dt> <dt>

[<span data-ttu-id="64cde-159">**IADsPropertyValue2**</span><span class="sxs-lookup"><span data-stu-id="64cde-159">**IADsPropertyValue2**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)
</dt> <dt>

[<span data-ttu-id="64cde-160">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="64cde-160">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> </dl>

 

