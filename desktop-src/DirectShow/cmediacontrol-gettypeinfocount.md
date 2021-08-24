---
description: 'Méthode CMediaControl. GetTypeInfoCount : récupère le nombre d’interfaces d’informations de type fournies par un objet.'
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
ms.openlocfilehash: a751c7ed9d10547d34ec491f2e90e5ca6f1ab1f19bc1221c04b15da427da4570
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832519"
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
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaControl, classe**](cmediacontrol.md)
</dt> </dl>

 

 




