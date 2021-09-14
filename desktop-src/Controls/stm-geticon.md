---
title: Message STM_GETICON (winuser. h)
description: Une application envoie le \_ message STM GETICON pour récupérer un handle vers l’icône associée à un contrôle statique avec le style d' \_ icône SS.
ms.assetid: e6b0a006-696b-401d-b894-b1db697c8939
keywords:
- STM_GETICON les contrôles de Windows de message
topic_type:
- apiref
api_name:
- STM_GETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64f55d2a2f8315b99526e51a69891f6f0056e8b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116957"
---
# <a name="stm_geticon-message"></a>\_Message GETICON STM

Une application envoie le message **STM \_ GETICON** pour récupérer un handle vers l’icône associée à un contrôle statique avec le style d' \_ icône SS.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est un handle de l’icône, ou **null** si le contrôle statique n’a pas d’icône associée ou si une erreur s’est produite.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETICON STM**](stm-seticon.md)
</dt> </dl>

 

 





