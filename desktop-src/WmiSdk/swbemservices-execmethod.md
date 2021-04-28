---
description: SWbemServices.Exeméthode cMethod-exécute une méthode exportée par un fournisseur de méthode.
ms.assetid: 2637efdc-fde5-4a44-a41f-67e0fb0df19d
ms.tgt_platform: multiple
title: SWbemServices.Exeméthode cMethod (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethod
- ISWbemServices.ExecMethod
- ISWbemServices.ExecMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 452c42c37e8dcb9f2b37b660b1f8899e587b5579
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103637"
---
# <a name="swbemservicesexecmethod-method"></a>SWbemServices.Exeméthode cMethod

La méthode **ExecMethod** de l’objet [**SWbemServices**](swbemservices.md) exécute une méthode qui est exportée par un fournisseur de méthode. Cette méthode bloque pendant l’exécution de la méthode qui est transférée au fournisseur approprié. Les informations et l’État sont ensuite renvoyés. Au lieu de WMI, le fournisseur implémente la méthode.

Cette méthode est appelée en mode synchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objOutParams = .ExecMethod( _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strObjectPath* 
</dt> <dd>

Obligatoire. Chaîne qui contient le chemin d’accès de l’objet pour lequel la méthode est exécutée. Pour plus d’informations, consultez [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*strMethodName* 
</dt> <dd>

Obligatoire. Nom de la méthode pour l’objet.

</dd> <dt>

*objWbemInParams* \[ facultatif\]
</dt> <dd>

Objet [**SWbemObject**](swbemobject.md) qui contient les paramètres d’entrée de la méthode en cours d’exécution. Par défaut, ce paramètre n’est pas défini. Pour plus d’informations, consultez [construction d’objets inparamètres et analyse d’objets de paramètres de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

</dd> <dt>

*IFlags* \[ facultatif\]
</dt> <dd>

Réservé. Cette valeur doit être zéro.

</dd> <dt>

*objWbemNamedValueSet* \[ facultatif\]
</dt> <dd>

En général, ce n’est pas défini. Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête. Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Si la méthode réussit, un objet [**SWbemObject**](swbemobject.md) est retourné. L’objet retourné contient les paramètres de sortie et la valeur de retour pour la méthode en cours d’exécution.

## <a name="error-codes"></a>Codes d’erreur

Une fois la méthode **ExecMethod** terminée, l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

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

Utilisez **SWbemServices.ExecMethod** comme alternative à l’accès direct pour l’exécution d’une [*méthode de fournisseur*](gloss-p.md) dans les cas où il n’est pas possible d’exécuter une méthode directement. La méthode **ExecMethod** vous permet d’obtenir des paramètres de sortie, si le fournisseur les fournit, à l’aide d’un langage de script qui ne prend pas en charge les paramètres de sortie. Dans le cas contraire, les méthodes recommandées pour appeler une méthode consiste à utiliser l’accès direct. Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md).

Par exemple, l’exemple de code suivant qui appelle la méthode du fournisseur [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) dans le [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service) utilise l’accès direct.


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



Cet exemple appelle **SWbemServices.ExecMethod** pour exécuter la méthode [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) . Notez qu’un chemin d’accès à l’objet est requis, car **SWbemServices.ExecMethod** ne fonctionne pas déjà sur l’objet, contrairement à [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).


```VB
Set WbemServices = GetObject("winmgmts:")
Set oService = GetObject("winmgmts:Win32_Service='Alerter'")
Set oPath = GetObject("winmgmts:Win32_Service='Alerter'").Path_
WbemServices.ExecMethod oPath, "StartService"
```



La méthode **SWbemServices.ExecMethod** requiert un chemin d’accès à un objet. Si le script contient déjà un objet [**SWbemObject**](swbemobject.md) , utilisez la méthode [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md) .

## <a name="examples"></a>Exemples

L’exemple suivant illustre la méthode **ExecMethod** . Le script crée un [**objet \_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) qui représente un processus qui exécute le bloc-notes. Il illustre la configuration d’un objet [**Parameters**](swbemmethod-inparameters.md) et l’obtention des résultats d’un objet de [**paramètres de paramètres**](swbemmethod-outparameters.md) . Pour obtenir un script qui montre les mêmes opérations exécutées de façon asynchrone, consultez [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md). Pour obtenir un exemple d’utilisation de l’accès direct, consultez [créer une méthode dans la classe \_ processus Win32](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Pour obtenir un exemple de la même opération à l’aide d’un [**SWbemObject**](swbemobject.md), consultez [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).


```VB
' Connect to WMI
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains obtains a class object that
' defines the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_ 
'can be called to create it.

Set oInParams = _
    oProcess.Methods_("Create").InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

'Call SWbemServices.ExecMethod with the WMI path Win32_Process
Set oOutParams = _
    Services.ExecMethod( "Win32_Process", "Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully."
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed" _
            & " but had error " _
            & "0x" & hex(oOutParams.ReturnValue)
    End If
End If
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

[**SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md)
</dt> <dt>

[Appel d’une méthode de fournisseur](calling-a-provider-method.md)
</dt> <dt>

[Manipulation des informations relatives aux classes et aux instances](manipulating-class-and-instance-information.md)
</dt> </dl>

 

