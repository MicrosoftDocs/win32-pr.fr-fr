---
description: La \_ méthode ExecMethodAsync de SWbemObject exécute de manière asynchrone une méthode exportée par un fournisseur de méthode.
ms.assetid: b848b38b-c0c3-49cd-b1e2-b0a440b82d61
ms.tgt_platform: multiple
title: SWbemObject.Exeméthode cMethodAsync_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 37d7a0ab0b2e4d1ab893619eda4b3d32b8b4e1f60791e0981125d4445bda5f98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857349"
---
# <a name="swbemobjectexecmethodasync_-method"></a>SWbemObject.Exe\_ méthode cMethodAsync

La **méthode \_ ExecMethodAsync** de [**SWbemObject**](swbemobject.md) exécute de manière asynchrone une méthode exportée par un fournisseur de méthode. Cette méthode est similaire à [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md), mais fonctionne directement sur l’objet de la méthode à exécuter. Windows WMI (Management Instrumentation) n’implémente pas cette méthode. Le fournisseur implémente cette méthode.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objOutParams = .ExecMethodAsync_( _
  ByVal objWbemSink, _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*objWbemSink* \[ dans\]
</dt> <dd>

Obligatoire. Il s’agit du récepteur d’objets qui reçoit les résultats de l’appel de la méthode. Les paramètres sortants sont envoyés à l’événement [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) du récepteur d’objets fourni. Les résultats du mécanisme d’appel sont envoyés à l’événement [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) du récepteur d’objets fourni. Notez que **SWbemSink. OnCompleted** ne reçoit pas le code de retour de la méthode. Toutefois, il reçoit le code de retour du mécanisme réel de retour d’appel et est utile uniquement pour vérifier que l’appel s’est produit ou qu’il a échoué pour des raisons mécaniques. Le code de résultat retourné par la méthode est retourné dans l’objet de paramètre sortant fourni à **SWbemSink. OnObjectReady**. Si un code d’erreur est retourné, l’objet [**IWbemObjectSink**](iwbemobjectsink.md) fourni n’est pas utilisé. Si l’appel réussit, l’implémentation **IWbemObjectSink** de l’utilisateur est appelée pour indiquer le résultat de l’opération.

</dd> <dt>

*strMethodName* \[ dans\]
</dt> <dd>

Obligatoire. Il s’agit du nom de la méthode pour l’objet.

</dd> <dt>

*objwbemInParams* \[ dans, facultatif\]
</dt> <dd>

Il s’agit d’un objet [**SWbemObject**](swbemobject.md) qui contient les paramètres d’entrée de la méthode en cours d’exécution. Par défaut, ce paramètre n’est pas défini. Pour plus d’informations, consultez [construction d’objets inparamètres](constructing-inparameters-objects.md) et [analyse d’objets de paramètres de paramètres](parsing-outparameters-objects.md).

</dd> <dt>

*IFlags* \[ dans, facultatif\]
</dt> <dd>

Entier qui détermine le comportement de l’appel. Ce paramètre peut accepter les valeurs suivantes.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus * * * * (128 (0x80))


</dt> <dd>

Fait en sorte que les appels asynchrones envoient des mises à jour d’État au gestionnaire d’événements [**SWbemSink. OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus * * * * (0 (0x0))


</dt> <dd>

Empêche les appels asynchrones d’envoyer des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ dans, facultatif\]
</dt> <dd>

En règle générale, il n’est pas défini. Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête. Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.

</dd> <dt>

*objWbemAsyncContext* \[ dans, facultatif\]
</dt> <dd>

Il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui retourne au récepteur d’objets pour identifier la source de l’appel asynchrone d’origine. Utilisez ce paramètre si vous effectuez plusieurs appels asynchrones à l’aide du même récepteur d’objets. Pour utiliser ce paramètre, créez un objet **SWbemNamedValueSet** et utilisez la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) pour ajouter une valeur qui identifie l’appel asynchrone que vous effectuez. Cet objet **SWbemNamedValueSet** est retourné au récepteur d’objets et la source de l’appel peut être extraite à l’aide de la méthode [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) . Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode n’a pas de valeur de retour. Si l’appel réussit, un objet de [**paramètres de paramètre**](swbemmethod-outparameters.md) , qui est également un objet [**SWbemObject**](swbemobject.md) , est fourni au récepteur spécifié dans *objWbemSink*. L’objet de **paramètres** de sortie retournés contient les paramètres de sortie et la valeur de retour pour la méthode en cours d’exécution.

