---
description: La méthode SendAnyway fournit tous les exemples en attente.
ms.assetid: b4e3a0c6-0f72-4a00-963e-65ceed265f01
title: Méthode COutputQueue. SendAnyway (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SendAnyway
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6fa5495371e020310e2367aea7e7bed9ef113f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533728"
---
# <a name="coutputqueuesendanyway-method"></a>Méthode COutputQueue. SendAnyway

La `SendAnyway` méthode remet tous les échantillons en attente.

## <a name="syntax"></a>Syntaxe


```C++
void SendAnyway();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si la variable membre [**COutputQueue :: m \_ bBatchExact**](coutputqueue-m-bbatchexact.md) a la **valeur true**, l’objet remplit le tableau [**COutputQueue :: m \_ ppSamples**](coutputqueue-m-ppsamples.md) avant de fournir un lot d’exemples. Appelez cette méthode pour remettre un lot partiel. Par exemple, la méthode [**COutputQueue :: EOS**](coutputqueue-eos.md) appelle `SendAnyway` pour sérialiser les messages de fin de flux.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




