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
ms.openlocfilehash: 075fba028dd045c831adb84a7133fd524398fc74037b7e3c31116b76a4c95a1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086039"
---
# <a name="errordatabasekeys-property"></a>Error. DatabaseKeys, propriété

La propriété **DatabaseKeys** en lecture seule de l’objet [**Error**](error-object.md) retourne une collection de chaînes qui contient les clés primaires de la ligne de base de données à l’origine de l’erreur. Il existe une clé par entrée dans la collection.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Error.DatabaseKeys
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Remarques

Le client est responsable de la libération de la collection de chaînes lorsqu’il n’est plus nécessaire.

La collection est vide si les valeurs ne s’appliquent pas au type de l’erreur. Vous pouvez déterminer le type d’erreur en appelant la propriété [**type**](error-type.md) de l’objet [**Error**](error-object.md) .

### <a name="c"></a>C++

Consultez la fonction [**obtenir \_ DatabaseKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

