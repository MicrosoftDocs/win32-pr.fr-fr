---
description: La méthode SetFormatType spécifie le type de format.
ms.assetid: e8ed9190-7169-4d51-ace7-597f43ff083e
title: Méthode CMediaType. SetFormatType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormatType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6a0582a882ffe40a9bd889ff48e70a52a4048bad57e01077263e607f13d9898
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954418"
---
# <a name="cmediatypesetformattype-method"></a>Méthode CMediaType. SetFormatType

La méthode SetFormatType «» spécifie le type de format.

## <a name="syntax"></a>Syntaxe


```C++
void SetFormatType(
   const GUID *pformattype
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pformattype* 
</dt> <dd>

Pointeur vers un **GUID** qui spécifie le type de format.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode définit le membre **formatType** . Le type de format définit la disposition du bloc de format. Par exemple, si le type de format est \_ VIDEOINFO format, le bloc de format doit contenir une structure **VIDEOINFOHEADER** . Pour définir le bloc de format, appelez la méthode [**CMediaType :: SetFormat**](cmediatype-setformat.md) . L’appelant est chargé de s’assurer que le bloc de format correspond au type de format.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 


``
