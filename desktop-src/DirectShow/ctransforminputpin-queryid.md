---
description: 'Méthode CTransformInputPin. QueryId : la méthode QueryId récupère un identificateur pour le code confidentiel. Cette méthode implémente la méthode IPin :: QueryId.'
ms.assetid: 91fde383-0288-4307-9ca8-e117b6111769
title: CTransformInputPin. QueryId, méthode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8bb7fa42453e15137be6770332496ea1f39c04c3a6055af00300da9bd6194961
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086999"
---
# <a name="ctransforminputpinqueryid-method"></a>CTransformInputPin. QueryId, méthode

La `QueryId` méthode récupère un identificateur pour le code confidentiel. Cette méthode implémente la méthode [**IPIN :: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .

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

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                   | Description                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Succès<br/>                   |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante<br/>       |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Argument de pointeur **null**<br/> |



 

## <a name="remarks"></a>Remarques

L’identificateur de code confidentiel est utilisé pour la persistance des graphiques. L’identificateur de code confidentiel de cette classe se trouve dans. Cette classe remplace le comportement de la classe [**CBasePin**](cbasepin.md) . Dans la classe **CBasePin** , l’identificateur de code confidentiel est le même que le nom du code confidentiel, spécifié dans le constructeur de classe. Dans la classe **CTransformInputPin** , l’identificateur de code confidentiel et le nom du code confidentiel ne sont pas identiques.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




