---
title: Méthodes de propriété IADsSession (IADs. h)
description: Les méthodes de propriété de l’interface IADsSession obtiennent ou définissent les propriétés décrites dans le tableau suivant. Pour plus d’informations et pour obtenir une discussion générale sur les méthodes de propriété, consultez Méthodes de propriété d’interface.
ms.assetid: b2366da7-c51c-4279-8931-2000d3110d72
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsSession ADSI
topic_type:
- apiref
api_name:
- IADsSession Property Methods
- IADsSession.Computer
- IADsSession.get_Computer
- IADsSession.ComputerPath
- IADsSession.get_ComputerPath
- IADsSession.ConnectTime
- IADsSession.get_ConnectTime
- IADsSession.IdleTime
- IADsSession.get_IdleTime
- IADsSession.User
- IADsSession.get_User
- IADsSession.UserPath
- IADsSession.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf7dd9abe25d731ba63385cd8d632c4212ea349
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843441"
---
# <a name="iadssession-property-methods"></a><span data-ttu-id="279ec-105">Méthodes de propriété IADsSession</span><span class="sxs-lookup"><span data-stu-id="279ec-105">IADsSession Property Methods</span></span>

<span data-ttu-id="279ec-106">Les méthodes de propriété de l’interface [**IADsSession**](/windows/desktop/api/Iads/nn-iads-iadssession) obtiennent ou définissent les propriétés décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="279ec-106">The property methods of the [**IADsSession**](/windows/desktop/api/Iads/nn-iads-iadssession) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="279ec-107">Pour plus d’informations et pour obtenir une discussion générale sur les méthodes de propriété, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="279ec-107">For more information and a general discussion about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="279ec-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="279ec-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="279ec-109">**Ordinateur**</span><span class="sxs-lookup"><span data-stu-id="279ec-109">**Computer**</span></span>
<span data-ttu-id="279ec-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="279ec-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="279ec-111">Nom de la station de travail cliente.</span><span class="sxs-lookup"><span data-stu-id="279ec-111">Name of the client workstation.</span></span>

<dt>

