---
description: La méthode QueueSample met en file d’attente un exemple.
ms.assetid: f34c0689-5afb-4941-bc3a-e4765fbbe525
title: Méthode COutputQueue. QueueSample (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.QueueSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3770029f732629f12d94c9304d144226d873f38cc1b8452036d39ca2abdd757a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909589"
---
# <a name="coutputqueuequeuesample-method"></a>Méthode COutputQueue. QueueSample

La `QueueSample` méthode met en file d’attente un exemple.

## <a name="syntax"></a>Syntaxe


```C++
void QueueSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSample* 
</dt> <dd>

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode ajoute un exemple à la fin de la file d’attente. Maintenez la section critique avant d’appeler cette méthode et appelez-la uniquement lorsque l’objet utilise un thread pour remettre des exemples. Pour déterminer si l’objet utilise un thread, appelez la méthode [**COutputQueue :: IsQueued**](coutputqueue-isqueued.md) .

Cette méthode peut également être utilisée pour placer des messages de contrôle dans la file d’attente. Un message de contrôle est une constante définie (castée en un \_ type PTR long) qui indique au thread d’effectuer une action. La classe **COutputQueue** définit les messages de contrôle présentés dans le tableau suivant.



| Étiquette | Valeur |
|---------------|----------------------------------------|
| Message       | Action                                 |
| \_paquet EOS   | Fournir une notification de fin de flux. |
| NOUVEAU \_ segment  | Fournissez un nouveau segment.                 |
| RÉINITIALISER le \_ paquet | Réinitialisez l’état de la file d’attente.          |
| Envoyer le \_ paquet  | Envoyer un lot partiel d’exemples.       |



 

Il s’agit d’une méthode protégée, que la classe **COutputQueue** utilise en interne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




