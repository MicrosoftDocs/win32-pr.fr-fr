---
description: La méthode BreakConnect libère la broche d’entrée d’une connexion.
ms.assetid: e295cec1-8c8f-471c-8832-075ac7708cb1
title: Méthode CBaseRenderer. BreakConnect (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cefaa91578f397a5ce967dc9cb6200acbe45f016e81f4552b9d185ad9ffa2609
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044059"
---
# <a name="cbaserendererbreakconnect-method"></a>Méthode CBaseRenderer. BreakConnect

La `BreakConnect` méthode libère la broche d’entrée à partir d’une connexion.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                         | Description                            |
|-----------------------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>             | Le pin n’était pas connecté.<br/>  |
| <dl> <dt>**\_OK**</dt> </dl>                | Réussite.<br/>                    |
| <dl> <dt>**VFW \_ E \_ non \_ arrêté**</dt> </dl> | Le filtre est toujours actif.<br/> |



 

## <a name="remarks"></a>Remarques

La broche d’entrée du filtre appelle cette méthode à l’intérieur de sa propre `BreakConnect` méthode. (Pour plus d’informations, consultez [**CBasePin :: BreakConnect**](cbasepin-breakconnect.md).) Le filtre effectue une comptabilité interne, telle que la réinitialisation de l’indicateur de fin de flux.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




