---
description: Se produit lorsqu’une touche est enfoncée et en position inférieure alors que le contrôle InkPicture a le focus.
ms.assetid: d83823ea-d863-4eb7-8f6b-fa7a3396e64b
title: InkPicture. KeyOut, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9cf86a8efaacd1094330861bff63d38ae03ef056f4686a1286e06c8aca1ef5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451108"
---
# <a name="inkpicturekeydown-event"></a>InkPicture. KeyOut, événement

Se produit lorsqu’une touche est enfoncée et en position inférieure alors que le contrôle [InkPicture](inkpicture-control-reference.md) a le focus.

## <a name="syntax"></a>Syntaxe


```C++
void KeyDown(
  [in, out] short *KeyCode,
  [in, out] short *Shift
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*KeyCode* \[ in, out\]
</dt> <dd>

Valeur ASCII de la touche enfoncée.

</dd> <dt>

*MAJ* \[ in, out\]
</dt> <dd>

État de la touche Maj.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode d’événement est définie dans l’interface **\_ IInkPictureEvents** . L’interface **\_ IInkPictureEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IPEKeyDown.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

