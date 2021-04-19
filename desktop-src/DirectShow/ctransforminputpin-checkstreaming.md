---
description: La méthode CheckStreaming détermine si le code pin peut accepter des exemples.
ms.assetid: fa063966-4c72-466e-933c-def6a6818621
title: Méthode CTransformInputPin. CheckStreaming (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e5c49a00054547193e3f492f0731f77af8331a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536021"
---
# <a name="ctransforminputpincheckstreaming-method"></a>Méthode CTransformInputPin. CheckStreaming

La `CheckStreaming` méthode détermine si le code pin peut accepter des exemples.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CheckStreaming();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.



| Code de retour                                                                                           | Description                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Opération réussie.<br/>                         |
| <dl> <dt>**S \_ false**</dt> </dl>               | Le code PIN est en cours de vidage.<br/>       |
| <dl> <dt>**VFW \_ E \_ non \_ connecté**</dt> </dl> | La broche de sortie n’est pas connectée.<br/> |
| <dl> <dt>**\_erreur d' \_ exécution VFW E \_**</dt> </dl> | Une erreur d’exécution s’est produite.<br/>       |
| <dl> <dt>**VFW \_ E \_ état incorrect \_**</dt> </dl>   | Le code PIN est arrêté.<br/>              |



 

## <a name="remarks"></a>Notes

Cette méthode remplace la méthode [**CBaseInputPin :: CheckStreaming**](cbaseinputpin-checkstreaming.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




