---
description: 'Méthode CMediaPosition. GetTypeInfoCount : la méthode GetTypeInfoCount récupère le nombre d’interfaces d’informations de type fourni par l’objet.'
ms.assetid: c98368f2-ae0c-4301-be30-7332b19f53ee
title: Méthode CMediaPosition. GetTypeInfoCount (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8cfc54f414a6722f7f69a0330fad2d1a0cfab425
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095477"
---
# <a name="cmediapositiongettypeinfocount-method"></a>Méthode CMediaPosition. GetTypeInfoCount

La `GetTypeInfoCount` méthode récupère le nombre d’interfaces d’informations de type fourni par l’objet.

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

Pointeur vers une variable qui reçoit le nombre d’interfaces d’informations de type fournies par l’objet. Lorsque la méthode retourne, la valeur est 1.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne l’une des valeurs suivantes.



| Code de retour                                                                               | Description                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Réussite.<br/>                   |
| <dl> <dt>**\_pointeur E**</dt> </dl> | Argument de pointeur **null** .<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaPosition, classe**](cmediaposition.md)
</dt> </dl>

 

 




