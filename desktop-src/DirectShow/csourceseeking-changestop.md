---
description: La méthode ChangeStop est appelée lorsque la position d’arrêt change.
ms.assetid: 3d4a73a4-68e6-449c-9637-62cad937c4b4
title: Méthode CSourceSeeking. ChangeStop (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 09473b5bbe20c6c31748f0079594424f7e0afa62e2594ff1cc80f33cb1f5e6bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103119"
---
# <a name="csourceseekingchangestop-method"></a>Méthode CSourceSeeking. ChangeStop

La `ChangeStop` méthode est appelée lorsque la position d’arrêt change.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT ChangeStop() = 0;
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

La méthode [**CSourceSeeking :: SetPositions**](csourceseeking-setpositions.md) appelle cette méthode si la position d’arrêt change. Cette méthode est virtuelle pure ; la classe dérivée doit l’implémenter. L’exemple suivant illustre une implémentation possible :


```C++
HRESULT CMyStream::ChangeStop( )
{
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceSeeking, classe**](csourceseeking.md)
</dt> </dl>

 

 




