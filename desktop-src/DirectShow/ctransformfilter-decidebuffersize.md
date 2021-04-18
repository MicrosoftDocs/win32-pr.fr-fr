---
description: La méthode DecideBufferSize définit les exigences de mémoire tampon de la broche de sortie.
ms.assetid: 33e41668-b4f6-4142-b22e-2ddfb96332df
title: Méthode CTransformFilter. DecideBufferSize (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71a506a9c9cd16a014418b24ad3fbd1186d6f48f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526528"
---
# <a name="ctransformfilterdecidebuffersize-method"></a>Méthode CTransformFilter. DecideBufferSize

La `DecideBufferSize` méthode définit les exigences de mémoire tampon de la broche de sortie.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAlloc* 
</dt> <dd>

Pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) sur l’allocateur de la broche de sortie.

</dd> <dt>

*ppropInputRequest* 
</dt> <dd>

Pointeur vers une structure de [**\_ Propriétés Allocator**](/windows/win32/api/strmif/ns-strmif-allocator_properties) qui contient des exigences de mémoire tampon à partir de la broche d’entrée en aval.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK ou une autre valeur **HRESULT** .

## <a name="remarks"></a>Notes

La méthode [**CTransformOutputPin ::D ecidebuffersize**](ctransformoutputpin-decidebuffersize.md) de la broche de sortie appelle cette méthode. La classe dérivée doit implémenter cette méthode. Pour plus d’informations, consultez [**CBaseOutputPin ::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




