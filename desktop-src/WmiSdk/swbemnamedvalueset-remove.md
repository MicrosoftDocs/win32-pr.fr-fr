---
description: La méthode Remove de l’objet SWbemNamedValueSet supprime une valeur nommée du contexte.
ms.assetid: 8cb353fb-c6d7-41d9-a2d0-ff1ad37264e4
ms.tgt_platform: multiple
title: SWbemNamedValueSet. Remove, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Remove
- ISWbemNamedValueSet.Remove
- ISWbemNamedValueSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d41ecd7d28b95534c8e6d88d1c57756c269cf790
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918736"
---
# <a name="swbemnamedvaluesetremove-method"></a>SWbemNamedValueSet. Remove, méthode

La méthode **Remove** de l’objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) supprime une valeur nommée du contexte.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
SWbemNamedValueSet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strName* \[ dans\]
</dt> <dd>

Obligatoire. Nom de la valeur à supprimer.

</dd> <dt>

*IFlags* \[ dans, facultatif\]
</dt> <dd>

Réservé. Cette valeur doit être égale à zéro si elle est spécifiée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

À la fin de la méthode **Remove** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erreur non spécifiée.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Un paramètre non valide a été spécifié ou l’espace de noms n’a pas pu être analysé.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

L'élément demandé est introuvable.

</dd> </dl>

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

 

 




