---
description: La méthode SourceThreadCanWait contient ou libère le thread de streaming.
ms.assetid: f68f5f0b-ef5b-49a9-a768-c4cc065c0cb3
title: Méthode CBaseRenderer. SourceThreadCanWait (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SourceThreadCanWait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f01be304ec2b5f845ea61c9609808c6e2f39fca9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999744"
---
# <a name="cbaserenderersourcethreadcanwait-method"></a>Méthode CBaseRenderer. SourceThreadCanWait

La `SourceThreadCanWait` méthode conserve ou libère le thread de streaming.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT SourceThreadCanWait(
   BOOL bCanWait
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bCanWait* 
</dt> <dd>

Valeur booléenne indiquant s’il faut conserver le thread de streaming. Si la **valeur est true**, le thread de streaming est bloqué lorsque le filtre attend pour afficher les exemples suivants. Si la **valeur est false**, le thread de streaming est libéré.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK.

## <a name="remarks"></a>Notes

L’appel de la `SourceThreadCanWait` méthode avec la valeur **false** force le filtre à retourner à partir d’un appel [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) bloqué. Lorsque le filtre est en cours d’exécution, il bloque les appels de **réception** jusqu’à l’heure de présentation de l’exemple actuel. Lorsque le filtre est suspendu, il bloque les appels de **réception** indéfiniment. Ce comportement régit le flux de données dans le flux. Toutefois, lorsque le filtre est arrêté ou vidé, il ne doit pas être bloqué.

Le blocage est contrôlé par la méthode [**CBaseRenderer :: WaitForRenderTime**](cbaserenderer-waitforrendertime.md) , qui attend deux événements : [**CBaseRenderer :: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) et [**CBaseRenderer :: m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md). L’événement **m \_ RenderEvent** est signalé lorsque l’heure de la présentation arrive. L’événement **m \_ ThreadSignal** est signalé lorsque `SourceThreadCanWait` est appelé avec la valeur **false**. L’appel `SourceThreadCanWait` de avec la valeur **true** réinitialise l’événement.

Les méthodes [**CBaseRenderer :: Stop**](cbaserenderer-stop.md) et [**CBaseRenderer :: BeginFlush**](cbaserenderer-beginflush.md) appellent `SourceThreadCanWait` avec la valeur **false** (en libérant le thread de diffusion en continu). Les méthodes [**CBaseRenderer ::P ause**](cbaserenderer-pause.md), [**CBaseRenderer :: Run**](cbaserenderer-run.md)et [**CBaseRenderer :: EndFlush**](cbaserenderer-endflush.md) appellent `SourceThreadCanWait` avec la valeur **true**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




