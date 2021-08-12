---
description: 'La méthode QueryVendorInfo récupère une chaîne contenant des informations sur le fournisseur. Cette méthode implémente la méthode IBaseFilter :: QueryVendorInfo.'
ms.assetid: 083c0556-d516-4daf-8621-e158ea78b5a3
title: Méthode CBaseFilter. QueryVendorInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryVendorInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff1cd8b966456df631a573ab2e8691b3be5d8bda47b21b042986204144e639b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659802"
---
# <a name="cbasefilterqueryvendorinfo-method"></a>Méthode CBaseFilter. QueryVendorInfo

La `QueryVendorInfo` méthode récupère une chaîne contenant des informations sur le fournisseur. Cette méthode implémente la méthode [**IBaseFilter :: QueryVendorInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryvendorinfo) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT QueryVendorInfo(
   LPWSTR *pVendorInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pVendorInfo* 
</dt> <dd>

Adresse d’une variable qui reçoit un pointeur vers une chaîne de caractères larges contenant les informations sur le fournisseur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne E \_ NOTIMPL.

## <a name="remarks"></a>Remarques

Pour fournir des informations sur le fournisseur d’un filtre, substituez cette méthode. Si vous implémentez cette méthode, utilisez la fonction **CoTaskMemAlloc** pour allouer de la mémoire à la chaîne. L’appelant est chargé d’appeler la fonction **CoTaskMemFree** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseFilter, classe**](cbasefilter.md)
</dt> </dl>

 

 




