---
description: 'La méthode ReleaseBuffer retourne un exemple de support à la liste des exemples de supports gratuits. Cette méthode implémente la méthode IMemAllocator :: ReleaseBuffer.'
ms.assetid: 35e4e426-044c-4e57-af13-2fddf8501db7
title: Méthode CBaseAllocator. ReleaseBuffer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.ReleaseBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e339f3a8186e845e28261633806a61b1b15c281
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531074"
---
# <a name="cbaseallocatorreleasebuffer-method"></a>Méthode CBaseAllocator. ReleaseBuffer

La `ReleaseBuffer` méthode retourne un exemple de support à la liste des exemples de supports gratuits. Cette méthode implémente la méthode [**IMemAllocator :: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ReleaseBuffer(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSample* 
</dt> <dd>

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’objet d’exemple de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Quand le nombre de références d’un exemple de média atteint zéro, l’exemple appelle **ReleaseBuffer** avec lui-même comme paramètre. Cette méthode effectue les actions suivantes.

-   Retourne l’exemple de support à la liste libre ([**CBaseAllocator :: m \_ lFree**](cbaseallocator-m-lfree.md)).
-   Appelle la méthode [**CBaseAllocator :: NotifySample**](cbaseallocator-notifysample.md) , qui libère tous les threads qui sont bloqués lors des appels à la méthode [**CBaseAllocator :: GetBuffer**](cbaseallocator-getbuffer.md) .
-   Si la méthode [**CBaseAllocator :: SetNotify**](cbaseallocator-setnotify.md) a été appelée précédemment, appelle la méthode **IMemAllocatorNotifyCallbackTemp :: NotifyRelease** .
-   Lorsque le dernier échantillon est publié, s’il y a un appel [**CBaseAllocator ::D ecommit**](cbaseallocator-decommit.md) , appelle la méthode [**CBaseAllocator :: Free**](cbaseallocator-free.md) pour libérer la mémoire tampon. (Dans la classe de base, **Free** est une méthode virtuelle pure.)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseAllocator, classe**](cbaseallocator.md)
</dt> </dl>

 

 




