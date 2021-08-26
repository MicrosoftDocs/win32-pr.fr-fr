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
ms.openlocfilehash: d33aab01e668f4b77e36a0a62b8eab75f3ee5db82188416c295c04cdf9bcb078
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084949"
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

## <a name="return-value"></a>Valeur retournée

La valeur de retour est un handle de l’icône, ou **null** si le contrôle statique n’a pas d’icône associée ou si une erreur s’est produite.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETICON STM**](stm-seticon.md)
</dt> </dl>

 

 





