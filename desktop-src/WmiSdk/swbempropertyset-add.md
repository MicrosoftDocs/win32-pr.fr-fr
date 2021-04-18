---
description: La méthode Add de l’objet SWbemPropertySet ajoute un objet SWbemProperty à la collection SWbemPropertySet. Si une propriété du même nom existe déjà dans la collection, son contenu est remplacé par la nouvelle définition.
ms.assetid: 52a5f964-3d53-441b-9a58-650afdc5b1b9
ms.tgt_platform: multiple
title: Méthode SWbemPropertySet. Add (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Add
- ISWbemPropertySet.Add
- ISWbemPropertySet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1ad5b40d31d162b287bdb1a387cd0602e0be1ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526930"
---
# <a name="swbempropertysetadd-method"></a>SWbemPropertySet. Add, méthode

La méthode **Add** de l’objet [**SWbemPropertySet**](swbempropertyset.md) ajoute un objet [**SWbemProperty**](swbemproperty.md) à la collection **SWbemPropertySet** . Si une propriété du même nom existe déjà dans la collection, son contenu est remplacé par la nouvelle définition.

> [!Note]  
> La valeur de la propriété ajoutée est **null** (non assigné) après cette opération. Pour définir ou modifier la valeur d’une propriété WMI, vous devez définir la propriété [**value**](swbemdatetime-value.md) de l’objet [**SWbemProperty**](swbemproperty.md) retourné.

 

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objProperty = .Add( _
  ByVal strName, _
  ByVal iCIMType, _
  [ ByVal bIsArray ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strName* \[ dans\]
</dt> <dd>

Obligatoire. Nom de la nouvelle propriété.

</dd> <dt>

*iCIMType* \[ dans\]
</dt> <dd>

Obligatoire. Entier qui représente le qualificateur **CimType** de la nouvelle propriété. Consultez [**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum) pour obtenir la liste avec les qualificateurs **CimType** et leurs valeurs.

</dd> <dt>

*bIsArray* \[ dans, facultatif\]
</dt> <dd>

Spécifie si la propriété est un type tableau. La valeur par défaut de ce paramètre est **false**.

</dd> <dt>

*IFlags* \[ dans, facultatif\]
</dt> <dd>

Réservé et doit être égal à zéro s’il est spécifié.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, cette méthode retourne un objet [**SWbemProperty**](swbemproperty.md) qui représente la nouvelle propriété. Dans le cas contraire, un objet **null** est retourné.

## <a name="error-codes"></a>Codes d’erreur

Une fois la méthode **Add** terminée, l’objet **Err** peut contenir l’un des codes d’erreur ci-dessous.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Échec non spécifié.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Un paramètre non valide a été spécifié.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Mémoire insuffisante pour l’exécution de cette méthode.

</dd> <dt>

**wbemErrInvalidPropertyType** -2147749930
</dt> <dd>

Le qualificateur **CimType** n’est pas reconnu.

</dd> </dl>

## <a name="examples"></a>Exemples

Pour obtenir un exemple de code qui utilise cette méthode, consultez la rubrique [**SWbemPropertySet**](swbempropertyset.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPropertySet<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemPropertySet<br/>                                                       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SWbemPropertySet**](swbempropertyset.md)
</dt> <dt>

[**SWbemPropertySet. Remove**](swbempropertyset-remove.md)
</dt> <dt>

[**SWbemProperty. Value**](swbemproperty-value.md)
</dt> </dl>

 

 




