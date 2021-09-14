---
description: La méthode OnRenderStart définit des informations pour le rendu.
ms.assetid: 698fe778-e2cb-4b87-a668-084b6c12c71f
title: Méthode CBaseVideoRenderer. OnRenderStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7327d25aafa6f6673b7ed70b658f675a9dab8f4d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123754"
---
# <a name="cbasevideorendereronrenderstart-method"></a>Méthode CBaseVideoRenderer. OnRenderStart

La `OnRenderStart` méthode définit des informations pour le rendu.

## <a name="syntax"></a>Syntaxe


```C++
void OnRenderStart(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Pointeur vers l’exemple de média.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette fonction membre récupère le temps horloge actuel du système et le stocke dans une variable membre à utiliser lorsque le dessin est terminé. La fonction effectue également la journalisation des performances. Cette fonction membre doit être appelée juste avant le début du dessin.

Cette fonction membre substitue [**CBaseRenderer :: OnRenderStart**](cbaserenderer-onrenderstart.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




