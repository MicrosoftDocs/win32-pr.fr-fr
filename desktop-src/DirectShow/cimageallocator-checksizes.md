---
description: La méthode CheckSizes vérifie les propriétés d’allocateur par rapport au type de média actuel.
ms.assetid: 040b4ed0-c1cc-4995-a0f8-86efa493f84b
title: Méthode CImageAllocator. CheckSizes (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CheckSizes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71184d4915911c29bff9d3a6fa9985942a4aaa44
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119993"
---
# <a name="cimageallocatorchecksizes-method"></a>Méthode CImageAllocator. CheckSizes

La `CheckSizes` méthode vérifie les propriétés d’allocateur par rapport au type de média actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CheckSizes(
   ALLOCATOR_PROPERTIES *pRequest
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pRequest* 
</dt> <dd>

Pointeur désignant une structure de [**\_ propriétés d’allocateur**](/windows/win32/api/strmif/ns-strmif-allocator_properties) qui décrit les propriétés d’allocateur demandées.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                                           | Description                                                                 |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Les propriétés demandées sont compatibles avec le type de média.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Les propriétés demandées ne sont pas compatibles avec le type de média.<br/> |
| <dl> <dt>**VFW \_ E \_ non \_ connecté**</dt> </dl> | Le pin propriétaire n’est pas connecté.<br/>                                 |



 

## <a name="remarks"></a>Notes

Lorsque la méthode est retournée, si la valeur de retour est \_ OK, le membre **cbBuffer** de la fonction *pRequest* contient la taille réelle de la mémoire tampon. Cela peut être plus grand que la taille demandée, mais ne sera jamais plus petit.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageAllocator, classe**](cimageallocator.md)
</dt> </dl>

 

 




