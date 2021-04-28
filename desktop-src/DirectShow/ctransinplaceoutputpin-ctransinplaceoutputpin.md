---
description: Méthode constructeur CTransInPlaceOutputPin. CTransInPlaceOutputPin.
ms.assetid: fe7b2d62-0e6a-4253-b469-6cede5dc9bb1
title: Constructeur CTransInPlaceOutputPin. CTransInPlaceOutputPin (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.CTransInPlaceOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6b63ee3aa52bc0363bcab90275be4148659b3bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094707"
---
# <a name="ctransinplaceoutputpinctransinplaceoutputpin-constructor"></a>Constructeur CTransInPlaceOutputPin. CTransInPlaceOutputPin

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CTransInPlaceOutputPin(
   TCHAR               *pObjectName,
   CTransInPlaceFilter *pFilter,
   HRESULT             *phr,
   LPCWSTR             pName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pObjectName* 
</dt> <dd>

Chaîne contenant le nom de débogage de l’objet. Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pFilter* 
</dt> <dd>

Pointeur vers le filtre qui a créé ce code confidentiel, qui doit être un objet [**CTransInPlaceFilter**](ctransinplacefilter.md) .

</dd> <dt>

*phr* 
</dt> <dd>

Pointeur vers une variable qui reçoit une valeur **HRESULT** indiquant la réussite ou l’échec de la méthode. Initialisez la valeur sur \_ OK avant de créer l’objet. La valeur est modifiée uniquement si une erreur se produit.

</dd> <dt>

*pName* 
</dt> <dd>

Chaîne de caractères larges contenant le nom du code confidentiel.

</dd> </dl>

## <a name="remarks"></a>Notes 

Le paramètre *pname* spécifie le nom du code confidentiel, qui est retourné par la méthode [**IPIN :: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) . Toutefois, la chaîne n’est pas utilisée pour l’identificateur de code confidentiel. L’identificateur de code confidentiel pour cette classe est toujours « out ». Pour plus d’informations, consultez [**QueryId**](ctransforminputpin-queryid.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceOutputPin, classe**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




