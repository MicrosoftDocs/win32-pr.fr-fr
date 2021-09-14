---
description: La méthode CRendererInputPin est une méthode de constructeur.
ms.assetid: 272f864e-d6a8-4a9e-b72f-892147db9970
title: Constructeur CRendererInputPin. CRendererInputPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6888b234b87a48fc89f70c0db36122cbf7289ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006670"
---
# <a name="crendererinputpincrendererinputpin-constructor"></a>Constructeur CRendererInputPin. CRendererInputPin

La `CRendererInputPin` méthode est une méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CRendererInputPin(
   CBaseRenderer *pRenderer,
   HRESULT       *phr,
   LPCWSTR       Name
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pRenderer* 
</dt> <dd>

Pointeur vers l’objet [**CBaseRenderer**](cbaserenderer.md) qui implémente le filtre.

</dd> <dt>

*phr* 
</dt> <dd>

Pointeur vers une variable qui reçoit une valeur **HRESULT** .

</dd> <dt>

*Nom* 
</dt> <dd>

Pointeur vers une chaîne de caractères larges contenant l’identificateur de code confidentiel.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CRendererInputPin, classe**](crendererinputpin.md)
</dt> </dl>

 

 




