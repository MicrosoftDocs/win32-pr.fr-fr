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
ms.openlocfilehash: f86bc35688ab0ec1c19053a95cbfd2025cf45ad666ef419fdb8440c6a844cb61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640469"
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

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers une structure de [**\_ filtre AMOVIESETUP**](amoviesetup-filter.md) contenant des informations d’inscription pour le filtre.

## <a name="remarks"></a>Remarques

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

 

 




