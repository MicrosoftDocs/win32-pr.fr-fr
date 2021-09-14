---
title: Message LVM_SETBKCOLOR (commctrl. h)
description: Définit la couleur d’arrière-plan d’un contrôle d’affichage de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SetBkColor.
ms.assetid: d579249d-421d-4e7e-8992-4c7fd7277593
keywords:
- LVM_SETBKCOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80977ed6c95a1353889265e52cfc05c26aaa2a5f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999781"
---
# <a name="lvm_setbkcolor-message"></a>\_Message SETBKCOLOR LVM

Définit la couleur d’arrière-plan d’un contrôle d’affichage de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkcolor) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Couleur d’arrière-plan à définir ou \_ valeur CLR None pour aucune couleur d’arrière-plan. Les contrôles d’affichage de liste avec des couleurs d’arrière-plan se redessinent beaucoup plus rapidement que ceux sans couleurs d’arrière-plan.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





