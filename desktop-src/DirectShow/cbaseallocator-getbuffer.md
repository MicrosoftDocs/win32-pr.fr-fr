---
description: 'La méthode GetBuffer récupère un exemple de support qui contient une mémoire tampon. Cette méthode implémente la méthode IMemAllocator :: GetBuffer.'
ms.assetid: 81694b9c-b325-47c8-94e4-f54d1329a684
title: Méthode CBaseAllocator. GetBuffer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f965885d4a7a12e09c8875f71032ce2fded61bd2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999772"
---
# <a name="cbaseallocatorgetbuffer-method"></a>Méthode CBaseAllocator. GetBuffer

La `GetBuffer` méthode récupère un exemple de média qui contient une mémoire tampon. Cette méthode implémente la méthode [**IMemAllocator :: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetBuffer(
   IMediaSample   **ppBuffer,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppBuffer* 
</dt> <dd>

Reçoit un pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de la mémoire tampon. L’appelant doit libérer l’interface.

</dd> <dt>

*pStartTime* 
</dt> <dd>

Pointeur vers l’heure de début de l’exemple.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Pointeur vers l’heure de fin de l’exemple.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Combinaison d’opérations de bits de zéro ou plusieurs indicateurs. La classe de base prend en charge l’indicateur suivant.



| Valeur                                                                                                                                                          | Signification                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="AM_GBF_NOWAIT"></span><span id="am_gbf_nowait"></span><dl> <dt>**AM \_ GBF \_ NOWAIT**</dt> </dl> | N’attendez pas qu’une mémoire tampon devienne disponible. <br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** suivantes.



| Code de retour                                                                                           | Description                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Réussite.<br/>                     |
| <dl> <dt>**VFW \_ E \_ non \_ validé**</dt> </dl> | Allocator n’a pas été validé.<br/> |
| <dl> <dt>**\_ \_ délai d’expiration VFW E**</dt> </dl>        | Expiration du délai d’attente.<br/>                   |



 

## <a name="remarks"></a>Notes

À moins que l’appelant ne spécifie l’indicateur **am \_ GBF \_ NOWAIT** dans *dwFlags*, cette méthode se bloque jusqu’à ce que l’exemple suivant soit disponible.

L’exemple de média récupéré possède un pointeur valide vers la mémoire tampon allouée. L’appelant est chargé de définir d’autres propriétés sur l’exemple, telles que les horodatages, les heures de média ou la propriété de point de synchronisation. Pour plus d’informations, consultez [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample).

Dans la classe de base, les paramètres *pStartTime* et *pEndTime* sont ignorés. Les classes dérivées peuvent utiliser ces valeurs. Par exemple, l’allocateur pour le filtre de [convertisseur vidéo](video-renderer-filter.md) utilise ces valeurs pour synchroniser le basculement entre les surfaces DirectDraw.

Si la méthode doit attendre un échantillon, elle incrémente le nombre d’objets en attente ([**CBaseAllocator :: m \_ lCount**](cbaseallocator-m-lcount.md)) et appelle la fonction [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) sur le sémaphore ([**CBaseAllocator :: m \_ hSem**](cbaseallocator-m-hsem.md)). Quand un exemple est disponible, il appelle la méthode [**CBaseAllocator :: ReleaseBuffer**](cbaseallocator-releasebuffer.md) sur l’allocateur, ce qui augmente le nombre de sémaphores par **m \_ lCount** (libérant ainsi les threads en attente) et définit **m \_ lCount** sur zéro.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseAllocator, classe**](cbaseallocator.md)
</dt> </dl>

 

