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
ms.openlocfilehash: d8a157f6a220f4932d39d13f08df79afa99d7348
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117698"
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

## <a name="return-value"></a>Valeur de retour

Retourne la position précédente.

## <a name="remarks"></a>Notes

Si *wParam* est en dehors de la plage du contrôle, la position est définie sur la limite la plus proche.

N’envoyez pas ce message à un contrôle dont le style [**PBS est \_ défilant**](progress-bar-control-styles.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





