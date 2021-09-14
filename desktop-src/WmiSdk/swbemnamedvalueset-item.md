---
description: La méthode Item de l’objet SWbemNamedValueSet obtient un objet SWbemNamedValue de la collection.
ms.assetid: ccebe65e-6032-43d5-9004-2247c3b96d6d
ms.tgt_platform: multiple
title: SWbemNamedValueSet. Item, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Item
- ISWbemNamedValueSet.Item
- ISWbemNamedValueSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a4932409fa7b8ac9e0f326e5de7e8ecf0f89c2b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918740"
---
# <a name="swbemnamedvaluesetitem-method"></a>SWbemNamedValueSet. Item, méthode

La méthode **Item** de l’objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) obtient un objet [**SWbemNamedValue**](swbemnamedvalue.md) de la collection.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objNamedValue = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strName* \[ dans\]
</dt> <dd>

Obligatoire. Nom de la valeur à récupérer.

</dd> <dt>

*IFlags* \[ dans, facultatif\]
</dt> <dd>

Réservé. Cette valeur doit être égale à zéro si elle est spécifiée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

En cas de réussite, l’objet [**SWbemNamedValue**](swbemnamedvalue.md) demandé est retourné.

## <a name="error-codes"></a>Codes d’erreur

À la fin de la méthode **Item** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erreur non spécifiée.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Un paramètre non valide a été spécifié ou l’espace de noms n’a pas pu être analysé.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Mémoire insuffisante pour terminer l’opération.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

L'élément demandé est introuvable.

</dd> </dl>

## <a name="remarks"></a>Notes

Pour obtenir des exemples d’ajout et de récupération de valeurs nommées, consultez [**SWbemNamedValue. Value**](swbemnamedvalue-value.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemNamedValueSet<br/>                                                    |
| IID<br/>                      | IID \_ ISWbemNamedValueSet<br/>                                                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SWbemNamedValueSet**](swbemnamedvalueset.md)
</dt> </dl>

 

 




