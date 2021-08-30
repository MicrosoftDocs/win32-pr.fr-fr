---
description: La méthode GetHRESULT, récupère la valeur HRESULT de la commande appelée.
ms.assetid: 7e88a2bd-6b1b-4e59-b185-5dfd501fc37a
title: Méthode CDeferredCommand. GetHRESULT, (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetHResult
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16513cd202d8ad1973a6aa4d2bfd69f8372cb9b611e1dc070e265685db2d2682
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910099"
---
# <a name="cdeferredcommandgethresult-method"></a>Méthode CDeferredCommand. GetHRESULT,

La `GetHResult` méthode récupère la valeur **HRESULT** à partir de la commande appelée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetHResult(
   HRESULT *phrResult
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*phrResult* 
</dt> <dd>

Pointeur vers la valeur **HRESULT** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne E \_ Abort si **m \_ PQueue** a la **valeur null**. Sinon, retourne S \_ OK.

## <a name="remarks"></a>Remarques

Cette fonction membre implémente la méthode [**IDeferredCommand :: GetHRESULT,**](/windows/desktop/api/Control/nf-control-ideferredcommand-gethresult) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDeferredCommand, classe**](cdeferredcommand.md)
</dt> </dl>

 

 




