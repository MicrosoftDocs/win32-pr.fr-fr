---
description: 'La méthode GetInfo récupère des informations sur les paramètres de contrôle de flux actuels, y compris les heures de démarrage et d’arrêt. Cette méthode implémente la méthode IAMStreamControl :: GetInfo.'
ms.assetid: 3bc9bb32-eb33-4752-b22c-9033c28b41f7
title: CBaseStreamControl. GetInfo, méthode (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.GetInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab0ba31fa5692a6bc92372860ec1a28ab776206f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544479"
---
# <a name="cbasestreamcontrolgetinfo-method"></a>CBaseStreamControl. GetInfo, méthode

La `GetInfo` méthode récupère des informations sur les paramètres de contrôle de flux actuels, y compris les heures de démarrage et d’arrêt. Cette méthode implémente la méthode [**IAMStreamControl :: GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-getinfo) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetInfo(
   AM_STREAM_INFO *pInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pInfo* 
</dt> <dd>

Pointeur vers une structure d' [**\_ \_ informations de flux am**](/windows/desktop/api/strmif/ns-strmif-am_stream_info) , allouée par l’appelant, qui reçoit les paramètres de contrôle de flux actuels.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le \_ pointeur S ou OK \_ .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Strmctl. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseStreamControl, classe**](cbasestreamcontrol.md)
</dt> </dl>

 

 




