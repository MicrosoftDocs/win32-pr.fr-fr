---
description: La méthode CheckMediaType détermine si un type de média proposé est compatible avec le format d’affichage.
ms.assetid: 567663cf-c79f-4549-9fa9-b16da957d2b1
title: Méthode CImageDisplay. CheckMediaType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8ebcdbe6bbfe6538a2ea166be0816f31954c7d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525157"
---
# <a name="cimagedisplaycheckmediatype-method"></a>Méthode CImageDisplay. CheckMediaType

La `CheckMediaType` méthode détermine si un type de média proposé est compatible avec le format d’affichage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CheckMediaType(
   const CMediaType *pmtIn
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pmtIn* 
</dt> <dd>

Pointeur vers un objet [**CMediaType**](cmediatype.md) qui contient le type de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                                  | Description                              |
|----------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**E \_ échec**</dt> </dl>       | Type de média non valide.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Type de média non valide.<br/>           |
| <dl> <dt>**\_OK**</dt> </dl>         | Le type de média est compatible.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageDisplay, classe**](cimagedisplay.md)
</dt> </dl>

 

 




