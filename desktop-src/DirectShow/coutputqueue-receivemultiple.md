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
ms.openlocfilehash: e17e0a8a4856b067907622ec3c8437f5e73a7e38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532514"
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
| <dl> <dt>**\_OK**</dt> </dl>    | Opération réussie.<br/>                                                           |



 

## <a name="remarks"></a>Notes

Si l’objet utilise un thread, cette méthode met en file d’attente tous les exemples passés dans le tableau. Dans le cas contraire, la méthode appelle la méthode [**IMemInputPin :: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) sur la broche d’entrée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




