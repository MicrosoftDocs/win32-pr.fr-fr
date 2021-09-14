---
description: Se produit lorsqu’un utilisateur clique sur le contrôle InkPicture.
ms.assetid: 326bac37-2d5d-434b-916c-8a675bab5052
title: InkPicture. Click, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1dd90cd69555f65531f5ab2684f886dab23e191
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127226348"
---
# <a name="inkpictureclick-event"></a>InkPicture. Click, événement

Se produit lorsqu’un utilisateur clique sur le contrôle [InkPicture](inkpicture-control-reference.md) .

## <a name="syntax"></a>Syntaxe


```C++
void Click();
```



## <a name="parameters"></a>Paramètres

Cet événement n’a pas de paramètres.

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le clic sur un contrôle génère des événements [**MouseDown**](inkpicture-mousedown.md) et [**MouseUp**](inkpicture-mouseup.md) en plus de l’événement Click.

> [!Note]  
> Pour faire la distinction entre les boutons gauche, droit et central de la souris, utilisez les événements [**MouseDown**](inkpicture-mousedown.md) et [**MouseUp**](inkpicture-mouseup.md) .

 

Si l’événement **Click** contient du code, l’événement [**DblClick**](inkpicture-dblclick.md) ne se déclenchera jamais, car l’événement **Click** est le premier événement déclenché entre les deux. Par conséquent, le clic de souris est intercepté par l’événement **Click** , si bien que l’événement **DblClick** ne se produit pas.

Cette méthode d’événement est définie dans l’interface **\_ IInkPictureEvents** . L’interface **\_ IInkPictureEvents** implémente l’interface IDispatch avec un identificateur de **DISPID \_ IPEClick**.

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

 

 




