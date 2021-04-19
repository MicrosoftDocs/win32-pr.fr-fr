---
description: La fonction GetInterface récupère un pointeur d’interface.
ms.assetid: 75fe8849-c779-4d47-a5ff-5a23308c8a21
title: GetInterface, fonction (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetInterface
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 317f08af2a4ff0e9410c61da8b19d14735a14f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539995"
---
# <a name="getinterface-function"></a>GetInterface, fonction

La `GetInterface` fonction récupère un pointeur d’interface.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetInterface(
   LPUNKNOWN pUnk,
   void      **ppv
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pUnk* 
</dt> <dd>

Pointeur vers l’interface **IUnknown** .

</dd> <dt>

*ppv* 
</dt> <dd>

Adresse d’un pointeur vers l’interface récupérée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Cette fonction membre effectue un incrément thread-safe du décompte de références. Pour récupérer l’interface et ajouter une référence, appelez cette fonction à partir de votre implémentation de substitution de la méthode **INonDelegatingUnknown :: NonDelegatingQueryInterface** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>ComBase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions d’assistance COM**](com-helper-functions.md)
</dt> <dt>

[**INonDelegatingUnknown**](inondelegatingunknown.md)
</dt> </dl>

 

 




