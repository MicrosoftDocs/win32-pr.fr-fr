---
description: La méthode Item de l’objet SWbemObjectSet obtient un SWbemObject à partir de la collection.
ms.assetid: da91683c-9895-4110-9f51-c340a0c52aec
ms.tgt_platform: multiple
title: SWbemObjectSet. Item, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Item
- ISWbemObjectSet.Item
- ISWbemObjectSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 69267b86a45cc1b95160e1400440b868426b7cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519818"
---
# <a name="swbemobjectsetitem-method"></a>SWbemObjectSet. Item, méthode

La méthode **Item** de l’objet [**SWbemObjectSet**](swbemobjectset.md) obtient un [**SWbemObject**](swbemobject.md) à partir de la collection.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objWbemObject = .Item( _
  ByVal strObjectPath _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strObjectPath* 
</dt> <dd>

Obligatoire. Chemin d’accès relatif de l’objet à récupérer de la collection. Exemple : \_ disque logique Win32 = "C :"

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, l’objet [**SWbemObject**](swbemobject.md) demandé retourne.

## <a name="error-codes"></a>Codes d’erreur

À la fin de la méthode **Item** , l’objet **Err** peut contenir l’un des codes d’erreur ci-dessous.

<dl> <dt>

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

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

L’élément demandé est introuvable.

</dd> </dl>

## <a name="remarks"></a>Notes

La méthode **Item** peut nécessiter beaucoup de temps processeur, car une énumération complète par le fournisseur des éléments de l’ensemble est nécessaire pour retourner le résultat.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectSet<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemObjectSet<br/>                                                         |



 

 




