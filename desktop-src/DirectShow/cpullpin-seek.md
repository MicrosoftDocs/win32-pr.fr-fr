---
description: La méthode Seek définit les positions de début et de fin du flux.
ms.assetid: d84476f5-688c-429d-a51b-7020a6316e35
title: CPullPin. Seek, méthode (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Seek
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 65ea4deddd000d1064adf8b8caf5a636eed87105856d506191d677e70978d096
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953988"
---
# <a name="cpullpinseek-method"></a>CPullPin. Seek, méthode

La `Seek` méthode définit les positions de début et de fin du flux.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Seek(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*tStart* 
</dt> <dd>

Spécifie la position de départ, en octets, multipliée par 10 millions.

</dd> <dt>

*tStop* 
</dt> <dd>

Spécifie la position d’arrêt, en octets, multipliée par 10 millions.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK si la méthode est réussie, ou un code d’erreur dans le cas contraire.

## <a name="remarks"></a>Remarques

Si le thread de travail est en cours d’exécution, la méthode suspend le thread, vide le graphique de filtre et reprend le thread. Le thread commence à extraire les données à partir de la nouvelle position de départ. Dans le cas contraire, les nouvelles valeurs de position prennent effet à chaque démarrage du thread.

Les positions sont relatives au début de la source d’origine. Multipliez les décalages d’octets souhaités par les unités constantes, qui sont définies dans la bibliothèque de classes de base sous la forme 10 millions.

Lorsque le code confidentiel se connecte pour la première fois, les positions arrêter et démarrer sont représentées par défaut au début et à la fin du flux.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPullPin, classe**](cpullpin.md)
</dt> </dl>

 

 




