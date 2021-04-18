---
description: La méthode Register ajoute le filtre au registre.
ms.assetid: 934e421a-25a6-40fa-a48b-6d7331f34b78
title: CBaseFilter. Register, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Register
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bd7ba5a57d670ef28ffda022c95c7dc5b12df77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540633"
---
# <a name="cbasefilterregister-method"></a>CBaseFilter. Register, méthode

La `Register` méthode ajoute le filtre au registre.

> [!Note]  
> Cette méthode est obsolète. Les nouveaux filtres doivent être inscrits à l’aide de la fonction [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) . Pour plus d’informations, consultez [comment inscrire des filtres DirectShow](how-to-register-directshow-filters.md).

 

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Register();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.



| Code de retour                                                                             | Description                                          |
|-----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>    | Opération réussie.<br/>                                  |
| <dl> <dt>**S \_ false**</dt> </dl> | Aucune information d’inscription n’est disponible.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseFilter, classe**](cbasefilter.md)
</dt> </dl>

 

 




