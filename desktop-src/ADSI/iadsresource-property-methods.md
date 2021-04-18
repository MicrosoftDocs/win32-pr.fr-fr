---
title: Méthodes de propriété IADsResource (IADs. h)
description: Les méthodes de propriété de l’interface IADsResource obtiennent ou définissent les propriétés décrites dans le tableau suivant. Pour une discussion générale sur les méthodes de propriété, consultez Méthodes de propriété d’interface.
ms.assetid: a2d6ed76-88e9-468f-928a-a038b73fb362
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsResource ADSI
topic_type:
- apiref
api_name:
- IADsResource Property Methods
- IADsResource.LockCount
- IADsResource.get_LockCount
- IADsResource.Path
- IADsResource.get_Path
- IADsResource.User
- IADsResource.get_User
- IADsResource.UserPath
- IADsResource.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0f2ab2642dd8d03062a26d096190cf7615977a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511941"
---
# <a name="iadsresource-property-methods"></a><span data-ttu-id="28aea-105">Méthodes de propriété IADsResource</span><span class="sxs-lookup"><span data-stu-id="28aea-105">IADsResource Property Methods</span></span>

<span data-ttu-id="28aea-106">Les méthodes de propriété de l’interface [**IADsResource**](/windows/desktop/api/Iads/nn-iads-iadsresource) obtiennent ou définissent les propriétés décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="28aea-106">The property methods of the [**IADsResource**](/windows/desktop/api/Iads/nn-iads-iadsresource) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="28aea-107">Pour une discussion générale sur les méthodes de propriété, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="28aea-107">For a general discussion of property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="28aea-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="28aea-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="28aea-109">**LockCount**</span><span class="sxs-lookup"><span data-stu-id="28aea-109">**LockCount**</span></span>
<span data-ttu-id="28aea-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="28aea-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="28aea-111">Nombre de verrous sur la ressource.</span><span class="sxs-lookup"><span data-stu-id="28aea-111">Number of locks on the resource.</span></span>

<dt>

<span data-ttu-id="28aea-112">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="28aea-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28aea-113">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="28aea-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LockCount(
  [out] LONG* plLockCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="28aea-114">**Chemin d’accès**</span><span class="sxs-lookup"><span data-stu-id="28aea-114">**Path**</span></span>
<span data-ttu-id="28aea-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="28aea-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="28aea-116">Chemin d’accès du système de fichiers de la ressource ouverte.</span><span class="sxs-lookup"><span data-stu-id="28aea-116">The file system path of the opened resource.</span></span>

<dt>

<span data-ttu-id="28aea-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="28aea-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28aea-118">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="28aea-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="28aea-119">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="28aea-119">**User**</span></span>
<span data-ttu-id="28aea-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="28aea-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="28aea-121">Nom de l’utilisateur qui a ouvert la ressource.</span><span class="sxs-lookup"><span data-stu-id="28aea-121">The name of the user who opened the resource.</span></span>

<dt>

<span data-ttu-id="28aea-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="28aea-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28aea-123">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="28aea-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="28aea-124">**UserPath**</span><span class="sxs-lookup"><span data-stu-id="28aea-124">**UserPath**</span></span>
<span data-ttu-id="28aea-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="28aea-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="28aea-126">ADsPath de l’objet utilisateur pour l’utilisateur qui a ouvert la ressource.</span><span class="sxs-lookup"><span data-stu-id="28aea-126">The ADsPath of the user object for the user who opened the resource.</span></span>

<dt>

<span data-ttu-id="28aea-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="28aea-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28aea-128">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="28aea-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="28aea-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="28aea-129">Examples</span></span>

<span data-ttu-id="28aea-130">L’exemple de code suivant montre comment examiner les ressources ouvertes d’un service de fichiers.</span><span class="sxs-lookup"><span data-stu-id="28aea-130">The following code example shows how to examine open resources of a file service.</span></span>


```VB
Dim fso As IADsFileServiceOperations
' Bind to a file service operations object on "myComputer" in the local domain.
Set fso = GetObject("WinNT://myComputer/LanmanServer")

' Enumerate resources.
If (IsEmpty(fso) = False) Then
    For Each resource In fso.resources
        MsgBox "Resource name: " & resource.name
        MsgBox "Resource path: " & resource.path
    Next resource
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fso = Nothing
```



<span data-ttu-id="28aea-131">L’exemple de code suivant énumère une collection de ressources.</span><span class="sxs-lookup"><span data-stu-id="28aea-131">The following code example enumerates a collection of resources.</span></span>


```C++
IADsFileServiceOperations *pFso = NULL;
IADsResource *pRes = NULL;
IADsCollection *pColl = NULL;
IUnknown *pUnk = NULL;
IEnumVARIANT *pEnum = NULL;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
HRESULT hr = S_OK;

LPWSTR adsPath =L"WinNT://aMachine/LanmanServer";
hr = ADsGetObject(adsPath, IID_IADsFileServiceOperations,(void**)&pFso);
if(FAILED(hr)) {goto Cleanup;}

hr = pFso->Resources(&pColl);
if(FAILED(hr)) {goto Cleanup;}


// Enumerate print jobs. Code omitted.
hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)) {goto Cleanup;}

hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)) {goto Cleanup;}

// Enumerate.
VariantInit(&var);
hr = pEnum->Next(1, &var, &lFetch);
while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsResource, (void**)&pRes);
        pRes->get_Name(&bstr);
        printf("Resource name: %S\n",bstr);
        SysFreeString(bstr);
        pRes->get_Path(&bstr);
        printf("Resource path: %S\n",bstr);
        SysFreeString(bstr);
        pRes->Release();
    }
    pDisp->Release();
    VariantClear(&var);
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pRes) pRes->Release();
    if(pDisp) pDisp->Release();
    if(pEnum) pEnum->Release();
    if(pUnk) pUnk->Release();
    if(pColl) pColl->Release();
    if(pFso) pFso->Release();
```



## <a name="requirements"></a><span data-ttu-id="28aea-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28aea-132">Requirements</span></span>



| <span data-ttu-id="28aea-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28aea-133">Requirement</span></span> | <span data-ttu-id="28aea-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="28aea-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28aea-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28aea-135">Minimum supported client</span></span><br/> | <span data-ttu-id="28aea-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="28aea-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="28aea-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28aea-137">Minimum supported server</span></span><br/> | <span data-ttu-id="28aea-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28aea-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="28aea-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="28aea-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="28aea-140"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="28aea-140"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="28aea-141">DLL</span><span class="sxs-lookup"><span data-stu-id="28aea-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28aea-142"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28aea-142"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="28aea-143">IID</span><span class="sxs-lookup"><span data-stu-id="28aea-143">IID</span></span><br/>                      | <span data-ttu-id="28aea-144">IID \_ IADsResource est défini en tant que 34A05B20-4AAB-11CF-AE2C-00AA006EBFB9</span><span class="sxs-lookup"><span data-stu-id="28aea-144">IID\_IADsResource is defined as 34A05B20-4AAB-11CF-AE2C-00AA006EBFB9</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="28aea-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28aea-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28aea-146">**IADsResource**</span><span class="sxs-lookup"><span data-stu-id="28aea-146">**IADsResource**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsresource)
</dt> <dt>

[<span data-ttu-id="28aea-147">**IADsFileServiceOperations :: Resources**</span><span class="sxs-lookup"><span data-stu-id="28aea-147">**IADsFileServiceOperations::Resources**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsfileserviceoperations-resources)
</dt> </dl>

 

 





