---
description: 'La méthode SetProperties définit les propriétés de l’exemple. Cette méthode implémente la méthode IMediaSample2 :: SetProperties.'
ms.assetid: 639aedf5-0c21-4578-b336-91859e40f3be
title: CMediaSample. SetProperties, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c5e6ef3c3839825586bf47259cf44783d167f503
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219108"
---
# <a name="cmediasamplesetproperties-method"></a>CMediaSample. SetProperties, méthode

La `SetProperties` méthode définit les propriétés de l’exemple. Cette méthode implémente la méthode [**IMediaSample2 :: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetProperties(
         DWORD cbProperties,
   const BYTE  *pbProperties
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cbProperties* 
</dt> <dd>

Longueur des données de propriété à définir, en octets.

</dd> <dt>

*pbProperties* 
</dt> <dd>

Pointeur vers une mémoire tampon de taille *cbProperties*.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                   | Description                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Succès<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Argument non valide<br/>          |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante<br/>       |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Argument de pointeur **null**<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

 




