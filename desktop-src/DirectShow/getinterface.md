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
ms.openlocfilehash: 289c6e56d4b5387fe9224e476c69865107102141b687825cdfd9a717f482632c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537029"
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

## <a name="remarks"></a>Remarques

Cette fonction membre effectue un incrément thread-safe du décompte de références. Pour récupérer l’interface et ajouter une référence, appelez cette fonction à partir de votre implémentation de substitution de la méthode **INonDelegatingUnknown :: NonDelegatingQueryInterface** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>combase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions d’assistance COM**](com-helper-functions.md)
</dt> <dt>

[**INonDelegatingUnknown**](inondelegatingunknown.md)
</dt> </dl>

 

 




