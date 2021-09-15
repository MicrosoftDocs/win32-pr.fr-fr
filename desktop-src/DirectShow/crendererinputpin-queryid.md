---
description: 'La méthode QueryId récupère l’identificateur de code confidentiel. Cette méthode remplace la méthode CBasePin :: QueryId.'
ms.assetid: 9543234c-5349-49d0-b410-1c461ee4eabe
title: CRendererInputPin. QueryId, méthode (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b56ae2a846b4d89da4c6a9d4c8f88bd3094c5cff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312449"
---
# <a name="crendererinputpinqueryid-method"></a>CRendererInputPin. QueryId, méthode

La `QueryId` méthode récupère l’identificateur de code confidentiel. Cette méthode remplace la méthode [**CBasePin :: QueryId**](cbasepin-queryid.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Id* 
</dt> <dd>

Reçoit une chaîne contenant l’identificateur de code confidentiel.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                   | Description                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Succès<br/>                   |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante<br/>       |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Argument de pointeur **null**<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode alloue la chaîne de caractères larges « in » et l’assigne au paramètre *ID* . L’appelant doit libérer la mémoire allouée à l’aide de la fonction **CoTaskMemFree** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CRendererInputPin, classe**](crendererinputpin.md)
</dt> </dl>

 

 




