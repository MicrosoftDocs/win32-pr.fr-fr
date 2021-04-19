---
description: La propriété Language en lecture seule de l’objet Error retourne l’ID de langue de l’erreur actuelle.
ms.assetid: f47cad5d-8e76-4210-b1ab-377d2d05379e
title: Propriété Error. Language (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Language
- IMsmError.get_Language
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 6c80802c41f076a2b1c0b320b591bc591da8546e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541384"
---
# <a name="errorlanguage-property"></a>Error. Language, propriété

La propriété **Language** en lecture seule de l’objet [**Error**](error-object.md) retourne l' **ID de langue** de l’erreur actuelle.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Error.Language
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Notes

La valeur de la propriété **Language** est-1, sauf si l’erreur est de type MsmErrorLanguageUnsupported ou msmErrorLanguageFailed. Vous pouvez déterminer le type d’erreur en appelant la propriété [**type**](error-type.md) de l’objet [**Error**](error-object.md) .

### <a name="c"></a>C++

Consultez [**obtenir une \_ fonction de langage (objet d’erreur)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

