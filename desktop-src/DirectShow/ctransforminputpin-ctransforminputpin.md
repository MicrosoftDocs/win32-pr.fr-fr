---
description: Méthode constructeur CTransformInputPin. CTransformInputPin.
ms.assetid: 097dce19-b430-42d6-8914-68350c7eca40
title: Constructeur CTransformInputPin. CTransformInputPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CTransformInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 76c19a883e7cfb416e557a23cf2a689e46dab36641ffc98cde5cbe5fe460f686
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053569"
---
# <a name="ctransforminputpinctransforminputpin-constructor"></a>Constructeur CTransformInputPin. CTransformInputPin

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CTransformInputPin(
   TCHAR            *pObjectName,
   CTransformFilter *pTransformFilter,
   HRESULT          *phr,
   LPCWSTR          pName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pObjectName* 
</dt> <dd>

Chaîne contenant le nom de débogage de l’objet. Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pTransformFilter* 
</dt> <dd>

Pointeur vers le filtre qui a créé ce code confidentiel, qui doit être un objet [**CTransformFilter**](ctransformfilter.md) .

</dd> <dt>

*phr* 
</dt> <dd>

Pointeur vers une variable qui reçoit une valeur **HRESULT** indiquant la réussite ou l’échec de la méthode. Initialisez la valeur sur \_ OK avant de créer l’objet. La valeur est modifiée uniquement si une erreur se produit.

</dd> <dt>

*pName* 
</dt> <dd>

Chaîne de caractères larges contenant le nom du code confidentiel.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le paramètre *pname* spécifie le nom du code confidentiel, qui est retourné par la méthode [**IPIN :: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) . Toutefois, la chaîne n’est pas utilisée pour l’identificateur de code confidentiel. L’identificateur de code confidentiel pour cette classe est toujours « in ». Pour plus d’informations, consultez [**QueryId**](ctransforminputpin-queryid.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




