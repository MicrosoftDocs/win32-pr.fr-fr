---
description: La méthode GetColourMask récupère les masques de couleur pour le format d’affichage actuel.
ms.assetid: 386d0439-8502-411d-935c-3c2153a8b5b4
title: Méthode CImageDisplay. GetColourMask (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetColourMask
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 018bdaf96e5b6508e13893290449d77041c453b3b28bb4c4d794cc5cc85fb945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655940"
---
# <a name="cimagedisplaygetcolourmask-method"></a>Méthode CImageDisplay. GetColourMask

La `GetColourMask` méthode récupère les masques de couleur pour le format d’affichage actuel.

## <a name="syntax"></a>Syntaxe


```C++
BOOL GetColourMask(
   DWORD *pMaskRed,
   DWORD *pMaskGreen,
   DWORD *pMaskBlue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMaskRed* 
</dt> <dd>

Pointeur vers une variable qui reçoit le masque de composant rouge.

</dd> <dt>

*pMaskGreen* 
</dt> <dd>

Pointeur vers une variable qui reçoit le masque de composant vert.

</dd> <dt>

*pMaskBlue* 
</dt> <dd>

Pointeur vers une variable qui reçoit le masque de composant bleu.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageDisplay, classe**](cimagedisplay.md)
</dt> </dl>

 

 




