---
description: Exécute une requête pour recevoir des événements.
ms.assetid: 0b0e8313-4ffd-4d4a-8965-d2c6743e7573
ms.tgt_platform: multiple
title: SWbemServices.Exeméthode cNotificationQueryAsync (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecNotificationQueryAsync
- ISWbemServices.ExecNotificationQueryAsync
- ISWbemServices.ExecNotificationQueryAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8e2ecddf290d83583b3108620b8b4bb23be7c957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524122"
---
# <a name="swbemservicesexecnotificationqueryasync-method"></a>SWbemServices.Exeméthode cNotificationQueryAsync

La méthode **ExecNotificationQueryAsync** de l’objet [**SWbemServices**](swbemservices.md) exécute une requête pour recevoir des événements. Cet appel est retourné immédiatement et les résultats et l’État sont retournés à l’appelant via des événements remis au récepteur spécifié dans *objWbemSink*.

Les événements spécifiés dans la requête peuvent être des événements intrinsèques Windows Management Instrumentation (WMI), tels que [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md), ou des événements extrinsèques, tels que [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent) ou [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent). Pour plus d’informations, consultez [détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md).

La méthode est appelée en mode asynchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
SWbemServices.ExecNotificationQueryAsync( _
  ByVal objWbemSink, _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*objWbemSink* 
</dt> <dd>

Obligatoire. Récepteur d’objets qui reçoit la notification d’événements de façon asynchrone. Créez un objet [**SWbemSink**](swbemsink.md) pour recevoir les objets.

</dd> <dt>

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

Entier qui détermine le comportement de la requête. Ce paramètre peut être défini sur les valeurs suivantes.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus * * * * (128 (0x80))


</dt> <dd>

Fait en sorte que les appels asynchrones envoient des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus * * * * (0 (0x0))


</dt> <dd>

Empêche les appels asynchrones d’envoyer des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ facultatif\]
</dt> <dd>

En général, ce n’est pas défini. Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui sert la demande. Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.

</dd> <dt>

*objWbemAsyncContext* \[ facultatif\]
</dt> <dd>

Il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui retourne au récepteur d’objets pour identifier la source de l’appel asynchrone d’origine. Utilisez ce paramètre pour effectuer plusieurs appels asynchrones à l’aide du même récepteur d’objets. Pour utiliser ce paramètre, créez un objet **SWbemNamedValueSet** et utilisez la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) pour ajouter une valeur qui identifie l’appel asynchrone que vous effectuez. L’objet **SWbemNamedValueSet** est retourné au récepteur d’objets et la source de l’appel peut être extraite à l’aide de la méthode [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) . Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur. En cas de réussite, le récepteur reçoit un événement [**OnObjectReady**](swbemsink-onobjectready.md) par instance. Après la dernière instance, le récepteur d’objets reçoit un événement [**OnCompleted**](swbemsink-oncompleted.md) .

## <a name="error-codes"></a>Codes d’erreur

À la fin de la méthode **ExecNotificationQueryAsync** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur identifiés dans la liste suivante.

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

Un paramètre non valide est spécifié.

</dd> <dt>

**wbemErrInvalidQuery** -2147749911 (0x80041017)
</dt> <dd>

La syntaxe de la requête n’est pas valide.

</dd> <dt>

**wbemErrInvalidQueryType** -2147749912 (0x80041018)
</dt> <dd>

Le langage de requête demandé n’est pas pris en charge.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Mémoire insuffisante pour terminer l’opération.

</dd> </dl>

## <a name="remarks"></a>Notes

La méthode **ExecNotificationQueryAsync** retourne les objets de type d’événement générés par les événements futurs. Les objets d’événement que les demandes **ExecNotificationQueryAsync** peuvent être intrinsèques (par exemple, [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) ou extrinsèques (par exemple, les événements [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) ou SNMP). Pour plus d’informations, consultez [détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md).

L’appel à **ExecNotificationQueryAsync** retourne immédiatement. Les objets et l’État demandés sont retournés à l’appelant via des rappels remis au récepteur spécifié dans *objWbemSink*. Pour traiter chaque objet lorsqu’il est retourné, créez un *objWbemSink*. Sous-routine d’événement [**OnObjectReady**](swbemsink-onobjectready.md) . Une fois tous les objets retournés, effectuez le traitement final pour implémenter le *objWbemSink*. Événement [**OnCompleted**](swbemsink-oncompleted.md) .

Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur. Cela pose des risques de sécurité pour vos scripts et vos applications. Pour éliminer les risques, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).

Il existe des limites concernant le nombre de mots clés **and** et **or** qui peuvent être utilisés dans les requêtes WQL. Un grand nombre de mots clés WQL utilisés dans une requête complexe peut faire en sorte que WMI retourne la valeur HRESULT Asan **HRESULT** du code d’erreur de **\_ \_ \_ violation de quota E WBEM** . La limite des mots clés WQL dépend de la complexité de la requête.

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant montre un script qui attend une notification d’événement WMI indiquant qu’un processus s’est terminé. Il attend un événement intrinsèque WMI, une instance de la classe d’événements [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md). **\_ \_ InstanceDeletionEvent** doit représenter la suppression d’une instance de [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process). Pour plus d’informations sur les événements intrinsèques WMI, consultez [détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md).

Le script suivant s’exécute indéfiniment jusqu’à ce que l’ordinateur soit redémarré, que WMI soit arrêté ou que le script soit arrêté. Pour arrêter le script manuellement, utilisez le gestionnaire des tâches pour arrêter le processus. Pour l’arrêter par programmation, utilisez la méthode [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) dans la classe de \_ processus Win32.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & _strComputer & "\root\CIMV2") 
Set MySink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync MySink, "SELECT * FROM __InstanceCreationEvent WITHIN 1 " _
                                               & "WHERE TargetInstance ISA 'Win32_Process'"

WScript.Echo "Waiting for events..."

While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    WScript.Echo "Event occurred."
End Sub

Sub SINK_OnCompleted(objObject, objAsyncContext)
    WScript.Echo "Event call complete."
End Sub
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

[**SWbemServices.ExecQuery**](swbemservices-execquery.md)
</dt> <dt>

[**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)
</dt> <dt>

[Inscription pour les événements du Registre système](registering-for-system-registry-events.md)
</dt> <dt>

[Détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[Appel d’une méthode](calling-a-method.md)
</dt> <dt>

[Définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md)
</dt> </dl>

 

