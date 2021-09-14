---
description: La méthode Add de l’objet SWbemQualifierSet ajoute un objet SWbemQualifier à la collection SWbemQualifierSet. Si un qualificateur portant le même nom existe déjà dans la collection, il est remplacé.
ms.assetid: 8f4c4da2-4890-4515-a3dc-76d154dae43c
ms.tgt_platform: multiple
title: Méthode SWbemQualifierSet. Add (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Add
- ISWbemQualifierSet.Add
- ISWbemQualifierSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: bbbef15ccc45aeba5b7e3c03f6cb9448cfe03ec4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010399"
---
# <a name="swbemqualifiersetadd-method"></a>SWbemQualifierSet. Add, méthode

La méthode **Add** de l’objet [**SWbemQualifierSet**](swbemqualifierset.md) ajoute un objet [**SWbemQualifier**](swbemqualifier.md) à la collection **SWbemQualifierSet** . Si un qualificateur portant le même nom existe déjà dans la collection, il est remplacé.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objQualifier = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal bPropagatesToSubclasses ], _
  [ ByVal bPropagatesToInstances ], _
  [ ByVal bOverridable ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strName* \[ dans\]
</dt> <dd>

Obligatoire. Nom du nouveau qualificateur.

</dd> <dt>

*varVal* \[ dans\]
</dt> <dd>

Obligatoire. Valeur de type Variant du nouveau qualificateur.

</dd> <dt>

*bPropagatesToSubclasses* \[ dans, facultatif\]
</dt> <dd>

Valeur booléenne qui indique si ce nouveau qualificateur est propagé aux sous-classes. La valeur par défaut est **true**.

</dd> <dt>

*bPropagatesToInstances* \[ dans, facultatif\]
</dt> <dd>

Valeur booléenne qui indique si ce nouveau qualificateur est propagé aux instances. La valeur par défaut est **true**.

</dd> <dt>

*bOverridable* \[ dans, facultatif\]
</dt> <dd>

Valeur booléenne qui indique si ce qualificateur peut être substitué lorsqu’il est propagé. La valeur par défaut est **true**.

</dd> <dt>

*IFlags* \[ dans, facultatif\]
</dt> <dd>

Réservé. La valeur par défaut est 0.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

En cas de réussite, cette méthode retourne un objet [**SWbemQualifier**](swbemqualifier.md) qui représente le nouveau qualificateur. Dans le cas contraire, un objet **null** est retourné.

## <a name="error-codes"></a>Codes d’erreur

Une fois la méthode **Add** terminée, l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

<dl> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Le paramètre *IFlags* n’est pas valide.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erreur non spécifiée.

</dd> <dt>

**wbemErrCannotBeKey** -2147749919 (0x8004101F)
</dt> <dd>

Tentative non autorisée de spécifier un qualificateur de **clé** sur une propriété qui ne peut pas être une clé. Les clés sont spécifiées dans la définition de classe pour un objet et ne peuvent pas être modifiées au niveau de l'instance.

</dd> <dt>

**wbemErrInvalidQualifierType** -2147749929 (0x80041029)
</dt> <dd>

Le paramètre *varVal* n’est pas un type de qualificateur légal.

</dd> <dt>

**wbemErrOverrideNotAllowed** -2147749914 (0x8004101A)
</dt> <dd>

Il n’est pas possible d’effectuer l’opération **SWbemQualifierSet. Add** sur ce qualificateur, car l’objet propriétaire n’autorise pas les remplacements.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemQualifierSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemQualifierSet<br/>                                                      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SWbemQualifierSet**](swbemqualifierset.md)
</dt> <dt>

[**SWbemQualifierSet. Remove**](swbemqualifierset-remove.md)
</dt> </dl>

 

 




