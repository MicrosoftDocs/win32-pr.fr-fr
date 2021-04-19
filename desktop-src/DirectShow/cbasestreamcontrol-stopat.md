---
description: 'La méthode STOPAT indique au code PIN quand arrêter la transmission de données. Cette méthode implémente la méthode IAMStreamControl :: STOPAT.'
ms.assetid: cc9f0fdc-253b-4feb-95ce-56ebc575a49b
title: CBaseStreamControl. STOPAT, méthode (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StopAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e6b794f5f05721f403d943252c2aabd48614519
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537309"
---
# <a name="cbasestreamcontrolstopat-method"></a>CBaseStreamControl. STOPAT, méthode

La `StopAt` méthode informe le code confidentiel quand il faut arrêter la transmission des données. Cette méthode implémente la méthode [**IAMStreamControl :: STOPAT**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT StopAt(
   const REFERENCE_TIME *ptStop = NULL,
         BOOL           bSendExtra = FALSE,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ptStop* 
</dt> <dd>

Pointeur vers une valeur de [**\_ temps de référence**](reference-time.md) qui spécifie quand le code confidentiel doit cesser de transmettre des données.

</dd> <dt>

*bSendExtra* 
</dt> <dd>

Spécifie une valeur booléenne qui indique s’il faut envoyer un échantillon supplémentaire après l’heure d’arrêt planifiée. Si la **valeur est true**, le code PIN envoie un échantillon supplémentaire.

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

 

 




