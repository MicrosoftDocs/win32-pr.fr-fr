---
title: Message TTM_SETDELAYTIME (commctrl. h)
description: Définit les durées initiales, contextuelles et de réaffichage pour un contrôle ToolTip.
ms.assetid: 0a73def0-550c-4d01-9cb1-1eb1f4356fa3
keywords:
- TTM_SETDELAYTIME les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TTM_SETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd5b4f3d20cd99872adeeb66776d71a1e4125a066890a3bab4793caf04de8f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914069"
---
# <a name="ttm_setdelaytime-message"></a>\_Message atténuation SETDELAYTIME

Définit les durées initiales, contextuelles et de réaffichage pour un contrôle ToolTip.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Indicateur qui spécifie la valeur de temps à définir. Ce paramètre peut prendre l’une des valeurs suivantes :



| Valeur                                                                                                                                                            | Signification                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <dt>**TTDT \_ AUTOPOP**</dt> </dl>       | Définir la durée pendant laquelle une fenêtre d’info-bulle reste visible si le pointeur est immobile dans le rectangle englobant d’un outil. Pour rétablir la valeur par défaut du délai autopop, affectez la valeur-1 à *lParam* .<br/>                                                                                                                                                         |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <dt>**TTDT \_ initial**</dt> </dl>       | Définissez la durée pendant laquelle un pointeur doit rester immobile dans le rectangle englobant d’un outil avant que la fenêtre d’info-bulle ne s’affiche. Pour rétablir la valeur par défaut du délai d’attente initial, affectez la valeur-1 à *lParam* .<br/>                                                                                                                                                    |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <dt>**TTDT \_ RÉafficher**</dt> </dl>          | Définissez la durée nécessaire pour que les fenêtres d’info-bulle suivantes s’affichent lorsque le pointeur se déplace d’un outil à un autre. Pour rétablir la valeur par défaut du délai de réaffichage, affectez la valeur-1 à *lParam* .<br/>                                                                                                                                                           |
| <span id="TTDT_AUTOMATIC"></span><span id="ttdt_automatic"></span><dl> <dt>**TTDT \_ automatique**</dt> </dl> | Définissez les trois délais de temporisation par défaut. L’heure de autopop sera 10 fois supérieure à l’heure initiale et l’heure de réaffichage sera le cinquième de l’heure initiale. Si cet indicateur est défini, utilisez une valeur positive de *lParam* pour spécifier l’heure initiale, en millisecondes. Affectez une valeur négative à *lParam* pour retourner les valeurs par défaut des trois retards.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie le délai, en millisecondes. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de ce message n’est pas utilisée.

## <a name="remarks"></a>Remarques

Les délais d’attente par défaut sont basés sur le temps de double-clic. Pour le double-clic par défaut de 500 ms, les temps de délai initial, autopop et de réaffichage sont de 500 ms, 5 000 MS et 100 ms respectivement. Le fragment de code suivant utilise la fonction [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime) pour déterminer les trois délais pour tous les systèmes.


```
initial = GetDoubleClickTime();

autopop = GetDoubleClickTime() * 10;

reshow = GetDoubleClickTime() / 5;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ATTÉNUATION \_ GETDELAYTIME**](ttm-getdelaytime.md)
</dt> </dl>

 

