---
description: SWbemServices. ExecMethodAsync, méthode-exécute une méthode exportée par un fournisseur de méthode.
ms.assetid: 933a4c64-7538-474e-9f6f-f94da6066b46
ms.tgt_platform: multiple
title: SWbemServices. ExecMethodAsync, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: fcdcd70b567a737cb8686ac841dc1ce0b55d3996
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403465"
---
# <a name="swbemservicesexecmethodasync-method"></a>SWbemServices. ExecMethodAsync, méthode

La méthode **ExecMethodAsync** de l’objet [**SWbemServices**](swbemservices.md) exécute une méthode qui est exportée par un fournisseur de méthode. L’appel retourne immédiatement au client tandis que les paramètres entrants sont transmis au fournisseur approprié dans lequel la méthode s’exécute. Les informations et l’État sont retournés à l’appelant via des événements remis au récepteur spécifié dans *objWbemSink*. le fournisseur, plutôt que Windows Management Instrumentation (WMI), implémente la méthode.

La méthode est appelée en mode asynchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

Pour plus d’informations et pour obtenir une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
SWbemServices.ExecMethodAsync( _
  ByVal objWbemSink, _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*objWbemSink* 
</dt> <dd>

Obligatoire. Créez un objet [**SWbemSink**](swbemsink.md) pour recevoir les objets. Récepteur d’objets qui reçoit le résultat de l’appel de méthode. Les paramètres sortants sont envoyés à l’événement [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) du récepteur d’objets fourni. Les résultats du mécanisme d’appel sont envoyés à l’événement [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) du récepteur d’objets fourni. N’oubliez pas que **SWbemSink. OnCompleted** ne reçoit pas le code de retour de la méthode WMI. Toutefois, elle reçoit le code de retour du mécanisme réel de retour d’appel et est utile uniquement pour vérifier que l’appel s’est produit ou qu’il a échoué pour des raisons mécaniques. Le code de résultat retourné par la méthode WMI est retourné dans l’objet de paramètre sortant fourni à **SWbemSink. OnObjectReady**. Si un code d’erreur est retourné, l’objet [**IWbemObjectSink**](iwbemobjectsink.md) fourni n’est pas utilisé. Si l’appel réussit, l’implémentation **IWbemObjectSink** de l’utilisateur est appelée pour indiquer le résultat de l’opération.

</dd> <dt>

*strObjectPath* 
</dt> <dd>

Obligatoire. Chaîne qui contient le chemin d’accès de l’objet pour lequel la méthode est exécutée. Pour plus d’informations, consultez [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*strMethodName* 
</dt> <dd>

Obligatoire. Nom de la méthode à exécuter.

</dd> <dt>

*objWbemInParams* \[ facultatif\]
</dt> <dd>

Objet [**SWbemObject**](swbemobject.md) qui contient les paramètres d’entrée de la méthode exécutée. Par défaut, ce paramètre n’est pas défini. Pour plus d’informations, consultez [construction d’objets inparamètres et analyse d’objets de paramètres de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

</dd> <dt>

*IFlags* \[ facultatif\]
</dt> <dd>

Entier qui détermine le comportement de l’appel. Ce paramètre peut accepter les valeurs suivantes.

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

*objWbemNamedValueSet* \[ facultatif\]
</dt> <dd>

En général, ce n’est pas défini. Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête. Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.

</dd> <dt>

*objWbemAsyncContext* \[ facultatif\]
</dt> <dd>

Objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui retourne au récepteur d’objets pour identifier la source de l’appel asynchrone d’origine. Utilisez ce paramètre si vous effectuez plusieurs appels asynchrones à l’aide du même récepteur d’objets. Pour utiliser ce paramètre, créez un objet **SWbemNamedValueSet** et utilisez la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) pour ajouter une valeur qui identifie l’appel asynchrone que vous effectuez. Cet objet **SWbemNamedValueSet** est retourné au récepteur d’objets et la source de l’appel peut être extraite à l’aide de la méthode [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) . Pour plus d’informations, consultez [création d’un appel asynchrone avec VBScript](making-an-asynchronous-call-with-vbscript.md).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur. Si l’appel réussit, un objet de [**paramètres de paramètre**](swbemmethod-outparameters.md) , qui est également un [**SWbemObject**](swbemobject.md) est fourni au récepteur spécifié dans *objWbemSink*. L’objet de **paramètres** de sortie retournés contient les paramètres de sortie et la valeur de retour pour la méthode en cours d’exécution. Pour plus d’informations, consultez [construction d’objets inparamètres et analyse d’objets de paramètres de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

## <a name="error-codes"></a>Codes d’erreur

Une fois la méthode **ExecMethodAsync** terminée, l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erreur non spécifiée.

</dd> <dt>

**wbemErrInvalidClass** -2147749904 (0x80041010)
</dt> <dd>

La classe spécifiée n’est pas valide.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Un paramètre spécifié n’est pas valide.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Mémoire insuffisante pour terminer l’opération.

</dd> <dt>

**wbemErrInvalidMethod** -2147749934 (0x8004102E)
</dt> <dd>

La méthode demandée n’était pas disponible.

</dd> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

L’utilisateur actuel n’a pas été autorisé à exécuter la méthode.

</dd> </dl>

## <a name="remarks"></a>Notes

Si la méthode exécutée a des paramètres d’entrée, [**l’objet**](swbemmethod-inparameters.md) InParameters dans le paramètre *objWbemInParam* doit être le même que la description dans les rubriques construire des objets inserts [et analyse des objets de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md) .

Utilisez **SWbemServices. ExecMethodAsync** comme alternative à l’accès direct pour l’exécution d’une [*méthode de fournisseur*](gloss-p.md) lorsqu’il n’est pas possible d’exécuter une méthode directement. Par exemple, utilisez-le avec un langage de script qui ne prend pas en charge les paramètres de sortie, autrement dit, si votre méthode a des paramètres de sortie. Dans le cas contraire, il est recommandé d’utiliser l’accès direct pour appeler une méthode. Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md).

La méthode **SWbemServices. ExecMethodAsync** requiert un chemin d’accès à l’objet. Si le script contient déjà un objet [**SWbemObject**](swbemobject.md) , vous pouvez appeler [**SWbemObject. ExecMethodAsync**](swbemobject-execmethodasync-.md).

Cet appel est retourné immédiatement. Les informations d’État sont retournées à l’appelant via les rappels remis au récepteur spécifié dans *objWbemSink*. Pour poursuivre le traitement lorsque l’appel est terminé, implémentez une sous-routine pour *objWbemSink*. Événement [**OnCompleted**](swbemsink-oncompleted.md) .

Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur. Cela pose des risques de sécurité pour vos scripts et vos applications. Pour plus d’informations sur la façon d’éliminer les risques, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).

Utilisez le paramètre *objWbemAsyncContext* pour vérifier la source d’un appel.

## <a name="examples"></a>Exemples

L’exemple de code suivant montre la méthode **ExecMethodAsync** . le script crée un [**objet \_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) qui représente un processus en cours d’exécution Bloc-notes. Il illustre la configuration d’un objet [**Parameters**](swbemmethod-inparameters.md) et l’obtention des résultats d’un objet de [**paramètres de paramètres**](swbemmethod-outparameters.md) . Pour obtenir un script qui montre les mêmes opérations exécutées de façon synchrone, consultez [**SWbemServices. ExecMethod**](swbemservices-execmethod.md). Pour obtenir un exemple d’utilisation de l’accès direct, consultez [créer une méthode dans la classe \_ processus Win32](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Pour obtenir un exemple de la même opération à l’aide de [**SWbemObject**](swbemobject.md), consultez [**SWbemObject. ExecMethodAsync**](swbemobject-execmethodasync-.md).


```VB
' Connect to WMI.
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object
' of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter required
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object, so SWbemObject.SpawnInstance_ 
' can be called to create it.

Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

' Create sink to receive event resulting
' from the ExecMethodAsync call.
set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink","Sink_")

' Call SWbemServices.ExecMethodAsync
' with the WMI path Win32_Process.

bDone = false
Services.ExecMethodAsync Sink, _
     "Win32_Process", "Create", oInParams

' Call the Win32_Process.Create method asynchronously.
' Set up a wait so the results of the method
' execution can be returned to 
' the sink subroutines.

while not bDone    
    wscript.sleep 1000  
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _ 
        &VBCR & "ReturnValue = " _
        & oOutParams.ReturnValue &VBCR & _
        "ProcessId = " & oOutParams.ProcessId
end sub

sub Sink_OnCompleted(HResult, LastErrorObj, oContext)
    wscript.echo "Sink_OnCompleted subroutine, hresult = " _
        & hex(HResult)
    bdone = true
end sub
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

[**SWbemObject. ExecMethod\_**](swbemobject-execmethod-.md)
</dt> <dt>

[**SWbemObject. ExecMethodAsync\_**](swbemobject-execmethodasync-.md)
</dt> <dt>

[**SWbemServices. ExecMethod**](swbemservices-execmethod.md)
</dt> <dt>

[Appel d’une méthode de fournisseur](calling-a-provider-method.md)
</dt> <dt>

[Manipulation des informations relatives aux classes et aux instances](manipulating-class-and-instance-information.md)
</dt> </dl>

 

