---
description: 'Méthode CTransInPlaceFilter. CompleteConnect : la méthode CompleteConnect termine une connexion de code confidentiel.'
ms.assetid: 0c02c455-dbd0-4606-b1b1-f965c2a5805b
title: Méthode CTransInPlaceFilter. CompleteConnect (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d9cc0bc839a4e35c4ce896acdf50da10f0c2bb0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224644"
---
# <a name="ctransinplacefiltercompleteconnect-method"></a>Méthode CTransInPlaceFilter. CompleteConnect

La `CompleteConnect` méthode termine une connexion de code confidentiel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CompleteConnect(
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

## <a name="return-value"></a>Valeur de retour

Retourne un **HRESULT**. Les valeurs possibles sont les suivantes :



| Code de retour                                                                                           | Description                                     |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Réussite.<br/>                             |
| <dl> <dt>**VFW \_ E \_ pas \_ dans le \_ graphique**</dt> </dl> | Le filtre n’est pas dans un graphique de filtre.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode remplace la méthode [**CTransformFilter :: CompleteConnect**](ctransformfilter-completeconnect.md) .

Le comportement du filtre dépend de l’ordre des connexions de code confidentiel :

-   Si la broche d’entrée est connectée en premier, la connexion utilise un allocateur temporaire. Lorsque la broche de sortie est connectée, le filtre reconnecte la broche d’entrée. Si vous reconnectez la broche d’entrée, le filtre en amont renégocie l’allocateur. À ce stade, la broche d’entrée propose un allocateur à partir du filtre en aval. Pour plus d’informations, consultez [**CTransInPlaceInputPin :: GetAllocator**](ctransinplaceinputpin-getallocator.md).
-   Si la broche de sortie est connectée en premier, la broche de sortie ne sélectionne pas d’allocateur. Lorsque la broche d’entrée est connectée, elle négocie un allocateur pour les deux connexions. Si les types de média d’entrée et de sortie ne sont pas identiques, le filtre reconnecte la broche de sortie à l’aide du type d’entrée.

Le filtre effectue toutes les reconnexions de code confidentiel en appelant la méthode [**CBaseFilter :: ReconnectPin**](cbasefilter-reconnectpin.md) . La méthode **ReconnectPin** appelle à son tour la méthode [**IFilterGraph2 :: ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) sur le gestionnaire de graphique de filtre.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceFilter, classe**](ctransinplacefilter.md)
</dt> </dl>

 

 




