---
description: La méthode GetDIBData récupère des informations sur la bitmap indépendante du périphérique (DIB) GDI que cet objet gère.
ms.assetid: ec337336-69ec-47ff-a522-42c0388f9bc0
title: Méthode CImageSample. GetDIBData (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.GetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 894d75512c6c7909f617e13999e7290efea663fa843bf64424aad8371965de75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655598"
---
# <a name="cimagesamplegetdibdata-method"></a>Méthode CImageSample. GetDIBData

La `GetDIBData` méthode récupère des informations sur la bitmap indépendante du périphérique (DIB) GDI que cet objet gère.

## <a name="syntax"></a>Syntaxe


```C++
DIBDATA* GetDIBData();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers une structure [**DIBDATA**](dibdata.md) .

## <a name="remarks"></a>Remarques

L’appelant doit initialiser la structure **DIBDATA** avant d’appeler cette méthode. Vérifiez la valeur de **CImageSample :: m \_ bInit**. Pour initialiser la structure, appelez la méthode [**CImageSample :: SetDIBData**](cimagesample-setdibdata.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageSample, classe**](cimagesample.md)
</dt> </dl>

 

 




