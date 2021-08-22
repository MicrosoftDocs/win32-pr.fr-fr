---
description: La méthode unregister Supprime le filtre du Registre.
ms.assetid: 2eb70e9f-1acf-433e-972f-24fb32eaeb13
title: CBaseFilter. Unregister, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Unregister
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c57d08c77c9c420cdc45b158a19fa610231f53f6b409d8b650953de0de8381a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317899"
---
# <a name="cbasefilterunregister-method"></a>CBaseFilter. Unregister, méthode

La `Unregister` méthode supprime le filtre du Registre.

> [!Note]  
> Cette méthode est obsolète. Les nouveaux filtres doivent être désinscrits à l’aide de la fonction [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) . pour plus d’informations, consultez [comment inscrire des filtres de DirectShow](how-to-register-directshow-filters.md).

 

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Unregister();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseFilter, classe**](cbasefilter.md)
</dt> </dl>

 

 




