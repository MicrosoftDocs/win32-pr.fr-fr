---
description: 'La méthode SetTimeFormat définit le format d’heure. Cette méthode implémente la méthode IMediaSeeking :: SetTimeFormat.'
ms.assetid: dbc7c950-8cc2-4f8e-adfa-8f5cdc1b56c7
title: Méthode CSourceSeeking. SetTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 61ab0cdf7c954e0fa5f370127f00529bb9ef7b16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537919"
---
# <a name="csourceseekingsettimeformat-method"></a>Méthode CSourceSeeking. SetTimeFormat

La `SetTimeFormat` méthode définit le format d’heure. Cette méthode implémente la méthode [**IMediaSeeking :: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetTimeFormat(
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



| Code de retour                                                                                  | Description                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Opération réussie.<br/>                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Le format spécifié n’est pas pris en charge.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>    | Argument de pointeur **null** .<br/>         |



 

## <a name="remarks"></a>Notes

Le seul format d’heure pris en charge par la classe de base est le format d’heure du \_ \_ \_ temps de support (unités de 100 nanosecondes).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceSeeking, classe**](csourceseeking.md)
</dt> </dl>

 

 




