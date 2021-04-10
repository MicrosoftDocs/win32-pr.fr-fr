---
description: Se produit après le redimensionnement du contrôle InkPicture, en particulier après la modification de la valeur de la propriété Width ou Height.
ms.assetid: a5fc6c82-f9c8-4104-8abe-082c47c56be9
title: InkPicture. SizeChanged, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5675d2a581d9e8973b88fa9fb6e213f54c0e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952916"
---
# <a name="inkpicturesizechanged-event"></a>InkPicture. SizeChanged, événement

Se produit après le redimensionnement du contrôle [InkPicture](inkpicture-control-reference.md) , en particulier après la modification de la valeur de la propriété [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) ou [**Height**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) .

## <a name="syntax"></a>Syntaxe


```C++
void SizeChanged(
  [in] long Left,
  [in] long Top,
  [in] long Right,
  [in] long Bottom
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

À *gauche* \[ dans\]
</dt> <dd>

Coordonnée x du côté gauche du contrôle [InkPicture](inkpicture-control-reference.md) .

</dd> <dt>

En *haut* \[ dans\]
</dt> <dd>

Coordonnée y du haut du contrôle [InkPicture](inkpicture-control-reference.md) .

</dd> <dt>

À *droite* \[ dans\]
</dt> <dd>

Coordonnée x du côté droit du contrôle [InkPicture](inkpicture-control-reference.md) .

</dd> <dt>

En *bas* \[ dans\]
</dt> <dd>

Coordonnée y du bas du contrôle [InkPicture](inkpicture-control-reference.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode d’événement est définie dans l’interface **\_ IInkPictureEvents** . L’interface **\_ IInkPictureEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IPESizeChanged.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

