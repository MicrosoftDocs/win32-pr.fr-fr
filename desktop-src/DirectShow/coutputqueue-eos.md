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
ms.openlocfilehash: ab05d4ab3f2620c11bd62d566be851e16b28cecd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413994"
---
# <a name="coutputqueueeos-method"></a>COutputQueue. EOS, méthode

La `EOS` méthode fournit un appel de fin de flux à la broche d’entrée.

## <a name="syntax"></a>Syntaxe


```C++
void EOS();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si l’objet utilise un thread, il met en file d’attente un \_ message de contrôle de paquet EOS. Le thread remet tous les échantillons en attente et appelle la méthode [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sur la broche d’entrée.

Si l’objet n’utilise pas de thread, il appelle la méthode [**COutputQueue :: SendAnyway**](coutputqueue-sendanyway.md) pour remettre tous les échantillons en attente. Ensuite, il appelle **IPIN :: EndOfStream** sur la broche d’entrée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




