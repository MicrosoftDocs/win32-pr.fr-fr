---
description: La méthode IsValid détermine si un type principal a été assigné à cet objet.
ms.assetid: 22d28019-f360-4b93-972c-d1dfe83938f0
title: CMediaType. IsValid, méthode (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsValid
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d8e1731060021b61eb5037e1baeeda95021e8f5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312505"
---
# <a name="cmediatypeisvalid-method"></a>CMediaType. IsValid, méthode

La `IsValid` méthode détermine si un type principal a été assigné à cet objet.

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsValid() const;
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** si un type principal a été assigné à cet objet. Sinon, retourne **false**.

## <a name="remarks"></a>Remarques

Par défaut, les objets [**CMediaType**](cmediatype.md) sont initialisés avec un type majeur de GUID \_ null. Appelez cette méthode pour déterminer si l’objet a été correctement initialisé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




