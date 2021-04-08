---
title: Méthodes de propriété IADsServiceOperations (IADs. h)
description: Les méthodes de propriété de l’interface IADsServiceOperations lisent et écrivent les propriétés décrites dans la liste suivante. Pour plus d’informations sur les méthodes de propriété, consultez Méthodes de propriété d’interface.
ms.assetid: ebddfc42-1d2f-495b-b57c-f57419b54ff8
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsServiceOperations ADSI
topic_type:
- apiref
api_name:
- IADsServiceOperations Property Methods
- IADsServiceOperations.Status
- IADsServiceOperations.get_Status
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 654a92be1052d4e4c70e0274d719a49be965d8cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843442"
---
# <a name="iadsserviceoperations-property-methods"></a><span data-ttu-id="79274-105">Méthodes de propriété IADsServiceOperations</span><span class="sxs-lookup"><span data-stu-id="79274-105">IADsServiceOperations Property Methods</span></span>

<span data-ttu-id="79274-106">Les méthodes de propriété de l’interface [**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations) lisent et écrivent les propriétés décrites dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="79274-106">The property methods of the [**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations) interface read and write the properties described in the following list.</span></span> <span data-ttu-id="79274-107">Pour plus d’informations sur les méthodes de propriété, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="79274-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="79274-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="79274-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="79274-109">**État**</span><span class="sxs-lookup"><span data-stu-id="79274-109">**Status**</span></span>
<span data-ttu-id="79274-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="79274-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="79274-111">État du service.</span><span class="sxs-lookup"><span data-stu-id="79274-111">Status of service.</span></span>

<span data-ttu-id="79274-112">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="79274-112">The following are possible values.</span></span>

<dt>

<span id="ADS_SERVICE_STOPPED"></span><span id="ads_service_stopped"></span>

<span data-ttu-id="79274-113">**Annonces \_ SERVICE \_ arrêté** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="79274-113">**ADS\_SERVICE\_STOPPED** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_START_PENDING"></span><span id="ads_service_start_pending"></span>

