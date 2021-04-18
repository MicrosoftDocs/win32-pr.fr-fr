---
description: La méthode active crée un thread de travail qui extrait les données de la broche de sortie. Cette méthode valide également l’allocateur.
ms.assetid: 9efa20f3-7909-4d87-bfa8-314d055b80f8
title: CPullPin. active, méthode (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 461f6554f828dc096029ee1e7a1832e12a7c262a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533494"
---
# <a name="cpullpinactive-method"></a>CPullPin. active, méthode

La méthode **active** crée un thread de travail qui extrait les données de la broche de sortie. Cette méthode valide également l’allocateur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Active();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                                  | Description                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Opération réussie.<br/>                                                   |
| <dl> <dt>**E \_ inattendu**</dt> </dl> | La connexion de code confidentiel n’a pas été établie correctement.<br/>          |
| <dl> <dt>**E \_ échec**</dt> </dl>       | Impossible de créer le thread ou le thread existe déjà.<br/> |



 

## <a name="remarks"></a>Notes

Appelez cette méthode lorsque le filtre propriétaire devient actif. (Si votre broche d’entrée dérive de [**CBasePin**](cbasepin.md), remplacez la méthode [**CBasePin :: active**](cbasepin-active.md) .)

Avant d’appeler cette méthode, appelez la méthode [**CPullPin :: Connect**](cpullpin-connect.md) pour établir la connexion avec la broche de sortie.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPullPin, classe**](cpullpin.md)
</dt> </dl>

 

 




