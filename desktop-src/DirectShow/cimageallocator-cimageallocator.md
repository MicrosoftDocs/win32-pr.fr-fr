---
description: Méthode de constructeur.
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
ms.openlocfilehash: a5f6873e8cc073e0b716f94c980ecceba8f4512f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543824"
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageAllocator, classe**](cimageallocator.md)
</dt> </dl>

 

 




