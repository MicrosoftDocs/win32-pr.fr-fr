---
description: 'Décrémente le décompte de références sur l’objet. Cette méthode implémente la méthode INonDelegatingUnknown :: NonDelegatingRelease.'
ms.assetid: 58610f7d-5524-450f-a0f8-b299944abc78
title: Méthode CUnknown. NonDelegatingRelease (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingRelease
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1ac5145e1776602c5bb358805c45ec271766fe918b7924d948e286ae32b31794
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821953"
---
# <a name="cunknownnondelegatingrelease-method"></a>Méthode CUnknown. NonDelegatingRelease

Décrémente le décompte de références sur l’objet. Cette méthode implémente la méthode **INonDelegatingUnknown :: NonDelegatingRelease** .

## <a name="syntax"></a>Syntaxe


```C++
ULONG NonDelegatingRelease();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne le nombre de références.

## <a name="remarks"></a>Remarques

Lorsque le nombre de références atteint zéro, l’objet se supprime lui-même.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>combase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




