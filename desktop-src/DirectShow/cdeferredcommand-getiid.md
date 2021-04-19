---
description: La méthode GetIID récupère l’identificateur d’interface (IID) de l’interface sur laquelle la méthode sera exécutée.
ms.assetid: d6eb7d46-294a-4169-96d3-4bed02c48c08
title: Méthode CDeferredCommand. GetIID (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetIID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d8677c70ab9c2c04224194bd825b106d33de8893
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541527"
---
# <a name="cdeferredcommandgetiid-method"></a>Méthode CDeferredCommand. GetIID

La `GetIID` méthode récupère l’identificateur d’interface (IID) de l’interface sur laquelle la méthode sera exécutée.

## <a name="syntax"></a>Syntaxe


```C++
REFIID GetIID();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne l’IID de l’interface sur laquelle la méthode sera exécutée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDeferredCommand, classe**](cdeferredcommand.md)
</dt> </dl>

 

 




