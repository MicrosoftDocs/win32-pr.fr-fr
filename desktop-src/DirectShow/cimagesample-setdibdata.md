---
description: La méthode SetDIBData spécifie des informations sur la bitmap indépendante du périphérique (DIB) GDI que cet objet gère. Appelez cette méthode pour initialiser l’objet CImageSample.
ms.assetid: 850fa16b-d4b9-4fe6-b202-7b54c49a4589
title: Méthode CImageSample. SetDIBData (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.SetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 418263da0416b325b1b080713dd6289f3bcc688e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525366"
---
# <a name="cimagesamplesetdibdata-method"></a>Méthode CImageSample. SetDIBData

La `SetDIBData` méthode spécifie des informations sur la bitmap indépendante du périphérique (DIB) GDI que cet objet gère. Appelez cette méthode pour initialiser l’objet **CImageSample** .

## <a name="syntax"></a>Syntaxe


```C++
void SetDIBData(
   DIBDATA *pDibData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDibData* 
</dt> <dd>

Pointeur vers une structure [**DIBDATA**](dibdata.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageSample, classe**](cimagesample.md)
</dt> </dl>

 

 




