---
title: Message HDM_DELETEITEM (commctrl. h)
description: Supprime un élément d’un contrôle header. Vous pouvez envoyer ce message explicitement ou utiliser l’en-tête de la \_ macro DeleteItem.
ms.assetid: 1dd1f233-2812-41ae-8a36-c42b9ac70ffc
keywords:
- HDM_DELETEITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- HDM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28b0a48d769117ffd68f2ba2af9695fe7fce00031f297626ae48c111d4574dd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697349"
---
# <a name="hdm_deleteitem-message"></a>\_Message HDM DELETEITEM

Supprime un élément d’un contrôle header. Vous pouvez envoyer ce message explicitement ou utiliser l' [**en \_ -tête**](/windows/desktop/api/Commctrl/nf-commctrl-header_deleteitem) de la macro DeleteItem.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’élément à supprimer.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





