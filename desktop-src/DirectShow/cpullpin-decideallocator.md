---
description: La méthode DecideAllocator négocie un allocateur avec la broche de sortie.
ms.assetid: 5c04f440-b177-4caa-989f-3aa783c4b348
title: Méthode CPullPin. DecideAllocator (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91ffa139b916b1594e0729a0f8d52f07c62eda12
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007607"
---
# <a name="cpullpindecideallocator-method"></a>Méthode CPullPin. DecideAllocator

La `DecideAllocator` méthode négocie un allocateur avec la broche de sortie.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT DecideAllocator(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAlloc* 
</dt> <dd>

Pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur préféré du code confidentiel d’entrée, ou **null**.

</dd> <dt>

*pProps* 
</dt> <dd>

Pointeur vers une structure de [**\_ propriétés d’Allocator**](/windows/win32/api/strmif/ns-strmif-allocator_properties) facultative qui contient les exigences de mémoire tampon du code confidentiel d’entrée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK en cas de réussite, ou un code d’erreur dans le cas contraire.

## <a name="remarks"></a>Notes

Cette méthode appelle la méthode [**IAsyncReader :: RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) pour négocier un allocateur. Elle transmet le paramètre *pAlloc* directement à la méthode **RequestAllocator** . Elle transmet le paramètre *pProps* à **RequestAllocator** si *pProps* n’est pas **null**; dans le cas contraire, elle crée une structure de **\_ Propriétés Allocator** avec une requête par défaut de trois tampons de 64 Ko.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPullPin, classe**](cpullpin.md)
</dt> <dt>

[**CPullPin :: Connecter**](cpullpin-connect.md)
</dt> </dl>

 

 




