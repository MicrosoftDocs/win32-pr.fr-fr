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
ms.openlocfilehash: f53e25058fee8fa5dcac218a641277ac46aed4e7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116650"
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

## <a name="return-value"></a>Valeur de retour

Retourne une valeur différente de zéro si le bouton est mis en surbrillance, ou zéro dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





