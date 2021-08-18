---
title: Message TB_ISBUTTONHIGHLIGHTED (commctrl. h)
description: Vérifie l’état de mise en surbrillance d’un bouton de barre d’outils.
ms.assetid: d5aab670-a989-46f2-b4f8-d8a8968cbe07
keywords:
- TB_ISBUTTONHIGHLIGHTED les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_ISBUTTONHIGHLIGHTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 903932fddb7bf356a89adda0513a045d099a22c459add6401818eec54a3f0657
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918369"
---
# <a name="tb_isbuttonhighlighted-message"></a>TO \_ ISBUTTONHIGHLIGHTED message

Vérifie l’état de mise en surbrillance d’un bouton de barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Identificateur de commande pour un bouton de barre d’outils.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro si le bouton est mis en surbrillance, ou zéro dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





