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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538160"
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

## <a name="remarks"></a>Notes

Cette fonction membre implémente la méthode [**IDeferredCommand :: GetHRESULT,**](/windows/desktop/api/Control/nf-control-ideferredcommand-gethresult) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDeferredCommand, classe**](cdeferredcommand.md)
</dt> </dl>

 

 




