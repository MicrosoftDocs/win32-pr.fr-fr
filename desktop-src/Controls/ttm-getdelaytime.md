---
title: Message TTM_GETDELAYTIME (commctrl. h)
description: Récupère les durées initiales, contextuelles et de réaffichages actuellement définies pour un contrôle ToolTip.
ms.assetid: f89a75ed-ba80-4741-927f-c571f3b2efe7
keywords:
- TTM_GETDELAYTIME les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_GETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff8c75f078465646333cae1f519049733a0c9f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115874"
---
# <a name="ttm_getdelaytime-message"></a>\_Message atténuation GETDELAYTIME

Récupère les durées initiales, contextuelles et de réaffichages actuellement définies pour un contrôle ToolTip.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Indicateur qui spécifie la valeur de durée qui sera extraite. Ce paramètre peut prendre l'une des valeurs suivantes :



| Valeur                                                                                                                                                      | Signification                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <dt>**TTDT \_ AUTOPOP**</dt> </dl> | Récupérez la durée pendant laquelle la fenêtre d’info-bulle reste visible si le pointeur est immobile dans le rectangle englobant d’un outil.<br/>      |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <dt>**TTDT \_ initial**</dt> </dl> | Récupérez la durée pendant laquelle le pointeur doit rester immobile dans le rectangle englobant d’un outil avant que la fenêtre d’info-bulle ne s’affiche.<br/> |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <dt>**TTDT \_ RÉafficher**</dt> </dl>    | Récupérez le temps nécessaire pour que les fenêtres d’info-bulle suivantes s’affichent lorsque le pointeur se déplace d’un outil à un autre.<br/>         |



 

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur de type INT avec la durée spécifiée en millisecondes.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ATTÉNUATION \_ SETDELAYTIME**](ttm-setdelaytime.md)
</dt> </dl>

 

 





