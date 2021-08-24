---
description: La méthode Add de l’objet SWbemNamedValueSet ajoute un objet SWbemNamedValue à la collection. Si un élément existe déjà dans la collection avec le même nom, le nouvel élément le remplace.
ms.assetid: 471b23f5-6c53-40e2-a2a9-0798044c9dfb
ms.tgt_platform: multiple
title: Méthode SWbemNamedValueSet. Add (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a7a911dcfa6371421fd4033524400d0c818e814d3bd52f90b677ac7c9fcf1b60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612119"
---
# <a name="swbemnamedvaluesetadd-method"></a>SWbemNamedValueSet. Add, méthode

La méthode **Add** de l’objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) ajoute un objet [**SWbemNamedValue**](swbemnamedvalue.md) à la collection. Si un élément existe déjà dans la collection avec le même nom, le nouvel élément le remplace.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objNamedValue = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strName* \[ dans\]
</dt> <dd>

Obligatoire. Nom de la nouvelle valeur.

</dd> <dt>

*varVal* \[ dans\]
</dt> <dd>

Obligatoire. Variant qui représente la nouvelle valeur.

</dd> <dt>

*IFlags* \[ dans, facultatif\]
</dt> <dd>

Réservé et doit avoir la valeur zéro si elle est spécifiée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, cette méthode retourne l’objet [**SWbemNamedValue**](swbemnamedvalue.md) nouvellement modifié ou nouvellement créé.

## <a name="remarks"></a>Remarques

Pour obtenir des exemples d’ajout et de récupération de valeurs nommées, consultez [**SWbemNamedValue. Value**](swbemnamedvalue-value.md).

## <a name="requirements"></a>Configuration requise



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

 

 




