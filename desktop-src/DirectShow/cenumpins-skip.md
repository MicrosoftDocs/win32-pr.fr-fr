---
description: 'La méthode Skip ignore un nombre spécifié de codes confidentiels dans la séquence d’énumération. Cette méthode implémente la méthode IEnumPins :: Skip.'
ms.assetid: d42f958c-f488-4730-ab84-fc4e4150b186
title: CEnumPins. Skip, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1865453a89130303f28f338d8b7567e856c64173
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539938"
---
# <a name="cenumpinsskip-method"></a>CEnumPins. Skip, méthode

La `Skip` méthode ignore un nombre spécifié de codes confidentiels dans la séquence d’énumération. Cette méthode implémente la méthode [**IEnumPins :: Skip**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-skip) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Skip(
   ULONG cPins
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cPins* 
</dt> <dd>

Nombre de broches à ignorer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                                | Description                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                    | Ignorée au-delà de la fin de la séquence.<br/>                                       |
| <dl> <dt>**\_OK**</dt> </dl>                       | Opération réussie.<br/>                                                                    |
| <dl> <dt>**VFW \_ E \_ enum \_ non \_ \_ synchronisé**</dt> </dl> | L’état du filtre a changé et est désormais incohérent avec l’énumérateur.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CEnumPins, classe**](cenumpins.md)
</dt> </dl>

 

 




