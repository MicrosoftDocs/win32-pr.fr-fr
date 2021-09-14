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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195511"
---
# <a name="ctransforminputpincheckstreaming-method"></a>Méthode CTransformInputPin. CheckStreaming

La `CheckStreaming` méthode détermine si le code pin peut accepter des exemples.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CheckStreaming();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.



| Code de retour                                                                                           | Description                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Réussite.<br/>                         |
| <dl> <dt>**S \_ false**</dt> </dl>               | Le code PIN est en cours de vidage.<br/>       |
| <dl> <dt>**VFW \_ E \_ non \_ connecté**</dt> </dl> | La broche de sortie n’est pas connectée.<br/> |
| <dl> <dt>**\_erreur d' \_ exécution VFW E \_**</dt> </dl> | Une erreur d’exécution s’est produite.<br/>       |
| <dl> <dt>**VFW \_ E \_ état incorrect \_**</dt> </dl>   | Le code PIN est arrêté.<br/>              |



 

## <a name="remarks"></a>Notes

Cette méthode remplace la méthode [**CBaseInputPin :: CheckStreaming**](cbaseinputpin-checkstreaming.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




