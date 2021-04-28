---
description: 'Méthode CTransInPlaceInputPin. NotifyAllocator : la méthode NotifyAllocator spécifie un allocateur pour la connexion. Cette méthode implémente la méthode IMemInputPin :: NotifyAllocator.'
ms.assetid: adc1c5b6-99da-4140-b644-7b98f6b8bad4
title: Méthode CTransInPlaceInputPin. NotifyAllocator (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca15be5dc1893a393e6052832cc7522f27355eeb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094747"
---
# <a name="ctransinplaceinputpinnotifyallocator-method"></a>Méthode CTransInPlaceInputPin. NotifyAllocator

La `NotifyAllocator` méthode spécifie un allocateur pour la connexion. Cette méthode implémente la méthode [**IMemInputPin :: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAllocator* 
</dt> <dd>

Pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur.

</dd> <dt>

*bReadOnly* 
</dt> <dd>

Indicateur qui spécifie si les exemples de cet allocateur sont en lecture seule. Si la **valeur est true**, les exemples sont en lecture seule.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                               | Description                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Opération réussie<br/>                   |
| <dl> <dt>**E \_ échec**</dt> </dl>    | Échec<br/>                   |
| <dl> <dt>**\_pointeur E**</dt> </dl> | Argument de pointeur **null**<br/> |



 

## <a name="remarks"></a>Notes 

Le filtre tente d’utiliser le même allocateur pour les deux connexions de code confidentiel.

-   Si la broche de sortie n’est pas connectée, la broche d’entrée accepte automatiquement l’allocateur. Lorsque la broche de sortie est connectée, le filtre reconnecte la broche d’entrée. À ce stade, le filtre réessaiera d’utiliser un allocateur unique.
-   Si la broche de sortie est connectée, la broche d’entrée accepte l’allocateur. La broche de sortie utilise également le même allocateur. Il appelle `NotifyAllocator` sur la broche d’entrée en aval.

Le cas précédent a l’exception suivante :

-   Si l’allocateur proposé est en lecture seule (autrement dit, si le paramètre *bReadOnly* a la **valeur true**) et que le filtre doit modifier les exemples, le filtre doit utiliser deux allocateurs différents. Dans ce cas, si le filtre en amont propose d’utiliser l’allocateur du filtre en aval, la méthode renvoie E \_ Fail.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceInputPin, classe**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




