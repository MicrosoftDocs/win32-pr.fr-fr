---
title: Méthodes de propriété IADsService (IADs. h)
description: Lisez et écrivez les propriétés décrites dans cette rubrique.
ms.assetid: ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsService ADSI
topic_type:
- apiref
api_name:
- IADsService Property Methods
- IADsService.Dependencies
- IADsService.get_Dependencies
- IADsService.put_Dependencies
- IADsService.DisplayName
- IADsService.get_DisplayName
- IADsService.put_DisplayName
- IADsService.ErrorControl
- IADsService.get_ErrorControl
- IADsService.put_ErrorControl
- IADsService.HostComputer
- IADsService.get_HostComputer
- IADsService.put_HostComputer
- IADsService.LoadOrderGroup
- IADsService.get_LoadOrderGroup
- IADsService.put_LoadOrderGroup
- IADsService.Path
- IADsService.get_Path
- IADsService.put_Path
- IADsService.ServiceAccountName
- IADsService.get_ServiceAccountName
- IADsService.put_ServiceAccountName
- IADsService.ServiceAccountPath
- IADsService.get_ServiceAccountPath
- IADsService.put_ServiceAccountPath
- IADsService.ServiceType
- IADsService.get_ServiceType
- IADsService.put_ServiceType
- IADsService.StartType
- IADsService.get_StartType
- IADsService.put_StartType
- IADsService.StartupParameters
- IADsService.get_StartupParameters
- IADsService.put_StartupParameters
- IADsService.Version
- IADsService.get_Version
- IADsService.put_Version
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b0e0d8b09618c7346280697843281ca74536c11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512801"
---
# <a name="iadsservice-property-methods"></a>Méthodes de propriété IADsService

Les méthodes de propriété de l’interface [**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice) lisent et écrivent les propriétés décrites dans cette rubrique. Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).

## <a name="properties"></a>Propriétés

<dl> <dt>

**Dépendances**
</dt> <dd> <dl>

Tableau de noms **BSTR** de services ou de groupes de charge qui doivent être chargés pour que ce service soit chargé. La syntaxe de l’entrée est « service : », suivie du nom du service ou « Group : », suivi du nom du groupe de charge.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **variante**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Dependencies(
  [out] VARIANT* pvServiceDepend
);
HRESULT put_Dependencies(
  [in] VARIANT vServiceDepend
);
```


</dt> </dl> </dd> <dt>

**DisplayName**
</dt> <dd> <dl>

Nom convivial du service.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DisplayName(
  [out] BSTR* pbstrDisplayName
);
HRESULT put_DisplayName(
  [in] BSTR bstrDisplayName
);
```


</dt> </dl> </dd> <dt>

**ErrorControl**
</dt> <dd> <dl>

Action à effectuer en cas d’échec de ce service au démarrage. Les valeurs valides pour cette propriété sont les suivantes.

<dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>\_erreur de service ADS \_ \_ ignorée * * * *


</dt> <dd>

Le programme de démarrage consigne l’erreur, mais poursuit l’opération de démarrage.

</dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>\_erreur de service ADS \_ \_ normale * * * *


</dt> <dd>

Le programme de démarrage consigne l’erreur et affiche une boîte de message, mais poursuit l’opération de démarrage.

</dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>\_erreur de service ADS \_ \_ critique * * * *


</dt> <dd>

Le programme de démarrage consigne l’erreur. Si la dernière bonne configuration connue est démarrée, l’opération de démarrage continue. Dans le cas contraire, le système est redémarré avec la dernière bonne configuration connue.

</dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>\_erreur de service ADS \_ \_ critique * * * *


</dt> <dd>

Le programme de démarrage consigne l’erreur, si possible. Si la dernière bonne configuration connue est en cours de démarrage, l’opération de démarrage échoue. Dans le cas contraire, le système est redémarré avec la dernière bonne configuration connue.

</dd> </dl> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ErrorControl(
  [out] LONG* plErrorControl
);
HRESULT put_ErrorControl(
  [in] LONG lErrorControl
);
```


</dt> </dl> </dd> <dt>

**HostComputer**
</dt> <dd> <dl>

Chaîne ADsPath de l’hôte de ce service.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **BSTR**
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

**LoadOrderGroup**
</dt> <dd> <dl>

Nom du groupe d’ordre de chargement dont ce service est membre.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LoadOrderGroup(
  [out] BSTR* pbstrLoadOrderGroup
);
HRESULT put_LoadOrderGroup(
  [in] BSTR bstrLoadOrderGroup
);
```


