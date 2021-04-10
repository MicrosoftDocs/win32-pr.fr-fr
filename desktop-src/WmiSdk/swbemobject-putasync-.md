---
description: La \_ méthode PutAsync de SWbemObject crée ou met à jour de manière asynchrone une instance ou un objet de classe à Windows Management Instrumentation (WMI).
ms.assetid: ff738412-fcca-4e4a-a178-0d1d391ec99b
ms.tgt_platform: multiple
title: Méthode SWbemObject.PutAsync_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.PutAsync_
- ISWbemObject.PutAsync_
- ISWbemObject.PutAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3530c3883763773f53bec81aeee8b0d199170133
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210552"
---
# <a name="swbemobjectputasync_-method"></a>SWbemObject. PutAsync, \_ méthode

La **méthode \_ PutAsync** de [**SWbemObject**](swbemobject.md) crée ou met à jour de manière asynchrone une instance ou un objet de classe à Windows Management Instrumentation (WMI). Vous pouvez utiliser cette méthode après avoir modifié des propriétés ou des méthodes dans **SWbemObject**, et vos modifications sont écrites dans WMI.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
SWbemObject.PutAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*objWbemSink* \[ dans\]
</dt> <dd>

Obligatoire. Récepteur d’objets qui reçoit de façon asynchrone le résultat de l’opération **put** .

</dd> <dt>

*IFlags* \[ dans, facultatif\]
</dt> <dd>

Détermine si l’appel crée ou met à jour la classe ou l’instance et si l’appel est retourné immédiatement. Ce paramètre peut accepter les valeurs suivantes.

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>wbemChangeFlagUpdateCompatible * * * * (0 (0x0))


</dt> <dd>

Permet à une classe d’être mise à jour s’il n’y a pas de classes dérivées et qu’il n’existe aucune instance pour cette classe. Il autorise également les mises à jour dans tous les cas si la modification concerne uniquement des qualificateurs peu importants (par exemple, le qualificateur de **Description** ). Il s’agit du comportement par défaut pour cet appel et est utilisé pour la compatibilité avec les versions précédentes de WMI. Si la classe a des instances, la mise à jour échoue.

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>wbemChangeFlagUpdateSafeMode * * * * (32 (0x20))


</dt> <dd>

Autorise les mises à jour des classes, même s’il existe des classes enfants, si la modification ne provoque pas de conflits avec les classes enfants. Vous pouvez utiliser cet indicateur lors de l’ajout d’une nouvelle propriété à une classe de base qui n’a pas été mentionnée précédemment dans une des classes enfants. Si la classe a des instances, la mise à jour échoue.

</dd> <dt>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>WbemChangeFlagUpdateForceMode * * * * (64 (0x40))


</dt> <dd>

Force les mises à jour des classes lorsque des classes enfants sont en conflit. Par exemple, cet indicateur force une mise à jour si un qualificateur de classe a été défini dans une classe enfant, et si la classe de base tente d’ajouter le même qualificateur en conflit avec l’identificateur existant. En mode de forçage, ce conflit est résolu en supprimant le qualificateur en conflit dans la classe enfant. Si la classe a des instances, la mise à jour échoue.

L’utilisation du mode force pour mettre à jour une classe statique entraîne la suppression de toutes les instances de cette classe. Une mise à jour forcée sur une classe de fournisseur ne supprime pas les instances de la classe.

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>wbemChangeFlagCreateOrUpdate * * * * (0 (0x0))


</dt> <dd>

Provoque la création de la classe ou de l’instance si elle n’existe pas ou est remplacée si elle existe déjà.

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>wbemChangeFlagCreateOnly * * * * (2 (0X2))


</dt> <dd>

Utilisé pour la création uniquement. L’appel échoue si la classe ou l’instance existe déjà.

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>wbemChangeFlagUpdateOnly * * * * (1 (0x1))


</dt> <dd>

