---
description: 'La méthode NonDelegatingAddRef incrémente le décompte de références sur l’objet. Cette méthode implémente la méthode INonDelegatingUnknown :: NonDelegatingAddRef.'
ms.assetid: abb6ee51-8fb8-4307-b127-b3667260e35a
title: Méthode CUnknown. NonDelegatingAddRef (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingAddRef
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f97260c03f0931e94e8ce6de8b7816789b2fe66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543291"
---
# <a name="cunknownnondelegatingaddref-method"></a>Méthode CUnknown. NonDelegatingAddRef

La `NonDelegatingAddRef` méthode incrémente le décompte de références sur l’objet. Cette méthode implémente la méthode **INonDelegatingUnknown :: NonDelegatingAddRef** .

## <a name="syntax"></a>Syntaxe


```C++
ULONG NonDelegatingAddRef();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne le nombre de références.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>ComBase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