</dt> </dl> </dd> <dt>

**Chemin d’accès**
</dt> <dd> <dl>

Chemin d’accès et nom de fichier du fichier exécutable de ce service.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> <dt>

**ServiceAccountName**
</dt> <dd> <dl>

Nom du compte utilisé par ce service pour s’authentifier au démarrage.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountName(
  [out] BSTR* pbstrServiceAccountName
);
HRESULT put_ServiceAccountName(
  [in] BSTR bstrServiceAccountName
);
```


</dt> </dl> </dd> <dt>

**ServiceAccountPath**
</dt> <dd> <dl>

Chemin d’accès du compte spécifié par la propriété **ServiceAccountPath** .

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountPath(
  [out] BSTR* pbstrServiceAccountPath
);
HRESULT put_ServiceAccountPath(
  [in] BSTR bstrServiceAccountPath
);
```


</dt> </dl> </dd> <dt>

**ServiceType**
</dt> <dd> <dl>

Description de la façon dont un service s’affiche sur l’ordinateur hôte. Cette propriété peut avoir la valeur zéro ou une combinaison d’une ou plusieurs des valeurs suivantes.

<dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

\_ \_ Pilote du noyau du service ADS \_ * * * (0x00000001)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

\_Pilote du \_ système de fichiers du service ADS * * * * \_ \_ (0x00000002)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

\_Processus propre au service ADS \_ \_ * * * * (0x00000010)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

\_ \_ \_ Processus de partage de service ADS * * * * (0x00000020)


</dt> <dd></dd> </dl> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceType(
  [out] LONG* plServiceType
);
HRESULT put_ServiceType(
  [in] LONG lServiceType
);
```


</dt> </dl> </dd> <dt>

**Type de démarrage**
</dt> <dd> <dl>

Détermine comment démarrer le service. Les valeurs valides pour cette propriété sont les suivantes.

<dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>démarrage du \_ démarrage du service ADS \_ \_ * * * *


</dt> <dd>

Le service est un pilote de périphérique Démarré par le chargeur du système. Cette valeur est uniquement valide pour les services de pilote.

</dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>\_démarrage du système de service ADS \_ \_ * * * *


</dt> <dd>

Le service est un pilote de périphérique Démarré par la fonction **IoInitSystem** . Cette valeur est uniquement valide pour les services de pilote.

</dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>\_démarrage automatique du service ADS \_ \_ * * * *


</dt> <dd>

Le service est démarré automatiquement par le gestionnaire de contrôle des services lors du démarrage du système.

</dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>\_démarrage de \_ la demande de service ADS \_ * * * *


</dt> <dd>

Le service est démarré par le gestionnaire de contrôle des services lorsqu’un processus appelle la fonction [**StartService**](/windows/desktop/api/winsvc/nf-winsvc-startservicea) .

</dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>\_service ADS \_ désactivé * * * *


</dt> <dd>

Le service ne peut pas être démarré. Les tentatives de démarrage du service entraînent la **\_ \_ désactivation du service d’erreur** de code d’erreur.

</dd> </dl> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartType(
  [out] LONG* plStartType
);
HRESULT put_StartType(
  [in] LONG lStartType
);
```


</dt> </dl> </dd> <dt>

**StartupParameters**
</dt> <dd> <dl>

Paramètres passés au service au démarrage.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartupParameters(
  [out] BSTR* pbstrStartupParameters
);
HRESULT put_StartupParameters(
  [in] BSTR bstrStartupParameters
);
```


</dt> </dl> </dd> <dt>

**Version**
</dt> <dd> <dl>

Version du service.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Version(
  [out] BSTR* pbstrVersion
);
HRESULT put_Version(
  [in] BSTR bstrVersion
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Exemples

L’exemple de code suivant montre comment répertorier tous les services système disponibles qui s’exécutent sur l’ordinateur hôte, « monordinateur », ainsi que l’emplacement où trouver les exécutables des services.


```VB
Dim cp As IADsComputer
On Error GoTo Cleanup

Set cp = GetObject("WinNT://myMachine,computer")
If (IsEmpty(cp) = False) Then
    cp.Filter = Array("Service")
    For Each service In cp
        MsgBox service.Name & " @" & service.path
    Next
End if

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cp = Nothing
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsService est défini en tant que 68AF66E0-31CA-11CF-A98A-00AA006BC149<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[Méthodes de propriété d’interface](interface-property-methods.md)
</dt> </dl>

 

