---
description: La propriété DatabaseKeys en lecture seule de l’objet Error retourne une collection de chaînes qui contient les clés primaires de la ligne de base de données à l’origine de l’erreur. Il existe une clé par entrée dans la collection.
ms.assetid: 416a6cef-4c70-4c06-a8d2-801c9440e25a
title: Erreur. DatabaseKeys, propriété (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseKeys
- IMsmError.get_DatabaseKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: c0de387c0101e7b79e64486089abcbd49f5d60d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091373"
---
# <a name="errordatabasekeys-property"></a>Error. DatabaseKeys, propriété

La propriété **DatabaseKeys** en lecture seule de l’objet [**Error**](error-object.md) retourne une collection de chaînes qui contient les clés primaires de la ligne de base de données à l’origine de l’erreur. Il existe une clé par entrée dans la collection.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Error.DatabaseKeys
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Notes

Le client est responsable de la libération de la collection de chaînes lorsqu’il n’est plus nécessaire.

La collection est vide si les valeurs ne s’appliquent pas au type de l’erreur. Vous pouvez déterminer le type d’erreur en appelant la propriété [**type**](error-type.md) de l’objet [**Error**](error-object.md) .

### <a name="c"></a>C++

Consultez la fonction [**obtenir \_ DatabaseKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

