---
description: 'La méthode CheckCapabilities interroge si un flux a spécifié des fonctionnalités de recherche. Cette méthode implémente la méthode IMediaSeeking :: CheckCapabilities.'
ms.assetid: 48096af6-bbce-4a1f-be9a-fd150ed4536e
title: Méthode CPosPassThru. CheckCapabilities (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 33f7a685684667d2f5d465b14070a595c70b178c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528863"
---
# <a name="cpospassthrucheckcapabilities-method"></a>Méthode CPosPassThru. CheckCapabilities

La `CheckCapabilities` méthode interroge si un flux a spécifié des fonctionnalités de recherche. Cette méthode implémente la méthode [**IMediaSeeking :: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCapabilities* 
</dt> <dd>

Pointeur vers une combinaison d’opérations de bits d’un ou de plusieurs attributs de [**\_ \_ \_ capacités de recherche**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) de recherche. Lorsque la méthode retourne, la valeur indique quels attributs sont disponibles.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur **HRESULT** de la broche connectée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPosPassThru, classe**](cpospassthru.md)
</dt> </dl>

 

 




