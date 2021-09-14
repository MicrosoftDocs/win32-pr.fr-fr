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
ms.openlocfilehash: 499b3677cd68444b58514d692d87cd4f631350b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119977"
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

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageDisplay, classe**](cimagedisplay.md)
</dt> </dl>

 

 




