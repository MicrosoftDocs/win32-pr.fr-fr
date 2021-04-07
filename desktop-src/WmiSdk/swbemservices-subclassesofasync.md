---
description: Retourne une collection de sous-classes pour une classe spécifiée.
ms.assetid: a9d16ee9-992e-4ce5-9c03-0a2c9958588c
ms.tgt_platform: multiple
title: SWbemServices. SubclassesOfAsync, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.SubclassesOfAsync
- ISWbemServices.SubclassesOfAsync
- ISWbemServices.SubclassesOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d8d325c96ea1a292d8ac3afc76bfea619fe5a143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952345"
---
# <a name="swbemservicessubclassesofasync-method"></a>SWbemServices. SubclassesOfAsync, méthode

La méthode **SubclassesOfAsync** de l’objet [**SWbemServices**](swbemservices.md) retourne une collection de sous-classes pour une classe spécifiée. Utilisez cette méthode uniquement pour les objets de classe.

Cette méthode est appelée en mode asynchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
SWbemServices.SubclassesOfAsync( _
  ByVal ObjWbemSink, _
  [ ByVal strSuperclass ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ObjWbemSink* 
</dt> <dd>

Obligatoire. Récepteur d’objets qui reçoit les sous-classes de manière asynchrone. Créez un objet [**SWbemSink**](swbemsink.md) pour recevoir les objets.

</dd> <dt>

*strSuperclass* \[ facultatif\]
</dt> <dd>

Spécifie un nom de classe parente. Seules les classes qui sont des sous-classes de cette classe sont retournées dans l’énumérateur. Si ce paramètre est vide et si *IFlags* est **wbemQueryFlagShallow**, seules les classes de niveau supérieur sont retournées (c’est-à-dire les classes qui n’ont pas de classe parente). Si ce paramètre est vide et si *IFlags* est **wbemQueryFlagDeep**, toutes les classes de l’espace de noms sont retournées.

</dd> <dt>

*IFlags* \[ facultatif\]
</dt> <dd>

Détermine la profondeur de l’énumération des appels. La valeur par défaut de ce paramètre est **wbemQueryFlagDeep**. Ce paramètre peut accepter les valeurs suivantes.

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow * * * * (1 (0x1))


</dt> <dd>

Force l’énumération à inclure uniquement les sous-classes immédiates de la classe parente spécifiée.

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep * * * * (0 (0x0))


</dt> <dd>

Valeur par défaut pour ce paramètre. Cette valeur force l’énumération récursive dans toutes les sous-classes dérivées de la classe parente spécifiée. La classe parente n’est pas retournée dans l’énumération.

</dd> <dt>

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

En général, ce paramètre n’est pas défini. Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête. Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.

</dd> <dt>

*objWbemAsyncContext* \[ facultatif\]
</dt> <dd>

Objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui retourne au récepteur d’objets pour identifier la source de l’appel asynchrone d’origine. Utilisez ce paramètre pour effectuer plusieurs appels asynchrones à l’aide du même récepteur d’objets. Pour utiliser ce paramètre, créez un objet **SWbemNamedValueSet** et utilisez la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) pour ajouter une valeur qui identifie l’appel asynchrone que vous effectuez. Cet objet **SWbemNamedValueSet** est retourné au récepteur d’objets et la source de l’appel peut être extraite à l’aide de la méthode [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) . Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur. En cas de réussite, le récepteur reçoit un événement [**OnObjectReady**](swbemsink-onobjectready.md) par instance. Après la dernière instance, le récepteur d’objets reçoit un événement [**OnCompleted**](swbemsink-oncompleted.md) .

## <a name="error-codes"></a>Codes d’erreur

À la fin de la méthode **SubclassesOfAsync** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

> [!Note]  
> Une collection retournée avec zéro élément n’est pas une erreur.

 

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

L’utilisateur actuel n’a pas l’autorisation d’afficher une ou plusieurs des classes retournées par l’appel.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erreur non spécifiée.

</dd> <dt>

**wbemErrInvalidClass** -2147749904 (0x80041010)
</dt> <dd>

La classe spécifiée n’existe pas.

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

Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur. Cela pose des risques de sécurité pour vos scripts et vos applications. Pour éliminer les risques, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).

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

[**SWbemObjectSet**](swbemobjectset.md)
</dt> </dl>

 

