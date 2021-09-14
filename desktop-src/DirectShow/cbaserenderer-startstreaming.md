---
description: La méthode StartStreaming lance la diffusion en continu lorsque le filtre passe à l’État en cours d’exécution.
ms.assetid: 198e9c1b-be69-4ba6-aa67-9f24ed080ab6
title: Méthode CBaseRenderer. StartStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bf1fcb1cbfb651221296054493688b2d9f33bd3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999742"
---
# <a name="cbaserendererstartstreaming-method"></a>Méthode CBaseRenderer. StartStreaming

La `StartStreaming` méthode lance la diffusion en continu lorsque le filtre passe à l’État en cours d’exécution.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK ou une autre valeur **HRESULT** .

## <a name="remarks"></a>Notes

Si le filtre a un exemple, il planifie l’exemple de rendu. Dans le cas contraire, si une notification de fin de flux est en attente, le filtre envoie un événement [**EC \_ complet**](ec-complete.md) au gestionnaire de graphes de filtre.

Cette méthode appelle la méthode [**CBaseRenderer :: OnStartStreaming**](cbaserenderer-onstartstreaming.md) . Cette méthode ne fait rien dans la classe de base, mais la classe dérivée peut la substituer.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




