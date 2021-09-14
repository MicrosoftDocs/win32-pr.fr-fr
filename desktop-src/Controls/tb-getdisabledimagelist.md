---
title: Message TB_GETDISABLEDIMAGELIST (commctrl. h)
description: Récupère la liste d’images utilisée par un contrôle de barre d’outils pour afficher les boutons inactifs.
ms.assetid: 8f6782d5-488b-4906-908a-e4bf8d512e0a
keywords:
- TB_GETDISABLEDIMAGELIST les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_GETDISABLEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fc847927ef14312c76e26303bec5de07b788266
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116785"
---
# <a name="tb_getdisabledimagelist-message"></a>TO \_ GETDISABLEDIMAGELIST message

Récupère la liste d’images utilisée par un contrôle de barre d’outils pour afficher les boutons inactifs.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne le handle de la liste d’images inactives, ou **null** si aucune liste d’images inactives n’est définie.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





