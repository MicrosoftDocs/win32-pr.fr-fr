---
description: La fonction LoadOLEAut32 charge la bibliothèque de liens dynamiques (OleAut32.dll) Automation.
ms.assetid: af907341-1e2c-4c63-bf4e-d6c49b4f6a6e
title: LoadOLEAut32 fonction) (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadOLEAut32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b23bad7e445eebc78ecf8a849ddde8fc23746131
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007488"
---
# <a name="loadoleaut32-function"></a>LoadOLEAut32 fonction)

La fonction **LoadOLEAut32** charge la bibliothèque de liens dynamiques (OleAut32.dll) Automation.

## <a name="syntax"></a>Syntaxe


```C++
HINSTANCE LoadOLEAut32(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Retourne un handle vers une instance de DLL Automation.

## <a name="remarks"></a>Notes

Lorsque le destructeur [**CBaseObject**](cbaseobject.md) détruit l’objet qui a chargé OleAut32.dll, il décharge la bibliothèque si elle est toujours chargée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>combase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions d’assistance COM**](com-helper-functions.md)
</dt> </dl>

 

 




