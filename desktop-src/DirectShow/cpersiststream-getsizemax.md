---
description: Récupère la taille maximale en octets nécessaire pour le flux actuel, y compris le numéro de version.
ms.assetid: 55ea4568-5ca4-4139-8def-bef20071835d
title: Méthode CPersistStream. GetSizeMax (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 746fb01102642f2d3e6b254ac741c284143aaecfd401fc220bf7a9d97d93e64e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813369"
---
# <a name="cpersiststreamgetsizemax-method"></a>Méthode CPersistStream. GetSizeMax

Récupère la taille maximale en octets nécessaire pour le flux actuel, y compris le numéro de version.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSizeMax(
   ULARGE_INTEGER *pcbSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PCB* 
</dt> <dd>

Pointeur vers la taille en octets nécessaire pour enregistrer ce flux, y compris le numéro de version.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette fonction membre implémente la méthode **IPersistStream :: GetSizeMax** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Pstream. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPersistStream, classe**](cpersiststream.md)
</dt> </dl>

 

 




