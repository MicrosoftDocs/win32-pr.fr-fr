---
title: Message TBM_GETPOS (commctrl. h)
description: Récupère la position logique actuelle du curseur dans un TrackBar. Les positions logiques sont les valeurs entières de la plage de la plage de la barre de défilement minimale à la position maximale du curseur.
ms.assetid: 6f082ab2-2f9a-4bc0-bfca-56f7b1a2d921
keywords:
- TBM_GETPOS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TBM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072ff9b8a107fe19afb1fee6107a2f05bad36025
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116454"
---
# <a name="tbm_getpos-message"></a>\_Message TBM GETPOS

Récupère la position logique actuelle du curseur dans un TrackBar. Les positions logiques sont les valeurs entières de la plage de la plage de la barre de défilement minimale à la position maximale du curseur.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur 32 bits qui spécifie la position logique actuelle du curseur de la barre de défilement.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TBM \_ SetPos**](tbm-setpos.md)
</dt> </dl>

 

 





