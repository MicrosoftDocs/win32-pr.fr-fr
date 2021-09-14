---
description: La \_ méthode ReferencesAsync de SWbemObject fournit une collection de toutes les classes d’association ou instances qui font référence à l’objet actuel. Cette méthode exécute la même fonction que les références WQL de la requête.
ms.assetid: 44989726-3f68-453b-b9f5-e76fb0fbb152
ms.tgt_platform: multiple
title: Méthode SWbemObject.ReferencesAsync_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ReferencesAsync_
- ISWbemObject.ReferencesAsync_
- ISWbemObject.ReferencesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: aa4b85475a0dc9f736254c8f207469a52897b7ae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921807"
---
# <a name="swbemobjectreferencesasync_-method"></a>SWbemObject. ReferencesAsync, \_ méthode

La **méthode \_ ReferencesAsync** de [**SWbemObject**](swbemobject.md) fournit une collection de toutes les classes d’association ou instances qui font référence à l’objet actuel. Cette méthode exécute la même fonction que les [références WQL de](references-of-statement.md) la requête.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
SWbemObject.ReferencesAsync_( _
  ByVal objWbemSink, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*objWbemSink* \[ dans\]
</dt> <dd>

Obligatoire. Récepteur d’objets qui reçoit les objets de manière asynchrone.

</dd> <dt>

*strResultClass* \[ dans, facultatif\]
</dt> <dd>

Chaîne qui contient un nom de classe. S’il est spécifié, ce paramètre indique que les objets d’association retournés doivent appartenir ou être dérivés de la classe spécifiée dans ce paramètre.

</dd> <dt>

*strRole* \[ dans, facultatif\]
</dt> <dd>

Chaîne qui contient un nom de propriété. Si ce paramètre est spécifié, ce paramètre indique que les objets d’association retournés doivent être limités à ceux dans lesquels l’objet source joue un rôle spécifique. Le nom d’une propriété de référence spécifiée définit le rôle d’une association.

</dd> <dt>

*bClassesOnly* \[ dans, facultatif\]
</dt> <dd>

Valeur booléenne qui indique si une liste de noms de classes doit être retournée plutôt que des instances réelles des classes. Il s’agit des classes auxquelles appartiennent les objets Association. La valeur par défaut de ce paramètre est **false**.

</dd> <dt>

*bSchemaOnly* \[ dans, facultatif\]
</dt> <dd>

Valeur booléenne qui indique si la requête s’applique au schéma plutôt qu’aux données. La valeur par défaut de ce paramètre est **false**. Elle peut uniquement avoir la valeur **true** si l’objet sur lequel cette méthode est appelée est une classe. Quand la valeur est **true**, le jeu de points de terminaison retournés représente des classes qui sont correctement associées à la classe source dans le schéma.

</dd> <dt>

*strRequiredQualifier* \[ dans, facultatif\]
</dt> <dd>

Chaîne qui contient un nom de qualificateur. S’il est spécifié, ce paramètre indique que les objets Association retournés doivent inclure le qualificateur spécifié.

</dd> <dt>

*IFlags* \[ dans, facultatif\]
</dt> <dd>

Entier spécifiant des indicateurs supplémentaires pour l’opération. Ce paramètre peut accepter les valeurs suivantes.

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

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers * * * * (131072 (0x20000))


</dt> <dd>

fait en sorte que Windows Management Instrumentation (WMI) retourne des données de modification de classe avec la définition de classe de base. Pour plus d’informations, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ dans, facultatif\]
</dt> <dd>

En général, ce n’est pas défini. Dans le cas contraire, il s’agit d’un objet [SWbemNamedValueSet](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête. Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.

</dd> <dt>

*objWbemAsyncContext* \[ dans, facultatif\]
</dt> <dd>

Il s’agit d’un objet [SWbemNamedValueSet](swbemnamedvalueset.md) qui retourne au récepteur d’objets pour identifier la source de l’appel asynchrone d’origine. Utilisez ce paramètre si vous effectuez plusieurs appels asynchrones à l’aide du même récepteur d’objets. Pour utiliser ce paramètre, créez un objet SWbemNamedValueSet et utilisez la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) pour ajouter une valeur qui identifie l’appel asynchrone que vous effectuez. Cet objet SWbemNamedValueSet est retourné au récepteur d’objets et la source de l’appel peut être extraite à l’aide de la méthode [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) . Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur. En cas de réussite, le récepteur reçoit un événement [**OnObjectReady**](swbemsink-onobjectready.md) par instance. Après la dernière instance, le récepteur d’objets reçoit un événement [**OnCompleted**](swbemsink-oncompleted.md) .

## <a name="error-codes"></a>Codes d’erreur

À la fin de la **méthode \_ ReferencesAsync** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

L’utilisateur actuel n’est pas autorisé à afficher une ou plusieurs des classes retournées par l’appel.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erreur non spécifiée.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Un paramètre non valide a été spécifié.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Mémoire insuffisante pour terminer l’opération.

</dd> </dl>

## <a name="remarks"></a>Notes

Cet appel est retourné immédiatement. Les objets et l’État demandés sont retournés à l’appelant via des rappels remis au récepteur spécifié dans *objWbemSink*. Pour traiter chaque objet lorsqu’il arrive, créez un *objWbemSink*. Sous-routine d’événement [**OnObjectReady**](swbemsink-onobjectready.md) . Une fois que tous les objets sont retournés, vous pouvez effectuer le traitement final dans votre implémentation de *objWbemSink*. Événement [**OnCompleted**](swbemsink-oncompleted.md) .

Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur. Cela pose des risques de sécurité pour vos scripts et vos applications. Pour éliminer les risques, utilisez une communication semi-synchrone ou une communication synchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

Pour plus d’informations sur les références des objets de requête WQL, d’instances source et d’association associés, consultez [ASSOCIATORS OF Statement](associators-of-statement.md).

## <a name="requirements"></a>Spécifications



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

[**SWbemObject. ASSOCIATORS\_**](swbemobject-associators-.md)
</dt> <dt>

[**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md)
</dt> <dt>

[**SWbemServices. ReferencesTo**](swbemservices-referencesto.md)
</dt> <dt>

[**SWbemServices. ReferencesToAsync**](swbemservices-referencestoasync.md)
</dt> </dl>

 

