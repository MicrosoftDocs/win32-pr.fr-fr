---
title: Message TB_SETTOOLTIPS (commctrl. h)
description: Associe un contrôle ToolTip à une barre d’outils.
ms.assetid: a645f1f2-9333-4e25-985a-107cffb9b97f
keywords:
- TB_SETTOOLTIPS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 781565658d2c362ca32e36736d6e2d80c3641514
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032614"
---
# <a name="tb_settooltips-message"></a>TO \_ SETTOOLTIPS message

Associe un contrôle ToolTip à une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle du contrôle ToolTip.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Les boutons ajoutés à une barre d’outils avant d’envoyer le message **to \_ SETTOOLTIPS** ne sont pas enregistrés avec le contrôle ToolTip.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





