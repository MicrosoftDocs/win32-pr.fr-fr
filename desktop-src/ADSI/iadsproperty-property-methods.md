---
title: Méthodes de propriété IADsProperty (IADs. h)
description: Lisez et écrivez les propriétés décrites dans le tableau suivant.
ms.assetid: dd348a3c-0386-4fa2-984d-cdea6f09bd72
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsProperty ADSI
topic_type:
- apiref
api_name:
- IADsProperty Property Methods
- IADsProperty.OID
- IADsProperty.get_OID
- IADsProperty.put_OID
- IADsProperty.Syntax
- IADsProperty.get_Syntax
- IADsProperty.put_Syntax
- IADsProperty.MaxRange
- IADsProperty.get_MaxRange
- IADsProperty.put_MaxRange
- IADsProperty.MinRange
- IADsProperty.get_MinRange
- IADsProperty.put_MinRange
- IADsProperty.MultiValued
- IADsProperty.get_MultiValued
- IADsProperty.put_MultiValued
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 233bd5411e1c82956ef745255418a1b176af5900
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512144"
---
# <a name="iadsproperty-property-methods"></a><span data-ttu-id="87b12-104">Méthodes de propriété IADsProperty</span><span class="sxs-lookup"><span data-stu-id="87b12-104">IADsProperty Property Methods</span></span>

<span data-ttu-id="87b12-105">Les méthodes de propriété de l’interface [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) lisent et écrivent les propriétés décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="87b12-105">The property methods of the [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) interface read and write the properties described in the following table.</span></span> <span data-ttu-id="87b12-106">Pour plus d’informations sur les méthodes de propriété, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="87b12-106">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="87b12-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="87b12-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="87b12-108">**MaxRange**</span><span class="sxs-lookup"><span data-stu-id="87b12-108">**MaxRange**</span></span>
<span data-ttu-id="87b12-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="87b12-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="87b12-110">Limite supérieure des valeurs.</span><span class="sxs-lookup"><span data-stu-id="87b12-110">Upper limit of values.</span></span>

<dt>

