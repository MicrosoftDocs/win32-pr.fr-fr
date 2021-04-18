---
description: Obsolète. Le PenInputPanel a été remplacé par le panneau de saisie de texte (TIP). Se produit lorsque l’objet PenInputPanel est déplacé.
ms.assetid: 0c51d875-cef9-4087-b17d-5c5af04f81a5
title: Événement PenInputPanel. PanelMoving (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be69e227188739cb656e6a1eb471716e1aa4feb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543136"
---
# <a name="peninputpanelpanelmoving-event"></a>Événement PenInputPanel. PanelMoving

Action déconseillée. Le [**PenInputPanel**](peninputpanel-class.md) a été remplacé par le [panneau de saisie de texte (TIP)](text-input-panel-reference.md).

Se produit lorsque l’objet [**PenInputPanel**](peninputpanel-class.md) est déplacé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PanelMoving(
  [in, out] long *Left,
  [in, out] long *Top
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

À *gauche* \[ in, out\]
</dt> <dd>

Nouvel axe horizontal, ou axe des x, position du bord gauche de l’objet [**PenInputPanel**](peninputpanel-class.md) , en coordonnées d’écran.

</dd> <dt>

En *haut* \[ in, out\]
</dt> <dd>

Nouvel axe vertical, ou axe y, position du bord gauche de l’objet [**PenInputPanel**](peninputpanel-class.md) , en coordonnées d’écran.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cet événement a la valeur, il retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

L’événement **PanelMoving** est conçu pour être utilisé pour modifier la position du panneau de saisie du stylet en modifiant les paramètres de *gauche* et du *haut* .

Les méthodes [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) et [**Refresh**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh) forcent l’objet [**PenInputPanel**](peninputpanel-class.md) à appeler son code de positionnement automatique qui déclenche un événement **PanelMoving** . Par conséquent, l’appel de ces méthodes à l’intérieur d’un gestionnaire **PanelMoving** peut entraîner une boucle infinie récursive.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PenInputPanel**](peninputpanel-class.md)
</dt> </dl>

 

 




