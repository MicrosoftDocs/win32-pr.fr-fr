---
title: Message LVM_SETHOTITEM (commctrl. h)
description: Définit l’élément réactif pour un contrôle d’affichage de liste. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView SetHotItem.
ms.assetid: 0aa2b15d-4983-4234-9863-f1fdee09f913
keywords:
- LVM_SETHOTITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6937cbed8150bf14eb71e167b8ed54d6f6b47ae995a3af989613cba30c7ca3fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077239"
---
# <a name="lvm_sethotitem-message"></a>\_Message SETHOTITEM LVM

Définit l’élément réactif pour un contrôle d’affichage de liste. Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ SetHotItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotitem) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de l’élément à définir comme élément réactif.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’index de l’élément qui était précédemment chaud.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