<span data-ttu-id="87b12-111">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="87b12-111">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="87b12-112">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="87b12-112">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxRange(
  [out] LONG* lnMaxRange
);
HRESULT put_MaxRange(
  [in] LONG lnMaxRange
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="87b12-113">**MinRange**</span><span class="sxs-lookup"><span data-stu-id="87b12-113">**MinRange**</span></span>
<span data-ttu-id="87b12-114"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="87b12-114"></dt> <dd> <dl></span></span>

<span data-ttu-id="87b12-115">Limite inférieure des valeurs.</span><span class="sxs-lookup"><span data-stu-id="87b12-115">Lower limit of values.</span></span>

<dt>

<span data-ttu-id="87b12-116">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="87b12-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="87b12-117">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="87b12-117">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MinRange(
  [out] LONG* lnMinRange
);
HRESULT put_MinRange(
  [in] LONG lnMinRange
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="87b12-118">**À valeurs multiples**</span><span class="sxs-lookup"><span data-stu-id="87b12-118">**MultiValued**</span></span>
<span data-ttu-id="87b12-119"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="87b12-119"></dt> <dd> <dl></span></span>

<span data-ttu-id="87b12-120">Indique si la propriété prend en charge des valeurs uniques ou multiples.</span><span class="sxs-lookup"><span data-stu-id="87b12-120">Whether property supports single or multiple values.</span></span>

<dt>

<span data-ttu-id="87b12-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="87b12-121">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="87b12-122">Type de données de script : **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="87b12-122">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MultiValued(
  [out] VARIANT_BOOL* fMultivalued
);
HRESULT put_MultiValued(
  [in] VARIANT_BOOL fMultivalued
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="87b12-123">**OID**</span><span class="sxs-lookup"><span data-stu-id="87b12-123">**OID**</span></span>
<span data-ttu-id="87b12-124"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="87b12-124"></dt> <dd> <dl></span></span>

<span data-ttu-id="87b12-125">Identificateur d’objet spécifique au répertoire.</span><span class="sxs-lookup"><span data-stu-id="87b12-125">Directory-specific object identifier.</span></span>

<dt>

<span data-ttu-id="87b12-126">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="87b12-126">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="87b12-127">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="87b12-127">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OID(
  [out] BSTR* bstrOID
);
HRESULT put_OID(
  [out] BSTR* bstrOID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="87b12-128">**Syntaxe**</span><span class="sxs-lookup"><span data-stu-id="87b12-128">**Syntax**</span></span>
<span data-ttu-id="87b12-129"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="87b12-129"></dt> <dd> <dl></span></span>

<span data-ttu-id="87b12-130">Chemin d’accès relatif de l’objet de syntaxe.</span><span class="sxs-lookup"><span data-stu-id="87b12-130">Relative path of syntax object.</span></span>

<dt>

<span data-ttu-id="87b12-131">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="87b12-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="87b12-132">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="87b12-132">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Syntax(
  [out] BSTR* bstrSyntax
);
HRESULT put_Syntax(
  [in] BSTR* bstrSyntax
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="87b12-133">Exemples</span><span class="sxs-lookup"><span data-stu-id="87b12-133">Examples</span></span>

<span data-ttu-id="87b12-134">L’exemple de code suivant examine l’attribut **OperatingSystem** d’un ordinateur sur un réseau par le biais du fournisseur Winnt.</span><span class="sxs-lookup"><span data-stu-id="87b12-134">The following code example examines the **OperatingSystem** attribute of a computer on a network through the WinNT provider.</span></span>


```VB
Dim obj As IADs
Dim cl As IADsClass
Dim pr As IADsProperty
Dim sc As IADsContainer

On Error GoTo Cleanup
 
Set obj = GetObject("WinNT://myMachine,computer")
Set cl = GetObject(obj.Schema)
Set sc = GetObject(cl.Parent)
Set pr = sc.GetObject("Property","OperatingSystem")
 
MsgBox "Attribute:  " & pr.Name
MsgBox "Syntax:     " & pr.Syntax
MsgBox "MaxRange:   " & pr.MaxRange
MsgBox "MinRange:   " & pr.MinRange
MsgBox "Multivalued:" & pr.Multivalued

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set obj = Nothing
    Set cl = Nothing
    Set pr = Nothing
    Set sc = Nothing
```



<span data-ttu-id="87b12-135">L’exemple de code suivant examine l’attribut **OperatingSystem** d’un ordinateur sur un réseau par le biais du fournisseur Winnt.</span><span class="sxs-lookup"><span data-stu-id="87b12-135">The following code example examines the **OperatingSystem** attribute of a computer on a network through the WinNT provider.</span></span> <span data-ttu-id="87b12-136">Par souci de concision, la vérification des erreurs est omise.</span><span class="sxs-lookup"><span data-stu-id="87b12-136">For brevity, error checking is omitted.</span></span>


```C++
IADs *pADs = NULL;
IADsClass *pCls = NULL;
IADsProperty* pProp = NULL;
IADsContainer *pCont = NULL;
long lval;
short bval;
HRESULT hr = CoInitialize(NULL);
 
hr = ADsGetObject(L"WinNT://myMachine,computer",
                  IID_IADs, (void**)&pADs);
if(FAILED(hr))
    goto Cleanup;

BSTR bstr;
hr = pADs->get_Schema(&bstr);
if(FAILED(hr))
    goto Cleanup;

hr = ADsGetObject(bstr, IID_IADsClass, (void**)&pCls);
hr = pCls->get_Parent(&bstr);
if(FAILED(hr))
    goto Cleanup;

hr = ADsGetObject(bstr, IID_IADsContainer, (void**)&pCont);
if(FAILED(hr))
    goto Cleanup;
SysFreeString(bstr);

hr = pCont->GetObject(CComBSTR("Property"), CComBSTR("OperatingSystem"), (IDispatch**)&pProp);
if(FAILED(hr))
    goto Cleanup;

hr = pProp->get_Name(&bstr);
if(FAILED(hr))
    goto Cleanup;
printf(" Name : %S\n",bstr);
SysFreeString(bstr);

hr = pProp->get_Syntax(&bstr);
if(FAILED(hr))
    goto Cleanup;
printf(" Syntax : %S\n",bstr);
SysFreeString(bstr);

hr = pProp->get_MaxRange(&lval);
if(FAILED(hr))
    goto Cleanup;
printf(" MaxRange : %d\n",lval);
SysFreeString(bstr);

hr = pProp->get_MinRange(&lval);
if(FAILED(hr))
    goto Cleanup;
printf(" MinRange : %d\n", lval);
SysFreeString(bstr);

hr = pProp->get_Multivalued(&bval);
if(FAILED(hr))
    goto Cleanup;
printf(" MultiValued : %b\n",bval);
SysFreeString(bstr);

Cleanup:
    if(pADs)
        pADs->Release();

    if(pCls)
        pCls->Release();

    if(pCont)
        pCont->Release();

    if(pProp)
        pProp->Release(); 
 
CoUninitialize();
```



## <a name="requirements"></a><span data-ttu-id="87b12-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87b12-137">Requirements</span></span>



| <span data-ttu-id="87b12-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87b12-138">Requirement</span></span> | <span data-ttu-id="87b12-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="87b12-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87b12-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87b12-140">Minimum supported client</span></span><br/> | <span data-ttu-id="87b12-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87b12-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="87b12-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87b12-142">Minimum supported server</span></span><br/> | <span data-ttu-id="87b12-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87b12-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="87b12-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="87b12-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="87b12-145"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="87b12-145"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="87b12-146">DLL</span><span class="sxs-lookup"><span data-stu-id="87b12-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87b12-147"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87b12-147"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="87b12-148">IID</span><span class="sxs-lookup"><span data-stu-id="87b12-148">IID</span></span><br/>                      | <span data-ttu-id="87b12-149">IID \_ IADsProperty est défini en tant que C8F93DD3-4AE0-11CF-9E73-00AA004A5691</span><span class="sxs-lookup"><span data-stu-id="87b12-149">IID\_IADsProperty is defined as C8F93DD3-4AE0-11CF-9E73-00AA004A5691</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="87b12-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87b12-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87b12-151">**IADsClass**</span><span class="sxs-lookup"><span data-stu-id="87b12-151">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="87b12-152">**IADsProperty**</span><span class="sxs-lookup"><span data-stu-id="87b12-152">**IADsProperty**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsproperty)
</dt> <dt>

[<span data-ttu-id="87b12-153">**IADsSyntax**</span><span class="sxs-lookup"><span data-stu-id="87b12-153">**IADsSyntax**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssyntax)
</dt> </dl>

 

 





