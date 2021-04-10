---
title: Méthodes de propriété IADsPrintQueue (IADs. h)
description: Les méthodes de propriété de l’interface IADsPrintQueue obtiennent ou définissent les propriétés décrites dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: 7f5b4200-65c8-4230-8561-ad4fefb391f3
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsPrintQueue ADSI
topic_type:
- apiref
api_name:
- IADsPrintQueue Property Methods
- IADsPrintQueue.BannerPage
- IADsPrintQueue.get_BannerPage
- IADsPrintQueue.put_BannerPage
- IADsPrintQueue.Datatype
- IADsPrintQueue.get_Datatype
- IADsPrintQueue.put_Datatype
- IADsPrintQueue.DefaultJobPriority
- IADsPrintQueue.get_DefaultJobPriority
- IADsPrintQueue.put_DefaultJobPriority
- IADsPrintQueue.Description
- IADsPrintQueue.get_Description
- IADsPrintQueue.put_Description
- IADsPrintQueue.HostComputer
- IADsPrintQueue.get_HostComputer
- IADsPrintQueue.put_HostComputer
- IADsPrintQueue.Location
- IADsPrintQueue.get_Location
- IADsPrintQueue.put_Location
- IADsPrintQueue.Model
- IADsPrintQueue.get_Model
- IADsPrintQueue.put_Model
- IADsPrintQueue.PrintDevices
- IADsPrintQueue.get_PrintDevices
- IADsPrintQueue.put_PrintDevices
- IADsPrintQueue.PrinterPath
- IADsPrintQueue.get_PrinterPath
- IADsPrintQueue.put_PrinterPath
- IADsPrintQueue.PrintProcessor
- IADsPrintQueue.get_PrintProcessor
- IADsPrintQueue.put_PrintProcessor
- IADsPrintQueue.Priority
- IADsPrintQueue.get_Priority
- IADsPrintQueue.put_Priority
- IADsPrintQueue.StartTime
- IADsPrintQueue.get_StartTime
- IADsPrintQueue.put_StartTime
- IADsPrintQueue.UntilTime
- IADsPrintQueue.get_UntilTime
- IADsPrintQueue.put_UntilTime
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e8b7b2260805dbf5fa144f239111b6e29f5ec78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200565"
---
# <a name="iadsprintqueue-property-methods"></a><span data-ttu-id="c4362-105">Méthodes de propriété IADsPrintQueue</span><span class="sxs-lookup"><span data-stu-id="c4362-105">IADsPrintQueue Property Methods</span></span>

<span data-ttu-id="c4362-106">Les méthodes de propriété de l’interface [**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue) obtiennent ou définissent les propriétés décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c4362-106">The property methods of the [**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="c4362-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="c4362-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="c4362-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c4362-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="c4362-109">**BannerPage**</span><span class="sxs-lookup"><span data-stu-id="c4362-109">**BannerPage**</span></span>
<span data-ttu-id="c4362-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c4362-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="c4362-111">Chemin d’accès du système de fichiers qui pointe vers la page de bannière utilisée pour séparer les travaux d’impression.</span><span class="sxs-lookup"><span data-stu-id="c4362-111">The file system path that points to the banner page used to separate print jobs.</span></span> <span data-ttu-id="c4362-112">Si la **valeur est null**, aucune page de bannière n’est utilisée.</span><span class="sxs-lookup"><span data-stu-id="c4362-112">If **NULL**, no banner page is used.</span></span>

<dt>

