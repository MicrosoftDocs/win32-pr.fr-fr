---
description: 'Méthode CTransformInputPin. EndOfStream : la méthode EndOfStream indique au code confidentiel qu’aucune donnée supplémentaire n’est attendue. Cette méthode implémente la méthode IPin :: EndOfStream.'
ms.assetid: db9896eb-3db2-4d58-a787-4d80ce8f0d0e
title: Méthode CTransformInputPin. EndOfStream (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2035d0261447826098162f480ddc959544b101b7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084977"
---
# <a name="ctransforminputpinendofstream-method"></a>Méthode CTransformInputPin. EndOfStream

La `EndOfStream` méthode indique au code confidentiel qu’aucune donnée supplémentaire n’est attendue. Cette méthode implémente la méthode [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                           | Description                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Réussite.<br/>                         |
| <dl> <dt>**S \_ false**</dt> </dl>               | Le code PIN est en cours de vidage.<br/>       |
| <dl> <dt>**VFW \_ E \_ non \_ connecté**</dt> </dl> | La broche de sortie n’est pas connectée.<br/> |
| <dl> <dt>**\_erreur d' \_ exécution VFW E \_**</dt> </dl> | Une erreur d’exécution s’est produite.<br/>       |
| <dl> <dt>**VFW \_ E \_ état incorrect \_**</dt> </dl>   | Le code PIN est arrêté.<br/>              |



 

## <a name="remarks"></a>Notes 

Cette méthode appelle la méthode [**CTransformFilter :: EndOfStream**](ctransformfilter-endofstream.md) du filtre pour remettre la notification de fin de flux en aval.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




