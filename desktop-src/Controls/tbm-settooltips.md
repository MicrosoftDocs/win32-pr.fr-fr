---
title: Message TBM_SETTOOLTIPS (commctrl. h)
description: Assigne un contrôle ToolTip à un contrôle TrackBar.
ms.assetid: 9bba1084-d04e-4631-a5cc-408849a14eb1
keywords:
- TBM_SETTOOLTIPS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TBM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a17aad8324946a96ab47344c2edc05abf76e02fba64a459b85f4af7b924bc7a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119261389"
---
# <a name="tbm_settooltips-message"></a>\_Message TBM SETTOOLTIPS

Assigne un contrôle ToolTip à un contrôle TrackBar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle vers un contrôle ToolTip existant.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de ce message n’est pas utilisée.

## <a name="remarks"></a>Remarques

Lorsqu’un contrôle TrackBar est créé avec le style des [**\_ info-bulles tbs**](trackbar-control-styles.md) , il crée un contrôle ToolTip par défaut qui apparaît à côté du curseur, en affichant la position actuelle du curseur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





