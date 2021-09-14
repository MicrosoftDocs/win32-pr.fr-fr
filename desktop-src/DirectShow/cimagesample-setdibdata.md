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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127239129"
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

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageSample, classe**](cimagesample.md)
</dt> </dl>

 

 




