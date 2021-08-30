---
title: Message PBM_SETPOS (commctrl. h)
description: Définit la position actuelle d’une barre de progression et redessine la barre pour refléter la nouvelle position.
ms.assetid: 9ebeaa19-0f42-4af7-85d8-aae22498fd6f
keywords:
- PBM_SETPOS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf9c6a4c21439f93f3459a5061daf28192081a042cc663a644110a1e54d2c54
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986149"
---
# <a name="pbm_setpos-message"></a>\_Message PBM SetPos

Définit la position actuelle d’une barre de progression et redessine la barre pour refléter la nouvelle position.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Entier signé qui devient la nouvelle position.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la position précédente.

## <a name="remarks"></a>Remarques

Si *wParam* est en dehors de la plage du contrôle, la position est définie sur la limite la plus proche.

N’envoyez pas ce message à un contrôle dont le style [**PBS est \_ défilant**](progress-bar-control-styles.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





