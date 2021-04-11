---
title: Message TB_GETINSERTMARK (commctrl. h)
description: Récupère la marque d’insertion actuelle pour la barre d’outils.
ms.assetid: b22770a4-e859-451d-a726-279bbc49b984
keywords:
- TB_GETINSERTMARK les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b45a4cafbd49c709e9ca5b8e9afeda51323de491
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032484"
---
# <a name="tb_getinsertmark-message"></a>TO \_ GETINSERTMARK message

Récupère la marque d’insertion actuelle pour la barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) qui reçoit la marque d’insertion.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne toujours la **valeur true**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TO \_ SETINSERTMARK**](tb-setinsertmark.md)
</dt> </dl>

 

 





