---
description: La méthode Remove de l’objet SWbemPropertySet supprime une propriété de la collection SWbemPropertySet.
ms.assetid: 2a1005db-033c-48f9-8ea0-0bd43b8c989f
ms.tgt_platform: multiple
title: SWbemPropertySet. Remove, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Remove
- ISWbemPropertySet.Remove
- ISWbemPropertySet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7a79c99243cbbb18e761295980b98e56a6db926e3885de6ed2d0b53aafe084db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897909"
---
# <a name="swbempropertysetremove-method"></a>SWbemPropertySet. Remove, méthode

La méthode **Remove** de l’objet [**SWbemPropertySet**](swbempropertyset.md) supprime une propriété de la collection **SWbemPropertySet** .

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
SWbemPropertySet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strName* \[ dans\]
</dt> <dd>

Obligatoire. Nom de l’élément à supprimer.

</dd> <dt>

*IFlags* \[ dans, facultatif\]
</dt> <dd>

Réservé. Cette valeur doit être égale à 0 (zéro) si elle est spécifiée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

À la fin de la méthode **Remove** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Échec non spécifié.

</dd> <dt>

**wbemErrInvalidOperation** -2147749910 (0x80041016)
</dt> <dd>

L’utilisateur a tenté de supprimer une propriété qui ne peut pas être supprimée.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Un paramètre non valide a été spécifié.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

La propriété spécifiée n’existe pas.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Mémoire insuffisante pour l’exécution de cette méthode.

</dd> <dt>

**wbemErrPropagatedProperty** -142927303552 (0x2147219380)
</dt> <dd>

L’utilisateur a tenté de supprimer une propriété qui n’était pas propriétaire. La propriété est héritée d'une classe parente.

</dd> <dt>

**wbemErrResetToDefault** -2147758082 (0x80043002)
</dt> <dd>

L’utilisateur a supprimé une valeur par défaut de remplacement pour la classe actuelle. La valeur par défaut de cette propriété dans la classe parente a été réactivée.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les propriétés ne peuvent pas être supprimées des instances de classe ou des classes dérivées avec des propriétés héritées. Une telle tentative de suppression génère une erreur et la propriété n’est pas supprimée. la propriété est réinitialisée à sa valeur par défaut.

Vous ne pouvez pas itérer une collection lors de la suppression d’éléments, car lorsque vous supprimez un élément d’une collection, le pointeur de collection est déplacé vers l’élément suivant. Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md).

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

[**SWbemPropertySet. Add**](swbempropertyset-add.md)
</dt> </dl>

 

 




