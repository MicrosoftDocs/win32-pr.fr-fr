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
ms.openlocfilehash: eefcc64b4692363c8caa8f39a3a0db9beb0d08b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923580"
---
# <a name="csourceseekingchangestop-method"></a>Méthode CSourceSeeking. ChangeStop

La `ChangeStop` méthode est appelée lorsque la position d’arrêt change.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT ChangeStop() = 0;
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

La méthode [**CSourceSeeking :: SetPositions**](csourceseeking-setpositions.md) appelle cette méthode si la position d’arrêt change. Cette méthode est virtuelle pure ; la classe dérivée doit l’implémenter. L’exemple suivant illustre une implémentation possible :


```C++
HRESULT CMyStream::ChangeStop( )
{
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceSeeking, classe**](csourceseeking.md)
</dt> </dl>

 

 




