---
description: Lit les données du filtre à partir du flux donné.
ms.assetid: 009f4812-8cc6-436a-9553-3a3161d5e992
title: Méthode CPersistStream. ReadFromStream (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.ReadFromStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce6c037fbce9fbaeabf7491b1b840000f67e25d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540503"
---
# <a name="cpersiststreamreadfromstream-method"></a>Méthode CPersistStream. ReadFromStream

Lit les données du filtre à partir du flux donné.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT ReadFromStream(
   IStream *pStream
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pStream* 
</dt> <dd>

Pointeur vers une interface **IStream** à partir de laquelle les données doivent être lues.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK. La classe dérivée doit retourner une valeur **HRESULT** valide.

## <a name="remarks"></a>Notes

La version par défaut ne lit rien ; Il peut être substitué pour lire des données spécifiques à votre classe.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PStream. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPersistStream, classe**](cpersiststream.md)
</dt> </dl>

 

 




