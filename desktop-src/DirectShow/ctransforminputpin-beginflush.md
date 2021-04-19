---
description: 'La méthode BeginFlush commence une opération de vidage. Cette méthode implémente la méthode IPin :: BeginFlush.'
ms.assetid: 7c76ca06-dc3c-4f9a-9761-32aea7db4c7e
title: Méthode CTransformInputPin. BeginFlush (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4d028634364ca59ae293d9ebb60a464974ccd74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528535"
---
# <a name="ctransforminputpinbeginflush-method"></a>Méthode CTransformInputPin. BeginFlush

La `BeginFlush` méthode commence une opération de vidage. Cette méthode implémente la méthode [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                           | Description                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Opération réussie.<br/>                     |
| <dl> <dt>**VFW \_ E \_ non \_ connecté**</dt> </dl> | La broche de sortie n’est pas connectée.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode appelle la méthode [**CBaseInputPin :: BeginFlush**](cbaseinputpin-beginflush.md) du pin. Elle appelle ensuite la méthode [**CTransformFilter :: BeginFlush**](ctransformfilter-beginflush.md) du filtre pour remettre l’appel en aval.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




