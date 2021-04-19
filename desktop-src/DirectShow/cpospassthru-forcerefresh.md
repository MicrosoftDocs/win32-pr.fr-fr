---
description: La méthode ForceRefresh est obsolète.
ms.assetid: 9895f72b-abf8-46a8-aa75-2a30901a4c41
title: Méthode CPosPassThru. ForceRefresh (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ForceRefresh
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1955afe069dc419b710978eecf662758916e4cb1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526330"
---
# <a name="cpospassthruforcerefresh-method"></a>Méthode CPosPassThru. ForceRefresh

La `ForceRefresh` méthode est obsolète.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ForceRefresh();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Initialement, cette classe a été conçue pour mettre en cache les pointeurs vers les interfaces [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) et [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) du pin connecté. La `ForceRefresh` méthode a publié ces interfaces.

Comme c’est actuellement le cas, cette classe ne met pas en cache ces interfaces. Pour des éléments de compatibilité, la `ForceRefresh` méthode est toujours incluse, mais retourne la valeur \_ OK sans rien faire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPosPassThru, classe**](cpospassthru.md)
</dt> </dl>

 

 




