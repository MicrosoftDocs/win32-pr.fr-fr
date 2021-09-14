---
description: 'Méthode CBasePin. EnumMediaTypes : la méthode EnumMediaTypes énumère les types de média préférés du pin. Cette méthode implémente la méthode IPin :: EnumMediaTypes.'
ms.assetid: 0360f9fc-6876-4a54-8de1-bf289e0e10ae
title: Méthode CBasePin. EnumMediaTypes (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c68fe1ab83724149dcd2fb58a60e9c6950d887ca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999334"
---
# <a name="cbasepinenummediatypes-method"></a>Méthode CBasePin. EnumMediaTypes

La `EnumMediaTypes` méthode énumère les types de média préférés du pin. Cette méthode implémente la méthode [**IPIN :: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppEnum* 
</dt> <dd>

Adresse d’une variable qui reçoit un pointeur vers l’interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                   | Description                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Réussite.<br/>                   |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>       |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Argument de pointeur **null** .<br/> |



 

## <a name="remarks"></a>Notes

Les broches d’entrée ne sont pas requises pour énumérer les types préférés. Les broches de sortie doivent énumérer au moins un type préféré. Dans le cas contraire, les deux broches ne peuvent pas avoir de type préféré, ce qui rend impossible la connexion.

L’interface **IEnumMediaTypes** fonctionne comme un énumérateur com standard. Pour plus d’informations, consultez [énumération d’objets dans un filtre Graph](enumerating-objects-in-a-filter-graph.md). Si la méthode est réussie, l’interface **IEnumMediaTypes** a un nombre de références en attente. Veillez à le libérer lorsque vous avez terminé.

La classe de base [**CEnumMediaTypes**](cenummediatypes.md) implémente **IEnumMediaTypes**. Elle appelle la méthode [**CBasePin :: GetMediaType**](cbasepin-getmediatype.md) du pin pour énumérer les types de médias.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




