---
description: 'Méthode CTransformFilter. CheckConnect : la méthode CheckConnect détermine si une connexion de code confidentiel est appropriée.'
ms.assetid: 4bec4b19-3f7c-43d8-9a45-2eb2cc15a0d4
title: Méthode CTransformFilter. CheckConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5927aac2fa58322c93a23489a22dc96a1e2a67f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234221"
---
# <a name="ctransformfiltercheckconnect-method"></a>Méthode CTransformFilter. CheckConnect

La `CheckConnect` méthode détermine si une connexion de code confidentiel est appropriée.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT CheckConnect(
   PIN_DIRECTION dir,
   IPin          *pPin
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dir* 
</dt> <dd>

Membre du type énuméré dans la [**\_ direction du code confidentiel**](/windows/win32/api/strmif/ne-strmif-pin_direction) , en spécifiant quelle broche du filtre effectue la connexion.

</dd> <dt>

*pPin* 
</dt> <dd>

Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de l’autre code confidentiel dans cette tentative de connexion.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Les méthodes [**CTransformInputPin :: CheckConnect**](ctransforminputpin-checkconnect.md) et [**CTransformOutputPin :: CheckConnect**](ctransformoutputpin-checkconnect.md) appellent cette méthode pendant le processus de connexion du code confidentiel. Cette méthode n’a aucun effet dans la classe de base. La classe dérivée peut la substituer. Par exemple, la classe dérivée peut interroger l’autre code confidentiel pour une interface particulière.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




