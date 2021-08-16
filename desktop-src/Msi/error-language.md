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
ms.openlocfilehash: 966725be2378292215ffaad6c7fc96fb36fd305d2bb2b6053849816dd1fb3f70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082889"
---
# <a name="errorlanguage-property"></a>Error. Language, propriété

La propriété **Language** en lecture seule de l’objet [**Error**](error-object.md) retourne l' **ID de langue** de l’erreur actuelle.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Error.Language
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Remarques

La valeur de la propriété **Language** est-1, sauf si l’erreur est de type MsmErrorLanguageUnsupported ou msmErrorLanguageFailed. Vous pouvez déterminer le type d’erreur en appelant la propriété [**type**](error-type.md) de l’objet [**Error**](error-object.md) .

### <a name="c"></a>C++

Consultez [**obtenir une \_ fonction de langage (objet d’erreur)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

