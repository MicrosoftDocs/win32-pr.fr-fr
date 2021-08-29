---
description: La méthode ReceiveMultiple fournit un lot d’exemples de supports à la broche d’entrée.
ms.assetid: e9c7d6ed-fbf9-4c90-8e1e-3bad66cb5d4f
title: Méthode COutputQueue. ReceiveMultiple (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2bb893c0d77907832e160d54c73ee404ccddf6932d94a2ec75d0ecfc984f9014
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831809"
---
# <a name="coutputqueuereceivemultiple-method"></a>Méthode COutputQueue. ReceiveMultiple

La `ReceiveMultiple` méthode remet un lot d’exemples de supports à la broche d’entrée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ReceiveMultiple(
   IMediaSample **ppSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppSamples* 
</dt> <dd>

Adresse d’un pointeur vers un tableau d’exemples.

</dd> <dt>

*nSamples* 
</dt> <dd>

Nombre d’échantillons dans le tableau.

</dd> <dt>

*nSamplesProcessed* 
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre d’exemples remis avec succès.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                             | Description                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Notification de fin de flux reçue avant le traitement de cet exemple.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Réussite.<br/>                                                           |



 

## <a name="remarks"></a>Remarques

Si l’objet utilise un thread, cette méthode met en file d’attente tous les exemples passés dans le tableau. Dans le cas contraire, la méthode appelle la méthode [**IMemInputPin :: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) sur la broche d’entrée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




