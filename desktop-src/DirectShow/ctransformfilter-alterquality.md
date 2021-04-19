---
description: La méthode AlterQuality avertit le filtre qu’une modification de qualité est demandée.
ms.assetid: 46743d6b-65cf-4d63-8913-114277d76da4
title: Méthode CTransformFilter. AlterQuality (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 592fc67dd5cee5e4f76b8171b6e842532d71371b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520833"
---
# <a name="ctransformfilteralterquality-method"></a>Méthode CTransformFilter. AlterQuality

La `AlterQuality` méthode notifie le filtre qu’une modification de qualité est demandée.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*question* 
</dt> <dd>

Structure de [**qualité**](/windows/win32/api/strmif/ns-strmif-quality) qui contient le message de contrôle qualité.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                             | Description                                                                           |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Le message de qualité n’a pas été géré. Le message doit être passé en amont.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Le message de qualité a été géré. Aucune action supplémentaire n’est nécessaire.<br/>               |



 

## <a name="remarks"></a>Notes

Substituez cette méthode si le filtre peut effectuer un contrôle de qualité. Pour plus d’informations, consultez [gestion du contrôle qualité](quality-control-management.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




