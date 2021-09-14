---
description: Méthode constructeur CImageAllocator. CImageAllocator.
ms.assetid: 8c215b16-98e5-42fb-a95b-b6df1ade180e
title: Constructeur CImageAllocator. CImageAllocator (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f17ae78b668f6cc35e454c5e4e83d38727077ef7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119989"
---
# <a name="cimageallocatorcimageallocator-constructor"></a>Constructeur CImageAllocator. CImageAllocator

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CImageAllocator(
   CBaseFilter *pFilter,
   TCHAR       *pName,
   HRESULT     *phr
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFilter* 
</dt> <dd>

Pointeur désignant le filtre propriétaire.

</dd> <dt>

*pName* 
</dt> <dd>

Pointeur vers une chaîne contenant le nom de débogage de l’allocateur. Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*phr* 
</dt> <dd>

Pointeur vers une valeur **HRESULT** . Définissez la valeur sur \_ OK avant de créer l’objet. Si le constructeur échoue, la valeur est définie sur un code d’erreur.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageAllocator, classe**](cimageallocator.md)
</dt> </dl>

 

 




