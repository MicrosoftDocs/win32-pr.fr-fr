---
description: L’événement OnCompleted d’un objet SWbemSink est déclenché lorsqu’un appel asynchrone est terminé. Cet événement indique à l’application cliente le résultat d’une opération asynchrone et fournit des informations d’erreur lorsque l’appel asynchrone échoue.
ms.assetid: 2723185d-5b8b-4cc7-ada3-51c3275272a9
ms.tgt_platform: multiple
title: 'ISWbemSinkEvents :: OnCompleted, événement (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnCompleted
- ISWbemSinkEvents.OnCompleted
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 16cb0362b5c1b1d432d72bb959103adbb7315069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114850"
---
# <a name="iswbemsinkeventsoncompleted-event"></a>Événement ISWbemSinkEvents :: OnCompleted

L’événement **OnCompleted** d’un objet [**SWbemSink**](swbemsink.md) est déclenché lorsqu’un appel asynchrone est terminé. Cet événement indique à l’application cliente le résultat d’une opération asynchrone et fournit des informations d’erreur lorsque l’appel asynchrone échoue.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
SWbemSink.OnCompleted( _
  ByVal iHResult, _
  ByVal objWbemErrorObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*iHResult* 
</dt> <dd>

HRESULT de la méthode asynchrone terminée. HRESULT est identique à la valeur retournée à partir d’une [API com](com-api-for-wmi.md) équivalente pour l’appel de méthode WMI. Vérifiez cette valeur pour déterminer si l’appel asynchrone a réussi ou non. Si l’appel asynchrone réussit, ce paramètre contient WBEM \_ S \_ no \_ Error (0). Si l’appel asynchrone échoue, ce paramètre contient un code d’erreur.

</dd> <dt>

*objWbemErrorObject* 
</dt> <dd>

Contient un objet [**SWbemLastError**](swbemlasterror.md) en cas d’échec de la méthode asynchrone.

</dd> <dt>

*objWbemAsyncContext* 
</dt> <dd>

Il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui est passé à l’appel asynchrone d’origine. Utilisez ce paramètre pour identifier l’origine de l’appel asynchrone qui déclenche cet événement lorsque plusieurs appels asynchrones sont effectués à l’aide de ce récepteur d’objets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Une fois l’événement **OnCompleted** terminé, l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur ci-dessous.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erreur non spécifiée.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Mémoire insuffisante pour terminer l’opération.

</dd> <dt>

**wbemErrTransportFailure** -2147749909 (0x80041015)
</dt> <dd>

Une erreur réseau s’est produite, empêchant le fonctionnement normal.

</dd> </dl>

## <a name="remarks"></a>Notes

Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur. Cela pose des risques de sécurité pour vos scripts et vos applications. Pour éliminer les risques, utilisez une communication semi-synchrone ou synchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Wbemdisp. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSink<br/>                                                             |
| IID<br/>                      | IID \_ ISWbemSinkEvents<br/>                                                        |



 

