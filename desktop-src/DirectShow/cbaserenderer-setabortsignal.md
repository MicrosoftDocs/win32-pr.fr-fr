---
description: La méthode SetAbortSignal définit un indicateur qui indique s’il faut arrêter le rendu et rejeter d’autres exemples.
ms.assetid: 2dbf3b4d-e285-4d17-a77c-01a16c09d148
title: Méthode CBaseRenderer. SetAbortSignal (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetAbortSignal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 819f279d20192ff82d9021e03780713f714682abf47aaf854b4568312572e8d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526531"
---
# <a name="cbaserenderersetabortsignal-method"></a>Méthode CBaseRenderer. SetAbortSignal

La `SetAbortSignal` méthode définit un indicateur qui indique s’il faut arrêter le rendu et rejeter d’autres exemples.

## <a name="syntax"></a>Syntaxe


```C++
void SetAbortSignal(
   BOOL bAbort
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bAbort* 
</dt> <dd>

Valeur booléenne indiquant s’il faut arrêter le rendu. Si la **valeur est true**, le filtre n’affiche plus d’échantillons.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode définit l’indicateur [**CBaseRenderer :: m \_ bAbort**](cbaserenderer-m-babort.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




