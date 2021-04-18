---
description: L’événement OnProgress de SWbemSink est déclenché lorsqu’un appel asynchrone retourne l’état d’un appel en cours.
ms.assetid: abb43916-f952-41fe-a5ba-0428864c0685
ms.tgt_platform: multiple
title: 'ISWbemSinkEvents :: OnProgress, événement (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnProgress
- ISWbemSinkEvents.OnProgress
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0d322309adcfad33b1c303d7efd6af28db1cac80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536663"
---
# <a name="iswbemsinkeventsonprogress-event"></a>ISWbemSinkEvents :: OnProgress, événement

L’événement **OnProgress** de [**SWbemSink**](swbemsink.md) est déclenché lorsqu’un appel asynchrone retourne l’état d’un appel en cours. Si les événements, les instances ou les classes sont produits à partir d’un fournisseur qui prend en charge les mises à jour d’État, vous pouvez placer le code dans cet événement pour fournir aux utilisateurs des commentaires sur l’état d’une opération asynchrone. Vous devez définir le paramètre *IFlags* de l’appel asynchrone à **wbemFlagSendStatus** (128/0x80) si vous souhaitez recevoir des mises à jour d’État, sinon cet événement n’est pas déclenché.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
SWbemSink.OnProgress( _
  ByVal iUpperBound, _
  ByVal iCurrent, _
  ByVal strMessage, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*iUpperBound* 
</dt> <dd>

Entier qui décrit le nombre total de tâches à effectuer.

</dd> <dt>

*iCurrent* 
</dt> <dd>

Élément en cours de traitement.

</dd> <dt>

*strMessage* 
</dt> <dd>

Message qui décrit l’état de la tâche en cours.

</dd> <dt>

*objWbemAsyncContext* 
</dt> <dd>

Objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui est passé à l’appel asynchrone d’origine. Utilisez ce paramètre pour identifier l’origine de l’appel asynchrone qui déclenche cet événement lorsque plusieurs appels asynchrones sont effectués à l’aide de ce récepteur d’objets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Une fois l’événement **OnProgress** terminé, l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur ci-dessous.

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

L’événement **OnProgress** est déclenché lorsqu’un appel asynchrone retourne l’état d’un appel en cours. Si les événements, les instances ou les classes sont produits à partir d’un fournisseur qui prend en charge les mises à jour d’État, vous pouvez placer le code dans cet événement pour permettre aux utilisateurs de fournir des commentaires sur l’état d’une opération asynchrone.

> [!Note]  
> Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur. Cela pose des risques de sécurité pour vos scripts et vos applications. Pour éliminer les risques, utilisez une communication semi-synchrone ou synchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

 

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

 

