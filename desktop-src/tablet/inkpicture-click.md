---
description: Se produit lorsqu’un utilisateur clique sur le contrôle InkPicture.
ms.assetid: 326bac37-2d5d-434b-916c-8a675bab5052
title: InkPicture. Click, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08ebde47609a36a92eca211f597345a9784fca03f66076ebb4db6f04ee6f5936
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218538"
---
# <a name="inkpictureclick-event"></a>InkPicture. Click, événement

Se produit lorsqu’un utilisateur clique sur le contrôle [InkPicture](inkpicture-control-reference.md) .

## <a name="syntax"></a>Syntaxe


```C++
void Click();
```



## <a name="parameters"></a>Paramètres

Cet événement n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Le clic sur un contrôle génère des événements [**MouseDown**](inkpicture-mousedown.md) et [**MouseUp**](inkpicture-mouseup.md) en plus de l’événement Click.

> [!Note]  
> Pour faire la distinction entre les boutons gauche, droit et central de la souris, utilisez les événements [**MouseDown**](inkpicture-mousedown.md) et [**MouseUp**](inkpicture-mouseup.md) .

 

Si l’événement **Click** contient du code, l’événement [**DblClick**](inkpicture-dblclick.md) ne se déclenchera jamais, car l’événement **Click** est le premier événement déclenché entre les deux. Par conséquent, le clic de souris est intercepté par l’événement **Click** , si bien que l’événement **DblClick** ne se produit pas.

Cette méthode d’événement est définie dans l’interface **\_ IInkPictureEvents** . L’interface **\_ IInkPictureEvents** implémente l’interface IDispatch avec un identificateur de **DISPID \_ IPEClick**.

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

 

 




