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
ms.openlocfilehash: 5b09049bc443991dabe07a7626ffc42097feceee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999295"
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

## <a name="return-value"></a>Valeur de retour

Retourne E \_ Abort si **m \_ PQueue** a la **valeur null**. Sinon, retourne S \_ OK.

## <a name="remarks"></a>Notes

Cette fonction membre implémente la méthode [**IDeferredCommand :: GetHRESULT,**](/windows/desktop/api/Control/nf-control-ideferredcommand-gethresult) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDeferredCommand, classe**](cdeferredcommand.md)
</dt> </dl>

 

 




