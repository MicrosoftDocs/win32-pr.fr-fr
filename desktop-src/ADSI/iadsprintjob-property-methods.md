---
title: Méthodes de propriété IADsPrintJob (IADs. h)
description: Les méthodes de propriété pour l’interface IADsPrintJob obtiennent ou définissent les propriétés décrites dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: 23e7cbf3-09ce-44ce-b618-2c0fa6b34428
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsPrintJob ADSI
topic_type:
- apiref
api_name:
- IADsPrintJob Property Methods
- IADsPrintJob.Description
- IADsPrintJob.get_Description
- IADsPrintJob.put_Description
- IADsPrintJob.HostPrintQueue
- IADsPrintJob.get_HostPrintQueue
- IADsPrintJob.Notify
- IADsPrintJob.get_Notify
- IADsPrintJob.put_Notify
- IADsPrintJob.NotifyPath
- IADsPrintJob.get_NotifyPath
- IADsPrintJob.put_NotifyPath
- IADsPrintJob.Priority
- IADsPrintJob.get_Priority
- IADsPrintJob.put_Priority
- IADsPrintJob.Size
- IADsPrintJob.get_Size
- IADsPrintJob.StartTime
- IADsPrintJob.get_StartTime
- IADsPrintJob.put_StartTime
- IADsPrintJob.TimeSubmitted
- IADsPrintJob.get_TimeSubmitted
- IADsPrintJob.TotalPages
- IADsPrintJob.get_TotalPages
- IADsPrintJob.UntilTime
- IADsPrintJob.get_UntilTime
- IADsPrintJob.User
- IADsPrintJob.get_User
- IADsPrintJob.UserPath
- IADsPrintJob.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d1680484ff16d563ef5bc89de6d5abbfec2ce6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466243"
---
# <a name="iadsprintjob-property-methods"></a><span data-ttu-id="4f5d6-105">Méthodes de propriété IADsPrintJob</span><span class="sxs-lookup"><span data-stu-id="4f5d6-105">IADsPrintJob Property Methods</span></span>

<span data-ttu-id="4f5d6-106">Les méthodes de propriété pour l’interface [**IADsPrintJob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob) obtiennent ou définissent les propriétés décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4f5d6-106">Property methods for the [**IADsPrintJob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="4f5d6-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="4f5d6-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="4f5d6-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4f5d6-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="4f5d6-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="4f5d6-109">**Description**</span></span>
<span data-ttu-id="4f5d6-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f5d6-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f5d6-111">Description du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="4f5d6-111">The description of the print job.</span></span>

<dt>

<span data-ttu-id="4f5d6-112">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f5d6-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f5d6-113">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4f5d6-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f5d6-114">**HostPrintQueue**</span><span class="sxs-lookup"><span data-stu-id="4f5d6-114">**HostPrintQueue**</span></span>
<span data-ttu-id="4f5d6-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f5d6-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f5d6-116">Chaîne ADsPath de la file d’attente à l’impression qui traite le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="4f5d6-116">The ADsPath string of the Print Queue that processes the print job.</span></span>

<dt>

