---
description: La méthode EOS met à jour les horodatages mis en cache après une notification de fin de flux.
ms.assetid: 7fb2f964-ec15-47f5-902b-29b9b121e876
title: CRendererPosPassThru. EOS, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10f87fbb66f8ad1d89ff31c6653780b3fde23ecbaf55d72b6f3de2f59546b49b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073413"
---
# <a name="crendererpospassthrueos-method"></a>CRendererPosPassThru. EOS, méthode

La `EOS` méthode met à jour les horodatages mis en cache après une notification de fin de flux.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EOS();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                            | Description                                               |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Réussite.<br/>                                       |
| <dl> <dt>**E \_ échec**</dt> </dl> | Échec. Le filtre n’est peut-être pas diffusé.<br/> |



 

## <a name="remarks"></a>Remarques

Le filtre doit appeler cette méthode lorsqu’il reçoit une notification de fin de flux ([**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)). La méthode définit les horodatages mis en cache comme étant égaux à la position d’arrêt, ce qui garantit que la méthode [**IMediaSeeking :: getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) retourne les valeurs correctes à la fin du flux.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




