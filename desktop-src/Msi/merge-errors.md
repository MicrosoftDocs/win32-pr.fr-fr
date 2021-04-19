---
description: La propriété des erreurs en lecture seule de l’objet Merge retourne une collection d’objets Error qui est le jeu actuel d’erreurs.
ms.assetid: 619f17cc-131a-4262-ad48-9ab1318142aa
title: Merge. Errors, propriété (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Errors
- IMsmMerge.get_Errors
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9f07bdbba9fecf48001aed1fbcd42e02abb5c5c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532619"
---
# <a name="mergeerrors-property"></a>Merge. Errors, propriété

La propriété des **Erreurs** en lecture seule de l’objet [**Merge**](merge-object.md) retourne une collection d’objets [**Error**](error-object.md) qui est le jeu actuel d’erreurs.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Merge.Errors
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Notes

La récupération est non destructrice. Plusieurs instances de la collection d’erreurs peuvent être récupérées en appelant à plusieurs reprises cette méthode.

### <a name="c"></a>C++

Consultez la fonction [**obtenir des \_ Erreurs**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