<span data-ttu-id="4f5d6-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f5d6-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f5d6-118">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4f5d6-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostPrintQueue(
  [out] BSTR* pbstrHostPrintQueue
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f5d6-119">**Notifier**</span><span class="sxs-lookup"><span data-stu-id="4f5d6-119">**Notify**</span></span>
<span data-ttu-id="4f5d6-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f5d6-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f5d6-121">Utilisateur à notifier lorsque la tâche est terminée.</span><span class="sxs-lookup"><span data-stu-id="4f5d6-121">The user to be notified when job is completed.</span></span>

<dt>

<span data-ttu-id="4f5d6-122">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f5d6-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f5d6-123">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4f5d6-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Notify(
  [out] BSTR* pbstrNotify
);
HRESULT put_Notify(
  [in] BSTR bstrNotify
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f5d6-124">**NotifyPath**</span><span class="sxs-lookup"><span data-stu-id="4f5d6-124">**NotifyPath**</span></span>
<span data-ttu-id="4f5d6-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f5d6-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f5d6-126">Chaîne ADsPath de l’objet utilisateur à notifier lorsque le travail d’impression est terminé.</span><span class="sxs-lookup"><span data-stu-id="4f5d6-126">The ADsPath string of the user object to be notified when the print job is completed.</span></span>

<dt>

<span data-ttu-id="4f5d6-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f5d6-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f5d6-128">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4f5d6-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NotifyPath(
  [out] BSTR* pbstrNotifyPath
);
HRESULT put_NotifyPath(
  [in] BSTR bstrNotifyPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f5d6-129">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="4f5d6-129">**Priority**</span></span>
<span data-ttu-id="4f5d6-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f5d6-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f5d6-131">Priorité du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="4f5d6-131">The priority of the print job.</span></span>

<dt>

<span data-ttu-id="4f5d6-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f5d6-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f5d6-133">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="4f5d6-133">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Priority(
  [out] LONG* plPriority
);
HRESULT put_Priority(
  [in] LONG lPriority
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f5d6-134">**Taille**</span><span class="sxs-lookup"><span data-stu-id="4f5d6-134">**Size**</span></span>
<span data-ttu-id="4f5d6-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f5d6-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f5d6-136">Taille, en octets, du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="4f5d6-136">The size, in bytes, of the print job.</span></span>

<dt>

<span data-ttu-id="4f5d6-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f5d6-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f5d6-138">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="4f5d6-138">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Size(
  [out] LONG* plSize
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f5d6-139">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="4f5d6-139">**StartTime**</span></span>
<span data-ttu-id="4f5d6-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f5d6-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f5d6-141">Heure à laquelle le travail d’impression doit être démarré au plus tôt.</span><span class="sxs-lookup"><span data-stu-id="4f5d6-141">The earliest time when the print job should be started.</span></span>

<dt>

<span data-ttu-id="4f5d6-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f5d6-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f5d6-143">Type de données de script : **Date**</span><span class="sxs-lookup"><span data-stu-id="4f5d6-143">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartTime(
  [out] DATE* pdateStartTime
);
HRESULT put_StartTime(
  [in] DATE dateStartTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f5d6-144">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="4f5d6-144">**TimeSubmitted**</span></span>
<span data-ttu-id="4f5d6-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f5d6-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f5d6-146">Heure à laquelle le travail a été soumis à la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="4f5d6-146">The time when the job was submitted to the queue.</span></span>

<dt>

<span data-ttu-id="4f5d6-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f5d6-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f5d6-148">Type de données de script : **Date**</span><span class="sxs-lookup"><span data-stu-id="4f5d6-148">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TimeSubmitted(
  [out] DATE* pdateTimeSubmitted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f5d6-149">**TotalPages**</span><span class="sxs-lookup"><span data-stu-id="4f5d6-149">**TotalPages**</span></span>
<span data-ttu-id="4f5d6-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f5d6-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f5d6-151">Nombre total de pages du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="4f5d6-151">The total number of pages in the print job.</span></span>

<dt>

<span data-ttu-id="4f5d6-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f5d6-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f5d6-153">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="4f5d6-153">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TotalPages(
  [out] LONG* plTotalPages
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f5d6-154">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="4f5d6-154">**UntilTime**</span></span>
<span data-ttu-id="4f5d6-155"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f5d6-155"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f5d6-156">Heure à laquelle le travail d’impression doit être démarré pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="4f5d6-156">The latest time when the print job should be started.</span></span>

<dt>

<span data-ttu-id="4f5d6-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f5d6-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f5d6-158">Type de données de script : **Date**</span><span class="sxs-lookup"><span data-stu-id="4f5d6-158">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UntilTime(
  [out] DATE* pdateUntilTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f5d6-159">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="4f5d6-159">**User**</span></span>
<span data-ttu-id="4f5d6-160"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f5d6-160"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f5d6-161">Nom de l’utilisateur qui a envoyé le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="4f5d6-161">The name of user who submitted the print job.</span></span>

<dt>

<span data-ttu-id="4f5d6-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f5d6-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f5d6-163">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4f5d6-163">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f5d6-164">**UserPath**</span><span class="sxs-lookup"><span data-stu-id="4f5d6-164">**UserPath**</span></span>
<span data-ttu-id="4f5d6-165"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4f5d6-165"></dt> <dd> <dl></span></span>

<span data-ttu-id="4f5d6-166">Chaîne ADsPath de l’objet utilisateur qui a envoyé ce travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="4f5d6-166">The ADsPath string of the user object that submitted this print job.</span></span>

<dt>

<span data-ttu-id="4f5d6-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f5d6-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f5d6-168">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4f5d6-168">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="4f5d6-169">Exemples</span><span class="sxs-lookup"><span data-stu-id="4f5d6-169">Examples</span></span>

<span data-ttu-id="4f5d6-170">L’exemple de code suivant montre comment utiliser les propriétés d’un objet de travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="4f5d6-170">The following code example shows how to work with properties of a print job object.</span></span>


```VB
Dim pqo As IADsPrintQueueOperations
Dim pj As IADsPrintJob
On Error GoTo Cleanup

Set pqo = GetObject("WinNT://aMachine/aPrinter")
For Each pj In pqo.PrintJobs
    MsgBox "Host Printer: " & pj.HostPrintQueue
    MsgBox "Job description: " & pj.Description
    MsgBox "job requester: " & pj.User 
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pqo = Nothing
    Set pj = Nothing
```



<span data-ttu-id="4f5d6-171">L’exemple de code suivant montre comment utiliser les propriétés d’un objet de travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="4f5d6-171">The following code example shows how to work with properties of a print job object.</span></span>


```C++
IADsPrintQueueOperations *pqo = NULL;
IADsPrintJob *pJob = NULL;
HRESULT hr = S_OK;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
IADsCollection *pColl = NULL;
IUnknown *pUnk = NULL;
LPWSTR adsPath =L"WinNT://aMachine/aPrinter";

VariantInit(&var);

hr = ADsGetObject(adsPath, 
                  IID_IADsPrintQueueOperations, 
                  (void**)&pqo);
if(FAILED(hr)){goto Cleanup;}


hr = pqo->PrintJobs(&pColl);

// Enumerate print jobs. Code omitted.

hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)){goto Cleanup;}


IEnumVARIANT *pEnum;
hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)){goto Cleanup;}


// Now Enumerate.
hr = pEnum->Next(1, &var, &lFetch);
if(FAILED(hr)){goto Cleanup;}

while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsPrintJob, (void**)&pJob);

        pJob->get_HostPrintQueue(&bstr);
        printf("HostPrintQueue: %S\n",bstr);
        SysFreeString(bstr);

        pJob->get_Description(&bstr);
        printf("Print job name: %S\n",bstr);
        SysFreeString(bstr);

        pJob->get_User(&bstr);
        printf("Requester: %S\n",bstr);
        SysFreeString(bstr);

        pJob->Release();
    }
    pDisp->Release();
    VariantClear(&var);
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pEnum) pEnum->Release();
    if(pUnk) pUnk->Release();
    if(pColl) pColl->Release();
    if(pqo) pqo->Release();
```



## <a name="requirements"></a><span data-ttu-id="4f5d6-172">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f5d6-172">Requirements</span></span>



| <span data-ttu-id="4f5d6-173">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f5d6-173">Requirement</span></span> | <span data-ttu-id="4f5d6-174">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f5d6-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f5d6-175">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f5d6-175">Minimum supported client</span></span><br/> | <span data-ttu-id="4f5d6-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f5d6-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4f5d6-177">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f5d6-177">Minimum supported server</span></span><br/> | <span data-ttu-id="4f5d6-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f5d6-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4f5d6-179">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f5d6-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f5d6-180"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f5d6-180"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="4f5d6-181">DLL</span><span class="sxs-lookup"><span data-stu-id="4f5d6-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f5d6-182"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f5d6-182"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="4f5d6-183">IID</span><span class="sxs-lookup"><span data-stu-id="4f5d6-183">IID</span></span><br/>                      | <span data-ttu-id="4f5d6-184">IID \_ IADsPrintJob est défini en tant que 32FB6780-1ED0-11CF-A988-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="4f5d6-184">IID\_IADsPrintJob is defined as 32FB6780-1ED0-11CF-A988-00AA006BC149</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="4f5d6-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f5d6-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f5d6-186">**IADsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="4f5d6-186">**IADsPrintJob**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintjob)
</dt> <dt>

[<span data-ttu-id="4f5d6-187">Méthodes de propriété d’interface</span><span class="sxs-lookup"><span data-stu-id="4f5d6-187">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





