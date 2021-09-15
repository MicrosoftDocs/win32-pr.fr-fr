---
description: Se produit lorsqu’une touche est enfoncée alors que le contrôle InkPicture a le focus.
ms.assetid: adb61eff-a92c-40b0-940c-02e14cd34e5f
title: Événement InkPicture. KeyPress (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f9ef48a0e117d6a3d4c29a9ca69aba3bf6e054
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404762"
---
# <a name="inkpicturekeypress-event"></a>Événement InkPicture. KeyPress

Se produit lorsqu’une touche est enfoncée alors que le contrôle [InkPicture](inkpicture-control-reference.md) a le focus.

## <a name="syntax"></a>Syntaxe


```C++
void KeyPress(
  [in, out] short *KeyAscii
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*KeyAscii* \[ in, out\]
</dt> <dd>

Valeur ASCII de la touche enfoncée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode d’événement est définie dans l’interface **\_ IInkPictureEvents** . L’interface **\_ IInkPictureEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IPEKeyPress.

## <a name="requirements"></a>Spécifications



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

 

