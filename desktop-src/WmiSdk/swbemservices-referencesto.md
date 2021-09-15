---
description: Retourne une collection de toutes les classes d’association ou instances qui font référence à une classe ou une instance source spécifique.
ms.assetid: 33425b1c-13f5-4c3d-8f8a-2922f3e95264
ms.tgt_platform: multiple
title: SWbemServices. ReferencesTo, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ReferencesTo
- ISWbemServices.ReferencesTo
- ISWbemServices.ReferencesTo
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 73addea189815d1594d0963fbdd6e20c562b3be3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403580"
---
# <a name="swbemservicesreferencesto-method"></a>SWbemServices. ReferencesTo, méthode

La méthode **ReferencesTo** de l’objet [**SWbemServices**](swbemservices.md) retourne une collection de toutes les classes d’association ou instances qui font référence à une classe ou une instance source spécifique. Cette méthode exécute la même fonction que les [références de](references-of-statement.md) la requête WQL.

Cette méthode est appelée en mode semi-synchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objWbemObjectSet = .ReferencesTo( _
  ByVal strObjectPath, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strObjectPath* 
</dt> <dd>

Obligatoire. Chaîne qui contient le chemin d’accès de l’objet de la source pour cette méthode. Pour plus d’informations, consultez [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*strResultClass* \[ facultatif\]
</dt> <dd>

Chaîne qui contient un nom de classe. Si ce paramètre est spécifié, ce paramètre indique que les objets d’association retournés doivent appartenir à la classe spécifiée dans ce paramètre ou en être dérivés.

</dd> <dt>

*strRole* \[ facultatif\]
</dt> <dd>

Chaîne qui contient un nom de propriété. Si ce paramètre est spécifié, ce paramètre indique que les objets d’association retournés doivent être limités à ceux dans lesquels l’objet source joue un rôle spécifique. Le rôle est défini par le nom d’une propriété spécifiée (qui doit être une propriété de référence) d’une association.

</dd> <dt>

*bClassesOnly* \[ facultatif\]
</dt> <dd>

Valeur booléenne qui indique si une liste de noms de classes doit être retournée plutôt que des instances réelles des classes. Il s’agit des classes auxquelles appartiennent les objets Association. La valeur par défaut de ce paramètre est **false**.

</dd> <dt>

*bSchemaOnly* \[ facultatif\]
</dt> <dd>

Valeur booléenne qui indique si la requête s’applique au schéma plutôt qu’aux données. La valeur par défaut de ce paramètre est **false**. Elle ne peut avoir la valeur **true** que si le paramètre *strObjectPath* spécifie le chemin d’accès à l’objet d’une classe. Quand la valeur est **true**, le jeu de points de terminaison retournés représente des classes qui sont correctement associées à la classe source dans le schéma.

</dd> <dt>

*strRequiredQualifier* \[ facultatif\]
</dt> <dd>

Chaîne qui contient un nom de qualificateur. S’il est spécifié, ce paramètre indique que les objets Association retournés doivent inclure le qualificateur spécifié.

</dd> <dt>

*IFlags* \[ facultatif\]
</dt> <dd>

Entier qui spécifie des indicateurs supplémentaires pour l’opération. La valeur par défaut de ce paramètre est **wbemFlagReturnImmediately**, qui indique à l’appel qu’il doit retourner immédiatement plutôt que d’attendre la fin de la requête. Ce paramètre peut accepter les valeurs suivantes.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly * * * * (32 (0x20))


</dt> <dd>

Entraîne le retour d’un énumérateur avant uniquement. Les énumérateurs avant uniquement sont généralement beaucoup plus rapides et utilisent moins de mémoire que les énumérateurs conventionnels, mais ils n’autorisent pas les appels à [**SWbemObject. Clone \_**](swbemobject-clone-.md).

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional * * * * (0 (0x0))


</dt> <dd>

fait en sorte que Windows Management Instrumentation (WMI) conserve des pointeurs vers les objets de l’énumération jusqu’à ce que le client libère l’énumérateur.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately * * * * (16 (0x10))


</dt> <dd>

Provoque le retour immédiat de l’appel.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete * * * * (0 (0x0))


</dt> <dd>

Provoque le blocage de cet appel jusqu’à ce que la requête soit terminée. Cet indicateur appelle la méthode en mode synchrone.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers * * * * (131072 (0x20000))


</dt> <dd>

Fait en sorte que WMI retourne des données de modification de classe avec la définition de la classe de base. Pour plus d’informations, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ facultatif\]
</dt> <dd>

En général, ce n’est pas défini. Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête. Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la méthode réussit, la méthode retourne un objet [**SWbemObjectSet**](swbemobjectset.md) .

## <a name="error-codes"></a>Codes d’erreur

À la fin de la méthode **ReferencesTo** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

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

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Un paramètre non valide a été spécifié.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Mémoire insuffisante pour terminer l’opération.

</dd> <dt>

**wbemFlagUseAmendedQualifiers** -131072 (0x20000)
</dt> <dd>

Fait en sorte que WMI retourne des données de modification de classe avec la définition de classe de base.

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour plus d’informations sur les références des objets de requête WQL, d’instances source et d’association associés, consultez [ASSOCIATORS OF Statement](associators-of-statement.md).

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

[**SWbemObject. ASSOCIATORS\_**](swbemobject-associators-.md)
</dt> <dt>

[**SWbemObject. References\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md)
</dt> </dl>

 

 




