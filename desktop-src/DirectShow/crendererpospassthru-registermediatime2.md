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
ms.openlocfilehash: 4e7d9fca04be9381fc739467647fedfa064040a0
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106540125"
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
| <dl> <dt>**\_OK**</dt> </dl> | Opération réussie.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode stocke les valeurs d’horodatage indiquées dans *StartTime* et *EndTime*. La méthode [**CRendererPosPassThru :: GetMediaTime**](crendererpospassthru-getmediatime.md) récupère les mêmes valeurs.

Le filtre doit appeler cette méthode pour chaque exemple qu’il reçoit. La méthode est surchargée pour accepter soit un pointeur vers l’exemple, soit les valeurs d’horodatage elles-mêmes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête  | Ctlutil. h (include streams. h)                                                                                   |
| Bibliothèque | Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |



 

 




