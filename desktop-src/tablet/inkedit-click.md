---
description: Se produit lorsqu’un utilisateur clique sur le contrôle InkEdit.
ms.assetid: 99fd7ef0-02cf-4390-9026-00ef2bbc1e37
title: InkEdit. Click, événement (Y2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55df62807ee78e0f083a301c83a756b4cffb729d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519495"
---
# <a name="inkeditclick-event"></a>InkEdit. Click, événement

Se produit lorsqu’un utilisateur clique sur le contrôle [InkEdit](inkedit-control-reference.md) .

## <a name="syntax"></a>Syntaxe


```C++
void Click();
```



## <a name="parameters"></a>Paramètres

Cet événement n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le clic sur un contrôle génère des événements [**MouseDown**](inkedit-mousedown.md) et [**MouseUp**](inkedit-mouseup.md) en plus de l’événement Click.

> [!Note]  
> Pour faire la distinction entre les boutons gauche, droit et central de la souris, utilisez les événements [**MouseDown**](inkedit-mousedown.md) et [**MouseUp**](inkedit-mouseup.md) .

 

Si l’événement **Click** contient du code, l’événement [**DblClick**](inkedit-dblclick.md) ne se déclenchera jamais, car l’événement **Click** est le premier événement déclenché entre les deux. Par conséquent, le clic de souris est intercepté par l’événement **Click** , si bien que l’événement **DblClick** ne se produit pas.

Cette méthode d’événement est définie dans l’interface **\_ IInkEditEvents** . L’interface **\_ IInkEditEvents** implémente l’interface IDispatch avec un identificateur de **DISPID \_ IeeClick**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>« Y2. h » (nécessite également l' \_ entrée i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

 




