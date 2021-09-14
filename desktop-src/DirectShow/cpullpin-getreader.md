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
ms.openlocfilehash: 3a20bbb689c4ee5e3ac12c510098163d9fbb224e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007601"
---
# <a name="cpullpingetreader-method"></a>Méthode CPullPin. GetReader

La `GetReader` méthode retourne un pointeur vers l’interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) de la broche de sortie.

## <a name="syntax"></a>Syntaxe


```C++
IAsyncReader* GetReader();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne un pointeur vers l’interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .

## <a name="remarks"></a>Notes

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

 

 




