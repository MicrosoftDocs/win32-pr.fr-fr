---
title: Message TB_INSERTBUTTON (commctrl. h)
description: Insère un bouton dans une barre d’outils.
ms.assetid: 6be27817-5d86-4649-bd63-173845197763
keywords:
- TB_INSERTBUTTON les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_INSERTBUTTON
- TB_INSERTBUTTONA
- TB_INSERTBUTTONW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 909a4e039450e001757cd054cf27a15d24af392d6a55841c2857e2312252145c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829650"
---
# <a name="tb_insertbutton-message"></a>TO \_ INSERTBUTTON message

Insère un bouton dans une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro d’un bouton. Le message insère le bouton nouveau à gauche de ce bouton.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) contenant des informations sur le bouton à insérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **To \_ INSERTBUTTONW** (Unicode) et **to \_ INSERTBUTTONA** (ANSI)<br/>           |



 

 





