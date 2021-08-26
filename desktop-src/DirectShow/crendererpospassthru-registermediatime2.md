---
description: La méthode RegisterMediaTime met en cache les horodatages de l’échantillon actuel. Cette méthode utilise les paramètres *StartTime* et *EndTime* .
ms.assetid: 65755906-cf54-46d6-8149-5ad982be55f3
title: CRendererPosPassThru. RegisterMediaTime, méthode (Ctlutil. h)-StartTime et EndTime, paramètres
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
ms.openlocfilehash: 944d78af6247e7237040f0260a51203a13ef506db36856cfb554d0f2982c0d14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084109"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh---starttime-and-endtime-parameters"></a>CRendererPosPassThru. RegisterMediaTime, méthode (Ctlutil. h)-StartTime et EndTime, paramètres

La méthode [**RegisterMediaTime**](crendererpospassthru-registermediatime.md) met en cache les horodatages de l’échantillon actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RegisterMediaTime(
   LONGLONG StartTime,
   LONGLONG EndTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StartTime* 
</dt> <dd>

Heure de début de l’exemple, en unités de 100 nanosecondes.

</dd> <dt>

*EndTime* 
</dt> <dd>

Heure de fin de l’échantillon, en unités de 100 nanosecondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                          | Description         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Réussite.<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode stocke les valeurs d’horodatage indiquées dans *StartTime* et *EndTime*. La méthode [**CRendererPosPassThru :: GetMediaTime**](crendererpospassthru-getmediatime.md) récupère les mêmes valeurs.

Le filtre doit appeler cette méthode pour chaque exemple qu’il reçoit. La méthode est surchargée pour accepter soit un pointeur vers l’exemple, soit les valeurs d’horodatage elles-mêmes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête  | Ctlutil. h (inclure Flux. h)                                                                                   |
| Bibliothèque | Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |



 

 




