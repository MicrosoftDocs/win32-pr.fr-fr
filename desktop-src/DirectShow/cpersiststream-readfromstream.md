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
ms.openlocfilehash: 39f40871e12a069045197d0cc61970c7d7f88c784f6b0873c294727b75121ae6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073643"
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

## <a name="remarks"></a>Remarques

La version par défaut ne lit rien ; Il peut être substitué pour lire des données spécifiques à votre classe.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Pstream. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPersistStream, classe**](cpersiststream.md)
</dt> </dl>

 

 




