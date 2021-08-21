---
description: Se produit après la modification de la propriété ModeAffichage du contrôle InkPicture.
ms.assetid: ae56b5a2-e3e2-468c-a572-a9b46eb1d39d
title: InkPicture. SizeModeChanged, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bebcd5a659894c6f70a87ea75f7a99321d94dba2826fd538530f7e6d060d5730
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032027"
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

## <a name="remarks"></a>Remarques

Cette méthode d’événement est définie dans l’interface **\_ IInkPictureEvents** . L’interface **\_ IInkPictureEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IPESizeModeChanged.

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

 

