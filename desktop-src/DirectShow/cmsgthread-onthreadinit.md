---
description: Fournit l’initialisation sur un thread.
ms.assetid: a9c330bb-0a2b-45bf-9b24-d03dd61d7dbf
title: Méthode CMsgThread. OnThreadInit (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.OnThreadInit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 80e15d6430da77c0f22f5566375394b8fe6994ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542496"
---
# <a name="cmsgthreadonthreadinit-method"></a>Méthode CMsgThread. OnThreadInit

Fournit l’initialisation sur un thread.

## <a name="syntax"></a>Syntaxe


```C++
virtual void OnThreadInit();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Substituez cette fonction si vous souhaitez effectuer votre propre initialisation spécifique au démarrage du thread.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Msgthrd. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMsgThread, classe**](cmsgthread.md)
</dt> </dl>

 

 




