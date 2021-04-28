---
description: 'Méthode CSourceSeeking. GetCapabilities : la méthode GetCapabilities récupère toutes les fonctionnalités de recherche du flux. Cette méthode implémente la méthode IMediaSeeking :: GetCapabilities.'
ms.assetid: a2ff7ea2-09bd-49a7-8e1b-d6360939036e
title: Méthode CSourceSeeking. GetCapabilities (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f1f354381c4c99cf880c75cbbc4b13355e386030
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098777"
---
# <a name="csourceseekinggetcapabilities-method"></a>Méthode CSourceSeeking. GetCapabilities

La `GetCapabilities` méthode récupère toutes les fonctionnalités de recherche du flux. Cette méthode implémente la méthode [**IMediaSeeking :: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCapabilities* 
</dt> <dd>

Pointeur vers une variable qui reçoit une combinaison d’opérations de bits des indicateurs de [**\_ \_ \_ fonctionnalités de recherche de AM**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.



| Code de retour                                                                               | Description                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Opération réussie<br/>                |
| <dl> <dt>**\_pointeur E**</dt> </dl> | Valeur de pointeur **null**<br/> |



 

## <a name="remarks"></a>Notes 

Les fonctionnalités de recherche sont spécifiées par la variable membre [**CSourceSeeking :: m \_ dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceSeeking, classe**](csourceseeking.md)
</dt> </dl>

 

 




