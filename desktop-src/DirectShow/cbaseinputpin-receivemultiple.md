---
description: 'La méthode ReceiveMultiple reçoit un tableau d’exemples. Cette méthode implémente la méthode IMemInputPin :: ReceiveMultiple.'
ms.assetid: 21e757c7-f623-4ccb-8e37-512ee4dd7aa7
title: Méthode CBaseInputPin. ReceiveMultiple (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63d71f47978a2eefdcbdacbe1c31bfe69c732c24a0479357b35aa1ddd2b0a9de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079399"
---
# <a name="cbaseinputpinreceivemultiple-method"></a>Méthode CBaseInputPin. ReceiveMultiple

La `ReceiveMultiple` méthode reçoit un tableau d’exemples. Cette méthode implémente la méthode [**IMemInputPin :: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ReceiveMultiple(
   IMediaSample **pSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSamples* 
</dt> <dd>

Adresse d’un tableau de pointeurs [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) , de taille *nSamples*.

</dd> <dt>

*nSamples* 
</dt> <dd>

Nombre d’échantillons à traiter.

</dd> <dt>

*nSamplesProcessed* 
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre d’exemples qui ont été traités.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                             | Description                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                    | Réussite.<br/>                                        |
| <dl> <dt>**S \_ false**</dt> </dl>                 | Le code PIN est en cours de vidage ; l’exemple a été rejeté.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>               | Argument de pointeur **null** .<br/>                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Type de média non valide.<br/>                             |
| <dl> <dt>**\_erreur d' \_ exécution VFW E \_**</dt> </dl>   | Une erreur d’exécution s’est produite.<br/>                      |
| <dl> <dt>**VFW \_ E \_ état incorrect \_**</dt> </dl>     | Le code PIN est arrêté.<br/>                             |



 

## <a name="remarks"></a>Remarques

Cette méthode se comporte comme la méthode [**CBaseInputPin :: Receive**](cbaseinputpin-receive.md) , mais reçoit un tableau d’exemples. Dans la classe de base, la méthode parcourt le tableau et appelle **Receive** avec chaque exemple. Substituez cette fonction si votre filtre peut traiter des lots d’exemples plus efficacement que les traiter un par un.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseInputPin, classe**](cbaseinputpin.md)
</dt> </dl>

 

 




