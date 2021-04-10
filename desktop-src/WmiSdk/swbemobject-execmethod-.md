---
description: La \_ méthode ExecMethod de l’objet SWbemObject exécute une méthode exportée par un fournisseur de méthode.
ms.assetid: 39a8a6e7-b499-410a-8c27-d4a05d1a61b9
ms.tgt_platform: multiple
title: SWbemObject.Exeméthode cMethod_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6b71d88a113e515d50ac01a23f070714fa467615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114867"
---
# <a name="swbemobjectexecmethod_-method"></a>SWbemObject.Exe\_ méthode cMethod

La **méthode \_ ExecMethod** de l’objet [**SWbemObject**](swbemobject.md) exécute une méthode exportée par un fournisseur de méthode.

Cette méthode s’interrompt pendant l’exécution de la méthode qui est transférée au fournisseur approprié. Les informations et l’État sont ensuite renvoyés. Le fournisseur plutôt que WMI implémente la méthode.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objOutParams = .ExecMethod_( _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strMethodName* \[ dans\]
</dt> <dd>

Obligatoire. Nom de la méthode pour l’objet.

</dd> <dt>

*objwbemInParams* \[ dans, facultatif\]
</dt> <dd>

Il s’agit d’un objet [**SWbemObject**](swbemobject.md) qui contient les paramètres d’entrée de la méthode en cours d’exécution. Par défaut, ce paramètre n’est pas défini. Pour plus d’informations, consultez [construction d’objets inparamètres et analyse d’objets de paramètres de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

</dd> <dt>

*IFlags* \[ dans, facultatif\]
</dt> <dd>

Réservé et doit avoir la valeur 0 (zéro) si elle est spécifiée.

</dd> <dt>

*objwbemNamedValueSet* \[ dans, facultatif\]
</dt> <dd>

En règle générale, il n’est pas défini. Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête. Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode réussit, un objet [**SWbemObject**](swbemobject.md) retourne. L’objet retourné contient les paramètres de sortie et la valeur de retour pour la méthode en cours d’exécution.

## <a name="error-codes"></a>Codes d’erreur

Une fois la méthode **ExecMethod \_** terminée, l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

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

Cette méthode est similaire à [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), mais elle fonctionne directement sur l’objet dont la méthode doit être exécutée. Par exemple, l’exemple de code suivant appelle la méthode du fournisseur [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) dans le [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service) et utilise l' [accès direct](manipulating-class-and-instance-information.md).


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



Cette version appelle **SWbemObject.ExecMethod \_** pour exécuter la méthode [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) .


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
Set outParam = process.ExecMethod_("StartService")
```



Utilisez **SWbemObject.ExecMethod \_** comme alternative à l’accès direct pour l’exécution d’une [*méthode de fournisseur*](gloss-p.md) dans les cas où il n’est pas possible d’exécuter une méthode directement. Par exemple, vous pouvez utiliser **SWbemObject.ExecMethod \_** avec un langage de script qui ne prend pas en charge les paramètres de sortie si votre méthode a des paramètres de sortie. Dans le cas contraire, les méthodes recommandées pour appeler une méthode consiste à utiliser l’accès direct.

-   La méthode **SWbemObject.Exe\_ cMethod** suppose que l’objet représenté par [**SWbemObject**](swbemobject.md) contient la méthode à exécuter. En revanche, [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) requiert un chemin d’accès à l’objet. Utilisez **SWbemObject.ExecMethod \_** si vous avez déjà obtenu l’objet dont vous souhaitez exécuter la méthode.

## <a name="examples"></a>Exemples

L’exemple suivant illustre la méthode [**ExecMethod**](swbemservices-execmethod.md) . Le script crée un [**objet \_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) représentant un processus qui exécute le bloc-notes. Pour plus d’informations sur un script illustrant les mêmes opérations exécutées de façon asynchrone, consultez [**SWbemObject.ExecMethodAsync \_**](swbemobject-execmethodasync-.md). Pour obtenir un exemple d’utilisation de l’accès direct, consultez [**créer une méthode dans la classe \_ processus Win32**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) . Pour obtenir un exemple de la même opération à l’aide d’un objet [**SWbemServices**](swbemservices.md) , consultez **SWbemServices.ExecMethod**.


```VB
' Connect to WMI and obtain a Win32_Process object.
' This is also an SWbemObject object.
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters
' object to hold the input parameter needed
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
Set oOutParams = oProcess.ExecMethod_("Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully"
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed but had error" _
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
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**M**](swbemobject.md)
</dt> <dt>

[**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md)
</dt> <dt>

[**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
</dt> </dl>

 

