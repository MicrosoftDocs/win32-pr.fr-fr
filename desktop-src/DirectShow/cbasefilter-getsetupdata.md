---
description: La méthode GetSetupData récupère les données d’inscription du filtre.
ms.assetid: 93582c75-4f40-492c-919c-c8a06dce7715
title: Méthode CBaseFilter. GetSetupData (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetSetupData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40223a22f4de4a078ce84f8ebe49bddd5ab13575
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007645"
---
# <a name="cbasefiltergetsetupdata-method"></a>Méthode CBaseFilter. GetSetupData

La `GetSetupData` méthode récupère les données d’inscription pour le filtre.

> [!Note]  
> Cette méthode est obsolète. Elle est appelée par les méthodes [**CBaseFilter :: Register**](cbasefilter-register.md) et [**CBaseFilter :: Unregister**](cbasefilter-unregister.md) .

 

## <a name="syntax"></a>Syntaxe


```C++
virtual LPAMOVIESETUP_FILTER GetSetupData();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne un pointeur vers une structure de [**\_ filtre AMOVIESETUP**](amoviesetup-filter.md) contenant des informations d’inscription pour le filtre.

## <a name="remarks"></a>Notes

La classe de base retourne la **valeur null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseFilter, classe**](cbasefilter.md)
</dt> </dl>

 

 