Provoque la mise à jour de cet appel. La classe ou l’instance doit exister pour que l’appel réussisse.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately * * * * (16 (0x10))


</dt> <dd>

Provoque le retour immédiat de l’appel.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete * * * * (0 (0x0))


</dt> <dd>

Provoque le blocage de cet appel jusqu’à ce que la requête soit terminée.

</dd> <dt>

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

Permet à WMI d’écrire des données de modification de classe avec la définition de classe de base. Pour plus d’informations sur les qualificateurs modifiés, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ dans, facultatif\]
</dt> <dd>

En général, ce n’est pas défini. Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête. Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.

</dd> <dt>

*objWbemAsyncContext* \[ dans, facultatif\]
</dt> <dd>

Il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui retourne au récepteur d’objets pour identifier la source de l’appel asynchrone d’origine. Utilisez ce paramètre si vous effectuez plusieurs appels asynchrones à l’aide du même récepteur d’objets. Pour utiliser ce paramètre, créez un objet **SWbemNamedValueSet** et utilisez la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) pour ajouter une valeur qui identifie l’appel asynchrone que vous effectuez. Cet objet **SWbemNamedValueSet** est retourné au récepteur d’objets et la source de l’appel peut être extraite à l’aide de la méthode [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) . Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur. Si l’appel réussit, l’événement [**OnObjectPut**](swbemsink-onobjectput.md) du récepteur d’objets fourni reçoit un objet [**SWbemObjectPath**](swbemobjectpath.md) , contenant le chemin d’accès à l’objet de l’instance ou de la classe qui est correctement validée dans WMI.

## <a name="error-codes"></a>Codes d’erreur

À la fin de la **méthode \_ PutAsync** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

L’utilisateur actuel n’est pas autorisé à mettre à jour une instance de la classe spécifiée.

</dd> <dt>

**wbemErrAlreadyExists** -2147749913 (0x80041019)
</dt> <dd>

L’indicateur **wbemChangeFlagCreateOnly** a été spécifié, mais l’instance existe déjà.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erreur non spécifiée.

</dd> <dt>

**wbemErrIllegalNull** -2147749898 (0x8004100A)
</dt> <dd>

La valeur **Nothing** a été spécifiée pour une propriété qui ne peut pas être **Nothing**. Un exemple d’une telle propriété est une propriété qui est marquée par un qualificateur de **clé**, **indexée** ou **not \_ null** .

</dd> <dt>

**wbemErrInvalidObject** -2147749908 (0x80041014)
</dt> <dd>

L'instance spécifiée n'est pas valide.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Un paramètre spécifié n’est pas valide.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

L’indicateur **wbemChangeFlagUpdateOnly** a été spécifié, mais l’instance ou la classe n’existe pas.

</dd> <dt>

**wbemErrIncompleteClass** -2147749920 (0x80041020)
</dt> <dd>

Les propriétés requises pour les classes n’ont pas toutes été définies.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Mémoire insuffisante pour terminer l’opération.

</dd> </dl>

## <a name="remarks"></a>Notes

Cet appel est retourné immédiatement, et le résultat de l’opération **put** est retourné à l’appelant via des rappels remis au récepteur spécifié dans *objWbemSink*. Implémentez *objWbemSink*. Méthode [**OnObjectPut**](swbemsink-onobjectput.md) pour obtenir le chemin d’accès de l’objet de l’instance ou de la classe écrite dans l’espace de stockage WMI. Pour plus d’informations sur les méthodes de récepteur, consultez [appel d’une méthode](calling-a-method.md).

Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur. Cela pose des risques de sécurité pour vos scripts et vos applications. Pour éliminer les risques, utilisez une communication semi-synchrone ou synchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

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

[**SWbemObjectPath. Class**](swbemobjectpath-class.md)
</dt> <dt>

[**SWbemProperty**](swbemproperty.md)
</dt> <dt>

[**SWbemQualifier**](swbemqualifier.md)
</dt> </dl>

 

