---
description: Méthode constructeur CBaseAllocator. CBaseAllocator.
ms.assetid: e697e377-6407-4316-9f04-fe3bdb814175
title: Constructeur CBaseAllocator. CBaseAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21da9f5dda7f60fd4a88e85eb28f2197bdc9847d0b56d413bd6b49cb5abfe658
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640999"
---
# <a name="cbaseallocatorcbaseallocator-constructor"></a>Constructeur CBaseAllocator. CBaseAllocator

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CBaseAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   BOOL      bEvent = TRUE,
   BOOL      fEnableReleaseCallback = FALSE
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pName* 
</dt> <dd>

Pointeur vers une chaîne contenant le nom de débogage de l’allocateur. Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pUnk* 
</dt> <dd>

Pointeur vers le propriétaire de cet objet. Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation. Sinon, affectez la valeur **null** à ce paramètre.

</dd> <dt>

*phr* 
</dt> <dd>

Pointeur vers une valeur **HRESULT** . Définissez la valeur sur \_ OK avant de créer l’objet. Si le constructeur échoue, la valeur est définie sur un code d’erreur.

</dd> <dt>

*à la vente* 
</dt> <dd>

Valeur booléenne indiquant s’il faut créer un sémaphore. Si la **valeur est true**, l’allocateur crée un sémaphore ([**CBaseAllocator :: m \_ hSem**](cbaseallocator-m-hsem.md)), qui est signalé chaque fois qu’un exemple devient disponible. Affectez la valeur **false** si vous implémentez une classe dérivée qui ne requiert pas de sémaphore.

</dd> <dt>

*fEnableReleaseCallback* 
</dt> <dd>

Valeur booléenne indiquant si le mécanisme de rappel de mise en version est activé. Définissez la valeur sur **true** si vous souhaitez fournir une interface de rappel, qui est appelée lorsque les mémoires tampons sont libérées. Spécifiez le rappel en appelant la méthode [**CBaseAllocator :: SetNotify**](cbaseallocator-setnotify.md) .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseAllocator, classe**](cbaseallocator.md)
</dt> </dl>

 

 




