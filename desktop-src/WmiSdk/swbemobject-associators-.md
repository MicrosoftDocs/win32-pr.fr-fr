---
description: La méthode Associatorsrs \_ de l’objet SWbemObject retourne une collection d’objets (classes ou instances) qui sont associés à l’objet actuel.
ms.assetid: 79f01853-c649-4cbe-b2fa-cff38fb4b733
ms.tgt_platform: multiple
title: Méthode SWbemObject.Associators_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Associators_
- ISWbemObject.Associators_
- ISWbemObject.Associators_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1f9ff4536936661ece54b5bff29e500ce6e98d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952683"
---
# <a name="swbemobjectassociators_-method"></a>SWbemObject. Associatorss, \_ méthode

La méthode **associatorsrs \_** de l’objet [**SWbemObject**](swbemobject.md) retourne une collection d’objets (classes ou instances) qui sont associés à l’objet actuel. Ces objets retournés sont appelés points de terminaison. Cette méthode exécute la même fonction que les ASSOCIateurs de la requête WQL.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objWbemObjectSet = .Associators_( _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strAssocClass* \[ dans, facultatif\]
</dt> <dd>

Chaîne qui contient une classe d’association. S’il est spécifié, ce paramètre indique que les points de terminaison retournés doivent être associés à la source par le biais de la classe d’association spécifiée ou d’une classe dérivée de cette classe d’association.

</dd> <dt>

*strResultClass* \[ dans, facultatif\]
</dt> <dd>

Chaîne qui contient un nom de classe. S’il est spécifié, ce paramètre indique que les points de terminaison retournés doivent appartenir ou être dérivés de la classe spécifiée dans ce paramètre.

</dd> <dt>

*strResultRole* \[ dans, facultatif\]
</dt> <dd>

Chaîne qui contient un nom de propriété. S’il est spécifié, ce paramètre indique que les points de terminaison retournés doivent jouer un rôle particulier dans leur association avec l’objet source. Le rôle est défini par le nom d’une propriété spécifiée (qui doit être une propriété de référence) d’une association.

</dd> <dt>

*strRole* \[ dans, facultatif\]
</dt> <dd>

Chaîne qui contient un nom de propriété. Si ce paramètre est spécifié, ce paramètre indique que les points de terminaison retournés doivent participer à une association avec l’objet source dans lequel l’objet source joue un rôle particulier. Le rôle est défini par le nom d’une propriété spécifiée (qui doit être une propriété de référence) d’une association.

</dd> <dt>

*bClassesOnly* \[ dans, facultatif\]
</dt> <dd>

Valeur booléenne qui indique si une liste de noms de classes doit être retournée plutôt que des instances réelles des classes. Il s’agit des classes auxquelles les instances de point de terminaison appartiennent. La valeur par défaut de ce paramètre est **false**.

</dd> <dt>

*bSchemaOnly* \[ dans, facultatif\]
</dt> <dd>

Il s’agit d’une valeur booléenne qui indique si la requête s’applique au schéma plutôt qu’aux données. La valeur par défaut de ce paramètre est **false**. Elle peut uniquement avoir la valeur **true** si l’objet sur lequel cette méthode est appelée est une classe. Quand la valeur est **true**, le jeu de points de terminaison retournés représente des classes qui sont correctement associées à la classe source dans le schéma.

</dd> <dt>

*strRequiredAssocQualifier* \[ dans, facultatif\]
</dt> <dd>

Chaîne qui contient un nom de qualificateur. Ce paramètre, s’il est spécifié, indique que les points de terminaison retournés doivent être associés à l’objet source par le biais d’une classe d’association qui inclut le qualificateur spécifié.

</dd> <dt>

*strRequiredQualifier* \[ dans, facultatif\]
</dt> <dd>

Chaîne qui contient un nom de qualificateur. Ce paramètre, s’il est spécifié, indique que les points de terminaison retournés doivent inclure le qualificateur spécifié.

</dd> <dt>

*IFlags* \[ dans, facultatif\]
</dt> <dd>

Entier spécifiant des indicateurs supplémentaires pour l’opération. La valeur par défaut de ce paramètre est **wbemFlagReturnImmediately**, qui indique à l’appel qu’il doit retourner immédiatement plutôt que d’attendre la fin de la requête. Ce paramètre peut accepter les valeurs suivantes.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly * * * * (32 (0x20))


</dt> <dd>

Entraîne le retour d’un énumérateur avant uniquement. Les énumérateurs avant uniquement sont généralement beaucoup plus rapides et utilisent moins de mémoire que les énumérateurs conventionnels, mais ils n’autorisent pas les appels à [**SWbemObject. Clone \_**](swbemobject-clone-.md).

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional * * * * (0 (0x0))


</dt> <dd>

Fait en sorte que WMI conserve les pointeurs vers les objets de l’énumération jusqu’à ce que le client libère l’énumérateur.

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

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers * * * * (131072 (0x20000))


</dt> <dd>

Fait en sorte que WMI retourne des données de modification de classe avec la définition de classe de base. L’inclusion de cet indicateur rend le texte localisé du qualificateur de description disponible pour les classes, les propriétés et les méthodes. Pour plus d’informations sur les qualificateurs modifiés, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ dans, facultatif\]
</dt> <dd>

En général, ce n’est pas défini. Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête. Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’appel réussit, un objet [**SWbemObjectSet**](swbemobjectset.md) est retourné.

## <a name="error-codes"></a>Codes d’erreur

À la fin de la méthode **associatorsrs \_** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

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

Un paramètre spécifié n’est pas valide.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894
</dt> <dd>

Mémoire insuffisante pour terminer l’opération.

</dd> </dl>

## <a name="remarks"></a>Notes

Pour plus d’informations sur les ASSOCIateurs de requêtes WQL, d’instances source et de points de terminaison associés, consultez [ASSOCIATORS OF Statement](associators-of-statement.md).

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

[**SWbemObject. References\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md)
</dt> <dt>

[**SWbemServices. ReferencesTo**](swbemservices-referencesto.md)
</dt> </dl>

 

 




