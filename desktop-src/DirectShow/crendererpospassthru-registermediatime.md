---
description: La méthode RegisterMediaTime met en cache les horodatages de l’échantillon actuel.
ms.assetid: 9ff8e4ec-3401-4272-894d-643f0fc029de
title: Méthode CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.RegisterMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3c829690572d55ea700d51124b99370f23e755a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541082"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh"></a>Méthode CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)

La méthode **RegisterMediaTime** met en cache les horodatages de l’échantillon actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RegisterMediaTime(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                                  | Description                                |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                         | Opération réussie.<br/>                        |
| <dl> <dt>**\_heure du média VFW E \_ \_ \_ non \_ définie**</dt> </dl> | L’exemple n’est pas horodaté.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode stocke les horodatages de l’échantillon actuel. La méthode [**CRendererPosPassThru :: GetMediaTime**](crendererpospassthru-getmediatime.md) récupère les mêmes valeurs.

Le filtre doit appeler cette méthode pour chaque exemple qu’il reçoit. La méthode est surchargée pour accepter soit un pointeur vers l’exemple, soit les valeurs d’horodatage elles-mêmes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




