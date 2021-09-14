---
description: La méthode ChangeRate est appelée lorsque la vitesse de lecture change.
ms.assetid: c4f1f9d0-6c09-4cab-8a37-dd1ff3f5619f
title: Méthode CSourceSeeking. ChangeRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02fab05d65929233b97f7d53e497bae6593c472a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923584"
---
# <a name="csourceseekingchangerate-method"></a>Méthode CSourceSeeking. ChangeRate

La `ChangeRate` méthode est appelée lorsque la vitesse de lecture change.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT ChangeRate() = 0;
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

La méthode [**CSourceSeeking ::**](csourceseeking-setrate.md) se, appelle cette méthode, que la classe dérivée doit implémenter. La méthode sesente met à **jour la variable** membre [**CSourceSeeking :: m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) , mais ne valide pas la nouvelle valeur. Un taux de zéro doit toujours être rejeté. Les taux inférieurs à zéro indiquent une lecture négative. La plupart des filtres ne prennent pas en charge les taux négatifs.

L’exemple suivant illustre une implémentation possible :


```C++
HRESULT CMyStream::ChangeRate( )
{
    {   // Scope for critical section lock.
        CAutoLock cAutoLockSeeking(CSourceSeeking::m_pLock);
        if( m_dRateSeeking <= 0 ) {
            m_dRateSeeking = 1.0;  // Reset to a reasonable value.
            return E_FAIL;
        }
    }
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

 

 




