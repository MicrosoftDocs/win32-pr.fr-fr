---
description: Obsolète. Utilisez AMovieSetupRegisterFilter2 à la place.
ms.assetid: 42278829-d09e-46c7-8f1a-fa4572f7cc00
title: AMovieSetupRegisterFilter, fonction (DLLSETUP. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieSetupRegisterFilter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 398d2d727e26feaca23d6bddbdcbc8a578d096eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528804"
---
# <a name="amoviesetupregisterfilter-function"></a>AMovieSetupRegisterFilter fonction)

Obsolète. Utilisez [**AMovieSetupRegisterFilter2**](amoviesetupregisterfilter2.md) à la place.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AMovieSetupRegisterFilter(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper              *pIFM,
         BOOL                       bRegister
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*psetupdata* 
</dt> <dd>

Réservé.

</dd> <dt>

*pIFM* 
</dt> <dd>

Réservé.

</dd> <dt>

*bRegister* 
</dt> <dd>

Réservé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DLLSETUP. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions de configuration des DLL**](dll-setup-functions.md)
</dt> </dl>

 

 




