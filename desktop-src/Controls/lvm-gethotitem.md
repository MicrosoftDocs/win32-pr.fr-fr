---
title: Message LVM_GETHOTITEM (commctrl. h)
description: Récupère l’index de l’élément réactif. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetHotItem.
ms.assetid: f80189da-6c8b-4faf-925a-0c33fedf8c4e
keywords:
- LVM_GETHOTITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56c7bbfb845518eb40b55556df5294d59cff3d7c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999820"
---
# <a name="lvm_gethotitem-message"></a>\_Message GETHOTITEM LVM

Récupère l’index de l’élément réactif. Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ GetHotItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotitem) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’index de l’élément qui est actif.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