<span data-ttu-id="279ec-112">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="279ec-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="279ec-113">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="279ec-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Computer(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="279ec-114">**ComputerPath**</span><span class="sxs-lookup"><span data-stu-id="279ec-114">**ComputerPath**</span></span>
<span data-ttu-id="279ec-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="279ec-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="279ec-116">ADsPath de l’objet ordinateur pour la station de travail cliente.</span><span class="sxs-lookup"><span data-stu-id="279ec-116">ADsPath of the computer object for the client workstation.</span></span>

<dt>

<span data-ttu-id="279ec-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="279ec-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="279ec-118">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="279ec-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerPath(
  [out] BSTR* pbstrComputerPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="279ec-119">**ConnectTime**</span><span class="sxs-lookup"><span data-stu-id="279ec-119">**ConnectTime**</span></span>
<span data-ttu-id="279ec-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="279ec-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="279ec-121">Temps écoulé, en secondes, depuis le début de la session.</span><span class="sxs-lookup"><span data-stu-id="279ec-121">Elapsed time, in seconds, since the session started.</span></span>

<dt>

<span data-ttu-id="279ec-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="279ec-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="279ec-123">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="279ec-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ConnectTime(
  [out] LONG* plConnectTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="279ec-124">**IdleTime**</span><span class="sxs-lookup"><span data-stu-id="279ec-124">**IdleTime**</span></span>
<span data-ttu-id="279ec-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="279ec-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="279ec-126">Durée d’inactivité, en secondes, de la session.</span><span class="sxs-lookup"><span data-stu-id="279ec-126">Idle time, in seconds, of the session.</span></span>

<dt>

<span data-ttu-id="279ec-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="279ec-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="279ec-128">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="279ec-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IdleTime(
  [out] LONG* plIdleTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="279ec-129">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="279ec-129">**User**</span></span>
<span data-ttu-id="279ec-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="279ec-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="279ec-131">Nom de l’utilisateur de la session.</span><span class="sxs-lookup"><span data-stu-id="279ec-131">The name of the user of the session.</span></span>

<dt>

<span data-ttu-id="279ec-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="279ec-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="279ec-133">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="279ec-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="279ec-134">**UserPath**</span><span class="sxs-lookup"><span data-stu-id="279ec-134">**UserPath**</span></span>
<span data-ttu-id="279ec-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="279ec-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="279ec-136">ADsPath de l’objet utilisateur pour l’utilisateur de cette session.</span><span class="sxs-lookup"><span data-stu-id="279ec-136">The ADsPath of the user object for the user of this session.</span></span>

<dt>

<span data-ttu-id="279ec-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="279ec-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="279ec-138">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="279ec-138">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="279ec-139">Exemples</span><span class="sxs-lookup"><span data-stu-id="279ec-139">Examples</span></span>

<span data-ttu-id="279ec-140">L’exemple de code suivant montre comment examiner des sessions pour un service de fichiers.</span><span class="sxs-lookup"><span data-stu-id="279ec-140">The following code example shows how to examine sessions for a file service.</span></span>


```VB
Dim fso As IADsFileServiceOperations
On Error GoTo Cleanup

' Bind to a file service operations object on "myComputer" in the local domain.
Set fso = GetObject("WinNT://myComputer/LanmanServer")

' Enumerate sessions.
If (IsEmpty(fso) = False) Then
    For Each session In fso.sessions
        MsgBox "Session Computer: " & session.Computer
        MsgBox "Session User: " & session.User
    Next Session
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fso = Nothing
```



<span data-ttu-id="279ec-141">L’exemple de code suivant énumère une collection de sessions.</span><span class="sxs-lookup"><span data-stu-id="279ec-141">The following code example enumerates a collection of sessions.</span></span>


```C++
IADsFileServiceOperations *pFso = NULL;
IADsSession *pSes = NULL;
IADsCollection *pColl = NULL;
HRESULT hr = S_OK;
IUnknown *pUnk = NULL;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
IEnumVARIANT *pEnum = NULL;

VariantInit(&var);

LPWSTR adsPath = L"WinNT://aMachine/LanmanServer";

hr = ADsGetObject(adsPath,IID_IADsFileServiceOperations,
                  (void**)&pFso);

if(FAILED(hr)) {goto Cleanup;}

hr = pFso->Sessions(&pColl);

// Enumerate sessions. 
hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)) {goto Cleanup;}

hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)) {goto Cleanup;}

// Enumerate.
hr = pEnum->Next(1, &var, &lFetch);
while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsSession, (void**)&pSes);
        pSes->get_Computer(&bstr);
        printf("Session host: %S\n",bstr);
        SysFreeString(bstr);

        pSes->get_User(&bstr);
        printf("Session user: %S\n",bstr);
        SysFreeString(bstr);

        pRes->Release();
    }

    VariantClear(&var);
    pDisp=NULL;
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pFso) pFso->Release();
    if(pColl) pColl->Release();
    if(pUnk) pUnk->Release();
    if(pEnum) pEnum->Release();
```



## <a name="requirements"></a><span data-ttu-id="279ec-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="279ec-142">Requirements</span></span>



| <span data-ttu-id="279ec-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="279ec-143">Requirement</span></span> | <span data-ttu-id="279ec-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="279ec-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="279ec-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="279ec-145">Minimum supported client</span></span><br/> | <span data-ttu-id="279ec-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="279ec-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="279ec-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="279ec-147">Minimum supported server</span></span><br/> | <span data-ttu-id="279ec-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="279ec-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="279ec-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="279ec-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="279ec-150"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="279ec-150"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="279ec-151">DLL</span><span class="sxs-lookup"><span data-stu-id="279ec-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="279ec-152"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="279ec-152"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="279ec-153">IID</span><span class="sxs-lookup"><span data-stu-id="279ec-153">IID</span></span><br/>                      | <span data-ttu-id="279ec-154">IID \_ IADsSession est défini en tant que 398B7DA0-4AAB-11CF-AE2C-00AA006EBFB9</span><span class="sxs-lookup"><span data-stu-id="279ec-154">IID\_IADsSession is defined as 398B7DA0-4AAB-11CF-AE2C-00AA006EBFB9</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="279ec-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="279ec-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="279ec-156">**IADsFileServiceOperations :: sessions**</span><span class="sxs-lookup"><span data-stu-id="279ec-156">**IADsFileServiceOperations::Sessions**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsfileserviceoperations-sessions)
</dt> <dt>

[<span data-ttu-id="279ec-157">**IADsSession**</span><span class="sxs-lookup"><span data-stu-id="279ec-157">**IADsSession**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssession)
</dt> </dl>

 

 





