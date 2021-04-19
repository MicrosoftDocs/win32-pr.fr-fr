---
description: La méthode CheckTransform vérifie si un type de média d’entrée est compatible avec un type de média de sortie.
ms.assetid: 349145e5-c12d-41df-ae37-7846f8aaa423
title: Méthode CTransformFilter. CheckTransform (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b3302304e6a0f9df41005f7ed63d9316a3cd410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520977"
---
# <a name="ctransformfilterchecktransform-method"></a>Méthode CTransformFilter. CheckTransform

La `CheckTransform` méthode vérifie si un type de média d’entrée est compatible avec un type de média de sortie.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mtIn* 
</dt> <dd>

Pointeur vers un objet [**CMediaType**](cmediatype.md) qui spécifie le type d’entrée.

</dd> <dt>

*mtOut* 
</dt> <dd>

Pointeur vers un objet [**CMediaType**](cmediatype.md) qui spécifie le type de sortie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                                | Description                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | Les types de média sont compatibles.<br/>     |
| <dl> <dt>**TYPE de VFW \_ E \_ \_ non \_ accepté**</dt> </dl> | Les types de média ne sont pas compatibles.<br/> |



 

## <a name="remarks"></a>Notes

La classe dérivée doit implémenter cette méthode. Retourne S \_ OK si le filtre peut accepter les deux types de média spécifiés, ou un code d’erreur dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




