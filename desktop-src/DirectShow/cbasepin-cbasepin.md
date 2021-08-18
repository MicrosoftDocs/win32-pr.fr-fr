---
description: Méthode constructeur CBasePin. CBasePin.
ms.assetid: e8cb5f1d-171f-4bf8-8ab6-6e547c4678d2
title: Constructeur CBasePin. CBasePin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CBasePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cbeead09843aa8bf66471caeaabbdb42ee8d97d01cdaa9a54809f35c437b52d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916899"
---
# <a name="cbasepincbasepin-constructor"></a>Constructeur CBasePin. CBasePin

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CBasePin(
   TCHAR         *pObjectName,
   CBaseFilter   *pFilter,
   CCritSec      *pLock,
   HRESULT       *phr,
   LPCWSTR       pName,
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pObjectName* 
</dt> <dd>

Chaîne contenant le nom de débogage de l’objet. Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pFilter* 
</dt> <dd>

Pointeur vers le filtre qui a créé ce code confidentiel.

</dd> <dt>

*pLock* 
</dt> <dd>

Pointeur vers un verrou [**CCritSec**](ccritsec.md) , utilisé pour sérialiser les modifications d’État. Il peut s’agir de la même section critique que le verrou de filtre, [**CBaseFilter :: m \_ pLock**](cbasefilter-m-plock.md).

</dd> <dt>

*phr* 
</dt> <dd>

Pointeur vers une variable qui reçoit une valeur **HRESULT** indiquant la réussite ou l’échec de la méthode. Initialisez la valeur sur \_ OK avant de créer l’objet. La valeur est modifiée uniquement si une erreur se produit.

</dd> <dt>

*pName* 
</dt> <dd>

Chaîne de caractères larges contenant le nom du code PIN. Pour plus d’informations, consultez [**CBasePin :: QueryPinInfo**](cbasepin-querypininfo.md).

</dd> <dt>

*dir* 
</dt> <dd>

Membre de l’énumération de [**\_ direction du code confidentiel**](/windows/win32/api/strmif/ne-strmif-pin_direction) spécifiant la direction du code confidentiel.

</dd> </dl>

## <a name="remarks"></a>Remarques

La section critique spécifiée par *pLock* sérialise l’état du pin, y compris son état de connexion, le choix de l’allocateur, le type de média et l’état des opérations de vidage. N’utilisez pas cette section critique pour sérialiser les opérations de diffusion en continu. pour plus d’informations, consultez [Flow de données dans le Graph de filtre](data-flow-in-the-filter-graph.md).

Un filtre peut créer des codes confidentiels dans sa méthode de constructeur, donc à ce stade, le pointeur *pFilter* peut ne pas faire référence à un objet valide. Stockez le pointeur, mais ne le déréférencez pas dans le constructeur du pin.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




