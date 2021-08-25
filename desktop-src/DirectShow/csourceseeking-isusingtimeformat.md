---
description: La méthode IsUsingTimeFormat détermine si un format d’heure spécifié est le format en cours d’utilisation.
ms.assetid: 86965bfc-fc9f-42d3-bcaa-2049195b98bd
title: Méthode CSourceSeeking. IsUsingTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b930746102bc43e3549b4565a7591f4ac5fee8cc6503d9fb6aadcbe1659a52f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054239"
---
# <a name="csourceseekingisusingtimeformat-method"></a>Méthode CSourceSeeking. IsUsingTimeFormat

La `IsUsingTimeFormat` méthode détermine si un format d’heure spécifié est le format en cours d’utilisation.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsUsingTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFormat* 
</dt> <dd>

Pointeur vers un GUID de format d’heure. Consultez [**GUID de format d’heure**](time-format-guids.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.



| Code de retour                                                                               | Description                                                |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | Le format spécifié n’est pas le format actuel.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>      | Le format spécifié est le format actuel.<br/>     |
| <dl> <dt>**\_pointeur E**</dt> </dl> | Argument de pointeur **null** .<br/>                      |



 

## <a name="remarks"></a>Remarques

Le seul format d’heure pris en charge par la classe de base est le format d’heure du \_ \_ \_ temps de support (unités de 100 nanosecondes).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceSeeking, classe**](csourceseeking.md)
</dt> </dl>

 

 




