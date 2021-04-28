---
description: 'Méthode CTransformFilter. CompleteConnect : la méthode CompleteConnect termine une connexion de code confidentiel.'
ms.assetid: b687d2ee-4aee-4fae-bc2f-23ee037d0e6d
title: Méthode CTransformFilter. CompleteConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2251ba45c7a39ec9bf205fdd6643e02392e40e5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095167"
---
# <a name="ctransformfiltercompleteconnect-method"></a>Méthode CTransformFilter. CompleteConnect

La `CompleteConnect` méthode termine une connexion de code confidentiel.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*direction* 
</dt> <dd>

Membre du type énuméré dans la [**\_ direction du code confidentiel**](/windows/win32/api/strmif/ne-strmif-pin_direction) , en spécifiant quelle broche du filtre effectue la connexion.

</dd> <dt>

*pReceivePin* 
</dt> <dd>

Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de l’autre code confidentiel dans cette tentative de connexion.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne S \_ OK.

## <a name="remarks"></a>Notes 

Les méthodes [**CTransformInputPin :: CompleteConnect**](ctransforminputpin-completeconnect.md) et [**CTransformOutputPin :: CompleteConnect**](ctransformoutputpin-completeconnect.md) appellent cette méthode pendant le processus de connexion du code confidentiel. Cette méthode n’a aucun effet dans la classe de base, mais la classe dérivée peut la substituer.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




