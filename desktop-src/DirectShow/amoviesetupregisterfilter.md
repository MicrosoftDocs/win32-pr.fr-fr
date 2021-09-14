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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112250"
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

## <a name="return-value"></a>Valeur de retour

Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Dllsetup. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions de configuration des DLL**](dll-setup-functions.md)
</dt> </dl>

 

 




