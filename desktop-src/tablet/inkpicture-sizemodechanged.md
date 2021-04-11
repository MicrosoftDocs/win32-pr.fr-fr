---
description: Se produit après la modification de la propriété ModeAffichage du contrôle InkPicture.
ms.assetid: ae56b5a2-e3e2-468c-a572-a9b46eb1d39d
title: InkPicture. SizeModeChanged, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f270ea141bc8803cbcf1ce4e54b0f73318ed69d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320438"
---
# <a name="inkpicturesizemodechanged-event"></a>InkPicture. SizeModeChanged, événement

Se produit après la modification de la propriété [**ModeAffichage**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) du contrôle [InkPicture](inkpicture-control-reference.md) .

## <a name="syntax"></a>Syntaxe


```C++
void SizeModeChanged(
  [in] InkPictureSizeMode NewMode,
  [in] InkPictureSizeMode OldMode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NewMode* \[ dans\]
</dt> <dd>

Nouvel État du contrôle [InkPicture](inkpicture-control-reference.md) , en fonction de la nouvelle valeur de la propriété [**ModeAffichage**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) .

</dd> <dt>

*OldMode* \[ dans\]
</dt> <dd>

Ancien état du contrôle [InkPicture](inkpicture-control-reference.md) , en fonction de l’ancienne valeur de la propriété [**ModeAffichage**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode d’événement est définie dans l’interface **\_ IInkPictureEvents** . L’interface **\_ IInkPictureEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IPESizeModeChanged.

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

 

