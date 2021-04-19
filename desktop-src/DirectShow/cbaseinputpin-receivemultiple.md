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
ms.openlocfilehash: 5725b7d8b70c8f7c61eb44231812997a903ba41a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526468"
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
| <dl> <dt>**\_OK**</dt> </dl>                    | Opération réussie.<br/>                                        |
| <dl> <dt>**S \_ false**</dt> </dl>                 | Le code PIN est en cours de vidage ; l’exemple a été rejeté.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>               | Argument de pointeur **null** .<br/>                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Type de média non valide.<br/>                             |
| <dl> <dt>**\_erreur d' \_ exécution VFW E \_**</dt> </dl>   | Une erreur d’exécution s’est produite.<br/>                      |
| <dl> <dt>**VFW \_ E \_ état incorrect \_**</dt> </dl>     | Le code PIN est arrêté.<br/>                             |



 

## <a name="remarks"></a>Notes

Cette méthode se comporte comme la méthode [**CBaseInputPin :: Receive**](cbaseinputpin-receive.md) , mais reçoit un tableau d’exemples. Dans la classe de base, la méthode parcourt le tableau et appelle **Receive** avec chaque exemple. Substituez cette fonction si votre filtre peut traiter des lots d’exemples plus efficacement que les traiter un par un.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseInputPin, classe**](cbaseinputpin.md)
</dt> </dl>

 

 




