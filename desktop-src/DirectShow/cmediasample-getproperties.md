---
description: 'La méthode GetProperties récupère les propriétés de l’exemple. Cette méthode implémente la méthode IMediaSample2 :: GetProperties.'
ms.assetid: c2a6d611-9c17-41fb-bb6d-f5b17f1c9966
title: CMediaSample. GetProperties, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 856da0c73f3dd93d0c660f55aa0a9de35d87ab1b270df2179d7ad0b520e6d0a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074023"
---
# <a name="cmediasamplegetproperties-method"></a>CMediaSample. GetProperties, méthode

La `GetProperties` méthode récupère les propriétés de l’exemple. Cette méthode implémente la méthode [**IMediaSample2 :: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetProperties(
   DWORD cbProperties,
   BYTE  *pbProperties
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cbProperties* 
</dt> <dd>

Longueur des données de propriété à récupérer, en octets.

</dd> <dt>

*pbProperties* 
</dt> <dd>

Pointeur vers une mémoire tampon de taille *cbProperties*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                               | Description                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Réussite.<br/>                   |
| <dl> <dt>**\_pointeur E**</dt> </dl> | Argument de pointeur **null** .<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

 




