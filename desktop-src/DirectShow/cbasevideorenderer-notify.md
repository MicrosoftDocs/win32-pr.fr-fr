---
description: La méthode Notify reçoit une notification indiquant qu’une modification de qualité est demandée.
ms.assetid: bb9aa1c3-caef-42fb-87d2-75cc3691f64f
title: CBaseVideoRenderer. Notify, méthode (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8674ecbf7951ca0c208f9ffb50c0e5d9591b16552fda266c7d641905edd09a4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052189"
---
# <a name="cbasevideorenderernotify-method"></a>CBaseVideoRenderer. Notify, méthode

La `Notify` méthode reçoit une notification indiquant qu’une modification de qualité est demandée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Notify(
  [in] IBaseFilter *pSelf,
  [in] Quality     q
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSelf* \[ dans\]
</dt> <dd>

Pointeur vers le filtre qui envoie la notification de qualité.

</dd> <dt>

*q* \[ dans\]
</dt> <dd>

Structure de notification de qualité.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette fonction membre implémente la méthode [**IQualityControl :: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) sur le convertisseur vidéo. Elle est appelée, généralement par le gestionnaire de graphe de filtre, lorsque la qualité doit être coupée. Cela peut se produire lorsque la qualité de la lecture audio a été augmentée jusqu’au point que la qualité de la lecture de la vidéo doit être réduite.

`Notify` définit le membre de données **m \_ trThrottle** sur une valeur de délai à insérer entre les frames par [**ThrottleWait**](cbasevideorenderer-throttlewait.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




