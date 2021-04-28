---
description: 'Méthode CMediaEvent. GetTypeInfoCount : récupère le nombre d’interfaces d’informations de type fournies par un objet.'
ms.assetid: e16bc324-bb49-4df2-afeb-2c2cd1620693
title: Méthode CMediaEvent. GetTypeInfoCount (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9402ad973a08afed4d338cfdc7b5df7fb14b9f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099117"
---
# <a name="cmediaeventgettypeinfocount-method"></a>Méthode CMediaEvent. GetTypeInfoCount

Récupère le nombre d’interfaces d’informations de type fournies par un objet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pctinfo* 
</dt> <dd>

Pointeur vers le nombre d’interfaces d’informations de type fournies par l’objet. Si l’objet fournit des informations de type, ce nombre est 1 ; dans le cas contraire, le nombre est 0.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne le \_ pointeur E si *pcTInfo* n’est pas valide ; sinon, retourne S \_ OK.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaEvent, classe**](cmediaevent.md)
</dt> </dl>

 

 




