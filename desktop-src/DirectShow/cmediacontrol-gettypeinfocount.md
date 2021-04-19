---
description: Récupère le nombre d’interfaces d’informations de type fournies par un objet.
ms.assetid: 29575325-8f97-4f39-8272-86a917d9144f
title: Méthode CMediaControl. GetTypeInfoCount (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2454e503a045a02db20c0dc457b6367f6d3b427
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537643"
---
# <a name="cmediacontrolgettypeinfocount-method"></a>Méthode CMediaControl. GetTypeInfoCount

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

Pointeur vers le nombre d’interfaces d’informations de type fourni par l’objet. Si l’objet fournit des informations de type, ce nombre est 1 ; dans le cas contraire, le nombre est 0.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le \_ pointeur E si *pcTInfo* n’est pas valide ; sinon, retourne S \_ OK.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaControl, classe**](cmediacontrol.md)
</dt> </dl>

 

 




