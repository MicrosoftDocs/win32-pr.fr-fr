---
title: Message HDM_DELETEITEM (commctrl. h)
description: Supprime un élément d’un contrôle header. Vous pouvez envoyer ce message explicitement ou utiliser l’en-tête de la \_ macro DeleteItem.
ms.assetid: 1dd1f233-2812-41ae-8a36-c42b9ac70ffc
keywords:
- HDM_DELETEITEM les contrôles de message Windows
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
ms.openlocfilehash: e6a3ec4b48c3dcc77579f70d26cd55b7127f5a6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033017"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





