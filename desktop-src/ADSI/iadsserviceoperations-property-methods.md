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
# <a name="iadsserviceoperations-property-methods"></a>Méthodes de propriété IADsServiceOperations

Les méthodes de propriété de l’interface [**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations) lisent et écrivent les propriétés décrites dans la liste suivante. Pour plus d’informations sur les méthodes de propriété, consultez [méthodes de propriété d’interface](interface-property-methods.md).

## <a name="properties"></a>Propriétés

<dl> <dt>

**État**
</dt> <dd> <dl>

État du service.

Les valeurs possibles sont les suivantes.

<dt>

<span id="ADS_SERVICE_STOPPED"></span><span id="ads_service_stopped"></span>

**Annonces \_ SERVICE \_ arrêté** (0x00000001)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_START_PENDING"></span><span id="ads_service_start_pending"></span>

**Annonces \_ Démarrage du SERVICE \_ \_ en attente** (0x00000002)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_STOP_PENDING"></span><span id="ads_service_stop_pending"></span>

**Annonces \_ Arrêt du SERVICE \_ \_ en attente** (0x00000003)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_RUNNING"></span><span id="ads_service_running"></span>

**Annonces \_ SERVICE \_ en cours d’exécution** (0x00000004)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_CONTINUE_PENDING"></span><span id="ads_service_continue_pending"></span>

**Annonces \_ Reprise du SERVICE \_ \_ en attente** (0x00000005)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSE_PENDING"></span><span id="ads_service_pause_pending"></span>

**Annonces \_ Suspension du SERVICE \_ \_ en attente** (0x00000006)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSED"></span><span id="ads_service_paused"></span>

**Annonces \_ SERVICE \_ suspendu** (0x00000007)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR"></span><span id="ads_service_error"></span>

**Annonces \_ \_Erreur de service** (0x00000008)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

**Annonces \_ \_ \_ Processus propre au service** (0x00000010)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

**Annonces \_ \_ \_ Processus de partage de services** (0x00000020)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

**Annonces \_ \_ \_ Pilote du noyau de service** (0x00000001)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

**Annonces \_ \_Pilote du \_ système \_ de fichiers du service** (0x00000002)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

**Annonces \_ démarrage \_ du \_ démarrage du service** (démarrage du service \_ \_ )


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

**Annonces \_ \_ \_ démarrage du système de service** (démarrage du système de service \_ \_ )


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

**Annonces \_ \_ \_ démarrage automatique du service** ( \_ démarrage automatique du service \_ )


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

**Annonces \_ \_ \_ début de la demande de service** ( \_ début de la demande du service \_ )


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

**Annonces \_ SERVICE \_ désactivé** (service \_ désactivé)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

**Annonces \_ Erreur de SERVICE \_ \_ ignorée** (0)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

**Annonces \_ Erreur de SERVICE \_ \_ normal** (1)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

**Annonces \_ Erreur de SERVICE \_ \_ grave** (2)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

**Annonces \_ Erreur de SERVICE \_ \_ critique** (3)


</dt> <dd></dd> </dl> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Type de données de script : **long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* pstatus
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Exemples

L’exemple de code suivant montre comment vérifier l’état d’un service Microsoft Fax s’exécutant sur Windows 2000.


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



L’exemple de code suivant vérifie l’état d’un service Microsoft Fax s’exécutant sur Windows 2000.


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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>IADs. h</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>  |
| IID<br/>                      | IID \_ IADsServiceOperations est défini en tant que 5D7B33F0-31CA-11CF-A98A-00AA006BC149<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IADsFileService**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)
</dt> <dt>

[**IADsFileServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations)
</dt> <dt>

[**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)
</dt> </dl>

 

 





