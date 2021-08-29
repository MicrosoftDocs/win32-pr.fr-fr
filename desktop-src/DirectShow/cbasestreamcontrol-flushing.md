---
description: La méthode de vidage indique à la classe de base que le code pin a démarré ou a arrêté le vidage.
ms.assetid: a3c000e1-18a1-48f7-9e2e-fe63cf13fc5c
title: CBaseStreamControl. Flush, méthode (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.Flushing
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: da25983f26a89d5b264ec616e887d465f0851e3c901e2f1fac1dbab0c48be5bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103179"
---
# <a name="cbasestreamcontrolflushing-method"></a>CBaseStreamControl. Flush, méthode

La `Flushing` méthode notifie la classe de base que le code confidentiel a démarré ou a arrêté le vidage.

## <a name="syntax"></a>Syntaxe


```C++
void Flushing(
   BOOL bInProgress
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bInProgress* 
</dt> <dd>

Spécifie une valeur booléenne qui indique si le code PIN est vidé. Utilisez la valeur **true** lorsque le code PIN commence une opération de vidage, et **false** lorsque le code PIN met fin à une opération de vidage.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Le code confidentiel doit appeler cette méthode à partir de ses méthodes [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) et [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) . Spécifiez **true** dans **BeginFlush** et **false** dans **EndFlush**.

Cette méthode provoque l’arrêt de l’attente de la méthode [**CBaseStreamControl :: CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) . Pendant le vidage du code PIN, **CheckStreamState** retourne toujours le flux \_ ignoré.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Strmctl. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseStreamControl, classe**](cbasestreamcontrol.md)
</dt> </dl>

 

 