## <a name="error-codes"></a>Codes d’erreur

Une fois la méthode **ExecMethodAsync \_** terminée, l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

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

## <a name="remarks"></a>Remarques

Utilisez la méthode **SWbemObject.Exe\_ cMethodAsync** comme alternative à l’accès direct pour l’exécution d’une [*méthode de fournisseur*](gloss-p.md) lorsque vous ne pouvez pas exécuter une méthode directement. Par exemple, si votre méthode a des paramètres out, utilisez la méthode **SWbemObject.ExecMethodAsync \_** avec un langage de script qui ne prend pas en charge les paramètres de sortie. Dans le cas contraire, il est recommandé d’appeler une méthode à l’aide d’un accès direct. Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md).

Cet appel est retourné immédiatement. Les objets et l’État demandés sont retournés à l’appelant via des rappels remis au récepteur spécifié dans *objWbemSink*. Pour traiter chaque objet lorsqu’il arrive, créez un *objWbemSink*. Sous-routine d’événement [**OnObjectReady**](swbemsink-onobjectready.md) . Une fois que tous les objets sont retournés, vous pouvez effectuer le traitement final dans votre implémentation de *objWbemSink*. Événement [**OnCompleted**](swbemsink-oncompleted.md) .

Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur. Cela pose des risques de sécurité pour vos scripts et vos applications. Pour éliminer les risques, utilisez une communication semi-synchrone ou une communication synchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

Si la méthode en cours d’exécution a des paramètres d’entrée, l’objet [**Parameters**](swbemmethod-inparameters.md) et le paramètre *objWbemInParam* doivent être construits comme décrit dans [construction d’objets inparamètres](constructing-inparameters-objects.md) et [analyse d’objets de paramètres](parsing-outparameters-objects.md)de sortie.

La méthode **SWbemObject.Exe\_ cMethodAsync** suppose que l’objet représenté par [**SWbemObject**](swbemobject.md) contient la méthode à exécuter. La méthode [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) requiert un chemin d’accès à un objet.

## <a name="examples"></a>Exemples

L’exemple suivant illustre la méthode [**ExecMethodAsync**](swbemservices-execmethodasync.md) . le script crée un [**objet \_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) qui représente un processus en cours d’exécution Bloc-notes. Il illustre la configuration d’un objet [**Parameters**](swbemmethod-inparameters.md) et explique comment obtenir les résultats d’un objet de [**paramètres de paramètres**](swbemmethod-outparameters.md) .

Pour obtenir un script qui montre les mêmes opérations exécutées de façon synchrone, consultez [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md). Pour obtenir un exemple d’utilisation de l’accès direct, consultez [**créer une méthode dans la classe \_ processus Win32**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Pour obtenir un exemple de la même opération à l’aide d’un objet [**SWbemServices**](swbemservices.md) , consultez [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).


```VB
On Error Resume Next

'Get a Win32_Process class description
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_
' can be called to create it.
Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_

' Specify the name of the process to be run.
oInParams.CommandLine = "Notepad.exe"

' Create a sink to receive event resulting
' from the ExecMethodAsync call.
Set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink", "Sink_")

' Call the Win32_Process.Create method asynchronously. Set up a 
' wait so the results of the method execution can be returned to 
' the sink subroutines.
bDone = false

' Call SWbemObject.ExecMethodAsync on the oProcess object.
oProcess.ExecMethodAsync_ Sink, "Create", oInParams, 0 
' 
while not bDone
    wscript.sleep 1000
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _
    & VBNewLine & "ReturnValue = " _
    & oOutParams.ReturnValue & VBNewLine & _
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
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**M**](swbemobject.md)
</dt> <dt>

[**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)
</dt> </dl>

 

