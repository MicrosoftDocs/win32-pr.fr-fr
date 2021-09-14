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
ms.openlocfilehash: 7b46838278414442d6c6fc64687fe21e02732e83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006772"
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

## <a name="return-value"></a>Valeur de retour

Retourne le \_ pointeur E si *pcTInfo* n’est pas valide ; sinon, retourne S \_ OK.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaControl, classe**](cmediacontrol.md)
</dt> </dl>

 

 




