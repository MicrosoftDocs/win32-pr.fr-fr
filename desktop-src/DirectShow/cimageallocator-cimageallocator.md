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
ms.openlocfilehash: 71d7ca547556c151107c35c9ece1f4ee0d0ca6a80feb6db0cebb06878ddbca01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131219"
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
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageAllocator, classe**](cimageallocator.md)
</dt> </dl>

 

 




