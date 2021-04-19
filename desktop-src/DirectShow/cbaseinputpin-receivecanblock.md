---
description: 'La méthode ReceiveCanBlock détermine si les appels à la méthode IMemInputPin :: Receive peuvent se bloquer. Cette méthode implémente la méthode IMemInputPin :: ReceiveCanBlock.'
ms.assetid: db96e389-e1bc-4b38-8d0a-a20f0d3a4460
title: Méthode CBaseInputPin. ReceiveCanBlock (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveCanBlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93c80d6c8f834b45381b89e80d2e0acc392bf25a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541759"
---
# <a name="cbaseinputpinreceivecanblock-method"></a>Méthode CBaseInputPin. ReceiveCanBlock

La `ReceiveCanBlock` méthode détermine si les appels à la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) peuvent se bloquer. Cette méthode implémente la méthode [**IMemInputPin :: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ReceiveCanBlock();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                             | Description                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Le pin ne se bloquera pas sur un appel à **Receive**.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Le code pin peut se bloquer sur un appel à **Receive**.<br/>    |



 

## <a name="remarks"></a>Notes

Retourne la \_ valeur false si les appels à la méthode **Receive** ne sont pas bloqués. Sinon, retourne S \_ OK ou un code d’erreur. Si la méthode de **réception** appelle **Receive** sur un code confidentiel en aval, le code pin en aval peut se bloquer. `ReceiveCanBlock` ce facteur doit être pris en compte.

Un filtre amont peut utiliser cette méthode pour déterminer sa stratégie de thread. Si la méthode de **réception** est bloquée, le filtre en amont peut décider d’utiliser un thread de travail qui met en mémoire tampon les données. Pour une implémentation de cette stratégie, consultez la classe [**COutputQueue**](coutputqueue.md) .

Dans la classe de base, cette méthode retourne S \_ OK lorsque l’une des conditions suivantes est vraie :

-   Le filtre n’a aucune broche de sortie.
-   Une broche d’entrée connectée à ce filtre signale qu’elle peut se bloquer.
-   Une broche d’entrée connectée à ce filtre ne prend pas en charge l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseInputPin, classe**](cbaseinputpin.md)
</dt> </dl>

 

 