<span data-ttu-id="79274-114">**Annonces \_ Démarrage du SERVICE \_ \_ en attente** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="79274-114">**ADS\_SERVICE\_START\_PENDING** (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_STOP_PENDING"></span><span id="ads_service_stop_pending"></span>

<span data-ttu-id="79274-115">**Annonces \_ Arrêt du SERVICE \_ \_ en attente** (0x00000003)</span><span class="sxs-lookup"><span data-stu-id="79274-115">**ADS\_SERVICE\_STOP\_PENDING** (0x00000003)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_RUNNING"></span><span id="ads_service_running"></span>

<span data-ttu-id="79274-116">**Annonces \_ SERVICE \_ en cours d’exécution** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="79274-116">**ADS\_SERVICE\_RUNNING** (0x00000004)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_CONTINUE_PENDING"></span><span id="ads_service_continue_pending"></span>

<span data-ttu-id="79274-117">**Annonces \_ Reprise du SERVICE \_ \_ en attente** (0x00000005)</span><span class="sxs-lookup"><span data-stu-id="79274-117">**ADS\_SERVICE\_CONTINUE\_PENDING** (0x00000005)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSE_PENDING"></span><span id="ads_service_pause_pending"></span>

<span data-ttu-id="79274-118">**Annonces \_ Suspension du SERVICE \_ \_ en attente** (0x00000006)</span><span class="sxs-lookup"><span data-stu-id="79274-118">**ADS\_SERVICE\_PAUSE\_PENDING** (0x00000006)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSED"></span><span id="ads_service_paused"></span>

<span data-ttu-id="79274-119">**Annonces \_ SERVICE \_ suspendu** (0x00000007)</span><span class="sxs-lookup"><span data-stu-id="79274-119">**ADS\_SERVICE\_PAUSED** (0x00000007)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR"></span><span id="ads_service_error"></span>

<span data-ttu-id="79274-120">**Annonces \_ \_Erreur de service** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="79274-120">**ADS\_SERVICE\_ERROR** (0x00000008)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

<span data-ttu-id="79274-121">**Annonces \_ \_ \_ Processus propre au service** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="79274-121">**ADS\_SERVICE\_OWN\_PROCESS** (0x00000010)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

<span data-ttu-id="79274-122">**Annonces \_ \_ \_ Processus de partage de services** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="79274-122">**ADS\_SERVICE\_SHARE\_PROCESS** (0x00000020)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

<span data-ttu-id="79274-123">**Annonces \_ \_ \_ Pilote du noyau de service** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="79274-123">**ADS\_SERVICE\_KERNEL\_DRIVER** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

<span data-ttu-id="79274-124">**Annonces \_ \_Pilote du \_ système \_ de fichiers du service** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="79274-124">**ADS\_SERVICE\_FILE\_SYSTEM\_DRIVER** (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

<span data-ttu-id="79274-125">**Annonces \_ démarrage \_ du \_ démarrage du service** (démarrage du service \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="79274-125">**ADS\_SERVICE\_BOOT\_START** (SERVICE\_BOOT\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

<span data-ttu-id="79274-126">**Annonces \_ \_ \_ démarrage du système de service** (démarrage du système de service \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="79274-126">**ADS\_SERVICE\_SYSTEM\_START** (SERVICE\_SYSTEM\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

<span data-ttu-id="79274-127">**Annonces \_ \_ \_ démarrage automatique du service** ( \_ démarrage automatique du service \_ )</span><span class="sxs-lookup"><span data-stu-id="79274-127">**ADS\_SERVICE\_AUTO\_START** (SERVICE\_AUTO\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

<span data-ttu-id="79274-128">**Annonces \_ \_ \_ début de la demande de service** ( \_ début de la demande du service \_ )</span><span class="sxs-lookup"><span data-stu-id="79274-128">**ADS\_SERVICE\_DEMAND\_START** (SERVICE\_DEMAND\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

<span data-ttu-id="79274-129">**Annonces \_ SERVICE \_ désactivé** (service \_ désactivé)</span><span class="sxs-lookup"><span data-stu-id="79274-129">**ADS\_SERVICE\_DISABLED** (SERVICE\_DISABLED)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

<span data-ttu-id="79274-130">**Annonces \_ Erreur de SERVICE \_ \_ ignorée** (0)</span><span class="sxs-lookup"><span data-stu-id="79274-130">**ADS\_SERVICE\_ERROR\_IGNORE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

<span data-ttu-id="79274-131">**Annonces \_ Erreur de SERVICE \_ \_ normal** (1)</span><span class="sxs-lookup"><span data-stu-id="79274-131">**ADS\_SERVICE\_ERROR\_NORMAL** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

<span data-ttu-id="79274-132">**Annonces \_ Erreur de SERVICE \_ \_ grave** (2)</span><span class="sxs-lookup"><span data-stu-id="79274-132">**ADS\_SERVICE\_ERROR\_SEVERE** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

<span data-ttu-id="79274-133">**Annonces \_ Erreur de SERVICE \_ \_ critique** (3)</span><span class="sxs-lookup"><span data-stu-id="79274-133">**ADS\_SERVICE\_ERROR\_CRITICAL** (3)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="79274-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79274-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79274-135">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="79274-135">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* pstatus
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="79274-136">Exemples</span><span class="sxs-lookup"><span data-stu-id="79274-136">Examples</span></span>

<span data-ttu-id="79274-137">L’exemple de code suivant montre comment vérifier l’état d’un service Microsoft Fax s’exécutant sur Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="79274-137">The following code example shows how to verify the status of a Microsoft Fax Service running on Windows 2000.</span></span>


```VB
Dim cp As IADsComputer
Dim sr As IADsService
Dim so As IADsServiceOperations
On Error GoTo Cleanup

Set cp = GetObject("WinNT://myMachine,computer")
Set sr = cp.GetObject("Service", "Fax")
Set so = sr

Select Case so.Status
    Case ADS_SERVICE_STOPPED
        MsgBox "Microsoft Fax Service has stopped."
    Case ADS_SERVICE_RUNNING
        MsgBox "Microsoft Fax Service is running."
    Case ADS_SERVICE_PAUSED
        MsgBox "Microsoft Fax Service has paused."
    Case ADS_SERVICE_ERROR
        MsgBox "Microsoft Fax Service has errors."
End Select

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cp = Nothing
    Set sr = Nothing
    Set so = Nothing
```



<span data-ttu-id="79274-138">L’exemple de code suivant vérifie l’état d’un service Microsoft Fax s’exécutant sur Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="79274-138">The following code example verifies the status of a Microsoft Fax Service running on Windows 2000.</span></span>


```C++
IADsContainer *pCont = NULL;
IADsServiceOperations *pSrvOp = NULL;
LPWSTR adsPath = L"WinNT://myMachine,computer";
IDispatch *pDisp = NULL;
long status = 0;

HRESULT hr = S_OK;

hr = ADsGetObject(adsPath,IID_IADsContainer,(void**)&pCont);
if(FAILED(hr)) {goto Cleanup;}

hr = pCont->GetObject(CComBSTR("Service"), CComBSTR("Fax"), &pDisp);
if(FAILED(hr)) {goto Cleanup;}

hr = pDisp->QueryInterface(IID_IADsServiceOperations,(void**)&pSrvOp);
if(FAILED(hr)) {goto Cleanup;}

hr = pSrvOp->get_Status(&status);
switch (status) 
{
    case ADS_SERVICE_STOPPED:
        printf("The service has stopped.\n");
        break;
    case ADS_SERVICE_RUNNING:
        printf("The service is running.\n");
        break;
    case ADS_SERVICE_PAUSED:
        printf("The service has paused.\n");
        break;
    case ADS_SERVICE_ERROR:
        printf("The service has errors.\n");
        break;
}

Cleanup:
    if(pDisp) pDisp->Release();
    if(pCont) pCont->Release();
    if(pSrvOp) pSrvOp->Release();
```



## <a name="requirements"></a><span data-ttu-id="79274-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79274-139">Requirements</span></span>



| <span data-ttu-id="79274-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79274-140">Requirement</span></span> | <span data-ttu-id="79274-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="79274-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="79274-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79274-142">Minimum supported client</span></span><br/> | <span data-ttu-id="79274-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="79274-143">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="79274-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79274-144">Minimum supported server</span></span><br/> | <span data-ttu-id="79274-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79274-145">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="79274-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="79274-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="79274-147"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="79274-147"><dt>Iads.h</dt></span></span> </dl>        |
| <span data-ttu-id="79274-148">DLL</span><span class="sxs-lookup"><span data-stu-id="79274-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79274-149"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79274-149"><dt>Activeds.dll</dt></span></span> </dl>  |
| <span data-ttu-id="79274-150">IID</span><span class="sxs-lookup"><span data-stu-id="79274-150">IID</span></span><br/>                      | <span data-ttu-id="79274-151">IID \_ IADsServiceOperations est défini en tant que 5D7B33F0-31CA-11CF-A98A-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="79274-151">IID\_IADsServiceOperations is defined as 5D7B33F0-31CA-11CF-A98A-00AA006BC149</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="79274-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79274-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79274-153">**IADsFileService**</span><span class="sxs-lookup"><span data-stu-id="79274-153">**IADsFileService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileservice)
</dt> <dt>

[<span data-ttu-id="79274-154">**IADsFileServiceOperations**</span><span class="sxs-lookup"><span data-stu-id="79274-154">**IADsFileServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations)
</dt> <dt>

[<span data-ttu-id="79274-155">**IADsService**</span><span class="sxs-lookup"><span data-stu-id="79274-155">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="79274-156">**IADsServiceOperations**</span><span class="sxs-lookup"><span data-stu-id="79274-156">**IADsServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)
</dt> </dl>

 

 





