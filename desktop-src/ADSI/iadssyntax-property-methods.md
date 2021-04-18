---
title: Méthodes de propriété IADsSyntax (IADs. h)
description: Les méthodes de propriété de l’interface IADsSyntax obtiennent ou définissent les propriétés énumérées dans le tableau suivant. Pour plus d’informations sur les méthodes de propriété, consultez Méthodes de propriété d’interface.
ms.assetid: a216a55d-63eb-4fdf-a67f-8d4b5eb74262
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsSyntax ADSI
topic_type:
- apiref
api_name:
- IADsSyntax Property Methods
- IADsSyntax.OleAutoDataType
- IADsSyntax.get_OleAutoDataType
- IADsSyntax.put_OleAutoDataType
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a41c84efb4f48171913156823e18a301236290
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508494"
---
# <a name="iadssyntax-property-methods"></a><span data-ttu-id="4ac07-105">Méthodes de propriété IADsSyntax</span><span class="sxs-lookup"><span data-stu-id="4ac07-105">IADsSyntax Property Methods</span></span>

<span data-ttu-id="4ac07-106">Les méthodes de propriété de l’interface [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) obtiennent ou définissent les propriétés énumérées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4ac07-106">The property methods of the [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) interface get or set the properties listed in the following table.</span></span> <span data-ttu-id="4ac07-107">Pour plus d’informations sur les méthodes de propriété, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="4ac07-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="4ac07-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4ac07-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="4ac07-109">**OleAutoDataType**</span><span class="sxs-lookup"><span data-stu-id="4ac07-109">**OleAutoDataType**</span></span>
<span data-ttu-id="4ac07-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4ac07-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="4ac07-111">Récupère et définit une valeur de type **long** qui contient la valeur de la constante **VT \_ xxx** pour le type de données Automation représentant cette syntaxe.</span><span class="sxs-lookup"><span data-stu-id="4ac07-111">Retrieves and sets a **LONG** that contains the value of the **VT\_xxx** constant for the Automation data type that represents this syntax.</span></span>

<span data-ttu-id="4ac07-112">Active Directory prend en charge les constantes **VT \_ xxx** suivantes pour le type de données Automation représentant la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4ac07-112">Active Directory supports the following **VT\_xxx** constants for the Automation data type that represents this syntax:</span></span>

-   <span data-ttu-id="4ac07-113">**VT \_ BOOL** bool</span><span class="sxs-lookup"><span data-stu-id="4ac07-113">**VT\_BOOL** BOOL</span></span>
-   <span data-ttu-id="4ac07-114">**VT \_ BSTR BSTR**</span><span class="sxs-lookup"><span data-stu-id="4ac07-114">**VT\_BSTR** BSTR</span></span>
-   <span data-ttu-id="4ac07-115">**VT \_ BSTRT** BSTRT</span><span class="sxs-lookup"><span data-stu-id="4ac07-115">**VT\_BSTRT** BSTRT</span></span>
-   <span data-ttu-id="4ac07-116">**VT \_ devise CY**</span><span class="sxs-lookup"><span data-stu-id="4ac07-116">**VT\_CY** CURRENCY</span></span>
-   <span data-ttu-id="4ac07-117">**VT \_ Date Date**</span><span class="sxs-lookup"><span data-stu-id="4ac07-117">**VT\_DATE** Date</span></span>
-   <span data-ttu-id="4ac07-118">**VT \_** **null** vide</span><span class="sxs-lookup"><span data-stu-id="4ac07-118">**VT\_EMPTY** **NULL**</span></span>
-   <span data-ttu-id="4ac07-119">**VT \_ ERREUR** non valide</span><span class="sxs-lookup"><span data-stu-id="4ac07-119">**VT\_ERROR** Not valid</span></span>
-   <span data-ttu-id="4ac07-120">**VT \_ I2** petit</span><span class="sxs-lookup"><span data-stu-id="4ac07-120">**VT\_I2** short</span></span>
-   <span data-ttu-id="4ac07-121">**VT \_ I4** long</span><span class="sxs-lookup"><span data-stu-id="4ac07-121">**VT\_I4** long</span></span>
-   <span data-ttu-id="4ac07-122">**VT \_ R4** réel</span><span class="sxs-lookup"><span data-stu-id="4ac07-122">**VT\_R4** real</span></span>
-   <span data-ttu-id="4ac07-123">**VT \_ R8** double</span><span class="sxs-lookup"><span data-stu-id="4ac07-123">**VT\_R8** double</span></span>
-   <span data-ttu-id="4ac07-124">**VT \_ Octet UI1**</span><span class="sxs-lookup"><span data-stu-id="4ac07-124">**VT\_UI1** BYTE</span></span>

