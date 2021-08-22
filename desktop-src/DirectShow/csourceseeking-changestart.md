---
description: La méthode modifiez l’est appelée lorsque la position de début change.
ms.assetid: d0a5497e-43e9-4d1f-9106-1f4cd8fcb372
title: Méthode CSourceSeeking. modifiez l' (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7f7c0d9a86d33d13c95295c5ef1ef46a3e6c02371d1b6520572750450320b1f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073363"
---
# <a name="csourceseekingchangestart-method"></a>Méthode CSourceSeeking. modifiez l'

La `ChangeStart` méthode est appelée lorsque la position de début change.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT ChangeStart() = 0;
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

La méthode [**CSourceSeeking :: SetPositions**](csourceseeking-setpositions.md) appelle cette méthode si la position de début change. Cette méthode est virtuelle pure ; la classe dérivée doit l’implémenter. Après une opération de recherche, les horodatages doivent redémarrer à partir de zéro. Les temps de support doivent refléter la nouvelle heure de début. L’exemple suivant illustre une implémentation possible :


```C++
HRESULT CMyStream::ChangeStart( )
{
    m_rtSampleTime = 0;          // Reset the time stamps.
    m_rtMediaTime = m_rtStart;   // Reset the media times.
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

 

 