<span data-ttu-id="c4362-113">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4362-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c4362-114">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c4362-114">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BannerPage(
  [out] BSTR* pbstrBannerPage
);
HRESULT put_BannerPage(
  [in] BSTR bstrBannerPage
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4362-115">**Décimal**</span><span class="sxs-lookup"><span data-stu-id="c4362-115">**Datatype**</span></span>
<span data-ttu-id="c4362-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c4362-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="c4362-117">Type de données qui peut être traité par cette file d’attente.</span><span class="sxs-lookup"><span data-stu-id="c4362-117">The data type that can be processed by this queue.</span></span>

<dt>

<span data-ttu-id="c4362-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4362-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c4362-119">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c4362-119">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Datatype(
  [out] BSTR* pbstrDatatype
);
HRESULT put_Datatype(
  [in] BSTR bstrDatatype
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4362-120">**DefaultJobPriority**</span><span class="sxs-lookup"><span data-stu-id="c4362-120">**DefaultJobPriority**</span></span>
<span data-ttu-id="c4362-121"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c4362-121"></dt> <dd> <dl></span></span>

<span data-ttu-id="c4362-122">Priorité par défaut assignée à chaque travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="c4362-122">The default priority assigned to each print job.</span></span>

<dt>

<span data-ttu-id="c4362-123">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4362-123">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c4362-124">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c4362-124">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DefaultJobPriority(
  [out] LONG* plDefaultJobPriority
);
HRESULT put_DefaultJobPriority(
  [in] BSTR lDefaultJobPriority
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4362-125">**Description**</span><span class="sxs-lookup"><span data-stu-id="c4362-125">**Description**</span></span>
<span data-ttu-id="c4362-126"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c4362-126"></dt> <dd> <dl></span></span>

<span data-ttu-id="c4362-127">Description textuelle de cette file d’attente à l’impression.</span><span class="sxs-lookup"><span data-stu-id="c4362-127">The text description of this print queue.</span></span>

<dt>

<span data-ttu-id="c4362-128">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4362-128">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c4362-129">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c4362-129">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="c4362-130">**HostComputer**</span><span class="sxs-lookup"><span data-stu-id="c4362-130">**HostComputer**</span></span>
<span data-ttu-id="c4362-131"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c4362-131"></dt> <dd> <dl></span></span>

<span data-ttu-id="c4362-132">Chaîne ADsPath qui fait référence à l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="c4362-132">The ADsPath string that references the host computer.</span></span>

<dt>

<span data-ttu-id="c4362-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4362-133">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c4362-134">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c4362-134">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostComputer(
  [out] BSTR* pbstrHostComputer
);
HRESULT put_HostComputer(
  [in] BSTR bstrHostComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4362-135">**Lieu**</span><span class="sxs-lookup"><span data-stu-id="c4362-135">**Location**</span></span>
<span data-ttu-id="c4362-136"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c4362-136"></dt> <dd> <dl></span></span>

<span data-ttu-id="c4362-137">Emplacement de la file d’attente comme décrit par un administrateur.</span><span class="sxs-lookup"><span data-stu-id="c4362-137">The location of the queue as described by an administrator.</span></span>

<dt>

<span data-ttu-id="c4362-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4362-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c4362-139">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c4362-139">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Location(
  [out] BSTR* pbstrLocation
);
HRESULT put_Location(
  [in] BSTR bstrLocation
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4362-140">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="c4362-140">**Model**</span></span>
<span data-ttu-id="c4362-141"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c4362-141"></dt> <dd> <dl></span></span>

<span data-ttu-id="c4362-142">Nom du pilote utilisé par cette file d’attente à l’impression.</span><span class="sxs-lookup"><span data-stu-id="c4362-142">The name of the driver used by this print queue.</span></span>

<dt>

<span data-ttu-id="c4362-143">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4362-143">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c4362-144">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c4362-144">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Model(
  [out] BSTR* pbstrModel
);
HRESULT put_Model(
  [in] BSTR bstrModel
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4362-145">**PrintDevices**</span><span class="sxs-lookup"><span data-stu-id="c4362-145">**PrintDevices**</span></span>
<span data-ttu-id="c4362-146"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c4362-146"></dt> <dd> <dl></span></span>

<span data-ttu-id="c4362-147">SAFEARRAY de **BSTR** qui contient les noms des périphériques d’impression auxquels cette file d’attente à l’impression met en file d’attente les travaux.</span><span class="sxs-lookup"><span data-stu-id="c4362-147">A SAFEARRAY of **BSTR** that contains the names of the print devices to which this print queue spools jobs.</span></span>

<dt>

<span data-ttu-id="c4362-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4362-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c4362-149">Type de données de script : **variante**</span><span class="sxs-lookup"><span data-stu-id="c4362-149">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrintDevices(
  [out] VARIANT* pvPrintDevices
);
HRESULT put_PrintDevices(
  [in] VARIANT vPrintDevices
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4362-150">**PrinterPath**</span><span class="sxs-lookup"><span data-stu-id="c4362-150">**PrinterPath**</span></span>
<span data-ttu-id="c4362-151"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c4362-151"></dt> <dd> <dl></span></span>

<span data-ttu-id="c4362-152">Chaîne qui fait référence au chemin d’accès par lequel une imprimante partagée est accessible.</span><span class="sxs-lookup"><span data-stu-id="c4362-152">The string that references the path by which a shared printer can be accessed.</span></span>

<dt>

<span data-ttu-id="c4362-153">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4362-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c4362-154">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c4362-154">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrinterPath(
  [out] BSTR* pbstrPrinterPath
);
HRESULT put_PrinterPath(
  [in] BSTR bstrPrinterPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4362-155">**PrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="c4362-155">**PrintProcessor**</span></span>
<span data-ttu-id="c4362-156"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c4362-156"></dt> <dd> <dl></span></span>

<span data-ttu-id="c4362-157">Processeur d’impression associé à cette file d’attente.</span><span class="sxs-lookup"><span data-stu-id="c4362-157">The print processor associated with this queue.</span></span>

<dt>

<span data-ttu-id="c4362-158">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4362-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c4362-159">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c4362-159">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrintProcessor(
  [out] BSTR* pbstrPrintProcessor
);
HRESULT put_PrintProcessor(
  [in] BSTR bstrPrintProcessor
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4362-160">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="c4362-160">**Priority**</span></span>
<span data-ttu-id="c4362-161"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c4362-161"></dt> <dd> <dl></span></span>

<span data-ttu-id="c4362-162">Priorité de la file d’attente des travaux de l’objet imprimante pour tous les appareils connectés.</span><span class="sxs-lookup"><span data-stu-id="c4362-162">The priority of this printer object job queue for any connected devices.</span></span> <span data-ttu-id="c4362-163">Toutes les tâches dans les objets de file d’attente à l’impression de priorité supérieure sont traitées en premier.</span><span class="sxs-lookup"><span data-stu-id="c4362-163">All jobs in higher priority print queue objects will be processed first.</span></span>

<dt>

<span data-ttu-id="c4362-164">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4362-164">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c4362-165">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="c4362-165">Scripting data type: **LONG**</span></span>
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

<span data-ttu-id="c4362-166">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="c4362-166">**StartTime**</span></span>
<span data-ttu-id="c4362-167"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c4362-167"></dt> <dd> <dl></span></span>

<span data-ttu-id="c4362-168">Heure à laquelle la file d’attente doit commencer le traitement des tâches.</span><span class="sxs-lookup"><span data-stu-id="c4362-168">The time when the queue should begin processing jobs.</span></span> <span data-ttu-id="c4362-169">La partie Date de l’heure est ignorée.</span><span class="sxs-lookup"><span data-stu-id="c4362-169">The date portion of the time is ignored.</span></span>

<dt>

<span data-ttu-id="c4362-170">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4362-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c4362-171">Type de données de script : **Date**</span><span class="sxs-lookup"><span data-stu-id="c4362-171">Scripting data type: **DATE**</span></span>
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

<span data-ttu-id="c4362-172">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="c4362-172">**UntilTime**</span></span>
<span data-ttu-id="c4362-173"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c4362-173"></dt> <dd> <dl></span></span>

<span data-ttu-id="c4362-174">Heure à laquelle la file d’attente doit arrêter le traitement des tâches.</span><span class="sxs-lookup"><span data-stu-id="c4362-174">The time when the queue should stop processing jobs.</span></span>

<dt>

<span data-ttu-id="c4362-175">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4362-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c4362-176">Type de données de script : **Date**</span><span class="sxs-lookup"><span data-stu-id="c4362-176">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UntilTime(
  [out] DATE* pdateUntilTime
);
HRESULT put_UntilTime(
  [in] DATE dateUntilTime
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="c4362-177">Exemples</span><span class="sxs-lookup"><span data-stu-id="c4362-177">Examples</span></span>

<span data-ttu-id="c4362-178">L’exemple de code suivant montre comment déterminer si une imprimante spécifiée est en ligne ou hors connexion.</span><span class="sxs-lookup"><span data-stu-id="c4362-178">The following code example shows how to determine if a specified printer is online or offline.</span></span>


```VB
Dim pq As IADsPrintQueue
Dim pqo As IADsPrintQueueOperations
On Error GoTo Cleanup
 
Set pq = GetObject("WinNT://aMachine/aPrinter")
Set pqo = pq
If pqo.status = ADS_PRINTER_OFFLINE Then
    MsgBox pq.Model & "@" & pq.Location & is offline."
Else
    MsgBox pq.Model & "@" & pq.Location & is online."
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pq = Nothing
    Set pqo = Nothing
```



<span data-ttu-id="c4362-179">L’exemple de code suivant montre comment déterminer si une imprimante spécifiée est en ligne ou hors connexion.</span><span class="sxs-lookup"><span data-stu-id="c4362-179">The following code example shows how to determine if a specified printer is online or offline.</span></span>


```C++
IADsPrintQueue *pq = NULL;
HRESULT hr = S_OK;
IADsPrintQueueOperations *pqo = NULL;
BSTR model = NULL;
BSTR location = NULL;

LPWSTR adsPath = L"WinNT://aMachine/aPrinter";
hr = ADsGetObject(adsPath,
                  IID_IADsPrintQueue,
                  (void**)&pq);
if(FAILED(hr)) {goto Cleanup;}


hr = pq->QueryInterface(IID_IADsPrintQueueOperations,(void**)&pqo);
if(FAILED(hr)) {goto Cleanup;}

long status;
hr = pqo->get_Status(&status);
if(FAILED(hr)) {goto Cleanup;}

hr = pq->get_Model(&model);
if(FAILED(hr)) {goto Cleanup;}

hr =pq->get_Location(&location);
if(FAILED(hr)) {goto Cleanup;}

if(status == ADS_PRINTER_OFFLINE) 
{
    printf("%S @ %S is offline.\n",model,location);
} 
else 
{
    printf("%S @ %S is online.\n",model,location);
}


Cleanup:
    SysFreeString(model);
    SysFreeString(location);
    if(pq) pq->Release();
    if(pqo) pqo->Release();
```



## <a name="requirements"></a><span data-ttu-id="c4362-180">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4362-180">Requirements</span></span>



| <span data-ttu-id="c4362-181">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4362-181">Requirement</span></span> | <span data-ttu-id="c4362-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4362-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4362-183">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4362-183">Minimum supported client</span></span><br/> | <span data-ttu-id="c4362-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4362-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c4362-185">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4362-185">Minimum supported server</span></span><br/> | <span data-ttu-id="c4362-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4362-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c4362-187">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4362-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4362-188"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4362-188"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="c4362-189">DLL</span><span class="sxs-lookup"><span data-stu-id="c4362-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4362-190"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4362-190"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="c4362-191">IID</span><span class="sxs-lookup"><span data-stu-id="c4362-191">IID</span></span><br/>                      | <span data-ttu-id="c4362-192">IID \_ IADsPrintQueue est défini en tant que B15160D0-1226-11CF-A985-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="c4362-192">IID\_IADsPrintQueue is defined as B15160D0-1226-11CF-A985-00AA006BC149</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c4362-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4362-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4362-194">**IADsPrintQueue**</span><span class="sxs-lookup"><span data-stu-id="c4362-194">**IADsPrintQueue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[<span data-ttu-id="c4362-195">Méthodes de propriété d’interface</span><span class="sxs-lookup"><span data-stu-id="c4362-195">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





