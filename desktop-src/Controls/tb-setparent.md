---
title: Message TB_SETPARENT (commctrl. h)
description: Définit la fenêtre à laquelle le contrôle de barre d’outils envoie des messages de notification.
ms.assetid: 4863bd9f-021b-4295-9483-459fc19325d9
keywords:
- TB_SETPARENT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_SETPARENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd97cdab230317feea65f2bffce74a7dec34ee336d69bb46ec4c6963ca9b3eff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078143"
---
# <a name="tb_setparent-message"></a>TO \_ SetParent, message

Définit la fenêtre à laquelle le contrôle de barre d’outils envoie des messages de notification.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la fenêtre pour recevoir des messages de notification.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est un handle vers la fenêtre de notification précédente, ou **null** s’il n’existe aucune fenêtre de notification précédente.

## <a name="remarks"></a>Remarques

Le message **to \_ SetParent,** ne modifie pas la fenêtre parente qui a été spécifiée lors de la création du contrôle. L’appel de la fonction [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) pour un contrôle ToolBar retourne la fenêtre parente réelle, et non la fenêtre spécifiée dans **to \_ SetParent,**. Pour modifier la fenêtre parente du contrôle, appelez la fonction [**SetParent,**](/windows/desktop/api/winuser/nf-winuser-setparent) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

