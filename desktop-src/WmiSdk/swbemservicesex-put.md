---
description: Retourne un objet SWbemObjectPath qui contient le chemin d’accès de l’objet dans lequel les données ont été écrites.
ms.assetid: 1a9a718d-875d-4102-9d9d-3d10be162f58
ms.tgt_platform: multiple
title: SWbemServicesEx. put, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx.Put
- ISWbemServicesEx.Put
- ISWbemServicesEx.Put
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e495a38262e6b6f7dd8b67424b74db74c025be62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519016"
---
# <a name="swbemservicesexput-method"></a>SWbemServicesEx. put, méthode

La méthode **put** de l’objet [**SWbemServicesEx**](swbemservicesex.md) enregistre l’objet dans l’espace de noms lié à l’objet et retourne un objet [**SWbemObjectPath**](swbemobjectpath.md) qui contient le chemin d’accès de l’objet dans lequel les données ont été écrites.

Cette méthode est appelée en mode semi-synchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objObjectPath = .Put( _
  ByVal objWbemObject, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*objWbemObject* 
</dt> <dd>

Obligatoire. Nouvel objet à placer dans l’espace de noms. Il peut s’agir d’un objet nouvellement créé ou d’un objet modifié.

</dd> <dt>

*IFlags* \[ facultatif\]
</dt> <dd>

Ce paramètre détermine si l’appel crée ou met à jour l’objet et si l’appel est retourné immédiatement. Ce paramètre peut accepter les valeurs suivantes.

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0x0))


</dt> <dd>

Permet à une classe d’être mise à jour s’il n’y a pas de classes dérivées et qu’il n’existe aucune instance pour cette classe. Il autorise également les mises à jour dans tous les cas si la modification ne concerne que des qualificateurs peu importants (par exemple, le qualificateur de **Description** ). Il s’agit du comportement par défaut pour cet appel et est utilisé pour la compatibilité avec les versions précédentes de WMI. Si la classe a des instances, la mise à jour échoue.

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20))


</dt> <dd>

Autorise les mises à jour des classes, même s’il existe des classes enfants, lorsque la modification n’entraîne pas de conflits avec les classes enfants. Vous pouvez utiliser cet indicateur lors de l’ajout d’une nouvelle propriété à une classe de base qui n’a pas été mentionnée précédemment dans une des classes enfants. Si la classe a des instances, la mise à jour échoue.

</dd> <dt>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40))


</dt> <dd>

Cet indicateur force les mises à jour des classes lorsque des classes enfants sont en conflit. Par exemple, cet indicateur force une mise à jour si un qualificateur de classe a été défini dans une classe enfant, et si la classe de base tente d’ajouter le même qualificateur en conflit avec l’identificateur existant. En mode forcé, ce conflit est résolu en supprimant le qualificateur en conflit dans la classe enfant. Si la classe a des instances, la mise à jour échoue.

L’utilisation du mode de force pour mettre à jour une classe statique entraîne la suppression de toutes les instances de cette classe. Une mise à jour forcée sur une classe de fournisseur ne supprime pas les instances de la classe.

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0x0))


</dt> <dd>

Provoque la création de la classe ou de l’instance si elle n’existe pas, ou si elle est remplacée si elle existe déjà.

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0X2))


</dt> <dd>

Utilisé pour la création uniquement. L’appel échoue si la classe ou l’instance existe déjà.

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1))


</dt> <dd>

Fait en sorte que cet appel effectue uniquement une mise à jour. La classe ou l’instance doit exister pour que l’appel réussisse.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))


</dt> <dd>

Provoque le retour immédiat de l’appel.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0x0))


</dt> <dd>

Entraîne le blocage de cet appel jusqu’à ce que l’opération soit terminée. Cet indicateur appelle la méthode en mode synchrone.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000))


</dt> <dd>

Permet à WMI d’écrire des données de modification de classe ainsi que la définition de la classe de base. Pour plus d’informations, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ facultatif\]
</dt> <dd>

En général, ce n’est pas défini. Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui sert la demande. Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’appel réussit, un objet [**SWbemObjectPath**](swbemobjectpath.md) est retourné. Cet objet contient le chemin d’accès à l’objet de l’instance ou de la classe qui a été correctement validée dans WMI.

## <a name="error-codes"></a>Codes d’erreur

Une fois la méthode **put** terminée, l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

L’utilisateur actuel n’a pas l’autorisation pour l’opération.

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

La valeur **null** a été spécifiée pour une propriété qui ne peut pas être **null**. Un exemple d’une telle propriété est une propriété marquée par un qualificateur de [**clé**](standard-qualifiers.md), **indexée** ou **not \_ null** .

</dd> <dt>

**wbemErrInvalidObject** -2147749908 (0x80041014)
</dt> <dd>

L’objet spécifié n’est pas valide.

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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ ISWbemServicesEx<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemServicesEx<br/>                                                        |



 

 




