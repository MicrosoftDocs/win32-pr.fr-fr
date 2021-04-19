---
description: La méthode SetConfigInfo spécifie le pointeur IGraphConfig et l’événement stop.
ms.assetid: 938fe8be-5622-4954-9ba3-31fc68fbfa31
title: Méthode CDynamicOutputPin. SetConfigInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SetConfigInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b0c14342a629a38a878649ac59d8f1f814874f12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522796"
---
# <a name="cdynamicoutputpinsetconfiginfo-method"></a>Méthode CDynamicOutputPin. SetConfigInfo

La `SetConfigInfo` méthode spécifie le pointeur [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) et l’événement stop.

## <a name="syntax"></a>Syntaxe


```C++
void SetConfigInfo(
   IGraphConfig *pGraphConfig,
   HANDLE       hStopEvent
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pGraphConfig* 
</dt> <dd>

Pointeur vers l’interface [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) , ou **null**.

</dd> <dt>

*hStopEvent* 
</dt> <dd>

Handle vers un événement qui est signalé lorsque le filtre s’arrête, ou **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le filtre doit appeler cette méthode lorsqu’il rejoint le graphique de filtre. Le gestionnaire de graphes de filtres prend en charge **IGraphConfig**. Pour le paramètre *hStopEvent* , créez un événement de réinitialisation manuelle. Lorsque le filtre quitte le graphique de filtre, appelez à nouveau cette méthode avec la **valeur null** pour les deux paramètres.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDynamicOutputPin, classe**](cdynamicoutputpin.md)
</dt> </dl>

 

 




