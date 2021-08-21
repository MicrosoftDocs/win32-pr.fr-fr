---
title: Message TB_GETSTATE (commctrl. h)
description: Récupère des informations sur l’état du bouton spécifié dans une barre d’outils, par exemple s’il est activé, appuyé ou activé.
ms.assetid: e8a9e1ff-506f-413b-8f8c-986c25bce736
keywords:
- TB_GETSTATE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1757cfd71427904dc7060cc0084c64b82f143e1a8db666e40fe9e08c64c7ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168235"
---
# <a name="tb_getstate-message"></a>TO \_ GETSTATE message

Récupère des informations sur l’état du bouton spécifié dans une barre d’outils, par exemple s’il est activé, appuyé ou activé.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Identificateur de commande du bouton pour lequel des informations doivent être récupérées.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne les informations d’État du bouton en cas de réussite, ou-1 dans le cas contraire. Les informations d’État du bouton peuvent être une combinaison des valeurs figurant dans États des boutons de la [**barre d’outils**](toolbar-button-states.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





