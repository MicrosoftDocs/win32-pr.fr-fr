---
description: 'La méthode EndOfStream indique au code confidentiel qu’aucune donnée supplémentaire n’est attendue. Cette méthode implémente la méthode IPin :: EndOfStream. Appelez cette méthode uniquement sur les broches d’entrée.'
ms.assetid: 52a71c30-bd68-4152-8901-71ef2e65913a
title: Méthode CBasePin. EndOfStream (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2324bae8ec1266dce2471049f8ba2f06b0c9e6e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999335"
---
# <a name="cbasepinendofstream-method"></a>Méthode CBasePin. EndOfStream

La `EndOfStream` méthode indique au code confidentiel qu’aucune donnée supplémentaire n’est attendue. Cette méthode implémente la méthode [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) . Appelez cette méthode uniquement sur les broches d’entrée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Le filtre doit passer des notifications de fin de flux en aval, aux broches d’entrée des filtres connectés. Si le filtre est un convertisseur, il doit envoyer une notification d’événements [**EC \_ complet**](ec-complete.md) au gestionnaire de graphes de filtre. pour plus d’informations, consultez [Flow de données dans le Graph de filtre](data-flow-in-the-filter-graph.md).

Dans la classe de base, cette méthode n’a aucun effet. Les classes dérivées doivent remplacer cette méthode.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




