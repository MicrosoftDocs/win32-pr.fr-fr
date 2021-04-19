---
description: 'La méthode Started indique au code confidentiel quand commencer à transmettre des données. Cette méthode implémente la méthode IAMStreamControl :: startat.'
ms.assetid: fd2943e8-8d35-4122-a99e-96d12459b335
title: CBaseStreamControl. StartAt, méthode (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StartAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7adcf7cbd435992333bb8ae59d5ab1674056223
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542216"
---
# <a name="cbasestreamcontrolstartat-method"></a>CBaseStreamControl. StartAt, méthode

La `StartAt` méthode informe le code confidentiel quand il faut commencer à transmettre des données. Cette méthode implémente la méthode [**IAMStreamControl :: startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT StartAt(
   const REFERENCE_TIME *ptStart = NULL,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ptStart* 
</dt> <dd>

Pointeur vers une valeur de [**\_ temps de référence**](reference-time.md) qui spécifie quand le code confidentiel doit commencer à transmettre des données.

</dd> <dt>

*dwCookie* 
</dt> <dd>

Spécifie une valeur à envoyer avec la notification de démarrage.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Strmctl. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseStreamControl, classe**](cbasestreamcontrol.md)
</dt> </dl>

 

 




