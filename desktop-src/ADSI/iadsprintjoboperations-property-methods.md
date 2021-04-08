---
title: Méthodes de propriété IADsPrintJobOperations (IADs. h)
description: Les méthodes de propriété de l’interface IADsPrintJobOperations lisent et écrivent les propriétés énumérées dans le tableau suivant. Pour plus d’informations sur les méthodes de propriété, consultez Méthodes de propriété d’interface.
ms.assetid: d1710bd4-e600-4d92-892a-16b4316851d4
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsPrintJobOperations ADSI
topic_type:
- apiref
api_name:
- IADsPrintJobOperations Property Methods
- IADsPrintJobOperations.Status
- IADsPrintJobOperations.get_Status
- IADsPrintJobOperations.TimeElapsed
- IADsPrintJobOperations.get_TimeElapsed
- IADsPrintJobOperations.PagesPrinted
- IADsPrintJobOperations.get_PagesPrinted
- IADsPrintJobOperations.Position
- IADsPrintJobOperations.get_Position
- IADsPrintJobOperations.put_Position
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2981fcdd8043c0eb0ee8b05cfd0331fe3abfabe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844013"
---
# <a name="iadsprintjoboperations-property-methods"></a><span data-ttu-id="fe396-105">Méthodes de propriété IADsPrintJobOperations</span><span class="sxs-lookup"><span data-stu-id="fe396-105">IADsPrintJobOperations Property Methods</span></span>

<span data-ttu-id="fe396-106">Les méthodes de propriété de l’interface [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) lisent et écrivent les propriétés énumérées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fe396-106">The property methods of the [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) interface read and write the properties listed in the following table.</span></span> <span data-ttu-id="fe396-107">Pour plus d’informations sur les méthodes de propriété, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="fe396-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="fe396-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fe396-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="fe396-109">**PagesPrinted**</span><span class="sxs-lookup"><span data-stu-id="fe396-109">**PagesPrinted**</span></span>
<span data-ttu-id="fe396-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fe396-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="fe396-111">Contient le nombre de pages imprimées.</span><span class="sxs-lookup"><span data-stu-id="fe396-111">Contains the number of pages printed.</span></span>

<dt>

<span data-ttu-id="fe396-112">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fe396-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe396-113">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="fe396-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PagesPrinted(
  [out] LONG* plPagesPrinted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe396-114">**Position**</span><span class="sxs-lookup"><span data-stu-id="fe396-114">**Position**</span></span>
<span data-ttu-id="fe396-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fe396-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="fe396-116">Contient la position de ce travail d’impression dans la file d’attente à l’impression.</span><span class="sxs-lookup"><span data-stu-id="fe396-116">Contains the position of this print job in the print queue.</span></span>

<dt>

<span data-ttu-id="fe396-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fe396-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fe396-118">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="fe396-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Position(
  [out] LONG* plPosition
);
HRESULT put_Position(
  [in] LONG lPosition
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe396-119">**État**</span><span class="sxs-lookup"><span data-stu-id="fe396-119">**Status**</span></span>
<span data-ttu-id="fe396-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fe396-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="fe396-121">Contient l’état actuel du travail d’impression comme indiqué par l’une des valeurs des [**constantes d’État du travail d’impression ADSI**](adsi-print-job-status-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="fe396-121">Contains the current status of the print job as indicated by one of the [**ADSI Print Job Status Constants**](adsi-print-job-status-constants.md) values.</span></span>

<dt>

<span data-ttu-id="fe396-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fe396-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe396-123">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="fe396-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* plStatus
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe396-124">**TimeElapsed**</span><span class="sxs-lookup"><span data-stu-id="fe396-124">**TimeElapsed**</span></span>
<span data-ttu-id="fe396-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fe396-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="fe396-126">Contient le nombre de millisecondes écoulées depuis le début du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="fe396-126">Contains the number of milliseconds elapsed since the print job started.</span></span>

<dt>

<span data-ttu-id="fe396-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fe396-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe396-128">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="fe396-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TimeElapsed(
  [out] LONG* plTimeElapsed
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="fe396-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="fe396-129">Examples</span></span>

<span data-ttu-id="fe396-130">L’exemple de code suivant montre comment les propriétés de [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) peuvent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="fe396-130">The following code example shows how the properties for [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) may be used.</span></span>


```VB
Dim pqo As IADsPrintQueueOperations
Dim pjo As IADsPrintJobOperations

On Error GoTo Cleanup

Set pqo = GetObject("WinNT://aMachine/aPrinter")
For Each pj In pqo.PrintJobs
    Set pjo = pj
    MsgBox pjo.PagesPrinted & " pages printed for job " & pj.Name
    If (pjo.position > 1) Then
        pjo.Position = pjo.status - 1
    End If
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pqo = Nothing
    Set pjo = Nothing
```



## <a name="requirements"></a><span data-ttu-id="fe396-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe396-131">Requirements</span></span>



| <span data-ttu-id="fe396-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe396-132">Requirement</span></span> | <span data-ttu-id="fe396-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe396-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe396-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe396-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fe396-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe396-135">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="fe396-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe396-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fe396-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe396-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="fe396-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="fe396-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe396-139"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe396-139"><dt>Iads.h</dt></span></span> </dl>         |
| <span data-ttu-id="fe396-140">DLL</span><span class="sxs-lookup"><span data-stu-id="fe396-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe396-141"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe396-141"><dt>Activeds.dll</dt></span></span> </dl>   |
| <span data-ttu-id="fe396-142">IID</span><span class="sxs-lookup"><span data-stu-id="fe396-142">IID</span></span><br/>                      | <span data-ttu-id="fe396-143">IID \_ IADsPrintJobOperations est défini en tant que 32FB6780-1ED0-11CF-A988-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="fe396-143">IID\_IADsPrintJobOperations is defined as 32FB6780-1ED0-11CF-A988-00AA006BC149</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fe396-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe396-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe396-145">**IADsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="fe396-145">**IADsPrintJob**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintjob)
</dt> <dt>

[<span data-ttu-id="fe396-146">**IADsPrintJobOperations**</span><span class="sxs-lookup"><span data-stu-id="fe396-146">**IADsPrintJobOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)
</dt> <dt>

[<span data-ttu-id="fe396-147">**IADsPrintQueue**</span><span class="sxs-lookup"><span data-stu-id="fe396-147">**IADsPrintQueue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[<span data-ttu-id="fe396-148">**Constantes d’État du travail d’impression ADSI**</span><span class="sxs-lookup"><span data-stu-id="fe396-148">**ADSI Print Job Status Constants**</span></span>](adsi-print-job-status-constants.md)
</dt> </dl>

 

 





