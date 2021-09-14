---
description: La méthode CompleteConnect termine la connexion de la broche d’entrée à une autre broche.
ms.assetid: 8dfc1a50-bc73-436a-a471-d8d3218410d3
title: Méthode CBaseRenderer. CompleteConnect (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9d2d35f99a3b3b8dc5b668b8ee9a9f94f0a53dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111333"
---
# <a name="cbaserenderercompleteconnect-method"></a>Méthode CBaseRenderer. CompleteConnect

La `CompleteConnect` méthode termine la connexion de la broche d’entrée à une autre broche.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de la broche de sortie.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK.

## <a name="remarks"></a>Notes

La broche d’entrée du filtre appelle cette méthode à l’intérieur de sa propre `CompleteConnect` méthode, qui est appelée pour terminer une connexion de code confidentiel. (Pour plus d’informations, consultez [**CBasePin :: CompleteConnect**](cbasepin-completeconnect.md).) Le filtre appelle la méthode [**CBaseRenderer :: SetRepaintStatus**](cbaserenderer-setrepaintstatus.md) pour activer les événements de [**\_ redessin ce**](ec-repaint.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




