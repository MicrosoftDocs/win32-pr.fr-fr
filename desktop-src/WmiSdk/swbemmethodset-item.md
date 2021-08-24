---
description: La méthode Item de l’objet SWbemMethodSet retourne un objet nommé SWbemMethod à partir de la collection.
ms.assetid: 4c1bbecc-b38b-4869-9c8c-b9321536b23e
ms.tgt_platform: multiple
title: SWbemMethodSet. Item, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet.Item
- ISWbemMethodSet.Item
- ISWbemMethodSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: fd78277be4611507a7f7a488dae0d4edda832afeac8c4a947d4c56277d9af397
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679449"
---
# <a name="swbemmethodsetitem-method"></a>SWbemMethodSet. Item, méthode

La méthode **Item** de l’objet [**SWbemMethodSet**](swbemmethodset.md) retourne un objet nommé [**SWbemMethod**](swbemmethod.md) à partir de la collection.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objMethod = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strName* \[ dans\]
</dt> <dd>

Obligatoire. Nom de la méthode à récupérer.

</dd> <dt>

*IFlags* \[ dans, facultatif\]
</dt> <dd>

Réservé. La valeur par défaut est 0.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, l’objet [**SWbemMethod**](swbemmethod.md) demandé retourne.

## <a name="error-codes"></a>Codes d’erreur

À la fin de la méthode **Item** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

<dl> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Le paramètre *IFlags* n’est pas valide.

</dd> <dt>

**wbemErrFailed** -2147749894
</dt> <dd>

Erreur non spécifiée.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

La méthode spécifiée n’existe pas.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemMethodSet<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemMethodSet<br/>                                                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SWbemMethodSet**](swbemmethodset.md)
</dt> <dt>

[**SWbemMethod**](swbemmethod.md)
</dt> </dl>

 

 




