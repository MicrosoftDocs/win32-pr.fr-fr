---
description: 'La méthode SetNotify définit ou supprime un rappel sur l’allocateur. L’allocateur appelle la méthode de rappel chaque fois que la méthode IMemAllocator :: ReleaseBuffer de l’allocateur est appelée.'
ms.assetid: ef9a6c66-d392-4130-b4fc-9eb6aecb6cbf
title: Méthode CBaseAllocator. SetNotify (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16e836be1610e8c2399a263120d847f3fada4b638332ee81914031f7a8e3ffb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108649"
---
# <a name="cbaseallocatorsetnotify-method"></a>Méthode CBaseAllocator. SetNotify

\[Les [**SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) peuvent être modifiés ou non disponibles dans les versions ultérieures.\]

La `SetNotify` méthode définit ou supprime un rappel sur l’allocateur. L’allocateur appelle la méthode de rappel chaque fois que la méthode [**IMemAllocator :: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) de l’allocateur est appelée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetNotify(
   IMemAllocatorNotifyCallbackTemp *pNotify
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pNotify* 
</dt> <dd>

Pointeur vers l’interface [**IMemAllocatorNotifyCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatornotifycallbacktemp) qui sera utilisée pour le rappel. L’appelant doit implémenter l’interface. Utilisez la valeur **null** pour supprimer le rappel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

Cette méthode implémente la méthode [**IMemAllocatorCallbackTemp :: SetNotify**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-setnotify) . L’Allocator n’expose pas l’interface [**IMemAllocatorCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatorcallbacktemp) , sauf si l’indicateur *fEnableReleaseCallback* a la valeur **true** dans le constructeur [**CBaseAllocator**](cbaseallocator.md) .

Cette méthode définit la variable de membre [**CBaseAllocator :: m \_ pNotify**](cbaseallocator-m-pnotify.md) sur la valeur *pNotify* et incrémente le décompte de références sur l’interface. Si *m \_ pNotify* n’est pas **null**, la méthode **ReleaseBuffer** de l’allocateur appelle [**IMemAllocatorNotifyCallbackTemp :: NotifyRelease**](/windows/desktop/api/Strmif/nf-strmif-imemallocatornotifycallbacktemp-notifyrelease). Consultez la section Notes dans cette méthode pour plus d’informations sur l’implémentation du rappel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseAllocator, classe**](cbaseallocator.md)
</dt> </dl>

 

 




