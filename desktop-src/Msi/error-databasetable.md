---
description: La propriété DatabaseTable en lecture seule de l’objet Error retourne le nom de la table dans la base de données qui a provoqué l’erreur.
ms.assetid: 38ff45ca-4bd6-43f3-88ad-db4077daeb77
title: Erreur. DatabaseTable, propriété (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseTable
- IMsmError.get_DatabaseTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: b9e52523b37c90de4c4592fdeb059e6269f4e05e240242e69e14f0be6d4d53a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378170"
---
# <a name="errordatabasetable-property"></a>Error. DatabaseTable, propriété

La propriété **DatabaseTable** en lecture seule de l’objet [**Error**](error-object.md) retourne le nom de la table dans la base de données qui a provoqué l’erreur.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Error.DatabaseTable
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Remarques

La collection est vide si les valeurs ne s’appliquent pas au type de l’erreur. Vous pouvez déterminer le type d’erreur en appelant la propriété [**type**](error-type.md) de l’objet [**Error**](error-object.md) .

### <a name="c"></a>C++

Consultez la fonction [**obtenir \_ DatabaseTable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasetable) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

