---
description: Se produit lors d’un double-clic sur le contrôle InkPicture.
ms.assetid: 5b2a6413-d415-4bf1-a291-35f4c3c5a0dc
title: InkPicture. DblClick, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 515d16d16fb585771a8e2e06e642476b6be7a29851b750add4d6de2ca1a89bda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717328"
---
# <a name="inkpicturedblclick-event"></a>InkPicture. DblClick, événement

Se produit lors d’un double-clic sur le contrôle [InkPicture](inkpicture-control-reference.md) .

## <a name="syntax"></a>Syntaxe


```C++
void DblClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Annuler* \[ in, out\]
</dt> <dd>

Indique si l’événement doit être annulé pour le contrôle parent.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

> [!Note]  
> Pour faire la distinction entre les boutons gauche, droit et central de la souris, utilisez les événements [**MouseDown**](inkpicture-mousedown.md) et [**MouseUp**](inkpicture-mouseup.md) . Si l’événement [**Click**](inkpicture-click.md) contient du code, l’événement **DblClick** ne se déclenchera jamais.

 

Cette méthode d’événement est définie dans l’interface **\_ IInkPictureEvents** . L’interface **\_ IInkPictureEvents** implémente l’interface IDispatch avec un identificateur de **DISPID \_ IPEDblClick**.

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

 

 