<dt>

<span data-ttu-id="4ac07-125">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4ac07-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4ac07-126">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="4ac07-126">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OleAutoDataType(
  [out] LONG* plAutoDataType
);
HRESULT put_OleAutoDataType(
  [in] LONG lAutoDataType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="4ac07-127">Notes</span><span class="sxs-lookup"><span data-stu-id="4ac07-127">Remarks</span></span>

<span data-ttu-id="4ac07-128">Un tableau d’octets non signés, le tableau VT **\_ UI1** VT \| **\_** peut signifier que le fournisseur a mappé une syntaxe qui ne peut pas être mappée à un type virtuel Automation.</span><span class="sxs-lookup"><span data-stu-id="4ac07-128">An array of unsigned bytes, **VT\_UI1**\|**VT\_ARRAY** could mean that the provider has mapped a syntax that cannot be mapped to an Automation virtual type.</span></span>

## <a name="examples"></a><span data-ttu-id="4ac07-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="4ac07-129">Examples</span></span>

<span data-ttu-id="4ac07-130">L’exemple de code suivant examine la syntaxe de l’attribut **operatingSystemVersion renvoyée** d’un ordinateur sur un réseau par le biais du fournisseur Winnt.</span><span class="sxs-lookup"><span data-stu-id="4ac07-130">The following code example examines the syntax of the **OperatingSystemVersion** attribute of a computer on a network through the WinNT provider.</span></span> <span data-ttu-id="4ac07-131">La syntaxe de résultat est une chaîne.</span><span class="sxs-lookup"><span data-stu-id="4ac07-131">The result syntax is a string.</span></span>


```VB
Dim obj As IADs
Dim cl As IADsClass
Dim pr As IADsProperty
Dim sy As IADsSyntax
Dim sc As IADsContainer
On Error GoTo Cleanup

Set obj = GetObject("WinNT://myMachine,computer")
Set cl = GetObject(obj.Schema)
Set sc = GetObject(cl.Parent)
Set pr = sc.GetObject("Property","OperatingSystemVersion")
Set sy = GetObject(sc.ADsPath & "/" & pr.Syntax)
 
MsgBox "Automation data types: " & sy.OleAutoDataType

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set obj = Nothing
    Set cl = Nothing
    Set pr = Nothing
    Set sy = Nothing
    Set sc = Nothing
```



<span data-ttu-id="4ac07-132">L’exemple de code suivant examine la syntaxe de l’attribut **operatingSystemVersion renvoyée** d’un ordinateur sur un réseau par le biais du fournisseur Winnt.</span><span class="sxs-lookup"><span data-stu-id="4ac07-132">The following code example examines the syntax of the **OperatingSystemVersion** attribute of a computer on a network through the WinNT provider.</span></span> <span data-ttu-id="4ac07-133">La syntaxe de résultat est une chaîne.</span><span class="sxs-lookup"><span data-stu-id="4ac07-133">The result syntax is a string.</span></span> <span data-ttu-id="4ac07-134">Par souci de concision, la vérification des erreurs est omise.</span><span class="sxs-lookup"><span data-stu-id="4ac07-134">For brevity, error checking is omitted.</span></span>


```C++
#include <stdio.h>
#include <activeds.h>
#include <atlbase.h>
 
IADs *pObj = NULL;
IADsClass *pCls = NULL;
IADsProperty *pProp = NULL;
IADsSyntax *pSyn = NULL;
IADsContainer *pCont = NULL;
 
HRESULT hr = ADsGetObject(L"WinNT://myMachine,computer",
                          IID_IADs,
                          (void**)&pObj);
if(FAILED(hr)){goto Cleanup;}
VARIANT var;
VariantInit(&var);
CComBSTR sbstr;
 
pObj->get_Schema(&sbstr);
printf("Object schema: %S\n",sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsClass,(void**)&pCls);
if(FAILED(hr)){goto Cleanup;}

pCls->get_Parent(&sbstr);
printf("Object class's container:  %S\n", sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsContainer, (void**)&pCont);
if(FAILED(hr)){goto Cleanup;}
pCont->QueryInterface(IID_IADs,(void**)&pObj);
pObj->get_ADsPath(&sbstr);
printf("Container's AdsPath:  %S\n",sbstr);
 
IDispatch *pDisp;
hr = pCont->GetObject(CComBSTR("Property"),
                      CComBSTR("OperatingSystemVersion"),
                      (IDispatch**)&pDisp);
if(FAILED(hr)){goto Cleanup;}
 
hr = pDisp->QueryInterface(IID_IADsProperty, (void**)&pProp);
if(FAILED(hr)){goto Cleanup;}
 
hr = pProp->get_Syntax(&sbstr);
if(FAILED(hr)){goto Cleanup;}
printf("Property Syntax:  %S\n",sbstr);
 
printf("ADsPath of the syntax object %S\n",sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsSyntax, (void**)&pSyn);
if(FAILED(hr)){goto Cleanup;}

long lType;
pSyn->get_OleAutoDataType(&lType);
printf("Property syntax's OleAutoDataType: %d\n", lType);

Cleanup:
    if(pObj)
        pObj->Release();

    if(pProp)
        pProp->Release();

    if(pCls)
        pCls->Release();

    if(pSyn)
        pSyn->Release();

    if(pCont)
        pCont->Release();
```



## <a name="requirements"></a><span data-ttu-id="4ac07-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ac07-135">Requirements</span></span>



| <span data-ttu-id="4ac07-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ac07-136">Requirement</span></span> | <span data-ttu-id="4ac07-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ac07-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ac07-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ac07-138">Minimum supported client</span></span><br/> | <span data-ttu-id="4ac07-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ac07-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4ac07-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ac07-140">Minimum supported server</span></span><br/> | <span data-ttu-id="4ac07-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ac07-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4ac07-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="4ac07-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ac07-143"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ac07-143"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="4ac07-144">DLL</span><span class="sxs-lookup"><span data-stu-id="4ac07-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ac07-145"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ac07-145"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="4ac07-146">IID</span><span class="sxs-lookup"><span data-stu-id="4ac07-146">IID</span></span><br/>                      | <span data-ttu-id="4ac07-147">IID \_ IADsSyntax est défini en tant que C8F93DD2-4AE0-11CF-9E73-00AA004A5691</span><span class="sxs-lookup"><span data-stu-id="4ac07-147">IID\_IADsSyntax is defined as C8F93DD2-4AE0-11CF-9E73-00AA004A5691</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="4ac07-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ac07-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ac07-149">**IADsClass**</span><span class="sxs-lookup"><span data-stu-id="4ac07-149">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="4ac07-150">**IADsProperty**</span><span class="sxs-lookup"><span data-stu-id="4ac07-150">**IADsProperty**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsproperty)
</dt> <dt>

[<span data-ttu-id="4ac07-151">**IADsSyntax**</span><span class="sxs-lookup"><span data-stu-id="4ac07-151">**IADsSyntax**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssyntax)
</dt> </dl>

 

 





