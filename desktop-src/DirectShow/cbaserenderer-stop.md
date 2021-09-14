---
description: La méthode Stop arrête le filtre.
ms.assetid: 80eac207-5db3-4b06-bbae-eca72e37d09d
title: CBaseRenderer. Stop, méthode (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ddd8194bbf76c4a4311aa90335f94d1e7548a356
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999743"
---
# <a name="cbaserendererstop-method"></a>CBaseRenderer. Stop, méthode

La `Stop` méthode arrête le filtre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Cette méthode remplace la méthode [**CBaseFilter :: Stop**](cbasefilter-stop.md) . Il effectue les actions suivantes :

-   Appelle [**CBaseFilter :: Stop**](cbasefilter-stop.md).
-   Annule la validation de l’allocateur. (Voir [**IMemAllocator ::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit).)
-   Annule tout rendu planifié et libère le thread de streaming.
-   Attend la fin d’un appel de **réception** en attente.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




