---
description: Écrit les données du filtre dans le flux donné.
ms.assetid: 1b405050-6cfd-4b69-b449-f00a6ecfac6a
title: Méthode CPersistStream. WriteToStream (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.WriteToStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 893d58986db92e50cbafefe74676481162808abf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526726"
---
# <a name="cpersiststreamwritetostream-method"></a>Méthode CPersistStream. WriteToStream

Écrit les données du filtre dans le flux donné.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT WriteToStream(
   IStream *pStream
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pStream* 
</dt> <dd>

Pointeur vers une interface **IStream** qui spécifie le flux de destination des données de filtre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK. La classe dérivée doit retourner une valeur **HRESULT** valide.

## <a name="remarks"></a>Notes

La version par défaut n’écrit rien. Il peut être substitué pour écrire des données spécifiques à votre classe.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PStream. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPersistStream, classe**](cpersiststream.md)
</dt> </dl>

 

 




