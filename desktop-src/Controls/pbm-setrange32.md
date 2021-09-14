---
title: Message PBM_SETRANGE32 (commctrl. h)
description: Définit les valeurs minimale et maximale d’une barre de progression sur les valeurs 32 bits et redessine la barre pour refléter la nouvelle plage.
ms.assetid: 7958ea14-17b4-4c0e-97ec-b09fa0d36e8b
keywords:
- PBM_SETRANGE32 les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PBM_SETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55fcf91c794ec9ae3880d67f8df947f87fec413d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117690"
---
# <a name="pbm_setrange32-message"></a>\_Message PBM SETRANGE32

Définit les valeurs minimale et maximale d’une barre de progression sur les valeurs 32 bits et redessine la barre pour refléter la nouvelle plage.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur de plage minimale. Par défaut, la valeur minimale est zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Valeur de plage maximale. Cette valeur doit être supérieure à *wParam*. Par défaut, la valeur maximale est 100.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **DWORD** qui contient la limite inférieure 16 bits précédente dans son [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) et la limite supérieure 16 bits précédente dans son [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)). Si les plages précédentes étaient des valeurs 32 bits, la valeur de retour est composée des **LOWORD** s des deux limites de 32 bits.

## <a name="remarks"></a>Notes

Pour récupérer les valeurs de 32 bits les plus élevées et les plus basses, utilisez le message [**PBM \_ GETRANGE**](pbm-getrange.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

