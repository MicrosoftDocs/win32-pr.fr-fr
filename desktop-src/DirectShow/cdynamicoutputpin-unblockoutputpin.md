---
description: La méthode UnblockOutputPin débloque le code confidentiel. Lorsque le code confidentiel est débloqué, il peut fournir des échantillons, modifier son format de sortie et se reconnecter.
ms.assetid: ea6e6312-8c7f-44db-ac7f-165dc45dec23
title: Méthode CDynamicOutputPin. UnblockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.UnblockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60bcde3ccad01e19f3802e2cd19f0f6b873380ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006790"
---
# <a name="cdynamicoutputpinunblockoutputpin-method"></a>Méthode CDynamicOutputPin. UnblockOutputPin

La `UnblockOutputPin` méthode débloque le code confidentiel. Lorsque le code confidentiel est débloqué, il peut fournir des échantillons, modifier son format de sortie et se reconnecter.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UnblockOutputPin();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                             | Description                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Le code pin a déjà été débloqué.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Réussite.<br/>                   |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDynamicOutputPin, classe**](cdynamicoutputpin.md)
</dt> </dl>

 

 




