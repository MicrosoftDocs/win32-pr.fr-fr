---
description: Récupère un objet, qui est une définition de classe ou une instance, en fonction du chemin d’accès de l’objet.
ms.assetid: 8da46851-52b8-4b5a-8c9d-1d492f57f4b6
ms.tgt_platform: multiple
title: SWbemServices. GetAsync, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.GetAsync
- ISWbemServices.GetAsync
- ISWbemServices.GetAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 451f13bde9458e7d57ec393f42b92a4092c99924
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923312"
---
# <a name="swbemservicesgetasync-method"></a>SWbemServices. GetAsync, méthode

La méthode **GetAsync** de l’objet [**SWbemServices**](swbemservices.md) récupère un objet, qui est une définition de classe ou une instance, en fonction du chemin d’accès de l’objet.

Cette méthode récupère uniquement les objets de l’espace de noms associé à l’objet [**SWbemServices**](swbemservices.md) actif.

Cette méthode est appelée en mode asynchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
SWbemServices.GetAsync( _
  ByVal objWbemSink, _
  [ ByVal strObjectPath ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*objWbemSink* 
</dt> <dd>

Obligatoire. Récepteur d’objets qui obtient des objets de manière asynchrone. Créez un objet [**SWbemSink**](swbemsink.md) pour recevoir les objets.

</dd> <dt>

*strObjectPath* \[ facultatif\]
</dt> <dd>

Chemin d’accès de l’objet que vous souhaitez récupérer. Si cette valeur est vide, l’objet vide retourné peut devenir une nouvelle classe. Pour plus d’informations, consultez [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md).

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

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers * * * * (131072 (0x20000))


</dt> <dd>

Fait en sorte que WMI retourne des données de modification de classe avec la définition de classe de base. Pour plus d’informations, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ facultatif\]
</dt> <dd>

En règle générale, cette valeur n’est pas définie. Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête. Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.

</dd> <dt>

*objWbemAsyncContext* \[ facultatif\]
</dt> <dd>

Objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui retourne au récepteur d’objets pour identifier la source de l’appel asynchrone d’origine. Utilisez ce paramètre si vous effectuez plusieurs appels asynchrones à l’aide du même récepteur d’objets. Pour utiliser ce paramètre, créez un objet **SWbemNamedValueSet** et utilisez la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) pour ajouter une valeur qui identifie l’appel asynchrone que vous effectuez. Cet objet **SWbemNamedValueSet** est retourné au récepteur d’objets et la source de l’appel peut être extraite à l’aide de la méthode [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) . Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur. En cas de réussite, le récepteur reçoit un événement [**OnObjectReady**](swbemsink-onobjectready.md) lorsque l’objet est disponible.

## <a name="error-codes"></a>Codes d’erreur

À la fin de la méthode **GetAsync** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

L’utilisateur actuel n’a pas l’autorisation d’accéder à l’objet.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erreur non spécifiée.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Un paramètre spécifié n’est pas valide.

</dd> <dt>

**wbemErrInvalidObjectPath** -2147749946 (0x8004103A)
</dt> <dd>

Le chemin d’accès spécifié n’est pas valide.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

L’objet demandé est introuvable.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Mémoire insuffisante pour terminer l’opération.

</dd> </dl>

## <a name="remarks"></a>Notes

Cet appel est retourné immédiatement. L’objet et l’État demandés sont retournés à l’appelant via un rappel remis au récepteur spécifié dans *objWbemSink*. Pour traiter l’objet lorsqu’il retourne, créez un *objWbemSink*. [**OnObjectReady**](swbemsink-onobjectready.md), ou *objWbemSink*. Sous-routine d’événement [**OnCompleted**](swbemsink-oncompleted.md) .

Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur. Cela pose des risques de sécurité pour vos scripts et vos applications. Pour éliminer les risques, utilisez une communication semi-synchrone ou synchrone. Pour plus d’informations, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).

## <a name="requirements"></a>Spécifications



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

[**M**](swbemobject.md)
</dt> </dl>

 

