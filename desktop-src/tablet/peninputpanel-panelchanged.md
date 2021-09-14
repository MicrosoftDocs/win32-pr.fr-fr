---
description: Obsolète. Le PenInputPanel a été remplacé par le panneau de saisie de texte (TIP). Se produit lorsque l’objet PenInputPanel change entre des dispositions.
ms.assetid: 21d38406-7ed9-4741-a092-ed3a369dc0dc
title: Événement PenInputPanel. PanelChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d6ff0f415e12131221a8dad1c0775a347ef96cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296046"
---
# <a name="peninputpanelpanelchanged-event"></a>Événement PenInputPanel. PanelChanged

Action déconseillée. Le [**PenInputPanel**](peninputpanel-class.md) a été remplacé par le [panneau de saisie de texte (TIP)](text-input-panel-reference.md).

Se produit lorsque l’objet [**PenInputPanel**](peninputpanel-class.md) change entre des dispositions.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PanelChanged(
  [in] PanelType NewPanelType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NewPanelType* \[ dans\]
</dt> <dd>

Nouveau type de panneau utilisé pour l’entrée dans l’objet [**PenInputPanel**](peninputpanel-class.md) , après le déclenchement de l’événement **PanelChanged** .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si cet événement a la valeur, il retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Lors de la création d’un objet [**PenInputPanel**](peninputpanel-class.md) , l' [**écriture manuscrite**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) est le **PanelType** par défaut. Si vous modifiez le panneau en définissant la propriété [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) avant que le panneau de saisie du stylet ne devienne actif pour la première fois, un événement **PanelChanged** se produit.

L’événement **PanelChanged** n’est pas déclenché lorsque l’utilisateur change de pavé d’écriture encadrée et boxed.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PenInputPanel**](peninputpanel-class.md)
</dt> </dl>

 

 
