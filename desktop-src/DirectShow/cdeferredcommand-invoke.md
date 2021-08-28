---
description: La méthode Invoke fournit l’accès aux méthodes et aux propriétés exposées par un objet.
ms.assetid: d9539b89-b7c2-4b4d-b6d6-6275cc6d7e7c
title: CDeferredCommand. Invoke, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1df087e71ba03ef67ea250235a4ef8a9ef5e6623efe67594381111de6088cf7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074373"
---
# <a name="cdeferredcommandinvoke-method"></a>CDeferredCommand. Invoke, méthode

La `Invoke` méthode fournit l’accès aux méthodes et aux propriétés exposées par un objet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Invoke();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne VFW \_ E \_ déjà \_ annulé si **m \_ pQueue** a la **valeur null**. Sinon, retourne le **HRESULT** résultant d’un appel à **IDispatch :: GetTypeInfo** ou **IUnknown :: QueryInterface**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDeferredCommand, classe**](cdeferredcommand.md)
</dt> </dl>

 

 




