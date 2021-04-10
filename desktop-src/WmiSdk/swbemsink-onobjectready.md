---
description: L’événement OnObjectReady d’un objet SWbemSink est déclenché lorsqu’une opération asynchrone retourne un objet.
ms.assetid: 14110ee7-a808-4786-b695-2ce54189d826
ms.tgt_platform: multiple
title: 'ISWbemSinkEvents :: OnObjectReady, événement (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectReady
- ISWbemSinkEvents.OnObjectReady
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1fa803339e7007a030881c3d5b47d67f354b5661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114846"
---
# <a name="iswbemsinkeventsonobjectready-event"></a>Événement ISWbemSinkEvents :: OnObjectReady

L’événement **OnObjectReady** d’un objet [**SWbemSink**](swbemsink.md) est déclenché lorsqu’une opération asynchrone retourne un objet. Utilisez cet événement pour traiter des objets à partir d’appels asynchrones tels que [**SWbemObject. InstancesAsync \_**](swbemobject-instancesasync-.md) ou [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md). **OnObjectReady** retourne un [**SWbemObject**](swbemobject.md) chaque fois que l’énumération est terminée.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
SWbemSink.OnObjectReady( _
  ByVal objWbemObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*objWbemObject* 
</dt> <dd>

Objet [**SWbemObject**](swbemobject.md) . Cela est similaire à ce qui est retourné par l’équivalent synchrone de l’appel asynchrone qui déclenche cet événement. Par exemple, un appel à la méthode [**SWbemServices. GetAsync**](swbemservices-getasync.md) renvoie un **SWbemObject** dans le *paramètre objWbemObject* de l’événement **OnObjectReady** de l’objet [**SWbemSink**](swbemsink.md) , qui est passé comme paramètre *objWbemObject* de l’appel d’origine. Le même objet **SWbemObject** peut être obtenu à l’aide d’un appel synchrone équivalent à [**SWbemServices. obtenir**](swbemservices-get.md).

</dd> <dt>

*objWbemAsyncContext* 
</dt> <dd>

Objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui est passé à l’appel asynchrone d’origine. Utilisez ce paramètre pour identifier l’origine de l’appel asynchrone qui déclenche cet événement lorsque plusieurs appels asynchrones sont effectués à l’aide de ce récepteur d’objets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Une fois l’événement **OnObjectReady** terminé, l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur ci-dessous.

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

Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur. Cela pose des risques de sécurité pour vos scripts et vos applications. Pour éliminer les risques, utilisez une communication semi-synchrone ou une communication synchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

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



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SWbemSink**](swbemsink.md)
</dt> </dl>

 

