---
title: Message TB_GETINSERTMARK (commctrl. h)
description: Récupère la marque d’insertion actuelle pour la barre d’outils.
ms.assetid: b22770a4-e859-451d-a726-279bbc49b984
keywords:
- TB_GETINSERTMARK les contrôles de Windows de message
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116758"
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

## <a name="return-value"></a>Valeur de retour

Retourne toujours la **valeur true**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TO \_ SETINSERTMARK**](tb-setinsertmark.md)
</dt> </dl>

 

 





