---
description: Obsolète. Le PenInputPanel a été remplacé par le panneau de saisie de texte (TIP). Se produit lorsque l’objet PenInputPanel change entre des dispositions.
ms.assetid: 21d38406-7ed9-4741-a092-ed3a369dc0dc
title: Événement PenInputPanel. PanelChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41f722609ae71761a2a2a05c743aba7bfd83b7d4ff8689333bf2093d4dc21345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856518"
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

## <a name="return-value"></a>Valeur retournée

Si cet événement a la valeur, il retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Lors de la création d’un objet [**PenInputPanel**](peninputpanel-class.md) , l' [**écriture manuscrite**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) est le **PanelType** par défaut. Si vous modifiez le panneau en définissant la propriété [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) avant que le panneau de saisie du stylet ne devienne actif pour la première fois, un événement **PanelChanged** se produit.

L’événement **PanelChanged** n’est pas déclenché lorsque l’utilisateur change de pavé d’écriture encadrée et boxed.

## <a name="requirements"></a>Configuration requise



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

 

 
