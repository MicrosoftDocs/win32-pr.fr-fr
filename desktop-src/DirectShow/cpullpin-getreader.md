---
description: La méthode GetReader retourne un pointeur vers l’interface IAsyncReader de la broche de sortie.
ms.assetid: bb7ed3f2-a5bc-496c-8a52-f9915a75105e
title: Méthode CPullPin. GetReader (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.GetReader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7880cba8e910c3da8ade049e18ae22e403c0c616246e4dfde94e587a1fcdeab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054999"
---
# <a name="cpullpingetreader-method"></a>Méthode CPullPin. GetReader

La `GetReader` méthode retourne un pointeur vers l’interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) de la broche de sortie.

## <a name="syntax"></a>Syntaxe


```C++
IAsyncReader* GetReader();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers l’interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .

## <a name="remarks"></a>Remarques

L’interface retournée a un nombre de références en attente. L’appelant doit libérer l’interface.

la méthode ne vérifie pas la valeur du pointeur d’interface avant d’appeler **AddRef**, donc n’appelez pas cette méthode tant que vous n’avez pas appelé la méthode [**CPullPin :: Connecter**](cpullpin-connect.md) . Dans le cas contraire, le pointeur d’interface peut être **null** et l’appel de **AddRef** lèvera une exception.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPullPin, classe**](cpullpin.md)
</dt> </dl>

 

 




