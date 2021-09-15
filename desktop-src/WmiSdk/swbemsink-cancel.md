---
description: La méthode Cancel de l’objet SWbemSink annule toutes les opérations asynchrones en suspens associées à ce récepteur d’objets.
ms.assetid: dbe1eb24-5d9d-407a-b7c6-c58ec6891d7a
ms.tgt_platform: multiple
title: 'ISWbemSink :: Cancel, méthode (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.Cancel
- ISWbemSink.Cancel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 37bb44e8c34aa3cd7f9d491656461097e5a2bb5a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403956"
---
# <a name="iswbemsinkcancel-method"></a>ISWbemSink :: Cancel, méthode

La méthode **Cancel** de l’objet [**SWbemSink**](swbemsink.md) annule toutes les opérations asynchrones en suspens associées à ce récepteur d’objets.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
SWbemSink.Cancel()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Une fois la méthode **Cancel** terminée, l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur ci-dessous.

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

</dd> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

Le nom d’utilisateur et le mot de passe actuels ou spécifiés ne sont pas valides ou autorisés à établir la connexion.

</dd> </dl>

## <a name="remarks"></a>Notes

Vous ne pouvez pas annuler un seul appel asynchrone. Si plusieurs appels asynchrones sont en attente qui utilisent ce récepteur d’objets, cette méthode annule tous les appels asynchrones à l’aide de ce récepteur d’objets. Les appels asynchrones associés à d’autres récepteurs d’objets ne sont pas affectés.

Vous ne pouvez pas assigner à ce récepteur la valeur **Nothing** pour annuler une opération asynchrone. Vous devez appeler la méthode **Cancel** pour que WMI interrompe l’opération et libère les ressources associées. Cela est très important avec les opérations asynchrones longues, telles que les requêtes, ou les opérations qui ne se terminent jamais, telles que [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).

> [!Note]  
> Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur. Cela pose des risques de sécurité pour vos scripts et vos applications. Pour éliminer les risques, utilisez une communication semi-synchrone ou synchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

 

L’exemple suivant montre comment annuler un appel asynchrone.


```VB
objwbemsink.Cancel()
set objwbemsink= Nothing
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Wbemdisp. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSink<br/>                                                             |
| IID<br/>                      | IID \_ ISWbemSink<br/>                                                              |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SWbemSink**](swbemsink.md)
</dt> </dl>

 

