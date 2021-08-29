---
description: Méthode constructeur CBaseRenderer. CBaseRenderer.
ms.assetid: df5efbb3-6bce-4e30-b1b1-d69bf64fa87d
title: Constructeur CBaseRenderer. CBaseRenderer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CBaseRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b7041444e40aa926efbeebd074d8e8bb736bdd1005c35730dac86a87303927f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043999"
---
# <a name="cbaserenderercbaserenderer-constructor"></a>Constructeur CBaseRenderer. CBaseRenderer

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CBaseRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   UINT      TimerResolution = 1
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RenderClass* 
</dt> <dd>

Identificateur de classe du convertisseur.

</dd> <dt>

*pName* 
</dt> <dd>

Pointeur vers une chaîne contenant le nom du filtre, à des fins de débogage.

</dd> <dt>

*pUnk* 
</dt> <dd>

Pointeur vers le propriétaire de cet objet. Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation. Sinon, affectez la valeur **null** à ce paramètre.

</dd> <dt>

*phr* 
</dt> <dd>

Reçoit une valeur **HRESULT** .

</dd> <dt>

*TimerResolution* 
</dt> <dd>

Résolution de la minuterie.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




