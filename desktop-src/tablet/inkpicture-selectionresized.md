---
description: Se produit lorsque la taille de la sélection actuelle a changé, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de sélection.
ms.assetid: 4e7f461f-2909-40ab-98d8-b763d489eb62
title: InkPicture. SelectionResized, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b90e04533e3551fd4e1ba4ac661d8060377e6d06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526274"
---
# <a name="inkpictureselectionresized-event"></a>InkPicture. SelectionResized, événement

Se produit lorsque la taille de la sélection actuelle a changé, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .

## <a name="syntax"></a>Syntaxe


```C++
void SelectionResized(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*OldSelectionRect* \[ dans\]
</dt> <dd>

Rectangle englobant de la collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) sélectionnée telle qu’elle existait avant le déclenchement de l’événement **SelectionResized** .

> [!Note]  
> Ce rectangle est spécifié dans les coordonnées d’espace d’encre, ce qui permet les scénarios d’annulation.

 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** (dispinterfaces) avec l’ID DISPID \_ IOESelectionResized.

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
</dt> <dt>

[**Propriété de sélection, \[ contrôle InkPicture\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)
</dt> <dt>

[**InkRectangle, classe**](inkrectangle-class.md)
</dt> </dl>

 

