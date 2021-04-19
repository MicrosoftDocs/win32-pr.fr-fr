---
description: La méthode Transform transforme un exemple en place.
ms.assetid: 2268041b-70d4-48a9-9bb8-4ab921cce649
title: CTransInPlaceFilter. Transform, méthode (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5b84f326807f730745268a217b6066dacb9aaa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533268"
---
# <a name="ctransinplacefiltertransform-method"></a>CTransInPlaceFilter. Transform, méthode

La `Transform` méthode transforme un exemple en place.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT Transform(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSample* 
</dt> <dd>

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                             | Description                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Ne fournissez pas cet exemple.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Opération réussie.<br/>                    |



 

## <a name="remarks"></a>Notes

La classe dérivée doit implémenter cette méthode. Transformez les exemples de données sur place. Si le filtre utilise deux allocations, il copie les données de l’exemple d’entrée vers un nouvel exemple et passe la copie à cette méthode.

Si le filtre ne doit pas livrer cet exemple (par exemple, pour prendre en charge le contrôle de qualité), la méthode doit retourner S \_ false.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceFilter, classe**](ctransinplacefilter.md)
</dt> </dl>

 

 




