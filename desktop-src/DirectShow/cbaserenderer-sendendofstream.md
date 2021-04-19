---
description: Si la fin du flux a été atteinte, la méthode SendEndOfStream planifie un \_ événement d’achèvement ce pour le gestionnaire de graphes de filtre.
ms.assetid: 3c10c956-e352-4796-a8cd-cc69a02066f2
title: Méthode CBaseRenderer. SendEndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f04e4c8c90796aafb64870a9d59d38b0a33e7435
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541275"
---
# <a name="cbaserenderersendendofstream-method"></a>Méthode CBaseRenderer. SendEndOfStream

Si la fin du flux a été atteinte, la `SendEndOfStream` méthode planifie un \_ événement d’achèvement ce pour le gestionnaire de graphes de filtre.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT SendEndOfStream();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                             | Description                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Le gestionnaire de graphique de filtre n’accepte pas les notifications d’événements.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Opération réussie.<br/>                                                       |



 

## <a name="remarks"></a>Notes

Le filtre peut recevoir une notification de fin de flux avant l’heure d’arrêt de l’exemple actuel. Si c’est le cas, le filtre doit attendre avant de publier une notification d' [**\_ achèvement ce**](ec-complete.md) dans le gestionnaire de graphes de filtre.

Par conséquent :

-   Si le filtre a reçu une notification EOS (End-of-Stream) précoce, cette méthode planifie un événement de minuterie. Lorsque l’événement du minuteur est activé, le filtre publie l' \_ événement EC Complete.
-   Si le filtre a reçu une notification EOS qui n’était pas précoce, cette méthode publie \_ immédiatement l’événement EC Complete.
-   Si le filtre n’a pas de notification EOS en attente, la méthode retourne sans rien faire.

La méthode de rappel de la minuterie est [**CBaseRenderer :: TimerCallback**](cbaserenderer-timercallback.md). Pour remettre l' \_ événement EC Complete, le filtre appelle la méthode [**CBaseRenderer :: NotifyEndOfStream**](cbaserenderer-notifyendofstream.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




