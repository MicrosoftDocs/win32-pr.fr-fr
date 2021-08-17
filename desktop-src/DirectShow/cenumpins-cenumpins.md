---
description: Méthode constructeur CEnumPins. CEnumPins.
ms.assetid: f696e433-b051-4de0-80e5-f9cd31fd0f23
title: Constructeur CEnumPins. CEnumPins (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1972533b86215e34563b9b1aa8f1b8ac3c14450b804fdae01ed7c7eafa78def4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131239"
---
# <a name="cenumpinscenumpins-constructor"></a>Constructeur CEnumPins. CEnumPins

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CEnumPins(
   CBaseFilter *pFilter,
   CEnumPins   *pEnumPins
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFilter* 
</dt> <dd>

Pointeur vers le filtre sur lequel énumérer les broches.

</dd> <dt>

*pEnumPins* 
</dt> <dd>

Pointeur vers l’interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) d’un énumérateur à cloner, ou **null**.

</dd> </dl>

## <a name="remarks"></a>Remarques

Si *pEnumPins* a la **valeur null**, cette méthode initialise l’énumérateur au début de la séquence d’énumération. Sinon, elle duplique l’état interne de l’énumérateur spécifié par *pEnumPins*.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CEnumPins, classe**](cenumpins.md)
</dt> </dl>

 

 




