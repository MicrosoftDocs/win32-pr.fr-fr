---
title: Message TB_ISBUTTONCHECKED (commctrl. h)
description: Détermine si le bouton spécifié dans une barre d’outils est activé.
ms.assetid: ce576951-8db6-4854-8457-211ece018ce8
keywords:
- TB_ISBUTTONCHECKED les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_ISBUTTONCHECKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26d93340668e926f99271e9acd450eed5d51aa454571e779601744dc4d283b1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876989"
---
# <a name="tb_isbuttonchecked-message"></a>TO \_ ISBUTTONCHECKED message

Détermine si le bouton spécifié dans une barre d’outils est activé.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Identificateur de commande du bouton.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro si le bouton est activé, ou zéro dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





