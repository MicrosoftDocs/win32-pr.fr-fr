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
ms.openlocfilehash: a6572ad0b415f4c1a51133d080e84a2e869787dea0c23614478b09c7b86296b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073523"
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
| <dl> <dt>**\_OK**</dt> </dl>         | Réussite.<br/>                                                   |
| <dl> <dt>**E \_ inattendu**</dt> </dl> | La connexion de code confidentiel n’a pas été établie correctement.<br/>          |
| <dl> <dt>**E \_ échec**</dt> </dl>       | Impossible de créer le thread ou le thread existe déjà.<br/> |



 

## <a name="remarks"></a>Remarques

Appelez cette méthode lorsque le filtre propriétaire devient actif. (Si votre broche d’entrée dérive de [**CBasePin**](cbasepin.md), remplacez la méthode [**CBasePin :: active**](cbasepin-active.md) .)

avant d’appeler cette méthode, appelez la méthode [**CPullPin :: Connecter**](cpullpin-connect.md) pour établir la connexion avec la broche de sortie.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPullPin, classe**](cpullpin.md)
</dt> </dl>

 

 




