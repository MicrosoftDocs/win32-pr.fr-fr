---
description: Méthode constructeur CDynamicOutputPin. CDynamicOutputPin.
ms.assetid: 996adc69-8727-431e-a7f5-8fbcc0e305ae
title: Constructeur CDynamicOutputPin. CDynamicOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CDynamicOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fe6dad14399b5b124b0146ea8b7ca101c8fa817
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099307"
---
# <a name="cdynamicoutputpincdynamicoutputpin-constructor"></a>Constructeur CDynamicOutputPin. CDynamicOutputPin

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CDynamicOutputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pObjectName* 
</dt> <dd>

Pointeur vers une chaîne contenant le nom de l’objet. Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pFilter* 
</dt> <dd>

Pointeur vers le filtre qui a créé ce code confidentiel.

</dd> <dt>

*pLock* 
</dt> <dd>

Pointeur vers un verrou [**CCritSec**](ccritsec.md) , utilisé pour sérialiser les modifications d’État. Utilisez la même section critique que le verrou de filtre, [ **CBaseFilter :: m \_ pLock**](cbasefilter-m-plock.md)

</dd> <dt>

*phr* 
</dt> <dd>

Pointeur vers une variable qui reçoit une valeur **HRESULT** indiquant la réussite ou l’échec de la méthode. Initialisez la valeur sur \_ OK avant de créer l’objet. La valeur est modifiée uniquement si une erreur se produit.

</dd> <dt>

*pName* 
</dt> <dd>

Pointeur vers une chaîne de caractères larges contenant l’identificateur de code confidentiel. Pour plus d’informations, consultez [**IPIN :: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDynamicOutputPin, classe**](cdynamicoutputpin.md)
</dt> </dl>

 

 




