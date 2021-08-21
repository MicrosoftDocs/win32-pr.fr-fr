---
description: La méthode EOS fournit un appel de fin de flux à la broche d’entrée.
ms.assetid: 65e8db14-6ca8-4c4f-8bd8-2442f743499e
title: COutputQueue. EOS, méthode (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3effb06498ae65cad8eefd9a3144cab140926006cd38acee45c553c4295b0a58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537139"
---
# <a name="coutputqueueeos-method"></a>COutputQueue. EOS, méthode

La `EOS` méthode fournit un appel de fin de flux à la broche d’entrée.

## <a name="syntax"></a>Syntaxe


```C++
void EOS();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Si l’objet utilise un thread, il met en file d’attente un \_ message de contrôle de paquet EOS. Le thread remet tous les échantillons en attente et appelle la méthode [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sur la broche d’entrée.

Si l’objet n’utilise pas de thread, il appelle la méthode [**COutputQueue :: SendAnyway**](coutputqueue-sendanyway.md) pour remettre tous les échantillons en attente. Ensuite, il appelle **IPIN :: EndOfStream** sur la broche d’entrée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




