---
description: Exécute une requête pour recevoir des événements. L’appel est retourné immédiatement.
ms.assetid: 3e1bb428-5395-4e90-9713-6d96242fef4e
ms.tgt_platform: multiple
title: SWbemServices. ExecNotificationQuery, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 44279d16e180d776dc4433c6d5246eab2419fca6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403464"
---
# <a name="swbemservicesexecnotificationquery-method"></a>SWbemServices. ExecNotificationQuery, méthode

La méthode **ExecNotificationQuery** de l’objet [**SWbemServices**](swbemservices.md) exécute une requête pour recevoir des événements. L’appel est retourné immédiatement. L’utilisateur peut interroger l’énumérateur retourné pour les événements à mesure qu’ils arrivent.

La méthode est appelée en mode semi-synchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objwbemEventsource = .ExecNotificationQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strQuery* 
</dt> <dd>

Obligatoire. Chaîne qui contient le texte de la requête relative aux événements. Ce paramètre ne peut pas être vide. Pour plus d’informations sur la création de chaînes de requête WMI, consultez [interrogation avec WQL](querying-with-wql.md) et la référence [WQL](wql-sql-for-wmi.md) .

</dd> <dt>

*strQueryLanguage* \[ facultatif\]
</dt> <dd>

Chaîne qui contient le langage de requête à utiliser. S’il est spécifié, cette valeur doit être « WQL ».

</dd> <dt>

*IFlags* \[ facultatif\]
</dt> <dd>

Il s’agit d’un entier qui détermine le comportement de la requête. La valeur par défaut est **wbemFlagReturnImmediately**  +  **wbemFlagForwardOnly**. Si vous spécifiez ce paramètre, ce paramètre doit être défini à la fois sur **wbemFlagReturnImmediately** et **wbemFlagForwardOnly** , sinon l’appel échoue. Ce paramètre peut accepter les valeurs suivantes.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly * * * * (32 (0x20))


</dt> <dd>

Entraîne le retour d’un énumérateur avant uniquement. Les énumérateurs avant uniquement sont généralement beaucoup plus rapides et utilisent moins de mémoire que les énumérateurs conventionnels, mais ils n’autorisent pas les appels à [**SWbemObject. Clone \_**](swbemobject-clone-.md).

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately * * * * (16 (0x10))


</dt> <dd>

Provoque le retour immédiat de l’appel.

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ facultatif\]
</dt> <dd>

En général, ce n’est pas défini. Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête. Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si aucune erreur ne se produit, cette méthode retourne un objet [**SWbemEventSource**](swbemeventsource.md) . Vous pouvez appeler la méthode [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md) pour récupérer les événements à mesure qu’ils arrivent.

## <a name="error-codes"></a>Codes d’erreur

À la fin de la méthode **ExecNotificationQuery** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

L’utilisateur actuel n’est pas autorisé à afficher le jeu de résultats.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erreur non spécifiée.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Un paramètre non valide a été spécifié.

</dd> <dt>

**wbemErrInvalidQuery** -2147749911 (0x80041017)
</dt> <dd>

La syntaxe de la requête n’est pas valide.

</dd> <dt>

**wbemErrInvalidQueryType** -2147749912 (0x80041018)
</dt> <dd>

Le langage de la requête demandé n'est pas pris en charge.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Mémoire insuffisante pour terminer l’opération.

</dd> </dl>

## <a name="remarks"></a>Notes

Contrairement à la méthode [**SWbemServices. ExecQueryAsync**](swbemservices-execqueryasync.md) , **ExecNotificationQuery** retourne les objets de type d’événement qui sont générés par des événements futurs plutôt que par des objets existants. Les objets d’événement que les demandes **ExecNotificationQuery** peuvent être intrinsèques (par exemple, [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) ou extrinsèques (tels que les événements de fournisseur de Registre comme les événements [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) ou SNMP). Pour plus d’informations, consultez [détermination du type d’événement pour la réception et la](determining-the-type-of-event-to-receive.md) [réception des notifications d’événements](receiving-event-notifications.md).

Il existe des limites concernant le nombre de mots clés **and** et **or** qui peuvent être utilisés dans les requêtes WQL. Un grand nombre de mots clés WQL utilisés dans une requête complexe peut faire en sorte que WMI retourne le code d’erreur de  **\_ \_ \_ violation de quota E WBEM** en tant que valeur HRESULT. La limite des mots clés WQL dépend de la complexité de la requête.

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant surveille les modifications apportées aux volumes sur un ordinateur local. Notez que [**Win32 \_ VolumeChangeEvent**](/windows/desktop/CIMWin32Prov/win32-volumechangeevent) est un événement extrinsèque qui est défini par un fournisseur qui n’est pas un événement intrinsèque défini par WMI. Pour plus d’informations, consultez [détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md).


```VB
Set colMonitoredEvents = _
   GetObject("Winmgmts:").ExecNotificationQuery_
      ("Select * from Win32_VolumeChangeEvent")

Do While i = 0
   Set strLatestEvent = colMonitoredEvents.NextEvent
   Wscript.Echo strLatestEvent.DriveName & "Time Created = " _
      & strLatestEvent.Time_Created

    Select Case strLatestEvent.EventType 
       Case 1        
            WScript.Echo "EventType = Configuration Changed"
       Case 2
            WScript.Echo "EventType = Device Arrival"
       Case 3
            WScript.Echo "EventType = Device Removal"
       Case 4
            WScript.Echo "EventType = Docking"

       Case Else
            WScript.Echo "Unrecognized EventType"
       End Select
Loop
```



L’exemple de code VBScript suivant surveille la suppression des processus. Si vous supprimez un processus dans le gestionnaire des tâches ou fermez une application, le script affiche un message. Notez que ce script interroge un événement intrinsèque défini par WMI- [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md).


```VB
Set objWMIService = GetObject( _
    "Winmgmts:{impersonationLevel=impersonate}" )
Set colMonitoredProcesses = _
    objWMIService.ExecNotificationQuery( _
    "SELECT * FROM __InstanceDeletionEvent WITHIN 10 WHERE " _
    & "TargetInstance ISA 'Win32_Process'")
i = 0
Do While i < 11
    Set strLatestProcess = colMonitoredProcesses.NextEvent
    WScript.Echo strLatestProcess.TargetInstance.Name
    WScript.Sleep 10000
    i= i + 1
Loop
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**M**](swbemservices.md)
</dt> <dt>

[**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md)
</dt> <dt>

[**SWbemServices. ExecQuery**](swbemservices-execquery.md)
</dt> <dt>

[Réception d’un événement WMI](receiving-a-wmi-event.md)
</dt> <dt>

[Interrogation avec WQL](querying-with-wql.md)
</dt> <dt>

[WQL (SQL pour WMI)](wql-sql-for-wmi.md)
</dt> <dt>

[Détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

