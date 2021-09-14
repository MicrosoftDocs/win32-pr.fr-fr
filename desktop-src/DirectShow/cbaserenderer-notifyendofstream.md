---
description: La méthode NotifyEndOfStream publie un \_ événement EC complet dans le gestionnaire de graphique de filtre.
ms.assetid: 9eec5b65-654d-4b2e-be39-93225a7674a5
title: Méthode CBaseRenderer. NotifyEndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.NotifyEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f1187705bfa678252237bd95d9a4cb21a0f97d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127230442"
---
# <a name="cbaserenderernotifyendofstream-method"></a>Méthode CBaseRenderer. NotifyEndOfStream

La `NotifyEndOfStream` méthode publie un événement [**EC \_ complet**](ec-complete.md) dans le gestionnaire de graphique de filtre.

## <a name="syntax"></a>Syntaxe


```C++
void NotifyEndOfStream();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer :: EndOfStream**](cbaserenderer-endofstream.md)
</dt> <dt>

[**CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md)
</dt> </dl>

 

 




